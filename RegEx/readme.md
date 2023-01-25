## Regular Expressions
A regular expression is a sequence of characters that makes a certain pattern and we look for that pattern in other strings or sets of strings.

Python has a builtin regex module ```re``` which we can import as ```import re```

### Contents
[1. Pattern matching functions](#1-pattern-matching-functions)

[2. Special Patterns](#2-special-pattern-maching)

[Password validation: A real application of pattern matching](/RegEx/regular1.ipynb)

---

### 1. Pattern matching functions
Lets say there is string as shown below 

```
string = 'Learning python is easy. Python is helpful. Now a days Python is in demand.'
```
Now we are looking for the word ```Python``` in the string. Let's say

```
pattern = 'Python'
```

We can use ```re.compile(pattern, flags=0)``` --> It returns the pattern as a pattern object.

Now we have several options to find the pattern in the string.

#### a) [re.match()](/RegEx/regular1.ipynb)

Syntax:

```
re.match(pattern, string)

#Or, using pattern as a pattern object

pattern.match(target_string, search_position) 
```
-  It checks the given pattern at the given position of the target string or by default in the begining.

- If no position is mentoned then re.match() looks for a matching pattern at the beginning of a string and will return a match object **only if the match is found at the starting of the string** otherwise it will return None.

- The match object contains information about the match, such as the matching string, **span(starting_index, ending_position)** etc.

#### b) [re.search(pattern, string)](/RegEx/regular1.ipynb)

- re.search() looks for a pattern in the entire string at any position, not at the begining only.

- Return a match object with match information for the 1st match found. 

- If no match found in the entire string then it returns None.

#### c) [fullmatch(pattern, string)](/RegEx/regular1.ipynb)

- Returns a match object with matching information when the pattern and the string fully matches with each other, i.e., the pattern and the string are exactly same.

- Otherwise it returns None, even if there is a partial match.

####  d) [finditer(pattern, string)](/RegEx/regular1.ipynb)

- It returns all the matching patterns from the entire string as a callable iterator object which can be iterated using a loop.

- If no matching found then returns None.

#### e) [findall(pattern, string)](/RegEx/regular1.ipynb)


- This returns all the matched patterns from the entire string in a  single list and we can print the list directly.


### [Other important functions of re module](/RegEx/regular1.ipynb)

- ```start() ``` --> gives starting index of a match

- ```end()``` --> gives the ending position (ending_index +1) of a match.

- ```group()``` --> returns the matched pattern itself.

- ```sub()```  --> substitute specified character with another specified character.

- ```subn()``` --> return the substituted string with no of characters replaced.

- ```split()``` --> splits a string using a separator/delimeter and returns a list of separated strings


### [2. Special pattern maching](/RegEx/regular1.ipynb)

- ```pattern = '[abc]'``` -->   looking for a string having a or b or c

- ```pattern = '[^abc]' ``` --> looking for a string or character  except a and b and c

### Meta characters

Pattern with meta characters | What it means
----------|---------------
``` [abc]```  | look for a string having a or b or c.
```[^abc]```| looking for a chracter except a and b and c
```^word``` | to check whether a string starts with this "word" or not.	
```word$```|  to check whether a string ends with this "word" or not.
``` "word1\|word2" ``` | 	Either "word1" or "word2" is there in the string.

### Quantifiers

Quantifiers are symbols used in pattern matching to findout machting characters/patterns according to number of occurances.

- ``` a ``` --> look for exactly 1 'a' in the string.

- ``` a+ ``` --> look for at least 1 'a'

- ``` a* ``` --> look for any number of a's including zero number of a's

- ``` a? ``` --> look for at most 1 'a' so, may be zero number of  'a' or 1 'a'

- ```a{m}``` --> look for exactly m number of 'a's

- ``` a{m,n} ``` --> look for minimum m number of a's and maximum n number of a's in the string.


### Pre-defined special pattern of classes
- ```\s```   --> search for space

- ```\S```  --> search except space

- ```\d``` -->  search digits

- ```\D ``` --> search except digits

- ```\w ``` --> any word character like uppercase, lowercase or alphanumeric digits.

- ```\W``` --> anything except words, special characters
