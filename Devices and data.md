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
  
## Export drivers
a) export-windowsdriver -online destination C:\thirdpartyonly or use the -all parameter to get all of the drivers exxported for a specific machine.

## Add a driver example
 pnputil /add-driver C;\sound_driver\example.inf  - select yes to the prompt. 
 
 ## add a driver to a offline image
 
The powershell and DISM share the same code base so it really does not matter which tool is used. I will use DISM here
dism /mount-image /imagefile:c:\test\test.wim /index:1 /mountdir:c:\mount  ( the mount directory is a created follder to store the mounted wim file while we make changes to it ) 
- dism /image:C:\mount /add-driver /driver:c:\some_driver\example.inf ( this will add the driver to the mounted image ) 
Unmount the image and /commit to save the wim file. ( dism /unmount-image /mountdir:c:\mount /commit

# *** Another way to do this is WSim tool , and create an answer file tat will add these drivers to the offline phase and use DISM to point to the xml file so that the process can inject multiple drivers if necessary 

## Check 3rd party driver

dism /image:C:\mount /get-drivers ( show any 3rd party drivers added 
 
 
  
