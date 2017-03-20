+++
date = "2017-03-18T14:37:12+13:00"
title = "Debugging Python"
tags = ["python"]
categories = ["python"]

+++

**Note:** this is still a draft...

### Name errors (usually typos)


```python

from turtle import *
from random import *

def randomcolour():
    red = randint(0, 255)
    green = randint(0, 255)
    blue = randint(0, 255)
    color(red, green, blue)

def randomplace():
    x = randint(-100, 100)
    y = randint(-100, 100)
    goto(x, y)

shape("turtle")
randomcolour()
```

### Indentation
