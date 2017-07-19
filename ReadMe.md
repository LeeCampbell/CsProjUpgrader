# CSProj Updater

Recently the .NET `.csproj` file format has been greatly simplified.
This repository is intended to house code to automatically upgrade your old (Pre VS2017) `.csproj` files to the new format.

This is not just a simple string replace operation.
Other files need to be read and modified/excluded from the working directory too.
`*.Nuspec`, `assemblyinfo.cs` and `Packages.config` are all effectively legacy concepts.

Data from these files needs to be read in, parsed and then potentially added to the new csproj format file.

The goal of this project will be to create a copy of your existing directory structure. 
i.e. a non destructive operation.
If you are happy with the result you can delete you existing directroy and move/rename the newly generated folder.