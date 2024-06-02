# Recommended BIOS settings

- **Disable network boot**

  If you don't boot from the network, it is a good idea to disable it as it will speed up the boot a little bit.
  
  1. Go to _System Options_.
  2. Select _Embedded NICs_.
  3. And set both _NIC 1 Boot Options_ and _NIC 2 Boot Options_ to _Disabled_.

- **Leave power control to operating system**

  Probably, leaving the power control to the operating system is a better idea.
  
  1. Go to _Power Management Options_.
  2. Set _HP Power Regulator_ to _OS Control Mode_.

- **Disable RAID controller**

  In case you don't plan to use the RAID controller, disable it:

  1. Go to _System Options_ → _SATA Controller Options_.
  2. Select _Enable SATA AHCI Support_.

- **Disable intelligent provisioning**

  If you don't use intelligent provisioning, it may be good idea to disable it as it may speed up the boot a little bit.
  
  1. Go to _Server Security_.
  2. And set _Intelligent Provisioning (F10 Prompt)_ to _Disabled_.
 
  _Note: disabling inteligent provisioning will also disable Smart Storage Administrator._

- **Set server name**

  You can set server name, which is used for example in iLO.
  
  1. Go to _Server Asset Text_ → _Server Info Text_.
  2. And set _Server Name_ to something.
