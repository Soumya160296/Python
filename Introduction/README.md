# Introduction to python.
### 1.1 Characteristics and advantages of python.
- Python is a high level **interpreted language** that executes each statement line by line using an interpreter. Python does not use any compiler.
- It is a **scripting language** because it does not require to compile the code before execution but it interprets the code directly. For example, a C program needs to be compiled before running, but in Python each line is interepreted directly.
- In python when we declare a variable we don't need to specify the data type of the variable. Data type of the variable is automatically declared by the interpreter by interpreting the value given to it during execution. Hence, Python is called a **dynamically Typed Language.**
- Syntax is easy to understand. Does not require semicolon at the end of a statement.
- Python does not use braces({}) to indicate blocks of code for class or function 
or flow control. Blocks of code are denoted by **line indentation and indentation is must**.
- It is case sensitive i.e python and Python are different.
- It is object oriented programming language.
### 1.2 General programming paradigm
- Python does not require to define an overall class or function. We can do basics stuff without using any function or class.
- #This  is a comment in python.
#### Multiline statements
```
total = item_one + \
item_two + \
item_three
```
#### Multiple statement in a single line
```
import sys; x = 'foo'; print(x + 'woo')
```

### Important note
**In python back-end, the variables that have same value are considered as the same single variable, they are just reffered with different names in the front end.**

For example:
```
a = 10
b = 10
``` 
Here for python, a and b is the same variable, just it has two different names.

And, 
```
a = 10 
a = 12
```
Here a = 10, a = 12 are two different variables in the backend, but we are just reffering both with the same name. 

**So in python variables are differentiated by values, not by names.**