# MVP project for VS 17.5 Bug

Visual Studio cannot load projects If a PropertyGroup has Condition containing an invalid path: "Visual Studio ran into an unexpected problem with one of more projects. You may need to reload affected projects or the solution to prevent further problems."

However, using msbuild or a pervious version of Visual Studio to build the solution works perfectly fine.

Error message:

LimitedFunctionality
System.AggregateException: One or more errors occurred. ---> System.NotSupportedException: The given path's format is not supported.
   at System.Security.Permissions.FileIOPermission.EmulateFileIOPermissionChecks(String fullPath)
   at System.Security.Permissions.FileIOPermission.QuickDemand(FileIOPermissionAccess access, String fullPath, Boolean checkForDuplicates, Boolean needFullPath)
  ...

## Screenshot of Visual Studio
![VSError](screenshots/visualstudioerror.JPG) 

## Sample project
A sample MVP project can be found in sample/Build/WpfApp1.sln
