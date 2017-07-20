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

![python-math-operator]({{ site.baseurl }} /images/Python/python-math-operator.png)
![python-common-datatype]({{ site.baseurl }} /images/Python/python-common-datatype.png)
![python-variable-names]({{ site.baseurl }} /images/Python/python-variable-names.png)

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

![comparison-operators]({{ site.baseurl }} /images/Python/comparison-operators.png)

### Boolean Operators

![boolean-and-operator]({{ site.baseurl }} /images/Python/boolean-and-operator.png)

![boolean-or-operator]({{ site.baseurl }} /images/Python/boolean-or-operator.png)

![boolean-not-operator]({{ site.baseurl }} /images/Python/boolean-not-operator.png)
