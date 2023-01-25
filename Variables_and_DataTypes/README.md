### 2.1 Variable declaration
- Variables are nothing but reserved memory locations to store values. It means that when we create a variable, we reserve some space in the memory to store values.
- Python variables do not need to declare variables before using it. The declaration happens automatically when we use a variable and assign value to it. The equal sign (=) is used
to assign values to variables.
> ### How to declare variables and initialize variables(assign values)
- Declaration happens automatically when we assign values to the variables.
```
x = 10
y = 20

# or
x , y = 10, 20
```

- By default python interpreter can understand the data type of the variable once a value is assigned. So we don't need to specify the data type but sometime to be sure about the data type we can specify it.
- Since python is dynamically typed language so variables and data types are checked during interpretation.

### 2.2 Python Identifiers
A Python identifier is a name given by the programmer to identify a variable, function, class, module or other object. 
- An identifier starts with a letter A to Z or a to z or an underscore (_) followed by zero or more letters, underscores and digits (0 to 9).
- Python does not allow punctuation characters such as @, $, and % within identifiers.

#### 2.2.1 Naming conventions for Python identifiers-
- Class names start with an uppercase letter. All other identifiers start with a lowercase letter.
- Starting an identifier with a single leading underscore indicates that the identifier is private.

- Starting an identifier with two leading underscores indicates a strong private
identifier.
- If the identifier also ends with two trailing underscores, the identifier is a languagedefined special name.

### 2.3 Python Data types
Python has the following data types built-in by default, in these categories:

- **Text/String Type:**	str
- **Numeric Types:**	int, float, complex
- **Boolean Type:**	bool
- **Sequence Types:**	list, tuple, range
- **Mapping Type:**	dict
- **Set Types:**	set, frozenset
- **Binary Types:**	bytes, bytearray, memoryview
- **None Type:**	None
