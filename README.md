# SidGautamScript-Libraries README

This is the README for the "SidGautamScript-Libraries" repository.

<a href="https://www.buymeacoffee.com/GautamBatta73" target="_blank"><img src="https://i.imgur.com/xPQdsF8.png" alt="Buy Me A Hot Chocolate" style="height: 47px !important;width: 200px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

## Terms

- **Package**: The Whole Directory Which Contains Compiled SidGautamScript Libraries, and Modules.
- **Library**: Compiled SidGautamScript File With Functions, Objects, Constants, etc To Import.
- **Module**: JavaScript Module File That Can Be Injected into A SidG Library For More Flexibility.

## What is this?

This repository is just a place to store all the packages/libraries that will not be packaged with the runtime environment for SidGautamScript.

The './libraries' directory has the package names as directories, and each directory has:
- **readme.md**: Documentation For The Library.
- **lib.sidg**: Source Code For The Library.
- **info.json**: Information About The Library (Name, Version, Size, Dependencies).
- **lib.sidgc**: Compiled Code For The Library (What will be installed).
- **/modules/?**: Optional JavaScript Module Exports That Can Be Injected into A SidG Library For More Flexibility.

<br>
You can install the packages in the current working directory with the following command (granted you have SidGautamScript >=2.6.5):

```
sgc install <packages...>
```

```PowerShell
sgc install Test ArrayList
```
<br>

**Note: Package Names are Case-Sensitive!**<br>
**Note: Any Dependencies Listed In The info.json Are Installed Automatically!**

<br>
You can also install it globally (This will allow you to use it like a native/built-in package/library):

```PowerShell
sgc install Test ArrayList -g
```

## Want A Library to Be Added?

Email the compiled file, documentation, and (preferably) the source code to me: 
[gbatta2005@gmail.com](mailto:gbatta2005@gmail.com)

I'll add it after some basic tests.

### Guidelines:

- Try to name your package/library as uniquely as possible. Avoiding conflicting package/library names, whether globally or locally.
- Try not to rely on injecting JavaScript modules as they can have some odd side effects. If something can be done easily in SidGautamScript, use that instead.

## For more information

* [SidGautamScript Documentation](https://github.com/GautamBatta73/SidGautam/blob/main/Versions/Prog_Language/Documentation/readme.md)
* [Download SidGautamScript Compiler and RuntimeEnvironment](https://drive.google.com/drive/folders/1bIonQZPRfJ_bTbHw-KjHeAVaPml8VYzj?usp=sharing)

**Enjoy!**