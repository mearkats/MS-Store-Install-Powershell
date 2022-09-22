![CroppedMK](https://user-images.githubusercontent.com/16869300/191701451-5550afce-b19f-4f8c-9e28-90777dd441e1.png)

# Microsoft Store Install Powershell Script - RMM Friendly!!

Hello and welcome!
This script allows the user to install a Microsoft Store App. As the title suggests, its RMM friendly, tested with Datto RMM and Tactical RMM.

The Script Uses the "RunAsUser" module created by Kelvin Tegelaar (https://github.com/KelvinTegelaar/RunAsUser). A user has to be logged in for the script to work. The script, as of 22/09/2022, will now feed the output of the installation into the RMM.

=======================================================================

Look for this line in the script:
```powershell
# Lets get it installed!
& $wingetsys install --id=9WZDNCRFJBH4 -e -h --accept-package-agreements --accept-source-agreements | ConvertTo-Json | Out-File 'C:\Air-IT\Temp\WinGet.txt'
}
```
the "--id=9WZDNCRFJBH4" needs to be changed to the ID of the MS App you are looking to install. This current one installs Microsoft Photos.

[Visit my website for more scripting goodness!](https://www.mearkats.co.uk)
