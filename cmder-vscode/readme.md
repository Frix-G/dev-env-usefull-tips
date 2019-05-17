# How to add cmder to VS Code

> Inside cmder root folder (in my case it's C:\Program Files (portable)\cmder), create a file named "vscode.bat"

> Add following code inside this new file

```
@echo off 
set CurrentWorkingDirectory=%CD%
set CMDER_ROOT=C:\Program Files (portable)\cmder
"%CMDER_ROOT%\vendor\init.bat" CD /D >nul
%CurrentWorkingDirectory%
```

> Open VS COde settings and add following lines

```
    "terminal.integrated.shell.windows": "C:\\WINDOWS\\system32\\cmd.exe",
    "terminal.integrated.shellArgs.windows": [
        "/K",
        "C:\\Program Files (portable)\\cmder\\vscode.bat"
    ]
```

> Restart VS Code and open terminal