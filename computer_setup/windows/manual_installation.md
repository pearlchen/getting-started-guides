# Set Up Your Computer - Windows (manual installation)

This setup document will guide you through manually preparing your Windows 32-bit or 64-bit computer with any Windows-specific software or drivers required for Intel® Edison development. 

---

**Are you running 64-bit Windows and have a good internet connection?**

For a more streamlined setup process, try the integrated program installer. Refer to [Set Up Your Computer - Windows (64-bit integrated installer) »](64bit_integrated_installer.md). 

---


**Table of contents**

* [Install Intel® Edison standalone drivers »](#install-intel-edison-standalone-drivers)
* [Install FTDI serial drivers »](#install-ftdi-serial-drivers)
* [Restart your computer »](#restart-your-computer)

**Related videos**

[Intel Edison: Set Up Your Computer Manually - Windows (preview video)](https://drive.google.com/open?id=0B6gHgawzKtxCbUxicmpBc2JZSmM&authuser=0)


## Install Intel® Edison standalone drivers

The [Windows standalone drivers](https://software.intel.com/iot/hardware/edison/downloads) for Intel® Edison include several USB drivers in one installer package. These drivers enable important features, such as:

* Composite Device Class (CDC) for programming the board via the Arduino IDE,
* Remote Network Driver Interface Spec (RNDIS) for Ethernet over USB, and
* Device Firmware Upgrade (DFU) for updating firmware on devices.

![Animated gif: installing Intel® Edison drivers](images/install_edison_drivers-animated.gif)

[View detailed instructions »](details-install_edison_drivers.md)


## Install FTDI serial drivers

[FTDI CDM drivers](http://ftdichip.com/Drivers/D2XX.htm) allow your computer to communicate with USB serial devices, including the Intel® Edison.

![Animated gif: installing Intel® Edison drivers](images/install_ftdi_cdm_drivers-animated.gif)

[View detailed instructions »](details-install_ftdi_cdm_drivers.md)


## Restart your computer

To ensure driver installation changes take effect, reboot your Windows computer at this point.

![Choose Restart from the Windows Start menu](images/restart_windows.png)

---

### Next Steps

[Confirm driver installation »](confirm_drivers.md)
