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
`softwareupdate -i -a`

**Update Debian/Ubuntu**  
`apt update && apt upgrade -y`


