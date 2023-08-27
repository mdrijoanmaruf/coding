# Python For Data Science

## Variable :
```py
x = 4           # type int
y = "saif"      # type string
x = str(3)      # x will be '3'
y = int(3)      # y will be 3
z = float(3)    # z will be 3.0
type(z)         # float

x = "saif"
x = 'saif'      # both are same
# variable are case sensitive
```
**Multiple values :**
```py
x, y, z = 12 , 13.5 , "Rioan"
```
**Unpacking a collection :**
```py
fruits = ["Apple" , "Banana"]
x , y = fruits      # x = Apple and Y = Banana
```


**Output Variable :**
```py
x = "rijoan"
y = "maruf"
print(x ,y)     # will print rijoan maruf
print(x + y)    # will print rijoanmaruf
```

**Globla Variable :**
* outside any function variable.

**Numbers**
```py
x = 1           # int
y = 1.11        # float
x = "saif"      # str
x = 1j          # complex
```

**Random Numbers :**
```py
import random
x = random.randrange(1 , 10)        # random number 1 - 10 will store in x
```

## String:
**Multiline String :**
```py
a = """This is 
Multi line of string"""

b = '''This is also
Multi line of sting'''
```

**Strings are array :**
```py
a = "saif"  # index start with 0
a[1]        # a
a[0]        # s
```
**Looping Though a string :**
```py
for i in "saif":
    print(i)   # print  # s
                        # a
                        # i
                        # f
```

**String Lenght :**
```py
y = len("saif")     # store lenght in y 
```

**Check String :**
```py
x = "my name is saif"
y = "saif" in x         # True
z = "rijoan" in x       # False
```

**String Slicing :**
```py
x = "Hello i am saif"
print(x[2:5])       # will print index 2 - 5
print(x[:5])        # will print index 0 - 5
print(x[2:])        # will print index 2 - end
```

**Negative Indexing :**
```py
x = "saif"          # -4 -3 -2 -1 
                    #  s  a  i  f
                    #  0  1  2  3
x[-3 : -1]          # aif
```
## Modify String :
```py
x.upper()           # convert intu upper case
x.lower()           # convert intu lawer case
x.split()           # remove whitespace form the begining or and
x.replace("s" , "x") # replace s to x . so saif will be xaif
```

**String Format() :**
```py
age = 36
text = "My age is {}"
text.format(age)    # age vlaue will set in {}
```

**Escape Characters :**
```py
    # \'        --> '
    # \\        --> \
    # \n        --> new line
    # \t        --> new tab
```
**String Methods :**
[w3shool](https://website-name.com)

**Booleans :**
```py
bool("abc")         # True
bool(29)            # True
bool(False)         # False
bool(None)          # False
bool(0)             # False
bool("")            # False
bool(())            # False
bool([])            # False
```

**Logical Operators :**
```py
# and , or , not
```

**Membership Operators :**
```py
x = ["apple" , "banana"]
print("banana" in x)        # True
print("banana" not in x)    # False
```

**Identity Operators :**
```py
x , y = 10 , 10
x is y      # True
x is not y  # False
```

**Bitwise Operators :**
```py
# & , | , ^ , << , >> 
```

## Lists
```py
mylist = ["apple" , "banana" , "jackfruit"]     # index start with 0
x = len(mylist)                                 # x = 3
list1 = ["abd" , 12 , True , "male"]            # Can store different data type
```

**List Constructor :**
```py
newlist = list(("saif" , "rihan" , "srabon"))   # newlist = ["saif" , "rihan" , "srabon"]
```

**Access Items :**
```py
newlist[0]      # saif
newlist[2]      # srabon
```

**Change List Items :**
```py
newlist[0] = "rijoan"       # newlist = ["rijoan" , "rihan" , srabon]
```

**Insert New Items :**
```py
newlist.insert(2 , "maruf")     # add "maruf" in 2 index
```

**Append Items :**
```py
newlist.append("mehedy")    # add "mehedy" in last of newlist
```

**Entend List :**
```py
list1 = ["saif" , "rijoan"]
list2 = ["srabon" , "rihan"]
list2.extend(list1)         # list2 = ["srabon" , "rihan" , "saif" , "rijoan"]
```

**Remove Specified Items :**
```py
list2.remove("srabon")      # list2 = ["rihan" , "saif" , "rijoan"]
```

**Remove Specified Index :**
```py
list2.pop(0)                # remove 1st index value
del list2[1]                # remove 2nd index. index 1
list2.pop()                 # remove all
```

**Clear the list :**
```py
list2.clear()               # will clear the list
```

**Sort list Alphanumerically :**
```py
list3 = ["sajib" , "rihan" , "azad" ]
list3.sort()                # ["azad" , "rihan" , "sajib"] 
```

**Reverse Order :**
```py
list3.reverse()
print(list3)                # ["sajib" , "rihan" , "azad"]
```

**Copy a list :**
```py
newlist = list3.copy()      # newlist = ["sajib" , "rihan" , "azad"]
```

**Jion a list :**
```py
list1 = ["saif" , "rioan"]
list2 = ["sajib" , "rihan"]
newlist = list1 + list2     # newlist = ["saif" , "rijoan" , "sajib" , "rihan"]

```

## Tuple
* Store multiple items in single variable
* A tuple is a collection which is ordered and unchangeable
* Allaw duplicates and index start with 0
* Can contain defferent datatype
```py
tuple1 = ("abc" , 34 , True)
```

**Tuple to list :**
```py
y = list(tuple1)        # y = ["abc" , 32 , True]
```

**List to tuple :**
```py
x = tuple(tuple1)       # x = ("abc" , 34 , True)
```

**Unpacking tuple :**
```py
fruits = ("apple" , "banana")
(green , yellow) = fruits       # green = apple , "yellow" = "banana"
```

## Dictionary :

```py
mydic = {
    "name" : "saif",
    "college" : "aiub",
}
# Now dictionary is orderd 
mydic["college"]        # aiub
# Duplicate is not allowed
mydic.keys()            # all key values
mydic.values()          # all values
mydic.items()           # all items
```

**Change value :**
```py
mydic.update({"name" : "rijoan"})   # replace "saif" with "rijoan"
```

**Add items :**
```py
mydic["address"] = "dhaka"          # Add new items "address" : "dhaka"
```

**Remove items :**
```py
mydic.pop("name")                   # Remove red items
del mydic["college"]                # Remove college items

```

**Copy dictionary :**
```py
newdic = mydic.copy()               # newdic now contain mydic copy values
# A dictionary can contain another dictionary and etc.
```

## Functions
```py
def myfunction(x):          # Function define
    print(x)
myfunction(100)             # Function call

```

## File
```py
f = open("new.c" , "w+")# file neame new.c and mode w+ = read and write
f.write("Hello wold")   # write file
f.read()                # read file
f.close()               # close file
                        # "a" --> will append end to file
```

**Create a new file :**
```py
# "x" --> acreate file and return error if file exist
# "a" --> append - will create file if it dose not exist
```

**Delete a file :**
```py
import os
os.remove("new.c")      # remove the new.c file
# os.rmdir("x")         # remove x folder
```

























