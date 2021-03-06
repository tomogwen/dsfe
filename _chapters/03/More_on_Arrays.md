---
interact_link: notebooks/03/More_on_Arrays.ipynb
title: '3.6 More on arrays'
permalink: 'chapters/03/More_on_Arrays'
previouschapter:
  url: chapters/03/Ranges
  title: '3.5 Ranges'
nextchapter:
  url: 
  title: ''
redirect_from:
  - 'chapters/03/more-on-arrays'
---

# More on Arrays

It's often necessary to compute something that involves data from more than
one array. If two arrays are of the same size, Python makes it easy to do
calculations involving both arrays.

For our first example, we return once more to the temperature data.  This
time, we create arrays of average daily
[high](http://berkeleyearth.lbl.gov/auto/Regional/TMAX/Text/global-land-TMAX-Trend.txt)
and
[low](http://berkeleyearth.lbl.gov/auto/Regional/TMIN/Text/global-land-TMIN-Trend.txt)
temperatures for the decades surrounding 1850, 1900, 1950, and 2000.

First we get Numpy, renamed as `np`:



{:.input_area}
```python
import numpy as np
```


Next we create the array:



{:.input_area}
```python
baseline_high = 14.48
highs = np.array([baseline_high - 0.880,
                  baseline_high - 0.093,
                  baseline_high + 0.105,
                  baseline_high + 0.684])
highs
```





{:.output_data_text}
```
array([ 13.6  ,  14.387,  14.585,  15.164])
```





{:.input_area}
```python
baseline_low = 3.00
lows = np.array([baseline_low - 0.872, baseline_low - 0.629,
                 baseline_low - 0.126, baseline_low + 0.728])
lows
```





{:.output_data_text}
```
array([ 2.128,  2.371,  2.874,  3.728])
```



Suppose we'd like to compute the average daily *range* of temperatures for
each decade.  That is, we want to subtract the average daily high in the 1850s
from the average daily low in the 1850s, and the same for each other decade.

We could write this laboriously using `.item`:



{:.input_area}
```python
np.array([
    highs.item(0) - lows.item(0),
    highs.item(1) - lows.item(1),
    highs.item(2) - lows.item(2),
    highs.item(3) - lows.item(3)
])
```





{:.output_data_text}
```
array([ 11.472,  12.016,  11.711,  11.436])
```



As when we converted an array of temperatures from Celsius to Fahrenheit,
Python provides a much cleaner way to write this:



{:.input_area}
```python
highs - lows
```





{:.output_data_text}
```
array([ 11.472,  12.016,  11.711,  11.436])
```



<img src="{{ site.baseurl }}/images/array_subtraction.png">

What we've seen in these examples are special cases of a general feature of arrays.

### Elementwise arithmetic on pairs of numerical arrays

If an arithmetic operator acts on two arrays of the same size, then the
operation is performed on each corresponding pair of elements in the two
arrays. The final result is an array. 

For example, if `array1` and `array2` have the same number of elements, then
the value of `array1 * array2` is an array. Its first element is the first
element of `array` times the first element of `array2`, its second element is
the second element of `array1` times the second element of `array2`, and so
on.
