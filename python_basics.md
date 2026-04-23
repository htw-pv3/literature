import numpy as np

def euler_Ver(f, y0, h, n):
    y = np.zeros(n+1)
    t = np.zeros(n+1)
    
    y[0] = y0
    t[0] = t0
    for k in range(n):
        y[k+1] = y[k] + f(t[k], y[k]) * h
        t[k+1] = t[k] + h
    return t, y