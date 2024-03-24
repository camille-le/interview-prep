## STRINGS
See [common string operations](https://www.w3schools.com/python/python_ref_string.asp) for a comprehensive list.
- Strings in Python are immutable.
- Casting a string to a list is `O(n)`.
- Character lists are mutable.

<hr>

## Table of Contents
- [Python String Iteration](#python-string-iteration)
- [Python Indexing](#python-indexing)
- [Python Count() Method](#python-count-method)
- [Python Find() Method](#python-find-method)
- [Python Index() Method](#python-index-method)
- [Python Replace() Method](#python-replace-method)
- [Python SplitLines() Method](#python-splitlines-method)
- [Python String join() Method](#python-string-join-method)

<hr>

### Python String Iteration
Without splitting the text, this loop will print over each character in a new line:
```python
text = "abc"
for ch in text:
    print(ch)
```
Output:
```md
a
b
c
```
By splitting the text (and not specifying the delimiter), we split based on " " and then 
print each substring on a newline:
```python
text = "abc abc"
for ch in text.split():
    print(ch)
```
Output:
```md
abc
abc
```

Here we specify what to split on and achieve the following result: 
```python
text = "abc # abc"
for ch in text.split("#"):
    print(ch)
```

Output:
```md
abc
 abc
```

[&uarr; Back to TOC](#table-of-contents)
<hr>

### Python Indexing
It is possible to access an index of a string and re-assign the value to a new string.
```python
text = "hello and welcome to my world"
x = text[0].upper() + text[1:]
```
Output:
```md
Hello and welcome to my world
```

[&uarr; Back to TOC](#table-of-contents)
<hr>

### Python Count() Method
This method returns the number of time a substring appears in a given string. 
```python
text = "apple apple apple"
counts = text.count("apple")
```
Output:
```md
3
```

In this case, we only found "le" twice: 
```python
text = "apple apple app"
counts = text.count("le")
```

Output:
```md
2
```

[&uarr; Back to TOC](#table-of-contents)
<hr>

### Python Find() Method

[&uarr; Back to TOC](#table-of-contents)
<hr>

### Python Index() Method

[&uarr; Back to TOC](#table-of-contents)
<hr>

### Python Replace() Method

[&uarr; Back to TOC](#table-of-contents)
<hr>

### Python SplitLines() Method 

[&uarr; Back to TOC](#table-of-contents)
<hr>

### Python String join() Method
This takes all methods in an iterable and joins them into one string.
An iterable is an object that can be looped over, allowing one to go
through one element in the object at a time. Some examples include a 
`list` and also a `dict`.
```python
# E1: Join without a separator
arr = ["1","2","3"]
res = "".join(arr)
# output: "123"

# E2: Join with a "," separator
arr = ["1","2","3"]
res = ",".join(arr)
# output: "1,2,3"

# E3: Join with a "#" separator
arr = ["1","2","3"]
res = "#".join(arr)
# output: 1#2#3

# E4: Join with dictionary keys
myDict = {"name": "John", "country": "Norway"}
mySeparator = "TEST"
x = mySeparator.join(myDict)
# output: nameTESTcountry
```

[&uarr; Back to TOC](#table-of-contents)
<hr>