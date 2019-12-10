# Modern-Desktop

### Search
** Search is one of the componenets of windows 10 that now gives you a modern feel to what you are trying to find. from documents to people , internet searchesec all built into one single pane of glass.

## Auto pilot

Vendor -- > Hardware ID's are added -- > Administrator configures deployment profiles--> Device is shipped  -- End user recieves --> Wifi needed -- > Deployment profile is pushed to the machine --> User logon corp ID --> Azure AD will verify and add to Azure AD -- > Intune is enrolled and apps/polocies are downloaded and installed.

## Device hgardware ID

a) Unique IDentifier
b) Individual Hardware only
c) Associated with the tenant.
d) 



# Windows 10 updating and Managing

Run the following command via the upgrade media.

- Start /wait setup.exe /auto upgrade /quiet /noreboot /dynamicupdates disabled /compat scanonly 
echo %errorlevel%   -  this will output the error level for the command. 

MAP toolkit is another good solution that is used locally for devices such as offline machines and specific machines to target.

Software readiness is anpotherpossible solution which is tied to Microsoft Analytics and allows you to gether information via GPO straight to the Azure cloud. This is free but requires configuration.
