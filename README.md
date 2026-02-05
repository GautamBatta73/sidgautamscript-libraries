# SidGautamScript-Libraries README

This is the README for the "SidGautamScript-Libraries" repository.

## What is this?

This repository is just a place to store all the libraries that will not be packaged with the runtime environment for SidGautamScript.

The './libraries' directory has the library names as directories, and each directory has:
- **readme.md**: Documentation For The Library.
- **lib.sidg**: Source Code For The Library.
- **lib.sidgc**: Compiled Code For The Library (What will be installed).

<br>
You can install the libraries in the current working directory with the following command (granted you have SidGautamScript >=2.6.5):

```
sgc install <libNames...>
```

```PowerShell
sgc install Test ArrayList
```
<br>

**Note: Library Names are Case-Sensitive!**

<br>
You can also install it globally (This will allow you to use it like a native/built-in library):

```PowerShell
sgc install Test ArrayList -g
```

## Want A Library to Be Added?

Email the compiled file, documentation, and (preferably) the source code to me: 
[gbatta2005@gmail.com](mailto:gbatta2005@gmail.com)

I'll add it after some basic tests.

## For more information

* [SidGautamScript Documentation](https://github.com/GautamBatta73/SidGautam/blob/main/Versions/Prog_Language/Documentation/readme.md)
* [Download SidGautamScript Compiler and RuntimeEnvironment](https://drive.google.com/drive/folders/1bIonQZPRfJ_bTbHw-KjHeAVaPml8VYzj?usp=sharing)

**Enjoy!**