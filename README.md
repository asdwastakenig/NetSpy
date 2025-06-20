
# NetSpy - [Latest release](https://github.com/asdwastakenig/NetSpy)

NetSpy is a fork of dnSpy designed to experiment with some cool (or maybe boring) modifications. It retains all the powerful features of dnSpy while adding some unique twists.

Main features:
- Debug .NET and Unity assemblies
- Edit .NET and Unity assemblies
- Custom modifications and experimental features
- Light and dark themes

![debug-animated](images/debug-animated.gif)

![edit-code-animated](images/edit-code-animated.gif)

## Binaries

https://github.com/asdwastakenig/NetSpy/releases

## Building

```PS
git clone --recursive https://github.com/asdwastakenig/NetSpy.git
cd NetSpy
# or dotnet build
./build.ps1 -NoMsbuild
```

To debug Unity games, you need this repo too: https://github.com/dnSpy/dnSpy-Unity-mono (or get the binaries from https://github.com/dnSpy/dnSpy/releases/unity)

# Debugger

- Debug .NET Framework, .NET and Unity game assemblies, no source code required
- Set breakpoints and step into any assembly
- Locals, watch, autos windows
- Variables windows support saving variables (eg. decrypted byte arrays) to disk or view them in the hex editor (memory window)
- Object IDs
- Multiple processes can be debugged at the same time
- Break on module load
- Tracepoints and conditional breakpoints
- Export/import breakpoints and tracepoints
- Call stack, threads, modules, processes windows
- Break on thrown exceptions (1st chance)
- Variables windows support evaluating C# / Visual Basic expressions
- Dynamic modules can be debugged (but not dynamic methods due to CLR limitations)
- Output window logs various debugging events, and it shows timestamps by default :)
- Assemblies that decrypt themselves at runtime can be debugged, NetSpy will use the in-memory image. You can also force NetSpy to always use in-memory images instead of disk files.
- Public API, you can write an extension or use the C# Interactive window to control the debugger

# Assembly Editor

- All metadata can be edited
- Edit methods and classes in C# or Visual Basic with IntelliSense, no source code required
- Add new methods, classes or members in C# or Visual Basic
- IL editor for low-level IL method body editing
- Low-level metadata tables can be edited. This uses the hex editor internally.

# Hex Editor

- Click on an address in the decompiled code to go to its IL code in the hex editor
- The reverse of the above, press F12 in an IL body in the hex editor to go to the decompiled code or other high-level representation of the bits. It's great to find out which statement a patch modified.
- Highlights .NET metadata structures and PE structures
- Tooltips show more info about the selected .NET metadata / PE field
- Go to position, file, RVA
- Go to .NET metadata token, method body, #Blob / #Strings / #US heap offset or #GUID heap index
- Follow references (Ctrl+F12)

# Other Features

- BAML decompiler
- Blue, light and dark themes (and a dark high contrast theme)
- Bookmarks
- C# Interactive window can be used to script NetSpy
- Search assemblies for classes, methods, strings, etc
- Analyze class and method usage, find callers, etc
- Multiple tabs and tab groups
- References are highlighted, use Tab / Shift+Tab to move to the next reference
- Go to the entry point and module initializer commands
- Go to metadata token or metadata row commands
- Code tooltips (C# and Visual Basic)
- Export to project
- Experimental modifications and features

# Open Source Components

NetSpy builds upon these excellent open source projects:
- [ILSpy decompiler engine](https://github.com/icsharpcode/ILSpy) (C# and Visual Basic decompilers)
- [Roslyn](https://github.com/dotnet/roslyn) (C# and Visual Basic compilers)
- [dnlib](https://github.com/0xd4d/dnlib) (.NET metadata reader/writer)
- [VS MEF](https://github.com/microsoft/vs-mef) (Improved MEF performance)
- [ClrMD](https://github.com/microsoft/clrmd) (Advanced debugging capabilities)
- [Iced](https://github.com/0xd4d/iced) (x86/x64 disassembler)

# License

NetSpy is licensed under [GPLv3](LicenseInfo/GPLv3.txt).

# [Credits](LicenseInfo/CREDITS.txt)

Note: This is a fork of dnSpy with additional experimental features. Check the repository for the latest modifications and changes.
