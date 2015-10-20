# -*- coding: utf-8 -*-
# Continuous Wavelet Transform
# Copyright 2006 by Flavio Codeco Coelho
import math,pylab
import numpy
import matplotlib.cm as cm
from detect_peaks import detect_peaks
from findpeak import findpeaks

from scipy.stats import scoreatpercentile
from applyThr import applyThr
#import numarray as numpy 
 
def cwt(x, nvoice, wavelet, oct=2, scale=4):

    #preparation
    x = numpy.asarray(x)
    n = len(x)
    xhat = numpy.fft.fft(x)
    xi = numpy.concatenate((numpy.arange(n/2+1), numpy.arange(-n/2+1,0))) * (2*numpy.pi/n)
    
    #root
    omega0 = 8
 
    # or(?)
    #omega0 = numpy.pi * 2
    
    #noctave = floor(log(n,2))-1
    noctave = int(math.floor(math.log(n,2))-oct)
    nscale  = nvoice * noctave
    #cwt = numpy.zeros((n,nscale),numpy.Float)
    
    cwt = []
   
    exp = numpy.exp
    sqrt = numpy.sqrt
    ifft = numpy.fft.ifft
    for jo in xrange(noctave):
        for jv in xrange(1,nvoice+1):
            qscale = scale*(2**(jv/float(nvoice)))
            omega = xi * (n/qscale)
 
            # fft of wavelet
            if wavelet == 'Gauss':
                #window = exp((-omega**2)/2.)
                # simple optimization - inumpylace operations
                omega *= omega
                omega *= -0.5
                exp(omega, omega)
                window = omega
 
            elif wavelet == 'DerGauss':
                window = 1j*omega*exp(-omega**2/2.)
            elif wavelet == 'Sombrero':
                window = (omega**2)*exp(-omega**2/2.)
            elif wavelet =='Morlet':
                window = exp(-(omega-omega0)**2/2.)-exp(-(omega**2+omega0**2)/2.)
 
            #Renormalization
            window *= 1./sqrt(qscale)
            what = window*xhat # convolution
            w = ifft(what)
 
            cwt.append(w.real)
             
        scale *= 2
    cwt = numpy.vstack(cwt)
    #rL = identify_ridge_lines(cwt, numpy.arange(156), numpy.ceil(scale))
    #filt = filter_ridge_lines(cwt, rL)
    #max_locs = [x[1][0] for x in filt]
    #maxSort = sorted(max_locs)
    #print maxSort
    #pylab.plot(maxSort, x[maxSort],'ro')
    return cwt
 
def calcCWTScale(sz):
    n = sz[1]; nscale = sz[0] #because the plot will be transposed
    noctave = math.floor(numpy.log2(n))-2
    nvoice  = nscale / noctave
    xtick   = pylab.linspace(0,n,n)
    ytick   = pylab.linspace(int(n/2),0,nscale)
    return (xtick,ytick)
