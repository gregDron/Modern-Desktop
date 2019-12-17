
####Registry 

NTUser.dat 
Resides in the current user folder and is the represantation of the user hive of the registry. 

## Specific system settings 
Reside in the C:\windows\system32\Config folder 

## Registry branches
a) HKCC - HKLM\SYSTEM\CurerntControlSet\Hardware Profiles\Current
b) HKCU - HKU\<SID Identifier>
c) HKCR - HKLM\SOFTWARE\Classes + HKCU\Software\Classes

## Registry Backup options
a) System restore includes the registry
b) Windows 7 Backup program - perform a "System state " , which includes the registry.
c) Export the specific key as a backup for the changes about to be made.

##Prefrences
Can be changed by the user , settings that can be re-applied constantly but the user can change these. Alot of preferences have been re-done the default registry settings.
Basically overlap tru policies , also have a different gui better fi;ltering

# GPO Denying
Within the delegates tab add the group you want to deny processing for and check the "deny" apply gpo settings option.

### MMAT
Free tool , figures out which GPO's apply to the computer of interest.
Gets the XML for those GPO's
Runs an analysis and produces reports on which GPO settings should correlate to one or more Intune settings
Gives you detail on which GPo can be translated to a mobile environment.

## ADMX-Backed Policies

- A manula method for getting GPO settings into Intune
- USes the Policy CSO
- ADMX files are "so8urce code" for Registry-based GPO
- Only works with select ADMX and is tedious

## 
