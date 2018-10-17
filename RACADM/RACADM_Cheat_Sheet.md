# RACADM Cheat Sheet 14G PowerEdge - iDRAC9
Official Dell EMC -
[iDRAC9 RACADM CLI GUIDE - 3.21.21.21](https://www.dell.com/support/manuals/us/en/04/poweredge-r740xd/idrac_3.21.21.21_racadm/introduction?guid=guid-3f6fb670-796a-4724-9d61-ad8a523b7b3e&lang=en-us)

## Local RACADM
Racadm command syntax
>racadm command
## Remote RACADM
Remote RACADM command syntax
>racadm -r (ip or hostname) -u (iDRACusername) -p (iDRACpassword) command

>racadm -r 192.168.1.1 -u root -p calvin command

## Top Commands
iDRAC reset
>racadm racrest

Shutdown Server
>racadm serveraction powerdown

>racadm serveraction graceshutdown


View current job queue
>racadm jobqueue view


Delete/Cancel all Job in Jobqueue
>racadm jobqueue delete --all


Get Systems information
>racadm getsysinfo


List Hardware
>racadm hwinventory


List Software
>racadm swinventory


Collect & Export Tech Support Report
>racadm techsupreport collect -t SysInfo,TTYLog

>racadm techsupport export -f tsr_repot.zip

>racadm techsupreport export -l //192.168.0/share -u myuser -p xxx

## Bonus Commands
 Custom LCD String
 
 racadm 
