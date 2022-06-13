[![PowerShell Gallery Download Count](https://img.shields.io/powershellgallery/dt/SetEnv?label=downloads%20from%20PSGallery)](https://www.powershellgallery.com/packages/SetEnv)

## Introduction
A PowerShell module that implements Set-EnvVar and Set-EnvPath

## Installation

```powershell
Install-Module -Name SetEnv
```

## Usage of  Set-EnvVar
```powershell
 Set-EnvVar [-Name] <String> [-Value] <String> [[-Process] <Boolean>] [[-User] <Boolean>]
     [[-Machine] <Boolean>] [-NoBroadcast] [<CommonParameters>]
```
    -Name :  The name of the environment variable
    -Parameter : The value of the environment variable
    -Process : Update the environment variable for the current process?
    -User : Update the environment variable for the current user?
    -Machine     Update the environment variable for the local machine?

```powershell
Set-EnvVar -Name 'MyVar' -Value 'MyValue' -Process $True -User $True -Machine $True
```
More Info
```powershell
    get-help Set-EnvVar -full
```


## Usage of  Set-EnvPath
```powershell
Set-EnvPath [-Operation] <String> [-Path] <String> [[-Persist] <String>]
   [-CurrentProcess] [<CommonParameters>]
```
    -Operation : The operation to be performed. (Add/Remove)
    -Path :  The path of the directory to be added to the PATH environment variable.
    -Persist :  When Operation is Add: permamently set the PATH for either the current user ('User') 
                or for the whole system  ('System').
    -CurrentProcess :    When Operation is Add: specify this switch to add Path to the current 
               PATH environment variable.

```powershell
    Set-EnvPath -Operation Remove -Path c:\php\php
    Set-EnvPath -Operation Add -Path c:\php\php -Persist System -CurrentProcess
```
More Info
```powershell
    get-help Set-EnvPath -full
```



  
