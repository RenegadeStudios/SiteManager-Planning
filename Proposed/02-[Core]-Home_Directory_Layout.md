# [Core] Home Directory Layout
**Status:** `Proposal`

## Scope

Documenting the proposed default Home Directory Layout.  Listing both pros and cons to doing it this way.


## Directory Layout

### Home

Use the default user directory of the system 

Linux: `/home/username`

Windows: `C:\Users\Username`

**Note:** The username _should_ always match the SiteManager account name given to the account.

### Domain/Site

All domain specific files should live in a folder matching the domain.

Eg. `/home/username/somedomain.com`


#### HTTP Files

All files pertaining to HTTP should be in the `http` sub-directory for the domain.  

##### Website files

All files that will be served via the webserver for the website should reside in `public` this not only promotes clean file structure but also allows us to support various web frameworks that use a `public` folder to server the website from.

***Note:*** Not all frameworks use a `public` folder, we may allow this to be reconfigured via the websites administration panel.

##### Temporary Storage

Temp files for the specific site will be stored in `temp`.

##### Site Logs

Site logs will be placed in `logs`. eg. error_log


#### FTP Files

All files pertaining to Public FTP will be stored in `ftp`.  By default this is not enabled.


#### Email

All email related files and folders will reside in `mail`.


#### Custom Compiled Software

All custom compiled software for a specific site will be located in `local` mimicking the `/usr/local` layout.  
eg. A custom compiled PHP would live in `local`


#### Configuration Files

All configuration files for all services for the domain will be stored in `config`.  There will be configurations for HTTP, FTP and Email stored here, along with any other services configured by SiteManager.

