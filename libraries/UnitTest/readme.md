# SidGautamScript UnitTest Library

This library adds UnitTests to SidGautamScript.
<br>
They work about the same as UnitTests in other languages.

## Instantiation

As this adds a class, you need to create an instance of the class:
```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

print(test); # Prints the UnitTest instance information
```
```javascript
"UnitTest: Example Test"
"Tests: 0"
```

<br>

## Methods
### UnitTest.getTestNum()
This method returns the size/length of the UnitTest instance.

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

print(test.getTestNum()); # Prints the UnitTest instance's test number (the next test number to be run)
```
```javascript
1
```

<br>

### UnitTest.assertTrue(toTest)
This method takes a value, and checks if it is true. If it is, it prints "Pass" in green. If it isn't, it prints "Fail" in red. It also increments the test number.

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertTrue(true); # Tests if true is true, and prints the result
```
```javascript
"Example Test 1:"
"Pass"
```

<br>

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertTrue((9 + 10) == 21); # Tests if the expression is true, and prints the result
```
```javascript
"Example Test 1:"
"Fail"
```

<br>

### UnitTest.assertFalse(toTest)
This method takes a value, and checks if it is false. If it is, it prints "Pass" in green. If it isn't, it prints "Fail" in red. It also increments the test number.

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertFalse(false); # Tests if false is false, and prints the result
```
```javascript
"Example Test 1:"
"Pass"
```

<br>

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertFalse((9 + 10) == 19); # Tests if the expression is false, and prints the result
```
```javascript
"Example Test 1:"
"Fail"
```

<br>

### UnitTest.assertNull(toTest)
This method takes a value, and checks if it is null. If it is, it prints "Pass" in green. If it isn't, it prints "Fail" in red. It also increments the test number.

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertNull(NULL); # Tests if null is null, and prints the result
```
```javascript
"Example Test 1:"
"Pass"
```

<br>

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertNull(); # Tests if passing no argument is null, and prints the result
```
```javascript
"Example Test 1:"
"Pass"
```

<br>

### UnitTest.assertEqual(toTest, expected)
This method takes two values, and checks if they are equal. If they are, it prints "Pass" in green. If they aren't, it prints "Fail" in red. It also increments the test number.

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertEqual(5, 5); # Tests if 5 is equal to 5, and prints the result
```
```javascript
"Example Test 1:"
"Pass"
```

<br>

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertEqual({1, 2}, {1, 2}); # Tests if the two lists are equal, and prints the result
```
```javascript
"Example Test 1:"
"Pass"
```

<br>

### UnitTest.assertError(error, code)
This method takes two values, the error message and the callback function. If the callback function throws an error with the specified message, it prints "Pass" in green. If they aren't, it prints "Fail" in red. It also increments the test number.

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertError("This is an error", () -> {
    Error("This is an error");
}); # Tests if the callback function throws the specified error, and prints the result
```
```javascript
"Example Test 1:"
"Pass"
```

<br>
If you want to test whether a function throws an error or not, you can use assertTrue and the native catchError function:

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertTrue(catchError(() -> {
    var string = "This is a string";
    var number = 123;
}).success); # Tests if the callback function throws an error, and prints the result
```
```javascript
"Example Test 1:"
"Pass"
```

<br>

```python
import "./UnitTest";

var test = UnitTest("Example Test"); # Declares and creates an instance of UnitTest, called 'test'

test.assertTrue(catchError(() -> {
    Error("This is an error");
}).success); # Tests if the callback function throws an error, and prints the result
```
```javascript
"Example Test 1:"
"Fail"
```

<br>