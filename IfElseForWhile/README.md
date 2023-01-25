### Contents
### 1. [Conditional Statements-if-else](#1-if-else)
&nbsp;&nbsp;  1.5 [Short hand if (Just like single if)](#15-short-hand-if)

&nbsp; &nbsp;1.6 [Short hand if-else](#16-short-hanf-if-else)

### 2. [Control Statement - for loop](#2-for-loop)
&nbsp; &nbsp; 2.1 [For loop with else](#21-for-loop-and-else)
### 3. [Control Statement - while loop](#3-while-loop)
&nbsp; &nbsp; 3.1 [While loop with else](#31-while-loop-with-else)
### 4. [For loop vs While loop](#4-for-loop-vs-while-loop-1)
### 5. [Break VS continue](#5-break-vs-continue-1)


Note: In python if-else or for loop or while loop indentation is must.

### 1. IF-ELSE

Remember that we can implement unlimited **nested if-else** statements.

[File: if-else examples](if_elif_else.ipynb)

### 1.1 Just if
```
a = 33
b = 200
if b > a:           #if this is true do the following
  print("b is greater than a")
```
### 1.2 if-elif  (multiple conditions)
```
a = 33
b = 33
if b > a:         # If this is true
  print("b is greater than a")

# If the first condition is false, check this one

elif a == b:    
  print("a and b are equal")
```
### 1.3 if-else (Condition -otherwise)
```
a = 33
b = 200
if b > a:     # if this is true do the following
  print("b is greater than a")
else:         # otherwise do this
  print("b is not greater than a")
``` 

### 1.4 if-elif-else (multiple conditions-otherwise)
```
a = 33
b = 33
if b > a:         # If this is true
  print("b is greater than a")

# If the first condition is false, check this one

elif a == b:    
  print("a and b are equal")

# If all conditions are false then do this.
else:     
  print('b is less than a')
```
### 1.5 Short hand if
It is like just a if statment bu in the same line.
```
if True: print("Yes, It's true") 
```
### 1.6 Short hanf if-else
```
a, b = 12,10
print(f'{a} is greater than {b}') if a>b else print('No it is not greater than')
```
## Control Statements
[File to see the examples](ForndWhileLoop.ipynb)
### 2. for loop
A for loop is used for iterating over a sequence like a range, that a list, a tuple, a dictionary, a set, or a string.
- The loop is executed once for each element in the range/list/tuple/dict/string.

Example:
```
for x in range(6):
  print(x)
```
- We can implement nested for loops.

### 2.1 For loop and else
- The else keyword in a for loop specifies a block of code to be executed only when  the for loop is completely executed.

- **The else block will NOT be executed** if the loop is stopped by a break statement.

Best Example: Finding prime numbers.
### 3. while loop
- A while loop is executed only when a given condition is true.
- We can execute a while loop by a condition unless and untill the condition becomes false.

e.g:
```
i = 1
while i < 6:
  print(i)
  i += 1
```
### 3.1 While loop with else
A while works as long as a condition is True. So we can use a 'else' statement to execute when the condition becomes false.
- Like in For, else block in While loop is executed when the main while loop is completely done and when condition becomes false.
- If we use a break statement in the while loop the else block will not be executed.

[See the examples](ForndWhileLoop.ipynb)

### 4. For loop vs While loop
For loop | While loop
---------|-----------
It depends on the number of iteration not on a condition. | It depends on the condition. It works only when the condition is true.
If we gonna execute the for loop using a range of numbers, we don't need to declare the numbers before. | If we gonna use any number to set a condition in while loop, we must declare it before.
Numbers are incremented/decremented automatically. | In while loop we need to increment/decrement the number manually.

### 5. Break vs Continue
- Break statement breaks the loop completely. 
- Continue statement breaks the current iteration of the loop and continues to next iteration. 
- Continue just stops the execution of the statements below it in a loop, but doesn't stop the loop completely.