+++
date = "2017-03-18T14:36:12+13:00"
title = "Scratch vs Python Examples"
tags = ["scratch", "python"]

+++

This page is for comparing Scratch code to Python code to help you use your knowledge of one to help learn the other. They aren't as different as you might think.


## Comments

Comments are bits of text in the code that don't do anything and are there for helping people reading the code to understand it.

```blocks
// This is a Scratch comment.
// You can create them by right clicking on the script background or a code block.
```

```python
# This is a Python comment.
# Anything after a hash symbol (#) on a line is a comment
```

## Variables

### Set a number variable

```blocks
set (age) to [9]
```

```python
age = 9
```

### Set a text variable
In computer language a chunk of text is also called a **string**

```blocks
set (name) to [Scratch]
```

In Python, a string variable needs to be wrapped in quote marks. They can be either single or double quotes.
```python
name = 'Scratch'
```
or
```python
name = "Scratch"
```
Double quotes are good if you want to put a single quote or apostrophe in your string:
```python
telling_off = "Don't pick your nose!"
```
Otherwise Python can't tell the difference between the apostrophe and the end of the string.

### Add a number on to a variable (the long way)

```blocks
set (score) to ((score) + (10))
```

```python
score = score + 10
```

### Add a number on to a variable (the short way)

```blocks
change (score) by [10]
```

```python
score += 10
```

### Subtract a number from a variable (the short way)

```blocks
change (score) by [-10]
```

```python
score -= 10
```

### Adding strings to each other

```blocks
set (full name) to (join (first name) (last name))
```

```python
full_name = first_name + last name
```


## Input and Output

### Display some text on the screen:

```blocks
say [Hello world!]
```

```python
print('Hello world!')
```

### Ask for some text and display it:

```blocks
ask [How many cookies can you eat?] and wait
say (join (answer) [ cookies is a lot! ])
```

```python
cookies = input('How many cookies can you eat?')
print(cookies + ' cookies is a lot!')
```

## Custom code

If you have some code that gets repeated a lot, it is a good idea to make a reusable block of code you can call from other bits of code. In Scratch these are called custom blocks, and in Python they are called functions. 


```blocks
define greeting (name)
say (join [Hello ] (name))

when flag clicked
greeting [Matilda]

```

In Python `def` is short for 'define function'
```python
def greeting(name):
    print("Hello " + name)

greeting('Matilda')
```

## Comparisons

Comparisons are tests where the answer can only be True or False. They can can be used as conditions in decisions or loops.

```blocks
< (age) = (10) > // Check age equals 10

< (age) > (10) > // Check age is greater than 10

< (age) < (10) > // Check age is less than 10

< not < (age) = (10) >> // Check age does NOT equal 10

< <(age) > (5)> and <(age) < (15)> > // Check age is greater than 5 and less than 15

```

```python
age == 10

age > 10

age < 10

age != 10

age > 5 and age < 15
```
In Python a double `==` is for comparing if two things are equal, while a single `=` is for setting a variable to a value.

## Decisions

### if then

Use this code when you want something to happen only if the condition is True.
```blocks
if < (age) > (20) > then
  say [You're old! ]
```

```python
if age > 20:
    print("You're old!")
```

### if then else

Use this code when you want two different things to happen depending on whether the condition is True or False.
```blocks
if < (age) > (20) > then
  say [You're old! ]
else
  say [You're young ]
```

```python
if age > 20:
    print("You're old!")
else:
    print("You're young")
```

## Loops

### Loop forever

```blocks
forever
  do something :: looks
```

```python
while True:
    something()
```

### Loop until

The Scratch loop runs while the condition is False, but the Python loop runs while the condition is True. This is why each one has a different condition.

```blocks
repeat until < (score) = (0) >
  do something :: looks
```

```python
while score > 0:
    something()
```

### Loop a number of times

```blocks
repeat (7)
  do something :: looks
```

```python
for i in range(7):
    something()
```

