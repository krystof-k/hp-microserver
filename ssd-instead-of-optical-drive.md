# SSD instead of optical drive

The MicroServer has a fifth SATA port for an optical drive, which can be used to connect an SSD while leaving all four 3.5" drive bays available.

## How to connect the SSD

To connect the SSD, use the SATA port intended for the optical disc drive, which is located on the left of the motherboard power connector.

However, it's a bit more complicated with the power. You have two options:

- buy a floppy 4-pin to SATA power cable (such as [Delock 83918](https://www.amazon.de/-/cs/dp/B018NKPZVW)) and place a 2.5" SSD in the optical drive's place, or
- buy a PCIe M.2 adapter (such as [AXAGON PCEM2-D](https://www.amazon.de/AXAGON-PCEM2-D-Anschluss-Festplatten-Computer/dp/B07VM1RV3Y)) and use an M.2 SATA SSD.

## How to boot from the SSD

The MicroServer always tries to boot from the first slot in SATA AHCI mode.

There are two workarounds how to boot from a different port, such as port 5.

### A) Switch to SATA legacy mode

This is the easiest option, however this approach results in poorer performance.

Follow these steps to switch to SATA legacy mode:

1. Boot into the BIOS by pressing F9.
2. Go to _System Options_.
3. Select _SATA Controller Options_.
4. Select _Embedded SATA Configuration_.
5. Select _Enable SATA Legacy Support_.
6. Reboot.

Then, change the SATA controller boot order:

7. Boot into the BIOS again.
8. Select _Boot Controller Order_.
9. Set the _Intel(R) SATA Controller #2_ as the first option.
10. Reboot.

### B) Create a RAID 0 array

The other option is to use the embedded RAID controller and create a single-drive RAID 0 array. **Warning: this will wipe your drive!**

Follow these steps to switch to RAID controller mode:

1. Boot into the BIOS by pressing F9.
2. Go to _System Options_.
3. Select _SATA Controller Options_.
4. Select _Embedded SATA Configuration_.
5. Select _Enable Dynamic HP Smart Array B120i RAID Support_.
6. Reboot.

Then, create the RAID 0 array:

7. Boot into the HPE Smart Storage Administrator by pressing F5. (You need to have Intelligent Provisioning enabled.)
8. Select _Dynamic Smart Array B120i RAID_ in the left menu.
9. Select _Configure_.
10. Select _Create Array_.
11. Pick the SSD drive and select _Create Array_.
12. Select _Create Logical Drive_.
13. Click _Finish_.
14. Click _Set Bootable Logical Drive/Volume_.
15. Mark the logical volume as _Primary Boot Logical Drive/Volume_.
16. Click _Finish_.
17. Reboot.
