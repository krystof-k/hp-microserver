# SSD instead of optical drive

MicroServer has a 5th SATA port for optical drive which can be used for connecting a SSD while leaving all four 3.5" drive bays available.

## How to connect the SSD

To connect the SSD, you can use the SATA port for the optical disc drive, located on the left of the motherboard power connector.

However, it gets a bit more complicated with the power. You have two options:

- buy a floppy 4-pin to SATA power cable (for example [Delock 83918](https://www.amazon.de/-/cs/dp/B018NKPZVW)) and place a 2.5" SSD in the place for optical drive or
- buy a PCIe M.2 adapter (for example [AXAGON PCEM2-D](https://www.amazon.de/AXAGON-PCEM2-D-Anschluss-Festplatten-Computer/dp/B07VM1RV3Y)) and use a M.2 SATA SSD.

## How to boot from the SSD

MicroServer always tries to boot from the first slot in SATA AHCI mode.

To boot from a different port, e.g. port 5, you need to switch to SATA legacy mode:

1. boot into the BIOS (press F9)
2. _System Options_
3. _SATA Controller Options_
4. _Embedded SATA Configuration_
5. _Enable SATA Legacy Support_
6. reboot
    
And change the SATA controller boot order:

7. boot into the BIOS again
8. _Boot Controller Order_
9. Set the _Intel(R) SATA Controller #2_ as first
10. reboot
