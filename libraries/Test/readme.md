# SidGautamScript Test Library

This is just a test library that is used to test the install command.

## Methods
### add(num1, num2)
This function adds two numbers (or I guess concatenates strings) together and returns the result.

```python
import "./Test"; # Library has print statement in top-level scope

var sum = add(5, 2); # Adds 5 and 2 together and stores the answer in sum

print(sum); # Prints 7
```
```javascript
"use add(a, b)"
7
```

<br>

```python
import "./Test"; # Library has print statement in top-level scope

var sum = add("Number Five: ", 5); # Concatenates "Number Five: " and 5 together and stores the answer in sum

print(sum); # Prints "Number Five: 5"
```
```javascript
"use add(a, b)"
"Number Five: 5"
```