# SidGautamScript ArrayList Library

This is also a test library, and adds ArrayLists to SidGautamScript.
<br>
They work the same as ArrayLists from Java.

## Instantiation

As this adds a class, you need to create an instance of the class:
```python
import "./ArrayList";

var cars = ArrayList(); # Declares and creates an instance of ArrayList, called 'cars'

print(cars); # Prints the currently empty ArrayList instance
```
```javascript
[]
```

## Properties
### ArrayList.size
This property holds the size/length of the ArrayList instance.

```python
import "./ArrayList";

var cars = ArrayList(); # Declares and creates an instance of ArrayList, called 'cars'

print(cars.size); # Prints the currently empty ArrayList instance's size

cars.add("Batmobile"); # Adds an element to the ArrayList instance

print(cars.size); # Prints the ArrayList instance's size
```
```javascript
0
1
```

<br>

## Methods
### ArrayList.get(idx)
This method returns the element in the ArrayList instance, at idx.

```python
import "./ArrayList";

var cars = ArrayList(); # Declares and creates an instance of ArrayList, called 'cars'

cars.add("Batmobile"); # Adds an element to the ArrayList instance

cars.add("Invisible Jet"); # Adds an element to the ArrayList instance

print(cars.get(1)); # Prints the element at index 1
```
```javascript
"Invisible Jet"
```

<br>

```python
import "./ArrayList";

var cars = ArrayList(); # Declares and creates an instance of ArrayList, called 'cars'

cars.add("Batmobile"); # Adds an element to the ArrayList instance

cars.add("Invisible Jet"); # Adds an element to the ArrayList instance

print(cars.get(3)); # Prints the element at a non-existent index
```
```javascript
null
```

<br>

### ArrayList.remove(idx)
This method returns the element at idx in the ArrayList instance, then removes the element from the instance.

```python
import "./ArrayList";

var cars = ArrayList(); # Declares and creates an instance of ArrayList, called 'cars'

cars.add("Batmobile"); # Adds an element to the ArrayList instance

cars.add("Invisible Jet"); # Adds an element to the ArrayList instance

print("Removed:", cars.remove(0)); # Removes the element at index 0, and prints it

print(cars); # Prints the ArrayList instance
```
```javascript
"Removed: Batmobile"
[
  "Invisible Jet"
]
```

<br>

```python
import "./ArrayList";

var cars = ArrayList(); # Declares and creates an instance of ArrayList, called 'cars'

cars.add("Batmobile"); # Adds an element to the ArrayList instance

cars.add("Invisible Jet"); # Adds an element to the ArrayList instance

print("Removed:", cars.remove(3)); # Removes the element at a non-existent index, and prints it

print(cars); # Prints the ArrayList instance
```
```javascript
"Removed: null"
[
  "Batmobile",
  "Invisible Jet"
]
```

<br>

### ArrayList.clear()
This method returns the ArrayList instance's values as a List, then removes all the elements.

```python
import "./ArrayList";

var cars = ArrayList(); # Declares and creates an instance of ArrayList, called 'cars'

cars.add("Batmobile"); # Adds an element to the ArrayList instance

cars.add("Invisible Jet"); # Adds an element to the ArrayList instance

print(cars.size); # Prints the size of the ArrayList instance

print("Removed:", cars.clear()); # Clears all the elements, and prints it

print(cars); # Prints the ArrayList instance

print(cars.size); # Prints the size of the ArrayList instance
```
```javascript
2
"Removed:" [
  "Batmobile",
  "Invisible Jet"
]
[]
0
```

<br>