## Handy (mostly) Powshell Scripts ##

**Activate Office 2019**  
`cscript "C:\'Program Files'\'Microsoft Office'\Office16\OSPP.VBS" /inpkey:<YOUR_OFFICE_KEY>`  
`cscript "C:\'Program Files'\'Microsoft Office'\Office16\OSPP.VBS" /act`

**Activate Windows**  
`slmgr -upk`  
`slmgr -ipk YOUR_WINDOWS_KEY`  
`slmgr -ato`

**Install .MSI File**  
`Start-Process msiexec.exe -Wait -ArgumentList  '/I C:\path_to_installer\installer.msi /quiet'`

**Get BIOS Manufacture Date**  
`$BIOS = Get-WmiObject -class Win32_BIOS`  
`$BIOS.ConvertToDateTime($BIOS.Releasedate).ToShortDateString()`

**Update MacOS**  
`softwareupdate -l`  
`softwareupdate -ia`

**Update Debian/Ubuntu**  
`apt update && apt upgrade -y`

**Install Office 2019 via Volume Licenese Installer**  
- You need to download the office setup.exe file from Micrsoft Volume Licensing Center  
- Use the xml file in ProPlus2019.xml as an example and tweak it as desired  
`./setup.exe /configure <PATH_TO_XML/settings.xml>`
