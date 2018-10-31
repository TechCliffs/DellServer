# Open Manage Server Administrator Cheat Sheet
## Windows Unattended OMSA
### Unattended Basics:

OMSA uses msiexec.exe to unattended install with Windows.
>msiexec.exe

i/ = Filelocation
>msiexec.exe /i <Filelocation\SysMgmtx64.msi>

/qn = Quiet  & No GUI
>msiexec.exe /i <Filelocation\SysMgmtx64.msi> /qn

#### Options

ADDLOCAL = Install specific Feature ID or multiple packages
>msiexec.exe /i SysMgmtx64.msi ADDLOCAL=iDRAC12G,SA /qn

REMOVE = Uninstall specific Feature ID or multiple Packages
>msiexec.exe /i SysMgmtx64.msi ADDLOCAL=iDRAC12G,SA /qn

REINSTALL = Reinstall specific Feature ID or multiple Packages
>msiexec.exe /i SysMgmtx64.msi REINSTALL=BRCM /qn

### Install Only RACADM Local
>msiexec.exe /i SysMgmtx64.msi ADDLOCAL=iDRAC12G /qn

### OMSA Packages include:

Feature ID|	Description
---|---
ALL| All features
BRCM |	Broadcom Network Interface Card (NIC) Agent
QLG|	QLogic SNMP Agent
INTEL	|Intel NIC Agent
IWS|	Server Administrator Web Server
OMSS|	Server Administrator Storage Management Service
iDRAC |(for 11th generation of PowerEdge servers)	Integrated DRAC Command Line Tools
iDRAC12G| (for 12th generation of PowerEdge servers)	Integrated DRAC Command Line Tools
SI |	Server Instrumentation
RmtMgmt |	Remote Enablement
CLI	|Command Line Interface of Server Instrumentation
WMI	|Windows Management Instrumentation Interface of Server Instrumentation
SNMP|	Simple Network Management Protocol Interface of Server Instrumentation
OSLOG	|Operating System Logging
SA|	Installs SI, CLI, WMI, SNMP, OSLOG
OMSM|	Installs SI, OMSS, CLI, WMI, SNMP, OSLOG
