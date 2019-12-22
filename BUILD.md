# Building

How to build todotxt.exe, without installing VisualStudio, on Windows 10.

- Download and Install MSBuild standalone [Microsoft website](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=16)
- Add MSBuild to Path, typically installed in `C:\Program Files (x86)\Microsoft Visual Studio\2019\BuildTools\MSBuild\Current\Bin`
- Download and Install NuGet client tool from [Nuget Microsoft website](https://docs.microsoft.com/en-us/nuget/reference/nuget-exe-cli-reference#installing-nugetexe)
- Add NuGet.exe to path
- `nuget.exe restore` to install the mshtml 7 dependency
- Download and Install .NET framework 3.5 to get the right version of Microsoft.Build.Utilities.v3.5, from [MS website](https://www.microsoft.com/en-us/download/details.aspx?id=21)
- Into the `Installer` folder, run `MSBuild.exe .\Build.xml`
- Enjoy, the installer and the portable version are in `Installer\Output`