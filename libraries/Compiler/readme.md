# SidGautamScript Compiler Library

This library adds nothing of value in SidGautamScript.
<br>
This is simply to be used as a dependency for other libraries.
<br>
This is a minified version of the SidGautamScript Compiler, which you can use in modules to compile Source SidGautamScript code.

## Usage

As this adds a JavaScript module, you need to import it into your module:
```javascript
const compile = require("./compiler");

console.log(compile("print(2 + 2);")); // Compiles the Source SidGautamScript code, and returns the compiled bytecode as stringified JSON
```
```powershell
'{"code":[{"op":"PUSH_CONST","arg":0,"loc":null},{"op":"LOAD","arg":"print","loc":{"line":1,"column":2}},{"op":"CALL","arg":1,"loc":{"line":1,"column":2}}],"constants":[4]}'
```