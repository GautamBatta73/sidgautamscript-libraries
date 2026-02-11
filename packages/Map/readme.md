# SidGautamScript Map Library

This library adds Maps (Dictionaries) to SidGautamScript.
<br>
They work the same as Maps from JavaScript.

## Instantiation

As this adds a class, you need to create an instance of the class:
```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

print(fruits); # Prints the currently empty Map instance
```
```javascript
{}
```

<br>

## Methods
### Map.size()
This method returns the size/length of the Map instance.

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

print(fruits.size()); # Prints the currently empty Map instance's size

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

print(fruits.size()); # Prints the Map instance's size
```
```javascript
0
1
```

<br>

### Map.keys()
This method returns the key names of the Map instance, as a list.

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print(fruits.keys()); # Prints the Map instance's key names
```
```javascript
[
  "Banana",
  "Apple"
]
```

<br>

### Map.values
This method returns the values of the Map instance, as a list.

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print(fruits.values()); # Prints the Map instance's values
```
```javascript
[
  2.99,
  2.45
]
```

<br>

### Map.set(key, value)
This method adds the key-value pair to the end of the Map instance, or, if the key already exists, sets the key's value to the new value.

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print(fruits); # Prints the Map instance
```
```javascript
{
  "Banana": 2.99,
  "Apple": 2.45
}
```

<br>

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print(fruits); # Prints the Map instance

fruits.set("Apple", 2.75); # Sets a new value to the key

print(fruits); # Prints the Map instance
```
```javascript
{
  "Banana": 2.99,
  "Apple": 2.45
}
{
  "Banana": 2.99,
  "Apple": 2.75
}
```

<br>

### Map.get(key)
This method returns the value of the Map instance, associated with the key.

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print(fruits.get("Apple")); # Prints the Map instance's value at the key
```
```javascript
2.45
```

<br>

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print(fruits.get("Orange")); # Prints the Map instance's value at the non-existent key
```
```javascript
null
```

<br>

### Map.delete(key)
This method returns the associated value of the key, in the Map instance, then removes the key-value pair from the instance.

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print("Removed:", fruits.delete("Apple")); # Removes the value of key, and prints it

print(fruits); # Prints the Map instance
```
```javascript
"Removed:" 2.45
{
  "Banana": 2.99
}
```

<br>

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print("Removed:", fruits.delete("Orange")); # Removes the value of a non-existent key, and prints it

print(fruits); # Prints the Map instance
```
```javascript
"Removed:" null
{
  "Banana": 2.99,
  "Apple": 2.45
}
```

<br>

### Map.clear()
This method returns the Map instance as a normal object, then removes all the key-values.

```python
import "./Map";

var fruits = Map(); # Declares and creates an instance of Map, called 'fruits'

fruits.set("Banana", 2.99); # Adds a key-value pair to the Map instance

fruits.set("Apple", 2.45); # Adds a key-value pair to the Map instance

print(fruits.size()); # Prints the size of the Map instance

print("Removed:", fruits.clear()); # Clears all the key-values, and prints it

print(fruits); # Prints the Map instance

print(fruits.size()); # Prints the size of the Map instance
```
```javascript
2
Removed: {
  "Banana": 2.99,
  "Apple": 2.45
}
{}
0
```

<br>