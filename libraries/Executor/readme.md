# SidGautamScript Executor Library

This library adds nothing of value in SidGautamScript.
<br>
This is simply to be used as a dependency for other libraries.
<br>
This is a minified version of the SidGautamScript Runtime Environment, which you can use in modules to execute Compiled SidGautamScript code. Everything in the Runtime Environment is available in this module (imports, native functions, etc.).

## Importing & Basic Usage
As this adds a JavaScript module, you need to import it into your module:

```javascript
const executor = require("./executor");

const code = {
  code: [
    { op: "PUSH_CONST", arg: 0, loc: null },
    { op: "LOAD", arg: "print", loc: { line: 1, column: 2 } },
    { op: "CALL", arg: 1, loc: { line: 1, column: 2 } },
  ],
  constants: [4],
}; // This is the compiled code for: print(4);

executor.runCode(JSON.stringify(code));
```

```powershell
4
```

<br>

## Properties
### executor.GLOBALS
This is where you can add global variables that you want to be accessible in the code that you run.

```javascript
const { runCode, GLOBALS } = require("./executor");
const compile = require("./compiler");

GLOBALS.testVar = {
  value: 42, // The value of the global variable
  constant: true, // Whether the variable is constant (cannot be reassigned)
};

const code = compile("print(testVar);"); // Compiles the code, and returns the compiled code as stringified JSON

runCode(code); // Executes the compiled code
```

```powershell
42
```

<br>

## Methods
### executor.NativeFunction(args, fn, name?)
This is the template for adding native functions that you want to be accessible in the code that you run.
**args** is an array of strings that specifies the argument names for the function (for stringifying).<br>
**fn** is the actual JavaScript function that will be executed when the native function is called (the parameter is an array).<br>
**name** is an optional parameter that specifies the name of the native function (for any reasion you'd want to check the name of a called function).

```javascript
const { runCode, GLOBALS, NativeFunction } = require("./executor");
const compile = require("./compiler");

GLOBALS.testFunc = {
  value: NativeFunction(["num"], (args) => {
    console.log(args[0]); // As args is an array, we access the first element to get the actual argument value
  }),
  constant: true, // Whether the variable is constant (cannot be reassigned)
};

const code = compile("testFunc(42);"); // Compiles the code, and returns the compiled code as stringified JSON

runCode(code); // Executes the compiled code
```

```powershell
42
```

<br>

### executor.runCode(code, runPath?, args?)
This method takes in a stringified version of the compiled code, and executes it.<br>
**runPath** is an optional parameter that specifies the path where the code should be run from (for relative imports).<br>
**args** is an optional parameter that specifies the "commandline" arguments to be passed to the code (for \_\_ARGS global constant).

```javascript
const { runCode } = require("./executor");
const compile = require("./compiler");

const code = compile("print('Hello World');"); // Compiles the code, and returns the compiled code as stringified JSON

runCode(code); // Executes the compiled code
```

```powershell
"Hello World"
```

<br>

### executor.runFunction(fn, runPath?, fnArgs?)
This method takes in a compiled SidGautamScript function object, and executes it. (This is typically for callbacks, as you can pass it to this method to execute it).<br>
**runPath** is an optional parameter that specifies the path where the function should be run from (for relative imports).<br>
**fnArgs** is an optional parameter that specifies the function arguments to be passed to the function.

```javascript
const { runCode, GLOBALS, NativeFunction, runFunction } = require("./executor");
const compile = require("./compiler");

GLOBALS.forEach = {
  value: NativeFunction(["list"], (args) => {
    const list = args[0]; // As args is an array, we access the first element to get the first argument
    const callback = args[1]; // The second element of args is the callback function
    list.forEach((el, idx) => runFunction(callback, null, [el, idx])); // We run the callback function for each element in the list, passing the element and its index as arguments
  }),
  constant: true, // Whether the variable is constant (cannot be reassigned)
};

const code = compile("forEach({ 1, 2, 3 }, (el, idx) -> print(el));"); // Compiles the code, and returns the compiled code as stringified JSON

runCode(code); // Executes the compiled code
```

```powershell
1
2
3
```
