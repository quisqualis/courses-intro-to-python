---
title: Functions
key: e523cc7552c034ad3633861a12d8062a

video_link:
    hls: https://videos.datacamp.com/transcoded/735_intro_to_python/wb1/hls-ch3_1.master.m3u8
    mp4: https://videos.datacamp.com/transcoded_mp4/735_intro_to_python/wb1/ch3_1.mp4



--- type:TitleSlide key:5204234d8b
## Functions

*** =lower_third
name: Filip Schouwenaars
title: Instructor, DataCamp

*** =script
In this video, I'm going to introduce you to functions. 


--- type:FullSlide key:3760ea4020
## Functions

*** =part1
- Nothing new! {{1}}
- `type()` {{2}}
- Piece of reusable code {{3}}
- Solves particular task {{4}}
- Call function instead of writing code yourself {{5}}

*** =script
Functions aren't entirely new for you actually: you've already used them. type, for example, is a function that returns the type of a value. But what is a function? Simply put, a function is a piece of reusable code, aimed at solving a particular task. You can call functions instead of having to write code yourself. Maybe an example can clarify things here.



--- type:TwoRows key:0ea3c3d8fe
## Example

*** =part1
```
In [1]: fam = [1.73, 1.68, 1.71, 1.89]

In [2]: fam
Out[2]: [1.73, 1.68, 1.71, 1.89]
```{{1}}
```
In [3]: max(fam)
Out[3]: 1.89
```{{2}}

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/fn_example_1.png){{3}}
*** =script
Suppose you have the list containing only the heights of your family, fam:

Say that you want to get the maximum value in this list. Instead of writing your own piece of Python code that goes through the list and finds the highest value, you can also use Python's max() function. This is one of Python's built-in functions, just like type(). We simply pass fam to max() inside parentheses:

The output makes sense: 1.89, the highest number in the list.

max() worked kind of like a black box here: you passed it a list, then the implementation of max(), that you don't know, did its magic, and produced an output. How max() actually did this, is not important to you, it just does what it's supposed to, and you didn't have to write your own code, which made your life easier.





--- type:FullSlide key:16d6e1da4b disable_transition:true
## Example

*** =part1
```
In [1]: fam = [1.73, 1.68, 1.71, 1.89]

In [2]: fam
Out[2]: [1.73, 1.68, 1.71, 1.89]

In [3]: max(fam)
Out[3]: 1.89
```

```
In [4]: tallest = max(fam)

In [5]: tallest
Out[5]: 1.89
```{{1}}

*** =script
Of course, it's possible to also assign the result of a function call to a new variable, like here. Now tallest is just like any other variable; you can use to continue your fancy calculations.



--- type:FullSlide key:cf058cf372
## `round()`

*** =part1
```
In [6]: round(1.68, 1)
Out[6]: 1.7
```{{1}}
```
In [7]: round(1.68)
Out[7]: 2
```{{2}}
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```{{3}}

*** =script
Another one of these built-in functions is round(). It takes two inputs: first, a number you want to round, and second, the precision with which to round, so how many digits behind the decimal point you want to keep. Say you want to round 1.68 to one decimal place. The first input is 1.68, the second input is 1. You separate the inputs with a comma:

But there's more. It's perfectly possible to call the round() function with only one input, like this. . This time, Python figured out that you didn't specify the second input, and automatically chooses to round the number to the closest integer.

To understand why both approaches work, let's open up the documentation. You can do this with yet another function, help, as follows:

--- type:TwoRows key:8ff481a989
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_1.png) {{1}}

*** =script
It appears that round() takes two inputs. In Python, these inputs, also called arguments, have names: number and ndigits.



--- type:TwoRows key:f9715d4344 disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_2.png)

*** =script
When you call the function round(), with these two inputs, Python matches the inputs to the arguments: 
--- type:TwoRows key:e130a52794 disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_3.png)

*** =script
number is set to 1.68



--- type:TwoRows key:9b5fa99417 disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_4.png)

*** =script
and ndigits is set to 1. 


--- type:TwoRows key:1c4e3e4755 disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_5.png)

*** =script
Next, The round() function does its calculations with number and ndigits as if they are variables in a Python script. We don't know exactly what code Python executes. 



--- type:TwoRows key:183848f1d7 disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_6.png)

*** =script
What is important, though, is that the function produces an output, namely the number 1.68 rounded to 1 decimal place.


--- type:TwoRows key:450e5e2ee4
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_7.png) {{1}}

*** =script

If you call the function round() with only one input,

--- type:TwoRows key:c458f7e61b disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_8.png)

*** =script
Python again tries to match the inputs to the arguments.


--- type:TwoRows key:b7848d7f3d disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_9.png)

*** =script
There's no input to match to the ndigits argument though. 

--- type:TwoRows key:a33f6fe5e2 disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_10.png)

*** =script
Luckily, the internal machinery of the round() function knows how to handle this. 


--- type:TwoRows key:d6cd99b054 disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```

*** =part2
![](https://s3.amazonaws.com/assets.datacamp.com/production/course_4550/datasets/round_11.png)

*** =script
When ndigits is not specified, the function simply rounds to the closest integer and returns that integer. That's why we got the number 2.



--- type:FullSlide key:d5a14cd4fe disable_transition:true
## `round()`

*** =part1
```
In [8]: help(round)   # Open documentation

#  Help on built-in function round in module builtins:
#
#  round(...)
#       round(number[, ndigits]) -> number
#
#       Round a number to a given precision in decimal digits 
#       (default 0 digits). This returns an int when called with 
#       one argument, otherwise the same type as the number. 
#       ndigits may be negative.
```
- `round(number)` {{1}}
- `round(number, ndigits)` {{2}}

*** =script
How was I so sure that calling the function with a single input would work? Well, in the documentation, there are square brackets around the comma and the ndigits here. This tells us that you can call round() in this form, as well as in this one. In other words, ndigits is an optional argument. Actually, Python offers yet another way to show that a function has optional arguments, but that's something for the exercises.


--- type:FullSlide key:0d4ff1139f
## Find functions

*** =part1
- How to know? {{1}}
- Standard task -> probably function exists! {{2}}
- The internet is your friend {{3}}

*** =script
By now, you have an idea about how to use max() and round(), but how could you know that a function such as round() exists in Python in the first place? Well, this is something you will learn with time. Whenever you are doing a rather standard task in Python, you can be pretty sure that there's already a function that can do this for you. In that case, you should definitely use it! Just do a quick internet search and you'll find the function you need with a nice usage example. And there is of course DataCamp, where you'll also learn about powerful functions and how to use them. 



--- type:FinalSlide key:dc622108df
## Let's practice!

*** =script
Get straight to it in the interactive exercises!
