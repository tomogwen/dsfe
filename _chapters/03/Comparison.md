---
interact_link: notebooks/03/Comparison.ipynb
title: '3.3 Comparison'
permalink: 'chapters/03/Comparison'
previouschapter:
  url: chapters/03/Strings
  title: '3.2 Strings'
nextchapter:
  url: chapters/03/Arrays
  title: '3.4 Arrays'
redirect_from:
  - 'chapters/03/comparison'
---

# Comparisons

A *Boolean* value is a value that can only be True or False.  It is called
"Boolean" after the mathematician and logician [George
Boole](https://en.wikipedia.org/wiki/George_Boole)

Boolean values most often arise from comparison operators. Python includes a
variety of operators that compare values. For example, `3` is larger than `1 +
1`.



{:.input_area}
```python
3 > 1 + 1
```





{:.output_data_text}
```
True
```



The value `True` indicates that the comparison is valid; Python has confirmed
this simple fact about the relationship between `3` and `1+1`. The full set of
common comparison operators are listed below.

| Comparison         | Operator | True example | False Example |
|--------------------|----------|--------------|---------------|
| Less than          | <        | 2 < 3        | 2 < 2         |
| Greater than       | >        | 3>2          | 3>3           |
| Less than or equal | <=       | 2 <= 2       | 3 <= 2        |
| Greater or equal   | >=       | 3 >= 3       | 2 >= 3        |
| Equal              | ==       | 3 == 3       | 3 == 2        |
| Not equal          | !=       | 3 != 2       | 2 != 2        |

Here are some more examples:



{:.input_area}
```python
4 < 5
```





{:.output_data_text}
```
True
```





{:.input_area}
```python
4 < 3
```





{:.output_data_text}
```
False
```





{:.input_area}
```python
4 <= 4
```





{:.output_data_text}
```
True
```



Notice the `==` in the table above.

The double equals ``==`` is different from the single `=` that we saw before
in assignment.   Here is assignment.



{:.input_area}
```python
a = 4
```


Notice it does not display a value.

``==`` is different - it's a comparison operator like `<` or `>`.  It checks
whether two values are equal, and returns True or False:



{:.input_area}
```python
a == 4
```





{:.output_data_text}
```
True
```



Strings can also be compared, and their order is alphabetical. A shorter
string is less than a longer string that begins with the shorter string.



{:.input_area}
```python
"Dog" > "Catastrophe"
```





{:.output_data_text}
```
True
```





{:.input_area}
```python
"Catastrophe" > "Cat"
```





{:.output_data_text}
```
True
```


