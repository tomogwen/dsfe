---
interact_link: notebooks/03/Ranges.ipynb
title: '3.5 Ranges'
permalink: 'chapters/03/Ranges'
previouschapter:
  url: chapters/03/Arrays
  title: '3.4 Arrays'
nextchapter:
  url: chapters/03/More_on_Arrays
  title: '3.6 More on arrays'
redirect_from:
  - 'chapters/03/ranges'
---

A *range* is an array of numbers in increasing or decreasing order, each
separated by a regular interval.  Ranges are useful in a surprisingly large
number of situations, so it's worthwhile to learn about them.

We will use the Numpy module, which we always rename as `np`, like this:



{:.input_area}
```python
import numpy as np
```


Ranges are defined  using the `np.arange` function, which takes either one,
two, or three arguments: a start, and end, and a 'step'.

If you pass one argument to `np.arange`, this becomes the `end` value, with `start=0`, `step=1` assumed.  Two arguments give the `start` and `end` with `step=1` assumed.  Three arguments give the `start`, `end` and `step` explicitly.

A range always includes its `start` value, but does not include its `end` value.  It counts up by `step`, and it stops before it gets to the `end`.

    np.arange(end): An array starting with 0 of increasing consecutive integers, stopping before end.



{:.input_area}
```python
np.arange(5)
```





{:.output_data_text}
```
array([0, 1, 2, 3, 4])
```



Notice how the array starts at 0 and goes only up to 4, not to the end value
of 5.


    np.arange(start, end): An array of consecutive increasing integers from start, stopping before end.



{:.input_area}
```python
np.arange(3, 9)
```





{:.output_data_text}
```
array([3, 4, 5, 6, 7, 8])
```



    np.arange(start, end, step): A range with a difference of step between each pair of consecutive values, starting from start and stopping before end.



{:.input_area}
```python
np.arange(3, 30, 5)
```





{:.output_data_text}
```
array([ 3,  8, 13, 18, 23, 28])
```



This array starts at 3, then takes a step of 5 to get to 8, then another step
of 5 to get to 13, and so on.

When you specify a step, the start, end, and step can all be either positive
or negative and may be whole numbers or fractions.



{:.input_area}
```python
np.arange(1.5, -2, -0.5)
```





{:.output_data_text}
```
array([ 1.5,  1. ,  0.5,  0. , -0.5, -1. , -1.5])
```


