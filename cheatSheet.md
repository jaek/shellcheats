# PowerShell Cheat Sheet

## Quick reference

| command | alias | description |
| --- | --- | --- |
| `Invoke-Item <PATH>` | ii | opens <PATH> in explorer | 


## Execution Policies 

Use `Set-ExecutionPolicy` and `Get-ExecutionPolicy` to set and access execution policy respectively.
The `Unblock-File` command can be used to allow unsigned scripts to run locally.

| policy | notes | 
| --- | --- |
| RemoteSigned | Default level for windows server. Requires signing for downloaded scripts, but not for local |

## Environment Variables

#### Profile File Locations

| file | environment |
| --- | --- |
| $PSHOME\profile.ps1 | All Users, All Hosts |
| $PSHOME\Microsoft.PowerShell_profile.ps1 | All Users, Current Host |
| $Home\[My ]Documents\WindowsPowerShell\Profile.ps1 | Current User, All Hosts | 
| $Home\[My ]Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1 | Current User, Current Host |

| Variable | Description | 
| --- | --- | 
| `$PSVersionTable` | Outputs version info for current PowerShell |

## Getting Help
`Get-Help` 
`Get-Command`


## Useful recipes

### curl / wget

```powershell
curl <URL> | select-object -expandproperty content | out-file <FILENAME> 
```
or  alternatively: 
```powershell
(New-Object System.Net.WebClient).DownloadString("http://www.example.com/hello-world.html","C:\hello-world.html")
```

