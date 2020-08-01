# PowerShell Cheat Sheet

## Environment Variable 

$PSVersionTable Outputs version info for 

## Help

`Get-Help`
`Get-Command`

| file | environment |
| --- | --- |
| $PSHOME\profile.ps1 | All Users, All Hosts |
| $PSHOME\Microsoft.PowerShell_profile.ps1 | All Users, Current Host |
| $Home\[My ]Documents\WindowsPowerShell\Profile.ps1 | Current User, All Hosts | 
| $Home\[My ]Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1 | Current User, Current Host |


## Useful recipes

### curl / wget

```powershell
curl <URL> | select-object -expandproperty content | out-file <FILENAME> 
```
or  alternatively: 
```powershell
(New-Object System.Net.WebClient).DownloadString("http://www.example.com/hello-world.html","C:\hello-world.html")
```

