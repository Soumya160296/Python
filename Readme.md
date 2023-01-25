# Python concepts and syntax (Inner files)
##### This repository contains Python cenceptual notes with syntax & examples. Helpful for quick revision and to use as a cheetsheet.

### Main Contents
### 1.[Introduction to python](#1-introduction-to-python)
### 2. [Variable declaration, identifiers and data types](#2-variable-declaration-identifiers-and-data-types-1)
### 3. [Python opearators](#3-python-operators)
### 4. [Data Structures](#4-python-data-structures)
### 5. [Input outputs](#5-taking-input-and-printing-output)
### 6. [Conditional and Control Statements](#6-conditional-and-control-statements-1)

---

## [1. Introduction to python*](/Introduction/README.md)
- Characteristics and advantages of python
- General programming paradigm

## [2. Variable declaration, identifiers and data types*](/Variables_and_DataTypes/README.md)
- Variable declaration
- How to declare variables and initialize variables(assign values)
- Python Identifiers
- Naming conventions for Python identifiers
- Python Data types
- Dealing with strings

#### Dealing with string data type
[File showing syntax and examples.](/Variables_and_DataTypes/dealingwithString.ipynb)
- Single string
- Multiple string
- String slicing
- Modify strings: lower(), upper(), strip()
- Split a string
- Join strings
- Check the presence of a character(s) in a string.

#### Other string methods
[Find out what else we can do with strings](https://www.w3schools.com/python/python_strings_methods.asp)

## 3. Python operators*
#### 3.1 Arithmatic Operator
```
e.g:
% modulus operator, a%b gives the remainder of a/b
** power operator, a**3 means cube of a.
# or, 
pow(a,3) means cube of a

// floor division operator. (Gives division results in integer and ignores the remainder)
```
#### 3.2 Assignment operator
```
x += 3 ---> means x = x+3
```
#### 3.3 Comparision operator 
e.g: == Equal   
 != Not equal
#### 3.4 Logical operator (and, or, not)
#### 3.5 Identity operator
```
>> x is y       # this return True if x and y are exactly same object.
a= ['q',3,43]
b= ['q',3,43]
c = b
print(a is b)    # Returns False
print(c is b)    # Returns True

# Another identity operator is: x is not y
```
#### 3.6 Membership operator
```
if x in list:
   print('True')
else: 
   print('False)

# Similarly another membership operator is: not in
```
#### 3.7 Bitwise operator
Deals with binary bits.

AND - Binary AND operation

NOT - Binary NOT operation

[More about python operators](https://www.w3schools.com/python/python_operators.asp)


## [4. Python data structures*](DataStructures/README.md)
- list, tuple, dict, set
- Basic differences.
- How to access elements from them.
- In which situation, which one to use!


## [5. Taking input and printing output*](InputOutputs/README.md)
- Taking multiplt inputs for different variables
- Taking mutiple inputs for the same variable.
- **Optimized way to print multiple strings and variables together**

## [6. Conditional and control statements*](/IfElseForWhile/README.md)
- Short hand if
- Short hand if else
- For loop and else
- While loop and else
- For loop vs While loop
- Break vs Continue

