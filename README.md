![Arduino Expansion Board with Intel® Edison](arduino_expansion_board_with_edison.jpg)

# How to go from Zero to Blinking Light Hero

_Instructions for **Intel® Edison** installed on an **Arduino-compatible expansion board** using the Intel® IoT Developer Kit **(C/C++ or JavaScript development workflow)**_


## 1. Get Started with Intel® Edison

Find out what hardware is included with your Intel® IoT Developer Kit ("dev kit"). And review important assembly and cable hook up instructions.

* [Assembly - Arduino expansion board »](assembly-arduino_expansion_board/assembly.md)
* [Connecting Cables - Arduino expansion board »](assembly-arduino_expansion_board/connecting_cables.md)


## 2. Set Up Your Computer

Install software and drivers specifically for your computer's operating system. 

* **Mac or Linux user?** 

  You have no special setup. Skip to [Step 3](#3-shell-access) below.

* **Windows 64-bit user?** 

  [Set Up Your Computer - Windows (64-bit integrated installer) »](set_up_your_computer-windows/64bit_integrated_installer.md)

* **Windows 32-bit user?** *Or can't get 64-bit integrated installer running?* 

  [Set Up Your Computer - Windows (manual installation) »](set_up_your_computer-windows/manual_installation.md)


## 3. Shell Access

Gain command line access of your IoT board. Execute special Linux commands to configure your IoT board such as setting up Wi-Fi.

* [Shell Access - Windows »](shell_access-windows/serial_connection.md)

* [Shell Access - Mac »](shell_access-mac-linux/serial_connection-mac.md)

* [Shell Access - Linux »](shell_access-mac-linux/serial_connection-linux.md)


## 4. Flash Edison Firmware

Some Edison boards have older firmware images on them. You **_may_** need to update the firmware to a newer version to get access to important features.

* [Flash Edison Firmware Manually »](flash_firmware/manually.md)


## 5. Get Your IoT Board Online

Get your board online in order to turn your IoT board into a true "Internet of Things" device. You also need the IP address of your IoT board to program it using the dev kit IDEs.

* **At a hackathon? On a busy or restricted Wi-Fi network?**

  * [Ethernet over USB - Windows »](ethernet_over_usb/windows.md)
  * [Ethernet over USB - Mac »](ethernet_over_usb/mac.md)
  * [Ethernet over USB - Linux »](ethernet_over_usb/linux.md)

* **At home? Have a dependable Wi-Fi connection?**

  * [Get Your Edison Board Online »](connect_to_wifi/connect.md)


## 6. Install an IDE

Based on your programming language preference, install an IDE for Intel® IoT development:

* **For C/C++:**
  * [Set Up IoT Dev Kit Eclipse »]()

* **For JavaScript:**
  * [Set Up Intel XDK for IoT »]()

* **For simplified C++:** 
  * [Set Up Arduino IDE »](https://software.intel.com/en-us/articles/install-arduino-ide-on-intel-iot-platforms)


## 7. Sensor Tutorials

Experiment with sample code supplied for available sensors and actuators.

* [Grove Starter Kit - JavaScript »]()

Also search for your component on [software.intel.com/en-us/iot/sensors](software.intel.com/en-us/iot/sensors).


## Now make your own creation!

Take pictures along the way. Create your own guide and
post them to [Instructables.com](http://instructables.com/id/intel).


## Running into issues?

Search for answers and post your questions to the [Intel® Edison Support Community](https://communities.intel.com/community/tech/edison).


## Resources

* [Intel® Edison Product Brief](http://www.intel.com/support/edison/sb/CS-035277.htm) (Specs)

* [Intel® Edison Arduino Expansion Board Hardware Guide](http://www.intel.com/support/edison/sb/CS-035275.htm) - For pinout listing, see page 7

* [Intel® Edison Mini Breakout Board Hardware Guide](http://www.intel.com/support/edison/sb/CS-035252.htm) - For pinout listing, see page 9 

* [Yocto Project: Foundation for the Internet of Things](https://www.youtube.com/watch?v=ztsnQ3p59jA&list=PLg-UKERBljNw254jnyMNZiu8yqF8pPq0m&index=24) (Introduction to Yocto video)

* [Intel® IoT Developer Kit Cloud-based Analytics User Guide](https://software.intel.com/en-us/intel-iot-developer-kit-cloud-based-analytics-user-guide) 

* [Seeed Studio Sketchbook Starter Kit](https://github.com/Seeed-Studio/Sketchbook_Starter_Kit_V2.0) (Sensor sample code for Arduino IDE)

