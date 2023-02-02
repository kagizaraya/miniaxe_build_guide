# MiniAxe build guide

[To people who purchased at Ten-key Vol.1](tenkey_vol1_en.md)

## Before build
* Please be aware of injuries with soldering irons, tools, parts etc.
* When you leave your seat during work, please confirm that the soldering iron is turned off.
* Very small parts are included, so be careful not to lose any.

## Confirm contents
The following parts are included in the kit. Please check whether there is any shortage before work.

The soldered kit includes only the part number (13) and later, so please check.



![Contents of kit](images/IMG_2761.jpg)

Number | Name | Value | Qty | Remarks | Place
:----|:--------|:-----|:----|:-----------------|:-------
1 | PCB | | 2 | 1 for left hand, 1 for right hand |
2 | Resistor | 10 kΩ | 5 | 1 spare, colored with green sticker or marker on tape package<sup>[1](#marker)</sup>. Marked "103" on the component. | R1, R4
3 | Resistor | 22 Ω | 5 | 1 spare, colored with yellow sticker or marker on tape package<sup>[1](#marker)</sup>. Marked "220" on the component. | R2, R3
4 | Capacitor | 1 μF | 5 | 1 spare, colored with blue sticker or marker on tape package<sup>[1](#marker)</sup>. | C1, C3
5 | Capacitor | 0.1 μF | 3 | 1 spare, no sticker or marker. | C2
6 | Capacitor | 22pF | 5 | 1 spare, colored with red sticker or marker on tape package<sup>[1](#marker)</sup> | C4, C5
7 | Schottky diode | | 2 | | D1
8 | Crystal oscillator | 16 MHz | 2 | | Y1
9 | MPU | ATMEGA 32 U 4 | 2 | | U1
10 | USB connector | Micro B female | 4 | | J1, J2
11 | Tact switch | | 2 | | SW20
12 | Switch socket | | 36 | | SW1 - SW18
13 | M2 screw | 8 mm | 8 |
14 | M2 screw <sup>[2](#screw)</sup> | 4 mm | 8 |
15 | M2 resin standoff | 3 mm | 8 |
16 | M2 Metal standoff <sup>[3](#metal_spacer)</sup> | 3.5 mm | 8 |
17 | Top plate | | 2 |
18 | Bottom plate | | 2 |
19 | Rubber feet | | 10 |
20 | USB cable | | 1 | Connect between left and right. |

## Other required items
In order to complete the kit, the following parts must be prepared separately.

* Key switch (CherryMX compatible only support. Low-profile type is not supported)
* Key caps
* USB Micro B cable (for connection with PC)

## Required tools
In order to build, the following tools are required at minimum.

* Soldering iron (preferred temperature controllable)
* Lead solder
* Tweezers
* Phillips head screwdriver
* Magnifier
* Flux (Seriously. Fine-pitch SMD soldering is no fun without flux.)

In addition, you may also prepare the following as necessary.

* Flux remover
* Solder wick
* Multimeter



# Buid procedure

For the soldered kit, proceed with building from the item [Verify that it is recognized as a USB device](#verify-that-it-is-recognized-as-a-usb-device).



## Solder MPUs
1. Place the ● mark (pin 1 marking) on the MPU aligned with the ○ mark on the board.
2. Make sure that all pins are on the pad and solder them.

![MPU](images/IMG_2794.jpg)

For the QFP package soldering, this [video](https://youtu.be/b9FC9fAlfQE?t=1172) may be helpful.

## Solder crystal oscilators
1. Align the long side of the crystal oscillator (which may be either long side) so that it sits parallel with the Y1 marking on the board and place it at the center of the four pads.
2. Since only a little bit of the PCB pads can be seen at the corners of the crystal oscillator, apply solder while warming the corners of the crystal.

![Crystal](images/IMG_2796.jpg)

This [video](https://www.youtube.com/watch?v=14fJTgFg03M) may be helpful for soldering SMD crystal oscillator.

## Solder resistors
1. SMD resistors and capacitors are very small and are easy to lose. During assembly, completely solder one component before removing the next one from the tape.

![Resistor](images/IMG_2802.jpg)

## Solder capacitors
1. The included capacitors do not have values printed on them. Be careful. 

![Capacitor](images/IMG_2803.jpg)

## Solder schottky diodes
1. The diode must be installed in the correct orientation. Align the part so that the white band is on the same side as the vertical bar of the diode symbol on the board.

![Diode](images/IMG_2775.jpg)

## Solder USB connectors
1. Solder the 5 central pins first, THEN the 4 outer tabs to ensure proper alignment.

![USBConnector](images/IMG_2779.jpg)

## Solder tact switches
1. Since the tactile switch has a little metallic part on the side, heat that area with a soldering iron and let the solder flow.

![TactSwitch](images/IMG_2806.jpg)

## Solder hotswap sockets
1. **CAUTION**  
   _There are 2 places (SW 7, SW 8) in the center of the PCB where the orientation of the socket is different from the others._  
   _If you install it in the wrong direction, the hole in the middle where the key switch is attached will be blocked._
2. Solder those two places first, check their orientation/placement, THEN solder the rest to avoid any issues.

![Socket](images/IMG_2807.jpg)

## Check whether the soldering is properly done
Refer to the schematic ([left side](files/MiniAxeLeft.pdf), [right side](files/MiniAxeRight.pdf)) and check whether soldering is correctly done.

Before connecting to the computer, at least check the following.

1. Check that there is no short circuit between UVCC - GND and VCC - GND.
2. Make sure the MPU pins are not bridged.
3. Make sure the USB connector pins are not bridged.

## Verify that it is recognized as a USB device  
1. Do not join the two sides of the keyboard yet.  
2. Insert a cable into the female microUSB port labeled J1 on one side of the keyboard only. Connect the other end of the cable to your computer.  
3. Confirm that it is recognized as a USB device. Unplug and repeat for the other side of the keyboard.  

* For Mac, start "System Information" and check whether the device named "ATm32U4DFU" is visible.
![System Information](images/system-info.png)

* For Windows, start "Device Manager" and under "libusb-win32 devices", check whether the device named "ATmega32U4" is visible.  
![System Information](images/device-manager.png)

* For the soldered kit, make sure that "MiniAxe" is visible on Mac or Windows.

If it is not recognized as a USB device, please double check the schematic to see if all parts are properly soldered.

## Assemble the top plate

**The cut surface of the key switch hole on the top plate is tapered due to the characteristics of the laser cutter, so the size of the hole is slightly different on the front and back sides. Try mounting the key switch to be installed on the front and back sides of the top plate, and treat the side that is easier to mount as the front side.**

1. Insert M2 x 8 mm screws into the top plate and fix screws with a masking tape.
![Top plate](images/IMG_2811.jpg)
2. Turn the top plate over and attach resin standoffs.
![Resin standoffs](images/IMG_2812.jpg)
3. Combine with the PCB.
4. Attach metal standoffs to screws exposed on the PCB and tighten screws.
![Metal standoffs](images/IMG_2814.jpg)

## Assemble the bottom plate
1. Insert an M3 x 3 mm screw into the bottom plate and turn a few times. Select the diagonally opposite screw and turn a few times (e.g. upper left → lower right → upper right → lower left etc.). Repeat until all screws are loosely attached. **Do not completely tighten the first screw and then do another one. Tighten evenly and gradually.**

![Bottom plate](images/IMG_2815.jpg)

# Attach rubber feet
1. Attach the rubber feet on the bottom plate.
![Rubber feet](images/IMG_2816.jpg)

## Install key switches and caps, USB cables

**The cut surface of the key switch hole on the top plate is tapered due to the characteristics of the laser cutter, so the size of the hole is slightly different on the front and back sides. Try mounting the key switch to be installed on the front and back sides of the top plate, and treat the side that is easier to mount as the front side.**

1. Install the key switches and key caps of your choice.  
* Only Cherry MX-compatible switches are supported on this version of the MiniAxe. The "MiniAxe LP" supports low-profile switches.  
* If the keyswitch is difficult to install on the top plate, try changing the front and back sides of the top plate. Also, inserting something between the top plate and the board to support the top plate so that it does not bend can prevent the top plate from cracking. Install the top plate carefully without forcing it into place.
* Ensure key switch pins are straight before inserting. **Remember that SW7 and SW8 are oriented opposite to the others.**  
2. Join the two halves with the male-male microUSB cable. Connect the microUSB port J2 on one side to J2 on the other side.

## Write firmware
__For the soldered kit, the default keymap firmware is already written.__

The firmware uses QMK. Please clone the following repository.

[qmk_firmware](https://github.com/qmk/qmk_firmware)

After cloning, move to the directory of the local repository and execute the following command. 

~~~
$ make miniaxe:default:dfu
~~~

After building, the program will enter a standby state. When that happens, please connect the keyboard. If the keyboard is already connected, writing will begin. 
It is not necessary to press the reset switch to write the firmware for the first time.
Repeat for the other side of the keyboard.

Please refer to [this document](https://docs.qmk.fm/#/getting_started_build_tools) for building the environment for building firmware.

## Completed!
Congratulations!

![Done](images/IMG_2819.jpg)

---
<a name="marker">1</a>: Some kits are colored with markers.  
<a name="screw">2</a>: In the Ten-key version M2 x 3 mm was included but it was changed to 4 mm.
<a name="metal_spacer">3</a>: Although the M2 metal standoff 3 mm was included in the Ten-key Vol.1 version, it was replaced by 3.5 mm.

