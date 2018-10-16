RACADM Server Configuration File Commands
# Commands

To Export : > racadm **get** -f (filename)

To Import : >racadm **set** -f (file_name).xml -t xml
### RACADM Remote example
export - **get**
> racadm -r (iDrac ip/hostname) -u (iDRAC username) -p (iDRAC Password) get -f (filename) -t (Type) -l (export location)
> racadm -r 192.168.1.20 -u root -p calvin get -f 14Gconfig - type xml -l 192.168.0:/myshare

import - **set**
> racadm -r (iDrac ip/hostname) -u (iDRAC username) -p (iDRAC Password) set -f (filename) -t (Type) -l (export location)

> racadm -r 192.168.1.20 -u root -p calvin set -f 14Gconfig - type xml -l 192.168.0:/myshare


### RACADM Local example
> racadm **get/set** -f (filename) -t (type)

export - **get**
> racadm get -f 14Gconfig -t xml

import - **set**
> racadm set -f 14Gconfig -t xml 


### get Commands options
* -f <filename>—This option enables you to export multiple object values to a file. This option is not supported in the Firmware RACADM interface.
* -u—Specifies user name of the remote CIFS share to which the file must be exported.
* -p—Specifies password for the remote CIFS share to which the file must be exported.
* -l—Specifies network share location to which the file is exported.
* -t—Specifies the file type to be exported.
The valid values are:

> * JSON—It exports the SCP JSON file to a network share file.
> * xml—It exports the SCP xml format file, either to a local or network share file.
> * ini—It exports the legacy configuration file. If -t is not specified, then the ini format file is exported. It can only be exported to a local file.

* NOTE: To import or export Server Configuration Profile xml files, Lifecycle Controller version 1.1 or later is required.
* --clone—Gets the configuration .xml files without system-related details such as service tag. The .xml file received does not have any virtual disk creation option.
* --replace—Gets the configuration .xml files with the system-related details such as service tag.
* -c—Specifies the FQDD or list of FQDDs separated by ',' of the components for which the configurations should be exported. If this option is not specified, the configuration related to all the components are exported.
* --includeph—Specifies that the output of the passwords included in the exported configuration .xml file are in the hashed format.
# Export Location:
## CIFS
> racadm get -f file -t xml -u cifuser -p cifpassword -l //192.168.0/share 
## NFS
> racadm get -f file -t xml -l 10.1.12.13:/myshare
## HTTP
> racadm get -f file -t xml -u httpuser -p httppwd -l http://test.com/myshare
## HTTPS
> racadm get -f file -t xml -u httpuser -p httppwd -l https://test.com/myshare
## Local
The default local export file location:
* Ubuntu: User Home directory 
* Windows: -...-
