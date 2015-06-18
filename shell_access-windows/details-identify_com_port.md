## Identify the serial COM port

Use Device Manager to find the COM port number for the "**USB Serial Port**" connection. You will need the COM # to configure PuTTY in Establish a serial connection.

![Animated gif: identifying the serial COM port](images/identify_com_port-animated.gif)

---

1. Open Device Manager and scroll down to the "**Ports (COM & LPT)**" section.

  _Don't know how? Refer to [Confirm Drivers → Open Device Manager](../set_up_your_computer-windows/confirm_drivers.md#open-windows-device-manager)._

2. **Make a note of your COM #** for the "**USB Serial Port**" device. 

  ![USB Serial Port entry in Device Manager](images/device_manager-usb_serial_highlighted.png)

---

**Do you have the right COM number?**

Use the COM # shown on your computer's Device Manager. In the screenshot, it is "COM3" but your computer will have unique COM port number assignments and may be different from the screenshot.

Do **not** use the COM number for "Intel Edison USB Composite Device" or "Intel Edison Virtual Com Port".

---

**Don't see a "USB Serial Port" device listed?**

* **Do you have the serial drivers installed?**
  * A serial connection cannot be detected without FTDI serial drivers. Refer to [Set Up Your Computer - Windows (64-bit integrated installer)](../set_up_your_computer-windows/64bit_integrated_installer.md) or Set Up Your Computer - Windows (manual).

* **Do you have the UART/serial cable connected?** Refer to [Connecting Cables → UART/serial micro-USB cable](../assembly-arduino_expansion_board/connecting_cables.md#uartserial-micro-usb-cable).

* Is your IoT board powered on?

---
