### Strings
For a common list of string operations, see this list here: 
https://www.w3schools.com/python/python_ref_string.asp
Below are some methods that may be used in an interviewing context.

### Python String Iteration
Without splitting the text, this loop will print over each character in a new line:
```python
text = "abc"
for ch in text:
    print(ch)
# output:
# a
# b
# c
```
By splitting the text (and not specifying the delimiter), we split based on " " and then 
print each substring on a newline:
```python
text = "abc abc"
for ch in text.split():
    print(ch)
# output: 
# abc
# abc
```

### Python Indexing
It is possible to access an index of a string and re-assign the value.
```python
text = "hello and welcome to my world"
x = text[0].upper() + text[1:]
# Output: Hello and welcome to my world
```

### Python Count() Method



### Python Find() Method


### Python Index() Method


### Python Replace() Method


### Python SplitLines() Method 


### Python String join() Method
This takes all methods in an iterable and joins them into one string.
An iterable is an object that can be looped over, allowing one to go
through one element in the object at a time. Some examples include a 
`list` and also a `dict`.
```python
# E1: Join without a separator
arr = ["1","2","3"]
res = "".join(arr)
# Output: "123"

# E2: Join with a "," separator
arr = ["1","2","3"]
res = ",".join(arr)
# Output: "1,2,3"

# E3: Join with a "#" separator
arr = ["1","2","3"]
res = "#".join(arr)
# Output: "1#2#3"

# E4: Join with dictionary keys
myDict = {"name": "John", "country": "Norway"}
mySeparator = "TEST"
x = mySeparator.join(myDict)
# Output: nameTESTcountry
```