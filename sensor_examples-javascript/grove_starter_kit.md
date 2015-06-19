# Create JavaScript-based Intel® IoT projects with the Grove Starter Kit

Instructions for the **Intel® Edison** and **Intel® Galileo**

The Grove System is an easy to use group of modules that minimise the effort required to get started with microcontroller-based experimentation and learning. Intel® has partnered with [Seeed](http://seeedstudio.com), the creators of Grove, to distribute the [Grove Starter Kit Plus - Intel IoT Edition](http://www.seeedstudio.com/depot/Grove-starter-kit-plus-Intel-IoT-Edition-for-Intel-Galileo-Gen-2-and-Edison-p-1978.html) which contains essential sensor and actuator modules to jump start your IoT prototyping.

![The components in the Grove Starter Kit](images/components_in_huddle.png)

This guide will demonstrate how you can use JavaScript and the Grove Starter Kit with any Intel® IoT board to go beyond blinking the onboard LED.


**Table of contents**

* [Inside the Grove Starter Kit box](#inside-the-grove-starter-kit-box)
* [Install the Grove Base Shield](#install-the-grove-base-shield)
* [Connect a Grove component](#connect-a-grove-component)
* [Programming Grove components](#programming-grove-components)
  * [Install code libraries](#install-code-libraries)
    * [MRAA](#mraa)
    * [UPM](#upm)
* [Find code samples](#find-code-samples)
* [Grove component types](#grove-component-types)
  * [Digital outputs](#digital-outputs)
  * [Digital inputs](#digital-inputs)
  * [Analog inputs](#analog-inputs)
  * [Analog outputs](#analog-outputs)
  * [I2C](#i2c)
* [Additional resources](#additional-resources)


**Related videos**

* [Create Intel® IoT projects with the Grove Starter Kit - Part 1 (preview)]()
* [Create Intel® IoT projects with the Grove Starter Kit - Part 2: JavaScript (preview)]()


---

**To follow the instructions in this guide, you will need:**

* the Intel® XDK IoT Edition installed on your development computer
* the Grove Starter Kit for Arduino or Grove Starter Kit Plus - Intel IoT Edition

You also should have already completed the [Set Up Intel XDK for IoT guide](../ide_setup-xdk/setup.md), and you can successfully blink the onboard LED on your Intel® Edison or Intel® Galileo.

---


## Inside the Grove Starter Kit box

The sensors and actuators in the Grove Starter Kit Plus – Intel® IoT Edition for Intel® Galileo Gen 2 work with both the Intel® Galileo and the Intel® Edison.

**Located in the plastic tray inside the green box:**

* Base Shield v2 (look underneath LCD)
* Grove LCD RGB Backlight
* Grove Buzzer
* Grove Sound Sensor
* Grove Touch Sensor
* Grove Temperature
* Grove Light Sensor
* Grove Rotary Angle
* Grove Button
* Grove LED Socket Kit
* Grove Smart Relay

**Look underneath the plastic tray:**

* Grove Servo Motor
* 26AWG Grove Cable (× 10)
* 9V to Barrel Jack Adapter - 126mm
* Red, green, and blue 3mm LEDs
* Grove Starter Kit manual

**Look elsewhere in the cardboard Grove box:**

* Micro-USB Cable
* Ethernet Cable
* 3.3V FTDI USB-to-Serial Cable
* 8GB microSD Card with an SD Card Adapter


## Install the Grove Base Shield

Arduino "shields" are add-ons that plug into standard Arduino header pin configurations. The use of shields allow for additional functionality without having to use an additional prototyping area such as a breadboard.

1. Unplug the Arduino expansion board from all power sources.

2. Line up the male header pins of the Grove Base Shield with the female pins on the Arduino expansion board. 

  Pin configurations of Arduino shields will only fit the Arduino expansion board in one direction so do not force the pins if they do not line up.

3. Push down firmly and evenly on both sides of the Grove Base Shield until the shield is securely installed.

4. Check the voltage toggle (marked VCC, next to A0) on the Grove Base Shield. It should be set to 5V. 

5. Power the expansion board back on. Allow 1 minute for your Intel® Edison or Intel® Galileo to finish booting up.


## Connect a Grove component 

All components in the Grove System use a 4-pin cable with JST connectors. This allows you to prototype without having to individually learn how to wire up each unique component.

1. Choose a component from the Grove System.

  See [Programming Grove components](#programming-grove-components) to help choose a component from the Grove Starter Kit.

2. Use a 4-pin Grove Cable and connect one end of the cable to the component.

  The cable connectors only fit in one direction so you can be confident that the wiring is correct.

3. For the other end of the cable, refer to the the Grove Shield labels for the correct pin to connect to.

  * Digital pins (D2-D8)
  * Analog pins (A0-A3)
  * I2C (bottom row)
  * UART (top right)


## Programming Grove components

### Install code libraries 

#### MRAA

Libmraa (pronounced "em-raah") is a C/C++ library (with bindings to JavaScript and Python) to interface with the GPIO pins on the Intel® Galileo, Intel® Edison, and other platforms. 

Intel® maintains the [MRAA library on Github](https://github.com/intel-iot-devkit/mraa). There is currently no JavaScript-specific API documentation but the method names and signatures are the same as seen in the Python docs.

1. Establish an SSH or serial connection to your Intel® Galileo or Intel® Edison.

  _Don't know how? Refer to [Shell Access](../shell_access/)._

2. Run the following commands on your board. The first command will edit the mraa-upm config file on the board. The last two commands use the board's built-in Opkg package manager to download and update the missing library.

  ```
  echo "src mraa-upm http://iotdk.intel.com/repos/1.1/intelgalactic" > /etc/opkg/mraa-upm.conf
  opkg update
  opkg install libmraa0
  ```

#### UPM

UPM is a higher level library that leverages libmraa for controlling more complex sensors or actuators. A supported sensor will have its own class file that needs to be imported into your project and instantiated. 

Intel® maintains the UPM library on Github. For JavaScript code samples, look for your specific component on [software.intel.com/iot/hardware/sensors](http://software.intel.com/iot/hardware/sensors) or in the [examples → javascript](https://github.com/intel-iot-devkit/upm/tree/master/examples/javascript) folder in the [UPM Github repo](https://github.com/intel-iot-devkit/upm/).

1. Establish a serial connection to your Intel® IoT board, if you're not already connected.

2. Run the following command to use the board's built-in Opkg package manager to download and update the UPM library.

  ```
  opkg install upm
  ```


### Find code samples

1. To find code samples for your component, start by visiting the hardware sensors page at [software.intel.com/en-us/iot/hardware/sensors](https://software.intel.com/en-us/iot/hardware/sensors).

    1. Browse for supported components by paging through the list. Filter the results using the drop down menus on the page.

    2. Click on a component to view additional information and view code samples in C/C++, JavaScript, and Python (when available).

2. Alternatively, to find the most up-to-date UPM code samples, browse the UPM "examples" folder at [github.com/intel-iot-devkit/upm/tree/master/examples](https://github.com/intel-iot-devkit/upm/tree/master/examples).

    3. Go into the "c++", "javascript", or "python" folder and look for your component by model or part name.

## Grove component types

The simpler components in the Grove Starter Kit fall into 2 categories: input or output. These two categories further subdivide into digital or analog. 

Other components in the Grove Starter Kit may use more complex communications protocols such as UART or I2C.

Identifying which category a component falls under is required in order to correctly attach the component to the Grove Base Shield and to understand what code library and commands are needed to control the component.


### Digital outputs

A digital output can write a value of either on (1) or off (0).

Connect to any pin labelled "D" (for "digital") on the Grove Base Shield such as D2 to D8.

<table>
  <tr>
    <td>Grove LED Socket Kit</td>
    <td>Grove Smart Relay</td>
  </tr>
  <tr>
    <td>UPM sample code</td>
    <td>UPM sample code</td>
  </tr>
  <tr>
    <td>require('jsupm_grove')</td>
    <td>require('jsupm_grove')</td>
  </tr>
</table>

**Low level MRAA-only example:**

```
var mraa = require('mraa');

var led = new mraa.Gpio(6);  // set up digital read on digital pin #6
led.dir(mraa.DIR_OUT);  // set the GPIO direction to output

led.write(1);  // set the digital pin to high (1)
```

**Higher level UPM example:**

```
var groveSensor = require('jsupm_grove');

var led = new groveSensor.GroveLed(6); // set up digital output on digital pin #6

led.on();                              // set the digital pin to high
```

If you want to make the LED turn on and off, add a setTimeout() or setInterval() to toggle between writing 1 or 0 to the digital pin.  

### Digital inputs

A digital input can read a value as either on (1) or off (0).

Connect to any pin labelled "D" (for "digital") such as D2 to D8 on the Grove Base Shield.

<table>
  <tr>
    <td>Grove Button</td>
    <td>Grove Touch Sensor (TTP223)</td>
  </tr>
  <tr>
    <td>UPM code samples</td>
    <td>UPM code samples</td>
  </tr>
  <tr>
    <td>require('jsupm_grove')</td>
    <td>require('jsupm_ttp223')</td>
  </tr>
</table>

**Low level MRAA-only example:**

```
var mraa = require('mraa');

var button = new mraa.Gpio(5);     // set up digital read on digital pin #5
button.dir(mraa.DIR_IN);           // set the GPIO direction to input

var buttonState = button.read();   // read the value of the digital pin
console.log(buttonState);          // write the value to the console for debugging
```

**Higher level UPM example:**

```
var groveSensor = require('jsupm_grove');

var button = new groveSensor.GroveButton(5); // set up digital input on pin #5

var buttonState = button.value();  // read the value of the digital pin
console.log(buttonState);          // write the value to the console for debugging
```

To react to button press beyond application startup, add a `setTimeout()` or `setInterval()` to periodically poll the pin state.

### Analog inputs

An analog input will read a value as between 0 and 1024.

Connect to any pin labelled "A" (for "analog") on the Grove Base Shield such as A0 to A3.

<table>
  <tr>
    <td>Grove Light Sensor</td>
    <td>Grove Rotary Angle</td>
    <td>Grove Temperature</td>
    <td>Grove Sound Sensor</td>
  </tr>
  <tr>
    <td>UPM code samples</td>
    <td>UPM code samples</td>
    <td>UPM code samples</td>
    <td>UPM code samples</td>
  </tr>
  <tr>
    <td>require('jsupm_grove')</td>
    <td>require('jsupm_grove')</td>
    <td>require('jsupm_grove')</td>
    <td>require("jsupm_mic")</td>
  </tr>
</table>


**Low level MRAA-only example:**

```
var mraa = require('mraa');

var light = new mraa.Aio(0);     // set up analog input on analog pin #0 (A0)

var lightValue = light.read();   // read the value of the analog pin
console.log(lightValue);         // write the value to the console for debugging
```

**Higher level UPM example:**

```
var groveSensor = require('jsupm_grove');

var light = new groveSensor.GroveLight(0); // set up analog input on pin #0 (A0)

var lightValueRaw = light.raw_value();     // read the raw value of the analog pin
var lightValue = light.value();            // read the converted value of the pin
console.log(lightValueRaw, lightValue);    // write values to console for debugging
```

To react to changes in light beyond application startup, add a `setTimeout()` or `setInterval()` to periodically poll the sensor value.

### Analog outputs

An analog output is a digital output in disguise. Intel® IoT boards are digital microcontrollers that can pretend to be analog using a concept called Pulse Width Modulation (PWM). 

Analog outputs will accept a floating-point value representing a duty cycle percentage between 0 (always off), 1.0 (always on). For example, a value of 0.5 will rapidly pulse equally between on and off.

Components will only work when connected to PWM-enabled pins! By factory default, these PWM pins are D3, D5, and D6. (Digital pin #9 is also available on the Arduino expansion board via the standard female header pin.)

<table>
  <tr>
    <td>Grove LED Socket Kit</td>
    <td>Grove Buzzer</td>
    <td>Grove Servo Motor (ES08A)</td>
  </tr>
  <tr>
    <td>(no UPM sample)</td>
    <td>UPM sample code</td>
    <td>UPM sample code</td>
  </tr>
  <tr>
    <td></td>
    <td>require("jsupm_buzzer")</td>
    <td>require("jsupm_servo")</td>
  </tr>
</table>


**Low level MRAA-only example:**

```
var mraa = require("mraa");

var led = new mraa.Pwm(3);  // initialize PWM on digital pin #3

led.write(0.5);             // make LED half brightness

///--- below example: fade over time ---

var brightness = 1;
var fadeInterval;

function fade(){
  led.write(brightness);
  brightness -= 0.01;
  if (brightness < 0) clearInterval(fadeInterval);
}

fadeInterval = setInterval(fade, 100);
```

**Higher level UPM example:**

Please see: [https://github.com/intel-iot-devkit/upm/blob/master/examples/javascript/es08a.js](https://github.com/intel-iot-devkit/upm/blob/master/examples/javascript/es08a.js)


### I2C

I²C (Inter-Integrated Circuit), pronounced both "I-two-C" or "I-squared-C", is a multi-master, multi-slave, single-ended, serial computer bus used for attaching lower-speed peripherals to processors on computer motherboards and embedded systems.

<table>
  <tr>
    <td>Grove LCD RGB Backlight (JHD1313M1)</td>
  </tr>
  <tr>
    <td>UPM code samples</td>
  </tr>
  <tr>
    <td>require ('jsupm_i2clcd')</td>
  </tr>
</table>

**Higher level UPM example:**

```
var jsUpmI2cLcd  = require ('jsupm_i2clcd');
 
var lcd = new jsUpmI2cLcd.Jhd1313m1(6, 0x3E, 0x62); // Initialize the LCD

lcd.setCursor(0,1); // go to the 1st row, 2nd column (0-indexed)
lcd.write("hello"); // print characters to the LCD screen
```

# Additional resources

* Article: [Using MRAA to Abstract Platform I/O Capabilities](https://software.intel.com/en-us/articles/internet-of-things-using-mraa-to-abstract-platform-io-capabilities) 

* For PWM hardware configuration on the Arduino expansion board, refer to section 3.2 "Intel® Edison kit for Arduino* PWM swizzler" in the Intel® Edison Kit for Arduino* Hardware Guide: http://www.intel.com/support/edison/sb/CS-035275.htm

* Sensor sample code for Arduino IDE: [Seeed Studio Sketchbook Starter Kit](https://github.com/Seeed-Studio/Sketchbook_Starter_Kit_V2.0)
