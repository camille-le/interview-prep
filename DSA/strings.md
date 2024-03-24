### Strings



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