the registry file sets the installation location,  
this part needed to be fixed to be more dynamic.

you can absolutly use it without applying the registry values into your registry,  
SharpDevelop uses your manual configuration anyway.

```reg
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\CodePlex\StyleCop]
"InstallDir"="C:\\Program Files (x86)\\StyleCop 4.7\\"
"TargetsDir"="C:\\Program Files (x86)\\MSBuild\\StyleCop\\v4.7\\"
"InstallDate"="18/07/2018"
"ProductVersion"="4.7.51.0"

;[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio\9.0\MSBuild\SafeImports]
;"StyleCop.v4.7"="C:\\Program Files (x86)\\MSBuild\\StyleCop\\v4.7\\StyleCop.Targets"
```

default values above are what I've extracted from a native installation of StyleCop on a clean PC.

