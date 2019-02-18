# Disable Boot Optimized Storage Solution (BOSS)
Objective: Disable Booting to OS of BOSS


Solution| API | Info
----|----|----
Disable UEFI Boot Option | iDRAC Web Console |Login > Configuration>BIOS Setting>Boot Settings> UEFI Boot Settings>Unselect AHCI Controller in SlotN (Boss)
Disable UEFI Boot Option | Console| F2>system Setup>  Bios Settings> Boot Settings> UEFI Boot Setting> UEFI Boot Settings>Unselect AHCI Controller in SlotN (Boss)
Disable Slot with BOSS| iDRAC Web Console| Login > Configuration> BIOS Settings> Intergraded Devices> Slot Disablement
Disable Slot with BOSS| Console| Login > F2>System Setup> System Bios Configuration – Intergraded Devices – Slot Disablement
Disable Slot with BOSS| RACADM| Login > F2>BIOS.SlotDisablement.Slot N Example:Racadm BIOS.SlotDisablement.Slot2 Disabled
