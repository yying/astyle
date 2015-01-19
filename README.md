Chocolatey package for AStyle
=============================

Building the package
--------------------
There should be a `cpack` (`choco pack`) tool that is package with Chocolatey. To build the nupkg file, do a `cpack` in the directory where `astyle.nuspec` is located. This should generate a `astyle-[version].nupkg` file.

cpack in root directory

Testing the package
-------------------
In the same directory as the `astyle-[version].nupkg` file, execute the following command: `choco install astyle -source '%cd%'`. This will install the package.

To uninstall the package, simply execute `choco uninstall astyle`.

Submitting the package
----------------------
Execute the following commands:
 * `choco install nuget.commandline`
 * `nuget SetApiKey [API_KEY_HERE] -source https://chocolatey.org/`
 * `cpush astyle.[version].nupkg`

Source
------
For more, see [https://github.com/chocolatey/chocolatey/wiki/CreatePackagesQuickStart](https://github.com/chocolatey/chocolatey/wiki/CreatePackagesQuickStart).
