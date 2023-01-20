# Data Structures in Python.
Python has 4 inbuilt data structures.
- [list = []  # can be created as **list()**](#list)
- [tuple = ()  # can be created as **tuple()**](#tuple)
- [dictionary = {'key':'value'}   # can be created as **dict()**](#dictionary--keyvalue)
- [Set{}   # can be created as **set()**](#set--el1el2)
![](DataStructures.png)

## [Differences](differences.ipynb)

Property|List	| Tuple	| Dictionary |	Set
--------|-------|-------| -----------|-------
ordered | Yes   | Yes   |	Yes      | No
Slicing Possible? |Yes, list[2]| Yes, tupe[3]|Yes, dict['Key']| Not possible. But can be accessed as iterators.
Mutable/changeable|Yes | No | Yes | No direct replacement (add, remove, update), No-Frozenset
add/remove/replace new | Yes | No |Yes | set- Only add and remove, frozenset- No
Allow duplicates?| Yes | Yes | NO (No duplicate keys) | NO


### What means ordered ?
- Ordered means that, the items we included in a list will always follow the particular order as they are included, and that order will never change.

- If we add new items to a list, the new items will be placed at the end of the list.

### What means mutable ?
Mutable means value can be replaced or changed.

### Notes:
- Since dictionary doesnot allow duplicate value for a key, if we add multiple key:value pair with same key name, the last key:value pair is considered and others are removed.

# list = []
- List items are ordered, changeable, and allow duplicate values.
- A list can contain items with different data types. There can be a list inside a list.
- We can defined a using list() or listName=[elements]

### To slice/access list items
```
listName[index]
```
- Index starts from 0. The last index is -1. 

- [See string slicing for more details](/Variables_and_DataTypes/dealingwithString.ipynb)

### Conditional slicing
```
listName[index_of_a_specific_item] > 300
# If true returns True, otherwise False
```

### To change/replace the values
```
listName[index] = newValue

e.g:
l[2] ='Quant'
```
- We can change multiple items at the same time by just mentioning the indeces.

### To see how many times a values appears in the list
```
Repeated_times = listName.count(specific_element)
```
### To reverse a list
```
l = [1,35,5,'2q',6,74,23]
print('Original list:',l)
l.reverse()   # If we do like r= l.reverse() it will return None
print('Reversed list:',l)
```
### To add a new element
```
# to add to the last position
listName.append(New_element)

# to add to specified index
listName.insert(index, new_element)
```

### To add all elements from another list/tuple
```
listName.extend(anotherListName)
# New list/tupe/any other iterable is extended to the end of the present list
```

### To join two lists
```
newList = list1 + list2
```

### To remove/delete items 
```
# Remove a specific item
listName.remove(listName[index])

# Remove an item by index position
listName.pop(index)   # By default index is -1.

#Delete item by index position
del listName[index]

# Delete the entire list

del listName

#or

listName.clear()

```
### Sorting the list items
```
listName.sort()  #By default in ascending order.

#or

listName.sort( reverse = True)  # to sort in descending order.

# To sort by a condition 

def makeNegative(n):
  return (-1*n)

thislist = [100, 50, 65, 82, 23]
#every element will be negative 

thislist.sort(key = makeNegative)
# arrange the negative numbers in ascending order--> smaller to higher.

print(thislist)
```

### Copy a list
```
# Lets say list1 is a list and we want to copy it

list2 = list1.copy()

# If we make a copy using list2 = list1, any changes to list1 will affect list2 also.
```

### Creating a new list using conditions
```
newlist = [expression for item in iterable if condition == True]
#e.g:
>> fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
>> newlist = [x for x in fruits if "a" in x]
```


# tuple()
- tuples can contain items with different data types.
- tuples are ordered, duplicates are allowed but items can't be changed.
- tuple methods like len(), count(), index() are similar to lists.


### [Access and slicing are similar to lists](#to-sliceaccess-list-items)
- Since tuples are imutable so we can't change a tuple directly.To change or update a tuple we can convert it into list, do whatever is needed and convert back to tuple.
- We cant add new items but can multiply the same items in a tuple.
```
>> t = ('A','B','C')
>> new_t = t*2
Output: 
```

### Unpacking values
- When we assign values to a variable its called packing. 
- When we extract values assigned to a variable as new variables, its called unpacking.

Example:
```
fruits = ("apple", "banana", "cherry")

(a, b, c) = fruits
# a is variable with value = 'apple' and so on for b and c.

print(a)
print(b)
print(c)
type(a)
```

### Join tuple
```
new_tuple = tuple1+ tuple2
```

# dictionary = {'key':'Value'}
- Dicrtionaries are ordered, mutable but doesnot allow duplicates.

### Access the items from a dictionary
```
dictName['Key']

#or

dictName.get('Key')
```
### Get all the keys and values
```
dictName.keys()

#to get values 
dictName.values()
```

### Get the (key, value) pairs as a tuple.
```
dictName.items()
```

### Change/Update the values
```
dictName['key'] = new_value_for_this_key

#0r
dictName.update({'key':'New_value'})
```
### [Add new item(s)](#changeupdate-the-values) 
Same as change/Update procedure.

### Remove items
```
dictName.pop('Key_you_want_to_Remove')

#To remove the last item inserted
dictName.popitem()
```
Also del and clear() method works similarly as with lists.


### How to construct a dictionary from tuples of keys and assign same values
```
# Create a tuple for keys
k = ('A','s','f','Q')
value = (4)

#now form a dictionary
d = dict.fromkeys(k,value)
print(d)
```
# set = {'el1','el2'}
- Not ordered, can't be accessed, can't be changed (only add and replace) and doesnot allow duplicates. 
- Set items can't be accessed directly but can be accessed as iterables using loops.

### Add items
```
setName.add(new_tem)

# to add multiple items
setName.update(list_of_multiple_items)
```
### Remove items
```
setName.remove(item_you_want_to_remove)

# if the specified item doesn't exits it will through an error is such case we can use discard()

setName.discard(discard_this_item)

#If the specified item doesn't exist in the set, it will not throw an error.

#Or
setName.pop()  #automatically removes the last item.
```

### [See the set methods for union, intersaction etc.](https://www.w3schools.com/python/python_sets_methods.asp)