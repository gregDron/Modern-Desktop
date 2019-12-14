# Driver Managementr
## All driver
  a) Get-windowsDriver -online
  b) dism /online /get-drivers
 ## Third-party drivers only
  a) Get-windowsDriver -online
  b) dism /online /get-drivers
  c) pnputil /enum-drivers
  
## Inf file 
  The reside in the C;\windows\system32\driverstore\Filerepository\name\*.inf
  
## Adding drivers to the Driver store

### Online:
a) pnputil /add-driver x:\driver.inf - ( wildcards allowed *.inf ) 

### Offline:
 a) dism /image:c:\imagefolder /add-driver /driver:C:\driverfolder\driver.inf ( /resurse if mmultiple sub directories )
  Powershell way - b) Add-Windows-Driver -Path "C:\imagefolder" -driver "C:\driverfolder"
  
  
 
 
  
