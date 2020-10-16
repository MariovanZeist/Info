# Configure Windows Terminal to Use VS 2019 Powershell

Open windows Terminal,
Open Settings.

Add following section to Profiles:List
```json
{
    "name": "Developer PowerShell",
    "commandline": "powershell.exe -NoExit -Command \"&{ $vsInstallPath=& \"${env:ProgramFiles(x86)}/'Microsoft Visual Studio'/Installer/vswhere.exe\" -prerelease -latest -property installationPath; Import-Module \"$vsInstallPath/Common7/Tools/Microsoft.VisualStudio.DevShell.dll\"; Enter-VsDevShell -VsInstallPath $vsInstallPath -SkipAutomaticLocation }\"",
}
```
Follow instructions at: https://docs.microsoft.com/nl-nl/windows/terminal/tutorials/powerline-setup
