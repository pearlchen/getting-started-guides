![Arduino Expansion Board with Intel® Edison](images/arduino_expansion_board_with_edison.jpg)

# How to go from Zero to Blinking Light Hero

_Instructions for **Intel® Edison** installed on an **Arduino-compatible expansion board** using the Intel® IoT Developer Kit **(C/C++ or JavaScript development workflow)**_


## 1. Get Started with Intel® Edison

Find out what hardware is included with your Intel® IoT Developer Kit ("dev kit"). And review important assembly and cable hook up instructions.

* [Assembly - Arduino expansion board »](/assembly/arduino_expansion_board/assembly.md)
* [Connecting Cables - Arduino expansion board »](/assembly/arduino_expansion_board/connecting_cables.md)


## 2. Set Up Your Computer

Install software and drivers specifically for your computer's operating system. 

* **Mac or Linux user?** 

  You have no special setup. Skip to [Step 3](#3-shell-access) below.

* **Windows user?**

  * **Do you have 64-bit Windows and a reliable internet connection?**  

      [Set Up Your Computer - Windows (64-bit integrated installer) »](/computer_setup/windows/64bit_integrated_installer.md)

  * **At a hackathon with unreliable internet? Or can't click 'Next' in the 64-bit integrated installer wizard?** 

      [Set Up Your Computer - Windows (manual installation) »](/computer_setup/windows/manual_installation.md)


## 3. Shell Access

Gain command line access of your IoT board. Execute special Linux commands to configure your IoT board such as setting up Wi-Fi.

* [Windows »](/shell_access/windows/serial_connection.md)
* [Mac »](/shell_access/mac/serial_connection.md)
* [Linux »](/shell_access/linux/serial_connection.md)


## 4. Flash Edison Firmware

Some Edison boards have older firmware images on them. You **_may_** need to update the firmware to a newer version to get access to important features.

* [Flash Edison Firmware Manually »](/flash_firmware/manually.md)


## 5. Get Your IoT Board Online

Get your board online in order to turn your IoT board into a true "Internet of Things" device. You also need the IP address of your IoT board to program it using the dev kit IDEs.

* **At a hackathon? On a busy or restricted Wi-Fi network?**
  
  Connect to the Intel® Edison using the device mode micro-USB cable and a virtual Ethernet connection known as "Ethernet over USB":
  
  * [Windows »](/connectivity/ethernet_over_usb/windows/connect.md)
  * [Linux »](/connectivity/ethernet_over_usb/linux/connect.md)
  * Note: At this time, Ethernet over USB on [Mac](/connectivity/ethernet_over_usb/mac/connect.md) is not officially supported.

* **At home? Have a dependable Wi-Fi connection?**

  * [Connect Your Intel Edison to Wi-Fi »](/connectivity/wifi/connect.md)


## 6. Install an IDE

Based on your programming language preference, install an IDE for Intel® IoT development:

* **For JavaScript:**
  * [Set Up Intel XDK for IoT »](/ide_setup/xdk/setup.md)
  * [Run a Sample Intel XDK for IoT Project »](/ide_setup/xdk/create_project.md)

* **For C/C++:**
  * [Set Up IoT Dev Kit Eclipse »](/ide_setup/eclipse/setup.md)
  * [Run a Sample Eclipse Project »](/ide_setup/eclipse/create_project.md)

* **For simplified C++:** 
  * [Set Up Arduino IDE »](https://software.intel.com/en-us/articles/install-arduino-ide-on-intel-iot-platforms)


## 7. Sensor Tutorials

Experiment with sample code supplied for available sensors and actuators.

* **For JavaScript:**
  * [Grove Starter Kit - JavaScript »](/sensor_examples/javascript/grove_starter_kit.md)

* **For C/C++:**
 * [Grove Starter Kit - C++ »](/sensor_examples/c/grove_starter_kit.md)

Also search for your component on [software.intel.com/en-us/iot/sensors](http://software.intel.com/en-us/iot/sensors).


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
