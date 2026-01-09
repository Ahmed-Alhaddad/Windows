# How to Silently Install your EXE using CMD
##How to run EXE from CMD?
```
application.exe /S /V/qn
```
Now, let’s say we want to edit a registry key after the installation. For CMD, you need to use the REG.EXE utility to perform changes on the registry.

For a full list of parameters, you can type the following:

```
Reg.exe /?
```
Like
```
application.exe /S /V/qn
REG ADD HKLM\SOFTWARE\application\app /v AppInfo /t REG_DWORD /d 1
```
