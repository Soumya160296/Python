# Functions in Python
A function is a block of code which only runs when it is called. A function is created as a procedure to perform a specific task.

**Note**:
- foo = File or Object. It is used as a place holder of an object variable or file name.
### Contents
1.[Basics of functions](#1-basics-of-functions-in-python)

&nbsp; &nbsp; &nbsp; 1.1 [Types of arguments](#11-types-of-arguments)

2.[Special functions](#2-special-functions)

&nbsp; &nbsp; &nbsp; 2.1 [Recursive functions](#21-recursive-functions)

&nbsp; &nbsp; &nbsp; 2.2 [Nested functions](#22-nested-functions)

&nbsp; &nbsp; &nbsp; 2.3 [Decorators](#23-decorators)

&nbsp; &nbsp; &nbsp; 2.4 [Generators](#24-generators)

&nbsp; &nbsp; &nbsp; 2.4 [Lambda and map](#25-lambda-and-map-function)

---

### [1. Basics of functions in Python](/FunctionsInPython/Basics_of_functions_in_Python.ipynb)
- A function is defined using ```def``` keyword.
- In python a function may or may not return someting.
- We must need to call the function to run the function for a task.
- **Parameters**: We can create a function with some predefined variables. This variables are called parameters.
- **Arguments**: The values passed to the parameters when a function is called are known as arguments.

- In terms of functions or procedural programming the variables are known as parameters and values to them are known as arguments.
```
# define a function
def function1(name):
  print(f"Hello {name}, let's study about python functions")
  return None

#call the function
function1('Shakh')
```
- Here in the above code of block, function1() is the function. It returns nothing. 'name' is parameter of the function. And 'Shakh' is the argument passed to the parameter 'name'.


### 1.1 Types of arguments

- We can include as many parameters in a function as we want. 
- If a function is defined with 5 parameters, the function should be called with same no. of arguments i.e. 5 arguments, not more not less.



#### 1.1.1 Default arguments 
- We can define a function with default parameter value  or default argument like this.

```
#define a function with default parameter value
def fun2(name = 'Shakh'):
    print('Hello Bro! Mr.',name)

#Now we can call the function without any argument
fun2()

# Or we can call the function with our own argument
fun2('Sultan')
```

#### 1.1.2 Arbitary arguments

- If we do not know how many arguments that will be passed into the function, we can add  * (called **Arbitary argument**) before the parameter name in the function definition.

- This way the function will receive a tuple of arguments, and can access the items accordingly.
```
#define a function with arbitary arguments
def my_function(*names):
    for i in range(len(names)):
        print(f'Hello {names[i]}')
    return None

# Call the function for 3 names
print(my_function('Alo', 'Bilo', 'Cilo'))
```
#### 1.1.3 Keyword arguments and Positional arguments
- Lets say we defined a function with 3 parameters. 
- Normally, when there are multiple parameters, respective arguments should be passed with a synchronised order with the parameters.

```
#define a function
def func(p1,p2,p3):
   print(p1,p2,p3)

#call the function
func(23,45,38)
#Here, 23 will be passed to p1, 45 to p2, 38 to p3. Means in ordered format.
```

- But we can pass some argument using ``` key = value ``` format. If we pass an argument in this format, it is known as keyword argument.

- **When we pass all arguments as keyword arguments then order does n't matter.** 
E.g:
```
func(p2 = 45, p1 = 23, p3 = 38)
```
- Also, what we can do, We can pass some arguments in ```key = value``` format and some other as normal arguments  as shown below.
```
func(23,45,p3= 38)

#here 23 is passed to p1 and 45 to p2 and ofcourse p3 = 38
# Here, p1,p2  are the parameters with positional arguments. Because their values are specified in ordered position.

``` 
- When we pass some arguments as keyword arguments and some arguments not as keyword arguments in the same function then the arguments passed in normal format are called **positional arguments**.

### Note: positional argument follows keyword argument
- This means that all the positional arguments should be specified first and then specify the keyword arguments.
- In any function call positional arguments should follow the order as parameters order in the function definition.
- The keyword arguments should be at the last.

### 2. Special functions
### [2.1 Recursive functions](/FunctionsInPython/RecursiveFunctions.ipynb)

- Recursive function is a function where the defined function can call itself.

- As a recursive function calls itself we can loop through data to reach a result.

- But we should be very careful with recursion as it can be quite easy to slip into writing a function which never terminates, or one that uses excess amounts of memory or processor power.

E.g:
```
def calculateFactorial(n):
    if n==0:
        result=1
    else:
        result=n*calculateFactorial(n-1)
    return result
a=calculateFactorial(4)
```
- The difference b/w iteration and recursion is - there is no sequential end to recursive code. It tests on a base condition and can go on as long as that is satisfied. 
- Recursion in python is used when problems can be broken into simpler parts for easier computation and more readable code.

### Types of Recursions
1) Direct Recursion - In this type of recursion, the function calls itself.
- **Tail Recursion:** If the recursion function call is the last statement to be executed then it is called tail-recursion.
- E.g: In the recursive function below the sequence of execution will be dispn(5) --> print 5 --> dispn(4) then print 4 and so on.
- I.e. once the printing of 5 is done then it will execute the recursive call dispn(4)
```
def dispn(n):
    if n == 0:
        return  # Base case
    print(n)
    dispn(n - 1)  # Tail Recursive Call

dispn(5)
```




- **Non-tail recursion/Head recursion**: If the recursive function is not executed as the last statement of the function then it is called as non-tail recursive.

- E.g: 
```
def dispn(n):
    if n == 0:
        return  # Base case
    dispn(n - 1)  # Not a Tail Recursive Call
    print(n)

dispn(5)
```
- Here sequence of execution is --> dispn(5), dispn(4), dispn(3), dispn(2), dispn(1). After this it will not go further because of the logic ``` if n== 0: return ```. And after all this it will start executing the print statements in LIFO order. So here recursion call is executed not as the last execution step.

2) Indirect recursion
- In this type of recursion, the function calls another function which calls the original function

```
def A(n):
    if n > 0:
        print("", n, end='')
        B(n + 1)

def B(n):
    if n > 1:
        print("", n, end='')
        A(n - 5)

A(20)
```

### [2.2 Nested functions](/FunctionsInPython/NestedFunctions.ipynb)

**Nested functions are functions that we define inside other functions.**

- The outer function is also called enclosing function.
- The inner function is also called nested function.
- The variables that are decalred inside the inner function are local variables for it. 
- If a variable is declared inside the outer function but not inside the inner function, it is a **non-local variable** for the inner function.
It is also called **enclosing variable or enclosing scope or global scope**.


- [The inner function can access the variables of the enclosing function but can't modify them normally.](/FunctionsInPython/NestedFunctions.ipynb)

**Notes:**
- In python everything is an object. A function is a first-class object. We can pass a function as a parameter to another function.
- A function can return another function. When a function returns another function then the concept of closure.

**Closures:** 
- Closure is defined as a function object that remembers the variable of enclosing function even if it is not present in memory.


#### Criteria to define closures:
- It is necessary to have nested function.
- Nested function should refer to variables from enclosing function.
- Nested function must returned by enclosing function.

Example:
```
#define a outer function
def squareOfSquare(x):
    
    s = x**2
    
    #define an inner function
    def raisePower(power):
        squareOfSquare_ = s**power
        #inner function refering to the enclosing function variable.

        return squareOfSquare_

        #delete s
        del globals()['s']

    return raisePower(2)
    #Here outer function is returning the inner function

#call the outer function 
squareOfSquare(2)
```
- When the interpreter detects the dependency of inner nested function on the outer function, it makes sure that the variables in which inner function depends on are available even if the outer function goes away.

- If we delete the outer function then technically the variable y should vanished away with outer function,but variable y still bound to the inner function.

### [2.3 Decorators](/FunctionsInPython/Decorators.ipynb)
A decorator in Python is a function that takes another function as an argument and extends its behavior without explicitly changing the defination of the original function.

**A decorator adds new functionality to a function without changing the original defiantion**
- We can specify a decorator function using the syntatic sugar '@decorator_function_name' before the function we want to decorate or modify.

Example: 
```
@modified_division     #modified_division is a decorator
def divide(a, b):
    return a/b

#now define the decorator to modify the function passed to it.
def modified_division(a_function): 

    def improvedDivision(a, b):  

        print("Divide", a, "by", b)

        if b == 0:
            print(f'You entered b = {b}. Division by {b} is not defined.')
         
            b=random()
            print('So b is replaced with,b=',b)
            
        return a_function(a, b)

    return improvedDivision


#call the divide function
divide(4,0)
```

### [2.4 Generators](/FunctionsInPython/generatorFunctions.ipynb)
**A generator function is kind of iterative funtion which can be called as a loop.**

- In a generator function, a yield statement is used rather than a return statement.
- A generator function doesn't return a direct value, but it returns an iterable object.
- we can use ``` next()``` to get the values from the iterative object retunred by the generator.

Example:
```
def genfun():
    yield 'A'
    yield 'B'
    yield 'C'

f1 = genfun()

next(f1)   #it will print 'A'

next(f1)   # it will print 'B'
```
### yield vs. return
- If we include both 'yield' and 'return' in a generator function, then 'return' statement will terminate the function.
- The difference between yield and return is that yield returns a value and pauses the execution while maintaining the internal states.
- Whereas the return statement returns a value and terminates the execution of the entire function.

### Generator expression
```
squres = (pow(x,2) for x in range(1,6))
#This is different from list. It is not list, it is a generator
print(type(squres))
```
Note that: It is different from list, because it is an generator object.

Advantages of generator function:
1. If we need to create iterative objects generator function acts faster than normal for loop or while loop iteration and takes less memory.
2. Best use to read data from large files
3. Suitable for web scrapping and crawling.

### [2.5 Lambda and map() function](/FunctionsInPython/SpecialFunctions.ipynb)

### lambda  function
A lambda function is an anonymous function which is defined without a name (instead keyword ```lambda``` is used). It can take any number of arguments but, evaluates and returns only one expression.

#### Syntax:
```
lambda arguments : return_expression
```
<h4> Example: greatest of two numbers </h4>

<pre>
greatest = lambda num1,num2: num1 if num1>num2 else num2

#call the function
greatest(10,20)
</pre>