# 
# 
def imageCWT(org,c,cmap=None, title='Scalogram',interpolation='bilinear',origin='image'):
    #pylab.subplot(211)
    #pylab.plot(org)
    #pylab.subplot(212)
    #xtick,ytick = calcCWTScale(c.shape)
    ##print len(xtick),len(ytick)
    #A=pylab.imshow(c,cmap=cm.bone,origin=origin, interpolation=interpolation)
    #xidx = pylab.linspace(0,len(xtick)-1,len(A.axes.get_xticks())).astype(numpy.int)
    #yidx = pylab.linspace(0,len(ytick)-1,len(A.axes.get_yticks())).astype(numpy.int)
    #A.axes.set_xticks(xidx)
    #A.axes.set_yticks(yidx)
    #A.axes.set_xticklabels([str(int(x)) for x in xtick[xidx]])
    #A.axes.set_yticklabels([str(int(y)) for y in ytick[yidx]])
    #A.axes.set_aspect('auto')
    #pylab.xlabel('time(samples)')
    #pylab.ylabel('scale')
    #pylab.title(title)    

    fig = pylab.figure()
    pylab.subplot(411)
    pylab.plot(org)
    pylab.subplot(412)
    xtick,ytick = calcCWTScale(c.shape)
    #print len(xtick),len(ytick)
    A=pylab.imshow(c,cmap=cm.bone,origin=origin, interpolation=interpolation)
    xidx = pylab.linspace(0,len(xtick)-1,len(A.axes.get_xticks())).astype(numpy.int)
    yidx = pylab.linspace(0,len(ytick)-1,len(A.axes.get_yticks())).astype(numpy.int)
    A.axes.set_xticks(xidx)
    A.axes.set_yticks(yidx)
    A.axes.set_xticklabels([str(int(x)) for x in xtick[xidx]])
    A.axes.set_yticklabels([str(int(y)) for y in ytick[yidx]])
    A.axes.set_aspect('auto')
    pylab.xlabel('time(samples)')
    pylab.ylabel('scale')
    pylab.title(title)
    pylab.subplot(413)
    pi = len(c)/1.5
    p = c[pi]
    pylab.plot(p)
    pylab.hold(True)
    s3= numpy.sign(p)  
    s3[s3==0] = -1     # replace zeros with -1  
    zero_crossings3 = numpy.where(numpy.diff(s3))[0] 
    pylab.plot(zero_crossings3,[0]*len(zero_crossings3),'ro')
    pylab.title('Plot of C_a,b = ' + str(pi))
    p = applyThr(p)
    pylab.subplot(414)
    pylab.plot(p)
    pylab.title('Thresholded Plot of C_a,b = ' + str(pi))
    

    pylab.subplots_adjust(hspace=0.9)
    #detect_peaks(c[len(c)/2])
    pylab.figure(2)
    pylab.plot(p)
    pylab.hold(True)
    #peak = findpeaks(p)
    #pylab.plot(peak,p[peak],'ro')
    s3= numpy.sign(p)  
    s3[s3==0] = -1     # replace zeros with -1  
    zero_crossings3 = numpy.where(numpy.diff(s3))[0] 
    pylab.plot(zero_crossings3,[0]*len(zero_crossings3),'ro')
    #numpy.savetxt(str('poop') + 'xx.txt', c[len(c)/2], delimiter=',')
    #pylab.show()
 
 
#if __name__=='__main__':
# 
#    #data = numpy.sin(numpy.linspace(0, 8*6.14, 512))
#  
#    x = numpy.linspace(0, 1024, 2*1024) 
#    data = 2*numpy.sin(2*numpy.pi/4 * x) * numpy.exp(-(x-400)**2/(2*300**2)) + \
#           numpy.sin(2*numpy.pi/32*x) * numpy.exp(-(x-700)**2/(2*100**2)) + \
#           numpy.sin(2*numpy.pi/32 * (x/(1+x/1000)) )
# 
#    
#    pylab.figure()
#    pylab.plot(data)
#    
#    #interpolation = 'nearest'
#    interpolation = 'bilinear'
#    origin = 'image'
# 
#    #import time
#    for wname in ['Gauss', 'DerGauss', 'Sombrero', 'Morlet']:
#        pylab.figure()
#        #t = time.clock()
#        c = cwt(data, nvoice=8, wavelet=wname, oct=2, scale=4)
#        #print time.clock() - t
#        #c = abs(c)
#        imageCWT(c,title='%s wavelet' % wname,origin=origin,interpolation=interpolation)
#    pylab.show()

