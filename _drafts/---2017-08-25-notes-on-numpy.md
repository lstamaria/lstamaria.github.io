---
layout: post
title: "Notes on NumPy"
date: 2017-08-25
---

My notes on [NumPy](http://www.numpy.org/):

%matplotlib
> integrates matplotlib module to Notebook 

test_list = list(range(1000))
> 

import numpy as np

test_array = np.arange(1000)

%timeit sum((test_list))

%timeit np.sum(test_array)

a = np.array([-1, 0, 1, 100], dtype='int8')

a

a / 0

1 / 0

100 ** 2

100 ** 4

100 ** 8

100 ** 10

a ** 2

b = a.astype('float32')

b

b / 0

np.nan == np.nan
> results to "False"

np.isnan
> Helper function

np.isnan(np.nan)
> Results to "True"

> Access pattern

np.zeros

np.ones

np.empty

np.empty((2, 2))

a

a[0]
> Access first item

a[-1]
> Accesses the last item

a[0:2]
> Slicing

a[:2]
>

a[::2]
> Grab from beginning of array up to the last element of array

a[-1] = 5
> Inserts value to numpy array

a
>

b = np.arange(12).reshape(4, 3)
> Shorthand method 

b
>

a.shape
>

b.shape
>

b[2, 2]
>

b[:2, :2]
>

b[1:3, -1]
>

b[1:3, -1:]
> ":" means "everything"; from 1-ith to 2-ith of first dimension and from last-ith to everything of second dimension

b.shape
>

b[1:3, -2]
>

b
>

(2)
>

2,
>

b[:1, :1]
>

b.shape
> Looks into a-ith of first dimension and b-ith second dimension

np.loadtxt?
>

c = np.arange(24).reshape(2, 3, 4)
>

c
>

c[1, 1, 1]
> Extracts value "17"

c[0, :, :]
>

c[1, 0, :]
>

c.flatten()
> from N-D to 1-D

a = np.arange(25).reshape(5, 5)
>

a
>

a[4, :]
>

a[-1, :]
>

a[:, 1::2] 
> Retrieves all from first dimension and performs step-size on second dimension

a[1::2, :3:2]
>


> Fancy indexing: (1) non-sequential integer location; (2) mask

a = np.arange(4)
>

a
>

a[[0, 3]]
>

 b[[0, 2], [2, 0]]
 >

c[[0], [1], [2]]
>

c[[0, 1], [1, 1], [2, 1]]
>

c > 16
>

c[c > 16]
>

d = c[:, 1:2, 1:3]
>

d
>

d.flags
>

d[0, 0, 0] = 1000
>

d
>

c
>

e = c[c > 16]
> Creates a new reference because of fancy indexing

e
>

c.strides
>

d
>

d.reshape(4, 1)
> 

d.T
>

c.flags

a = np.arange(25).reshape(5, 5)
>
a

>
a[[0, 1, 2, 3], [1, 2, 3, 4]]
>

a % 3
>

a % 3 == 0
>

a[a % 3 == 0]
>

from numpy import loadtxt, sum, where
import matplotlib.pyplot as plt
# Constants that indicate what data is held in each column of
# the 'dow' array.
OPEN = 0
HIGH = 1
LOW = 2
CLOSE = 3
VOLUME = 4
ADJ_CLOSE = 5
>

dow = loadtxt('/Users/lorenzostamaria/Dropbox/Notebooks/Numpy-Tutorial-SciPyConf-2017-master/exercises/dow_selection/dow.csv', delimiter=',')
>

dow
>

dow.shape
>

dow[dow > 5.5e9]
>

dow > 5.5e9
>

dow[:, 4]
>

dow[:, 4] > 5.5e9
>

mask = dow[:, 4] > 5.5e9
>

np.sum(mask)
>


