# Install and configure samba share
## Install Samba
`sudo apt install samba`

## Create the directories to be shared
If not already existing, create the directories that should be shared later on
`mkdir /home/<username>/sambashare

## Add share to config file
Add the samba share to the config file. The structure of the file and the various options are explained below.
The config file is under the following directory:
> /etc/samba/smb.conf

## Restart the server
`sudo service smbd restart`

## Set up user accounts
Sambausers have also to be users on the server. For each of those users, a new samba password can be given, since samba doesn't use the system account password
`sudo smbpasswd -a username`

## Connect to the share
On ubuntu: Open a file manager and enter 
> smb://ip-address/sambashare 

where sambashare is the directory, on which should be connected

# Configuration
## Add a new directory to share
Add the following to the section *Share Definitions* in the config file. In the parenthesis are explanations.

[sambashare] *(This name will be used to connect to the share)*   
&nbsp;&nbsp;comment = Directory to be shared with name sambashare  
&nbsp;&nbsp;path = /path/to/directory *(The absolute path to the directory)*  
&nbsp;&nbsp;read only = no  
&nbsp;&nbsp;browsable = yes  
&nbsp;&nbsp;valid users = pi *(A list of all users who can access this share)*     

