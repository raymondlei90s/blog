---
layout: post
title: Introduction to Python
categories: [Python]
---

Learning Python with virtual environment

```sh
[sudo] pip install virtualenv
source bin/activate
deactivate
```

Read Documentations [Here](https://virtualenv.pypa.io/en/stable/userguide/#usage)
Check my script collections [Here](https://github.com/raymondlei90s/Python-Playground)

## Python Basics

![python-math-operator]({{ site.baseurl }}/images/Python/python-math-operator.png)
![python-common-datatype]({{ site.baseurl }}/images/Python/python-common-datatype.png)
![python-variable-names]({{ site.baseurl }}/images/Python/python-variable-names.png)

### String concatenation

```python
>>> 'Alice' + 'Bob'
'AliceBob'

>>> 'Alice' + 42 #Error

>>> 'Alice' * 5
'AliceAliceAliceAliceAlice'

>>> 'Alice' * 'Bob' #Error

>>> 'Alice' * 5.0 #Error
```

### Common functions

```python
print('what is your name?') # This is comment

myName = input()

print('It is good to meet you, ' + myName)

print('The length of your name is: ')
print(len(myName))

str()
int()
float()
```

## Flow control

### Boolean values

![comparison-operators]({{ site.baseurl }}/images/Python/comparison-operators.png)

### Boolean Operators

![boolean-and-operator]({{ site.baseurl }}/images/Python/boolean-and-operator.png)

![boolean-or-operator]({{ site.baseurl }}/images/Python/boolean-or-operator.png)

![boolean-not-operator]({{ site.baseurl }}/images/Python/boolean-not-operator.png)

### If Statement

```python
if name === 'Alice':
  print('Hi, Alice')
elif age < 12:
  print('You are not Alice, kiddo.')
else:
  print('Hello, stranger.')
```

### Loops

```python
spam = 0
while spam < 5:
  print('hello.')
  spam = spam + 1 # break, continue, applies

for i in range(5) # range([start], end, [step])
  print('Count (' + i + ')')
```

## Functions

```python
def hello():
  print('Howdy!')

hello() # Function call

def hello(name):
  print('Hello ' + name)

hello('Bob') # Function call with arguments
```

### The None Value
```python
>>> spam = print('Hello!')
Hello!
>>> None == spam
True
```

### Keyword Arguments and print()

```python
print('Hello')
print('World')
# output:
# Hello
# World

print('Hello', end='')
print('World')
# output:
# HelloWorld

>>> print('cats', 'dogs', 'mice')
cats dogs mice

>>> print('cats', 'dogs', 'mice', sep=',')
cats,dogs,mice

```

### Local and Global scopes applies
```python
def spam():
  global eggs # global keyword to make changes in local scopes
  eggs = 'spam'
def bacon():
  eggs = 'bacon' # this is local var

eggs = 'global'  
spam()
print(eggs)
```

### Exception
```python
def spam(divideBy):
  try:
    return 42/divideBy
  except ZeroDivisionError:
    print('Error: Invalid argument.')
```
