# [Inputs](#taking-inputs) and [Outputs](#multiple-inputs-for-a-single-variable) in Python
## [Taking inputs](inputs.ipynb)
We can take user imputs using input() function.

e.g:
```
inp = input('Enter your name')
print('Hello ', inp)
```
### Taking input as a specific data type
Sometimes it is important to specify the data type of the input we are taking.
```
num = int(input('Enter a number'))
```

### Taking multiple inputs

We can take multiple inputs using a single input() function and then we can split the inputs into single values.

#### If we need to take different inputs for different variables at the same time. 
```
x,y,z = input('Enter the numbers:').split(',')

# Here we need to enter the inputs separated by comma delimeter.
```
#### Multiple inputs for a single variable

#### Way 1: Using a list and split() function if necessary 
```
x = [int(x) for x in input('Enter the values for x')]
#take input from the input function convert it into an specified data type and add into a list.
for i in range(len(x)):
    print('x = ',i )
```
- In this method we dont need to enter the values separated by a delimeter if we don't use the split() function. 
- If necessary we can use split() function with this method also if we want to enter the values separated by a delimeter. 
- But most of the time it is not required because when we enter 12345678 by default python will add one by one to the list not 12345678 as a single element.

#### Way 2: Using map() class
```
map(fun, iterable)
```
The map class applies the specified function fun() to each item of the iterable and returns a interable map object.

So we can use the map class to take multiple inputs for the same variable as shown below.

```
x = map(int, input("Enter multiple values: "))

# x will be a map objec which is again an iterable. We can extract values from x using a loop

for i in x:
    print('x = ' , i)

# Too avoid the loop we can convert the map object into a list at the initial stage like

x = list(map(int, input("Enter multiple values: ").split()))
```


## [Printing Outputs](outputs.ipynb)
- Optiized way to print multiple strings and variables together.
- [Check the file for more details.](outputs.ipynb)