def identify_ridge_lines(matr, max_distances, gap_thresh):
    if(len(max_distances) < matr.shape[0]):
        raise ValueError('Max_distances must have at least as many rows as matr')

    all_max_cols = _boolrelextrema(matr, numpy.greater, axis=1, order=1)
    #Highest row for which there are any relative maxima
    has_relmax = numpy.where(all_max_cols.any(axis=1))[0]
    if(len(has_relmax) == 0):
        return []
    start_row = has_relmax[-1]
    #Each ridge line is a 3-tuple:
    #rows, cols,Gap number
    ridge_lines = [[[start_row],
                   [col],
                   0] for col in numpy.where(all_max_cols[start_row])[0]]
    final_lines = []
    rows = numpy.arange(start_row - 1, -1, -1)
    cols = numpy.arange(0, matr.shape[1])
    for row in rows:
        this_max_cols = cols[all_max_cols[row]]

        #Increment gap number of each line,
        #set it to zero later if appropriate
        for line in ridge_lines:
            line[2] += 1

        #XXX These should always be all_max_cols[row]
        #But the order might be different. Might be an efficiency gain
        #to make sure the order is the same and avoid this iteration
        prev_ridge_cols = numpy.array([line[1][-1] for line in ridge_lines])
        #Look through every relative maximum found at current row
        #Attempt to connect them with existing ridge lines.
        for ind, col in enumerate(this_max_cols):
            """
            If there is a previous ridge line within
            the max_distance to connect to, do so.
            Otherwise start a new one.
            """
            line = None
            if(len(prev_ridge_cols) > 0):
                diffs = numpy.abs(col - prev_ridge_cols)
                closest = numpy.argmin(diffs)
                if diffs[closest] <= max_distances[row]:
                    line = ridge_lines[closest]
            if(line is not None):
                #Found a point close enough, extend current ridge line
                line[1].append(col)
                line[0].append(row)
                line[2] = 0
            else:
                new_line = [[row],
                            [col],
                            0]
                ridge_lines.append(new_line)

        #Remove the ridge lines with gap_number too high
        #XXX Modifying a list while iterating over it.
        #Should be safe, since we iterate backwards, but
        #still tacky.
        for ind in xrange(len(ridge_lines) - 1, -1, -1):
            line = ridge_lines[ind]
            if line[2] > gap_thresh:
                final_lines.append(line)
                del ridge_lines[ind]

    out_lines = []
    for line in (final_lines + ridge_lines):
        sortargs = numpy.array(numpy.argsort(line[0]))
        rows, cols = numpy.zeros_like(sortargs), numpy.zeros_like(sortargs)
        rows[sortargs] = line[0]
        cols[sortargs] = line[1]
        out_lines.append([rows, cols])

    return out_lines

def filter_ridge_lines(cwt, ridge_lines, window_size=None, min_length=None,
                       min_snr=1, noise_perc=10):
    num_points = cwt.shape[1]
    if min_length is None:
        min_length = numpy.ceil(cwt.shape[0] / 4)
    if window_size is None:
        window_size = numpy.ceil(num_points / 20)

    window_size = int(window_size)
    hf_window, odd = divmod(window_size, 2)

    #Filter based on SNR
    row_one = cwt[0, :]
    noises = numpy.zeros_like(row_one)
    for ind, val in enumerate(row_one):
        window_start = max(ind - hf_window, 0)
        window_end = min(ind + hf_window + odd, num_points)
        noises[ind] = scoreatpercentile(row_one[window_start:window_end],
                                        per=noise_perc)

    def filt_func(line):
        if len(line[0]) < min_length:
            return False
        snr = abs(cwt[line[0][0], line[1][0]] / noises[line[1][0]])
        if snr < min_snr:
            return False
        return True

    return list(filter(filt_func, ridge_lines))

def _boolrelextrema(data, comparator,
                  axis=0, order=1, mode='clip'):

    if((int(order) != order) or (order < 1)):
        raise ValueError('Order must be an int >= 1')

    datalen = data.shape[axis]
    locs = numpy.arange(0, datalen)

    results = numpy.ones(data.shape, dtype=bool)
    main = data.take(locs, axis=axis, mode=mode)
    for shift in xrange(1, order + 1):
        plus = data.take(locs + shift, axis=axis, mode=mode)
        minus = data.take(locs - shift, axis=axis, mode=mode)
        results &= comparator(main, plus)
        results &= comparator(main, minus)
        if(~results.any()):
            return results
    return results

