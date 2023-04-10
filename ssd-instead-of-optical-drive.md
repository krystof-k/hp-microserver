# SSD instead of optical drive

The MicroServer has a fifth SATA port for an optical drive, which can be used to connect an SSD while leaving all four 3.5" drive bays available.

## How to connect the SSD

To connect the SSD, use the SATA port intended for the optical disc drive, which is located on the left of the motherboard power connector.

However, it's a bit more complicated with the power. You have two options:

- buy a floppy 4-pin to SATA power cable (such as [Delock 83918](https://www.amazon.de/-/cs/dp/B018NKPZVW)) and place a 2.5" SSD in the optical drive's place, or
- buy a PCIe M.2 adapter (such as [AXAGON PCEM2-D](https://www.amazon.de/AXAGON-PCEM2-D-Anschluss-Festplatten-Computer/dp/B07VM1RV3Y)) and use an M.2 SATA SSD.

## How to voot from the SSD

The MicroServer always tries to boot from the first slot in SATA AHCI mode.

To boot from a different port, such as port 5, follow these steps to switch to SATA legacy mode:

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
