# YF-020H dev board
Everything I could gather about the YF-020H development board

![alt banner](figures/YF-020H_dev_board.jpg)

This is a rockchip RK3288 develipement board I found in a touchscreen table who was given to me by a friend. 
It is currently running on android 6.0 lollipop

# Technical information about the board
I contacted Maria (maria@cndlcd.com) from CND Electronic Technology (Shenzhen) Co. Ltd. who confirmed me that the board is no more in production but she gave me the some information about the board

Main Hardware Specification
- CPU: RK3288 ,quad-core Cortex-A17+GPU Mail-T764, Up to 1.8G
- RAM: 2G DDR3(up to 4G)
- ROM: EMMC8G/16G/32G(Optional) Standard 16G
- Resolution: 1080P/H.265(4K2K)
- OS: Android 6.0.1 7.0 8.0 Linux
- Display mode: Loop Display, Timing display, Inserting playing etc.
- Network: Gigabit Ethernet, Wifi, Bluetooth 4.1, wireless expending
- USB2.0: 6 USB interface
- Audio Output: 5W (8ohm)Double Sound channel
- Video Output: LVDS EDP Up to 1920*1200
- HDMI: 1 x HDMI 2.0
- RTC: Support
- Watch-dog: Support
- Timing on/off: Support
- OS Updating: SD card and PC
- Others: SD/USB input resolution and starting logo

<p align="center">
  <img src="figures/YF-020H_board_front_side.png" width="1200px" />
</div>
<p align="center">Front side of the board</p>

Built-in power control interface:
- Pin 1: STANDBY
- Pin 2: STANDBY-5V (Power supply)
- Pin 3: GND 
- Pin 4: GND
- Pin 5: VCC 12V in
- Pin 6: VCC 12V in

RTC interface:
- Pin 1: RTC (3V)
- Pin 2: GND

IR receiver interface:
- Pin 1: VCC
- Pin 2: GND
- Pin 3: IR

On/Off indicator light interface
- Pin 1: Red LED
- Pin 2: GND
- Pin 3: Green LED

I2C TP interface:
- Pin 1: VCC
- Pin 2: INT (input/output)
- Pin 3: RST (input/output)
- Pin 4: SDA (data)
- Pin 5: SCL (clock)
- Pin 6: GND

Serial interfaces (UART):
- Pin 1: VCC (3.3V)
- Pin 2: TX
- Pin 3: RX
- Pin 4: GND

Loudpeaker interface:
- Pin 1: R+
- Pin 2: R-
- Pin 3: L-
- Pin 4: L+

MIC interface
- Pin 1: Mic -
- Pin 2: Mic +

Backlight control interface:
- Pin 1: GND
- Pin 2: GND
- Pin 3: Backlight brightness control
- Pin 4: Backlight enable control
- Pin 5: VCC 12V Out
- Pin 6: VCC 12V Out

I/0 control interface (First six pin connector under wifi antenna connector)
- Pin 1: GND
- Pin 2: ADKEY
- Pin 3: GPIO-3
- Pin 4: GPIO-1
- Pin 5: GPIO-0
- Pin 6: VCC 3.3V output

LVDS interface:
| Pin Number | Function | Attributes | Description                              |
|------------|----------|------------|------------------------------------------|
| 1-2-3         | PVCC     | power output | LCD power output, +3.3V/+5V/+12V optional, selected through CN5 |
| 4-5-6          | GND      | ground     | Ground                                   |
| 7          | RXO0-    | output     | Pixel0 Negative Data (Odd)               |
| 8          | RX00+    | output     | Pixel0 Positive Data (Odd)               |
| 9          | RX01-    | output     | Pixel1 Negative Data (Odd)               |
| 10         | RX01+    | output     | Pixel1 Positive Data (Odd)               |
| 11         | RXO2-    | output     | Pixel2 Negative Data (Odd)               |
| 12         | RXO2+    | output     | Pixel2 Positive Data (Odd)               |
| 13         | GND      | ground     | Ground                                   |
| 14         | GND      | ground     | Ground                                   |
| 15         | RXOC-    | output     | Negative Sampling Clock (Odd)            |
| 16         | RXOC+    | output     | Positive Sampling Clock (Odd)            |
| 17         | RX03-    | output     | Pixel3 Negative Data (Odd)               |
| 18         | RXO3+    | output     | Pixel3 Positive Data (Odd)               |
| 19         | RXEO-    | output     | Pixel0 Negative Data (Even)              |
| 20         | RXEO+    | output     | Pixel0 Positive Data (Even)              |
| 21         | RXE1-    | output     | Pixel1 Negative Data (Even)              |
| 22         | RXE1+    | output     | Pixel1 Positive Data (Even)              |
| 23         | RXE2-    | output     | Pixel2 Negative Data (Even)              |
| 24         | RXE2+    | output     | Pixel2 Positive Data (Even)              |
| 25         | GND      | ground     | Ground                                   |
| 26         | GND      | ground     | Ground                                   |
| 27         | RXEC-    | output     | Negative Sampling Clock (Even)           |
| 28         | RXEC+    | output     | Positive Sampling Clock (Even)           |
| 29         | RXE3-    | output     | Pixel3 Negative Data (Even)              |
| 30         | RXE3+    | output     | Pixel3 Positive Data (Even)              |
| 31         | RX04-    | output     | Pixel4 Negative Data (Odd)               |
| 32         | RXO4+    | output     | Pixel4 Positive Data (Odd)               |
| 33         | RXE4-    | output     | Pixel4 Negative Data (Even)              |
| 34         | RXE4+    | output     | Pixel4 Positive Data (Even)              |


<p align="center">
  <img src="figures/YF-020H_pcb_dimensions.png" width="1200px" />
</div>
<p align="center">PCB Size and Port Layout. Square pads normally represent Pin 1</p>

## Board enclosure designs

<a href="enclosure/Top_part.STL" download>Top plate</a><br>
<a href="enclosure/Bottom_part.STL" download>Bottom plate</a>

Laser cut:
The images have been generated from STL models to be used for laser cut and engraving
The color code is adapted for [TROTEC](https://www.troteclaser.com/en-us/) JobControl software. Red color cuts and black engraves

3D print:
The STL files allow to print the two plates that go over and under the board.

For both Laser cut and 3D pritned plates screws and risers are necessary. The models have been designed to fit a 40mm fan for board cooling and a 12mm power pushbutton

The models are free to use and licensed under CC BY-NC-SA 4.0. To view a copy of this license, [visit creativecommons.org/licenses/by-nc-sa/4.0/](http://creativecommons.org/licenses/by-nc-sa/4.0/)
