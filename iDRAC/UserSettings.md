# iDRAC Users Settings for iDRAC9 and 14G PowerEdge Servers
RACADM - > iDRAC.User
## Changing Login Password Using RACADM
To change the password, run the following RACADM command:
> racadm set iDRAC.Users.(index).Password (Password)

* (index) is a value from 1 to 16 (indicates the user account)
* (password) is the new user—defined password.
### Change Default user Password:
Default user <index> value of 1
> racadm set iDRAC.Users.1.Password ADMIN
##  User Permissions or Privilege  (WIP - MAYBE WRONG!)

|iDRAC Specific User Privilege	|Privilege Bit Mask|
|---|---|
|Log in to iDRAC | 0x00000001 |
|Configure iDRAC|0x00000002|
|Configure Users|0x00000004|
|Clear Logs|0x00000008|
|Execute Server Control Commands|0x00000010|
|Access Virtual Console|0x00000020|
|Access Virtual Media|0x00000040|
|Test Alerts|0x00000080|
|Execute Debug Commands|0x00000100|
## Create second user with Administrator Privileges:
1. Set the index and user name.
> racadm set idrac.users.<index>.username <user_name>
Example> racadm set idrac.users.2.username ADMIN
2. Set the password.
> racadm set idrac.users.<index>.password <password>
Example> racadm set idrac.users.2.password ADMIN
3. Set the user privileges.

4. Enable the user.
> racadm set.idrac.users.<index>.enable 1

### Settings to Know:
* iDRAC.Users.Enable (Read or Write)
* iDRAC.Users.IpmiLanPrivilege (Read or Write)
* iDRAC.Users.IpmiSerialPrivilege (Read or Write)
* iDRAC.Users.MD5v3Key (Read or Write)
* iDRAC.Users.Password (Read or Write)
* iDRAC.Users.SHA256Password (Read or Write)
* iDRAC.Users.SHA256PasswordSalt (Read or Write)
* iDRAC.Users.Privilege (Read or Write)
* iDRAC.Users.SHA1v3Key (Read or Write)
* iDRAC.Users.SNMPv3AuthenticationType (Read or Write)
* iDRAC.Users.SNMPv3Enable (Read or Write)
* iDRAC.Users.SNMPv3PrivacyType (Read or Write)
* iDRAC.Users.SolEnable (Read or Write)
* iDRAC.Users.UserName (Read or Write)
