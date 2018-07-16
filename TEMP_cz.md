# octopuslab
devBoards for:
- ESP8266/32 - NodeMcu (LoLin) and octopus ESP-interface-board 
- Raspberry Pi 2/3/ZERO
- Attiny 85/45
- Arduino
- ....
<br />
<hr />
<b>Boards</b>
General Shield RPi - gsR<br />
General Shield ESP - gsE1 (ESP8266) gsE2 (ESP32) <br />
Dev board basic<br />
I2C board<br />
Power board<br />
#tickernator (basic SPI &I2C)<br />
Big displya<br />
Mechatronic1 - I2C 8bit-expander & darlington bus ULN<br />
<br />

<hr />

oeLAB - esp8266 pins:<br />
<pre>
     -----------   (GPIO)
 A0 -           - D0(16)     PIEZZO 1k 
  G -           - D1(05)   > I2C-CLK
 VU -           - D2(04)  <> I2C-DATA
 S3 -           - D3(00)   < FLASH/BTN
 S2 -  NodeMcu  - D4(02)  <> DIN-ONEWIRE/LED
 S1 -           - 3V         +
 SC -  (Lolin)  - G          x/GND
 S0 -           - D5(14)   > SPI-CLK
 SK -           - D6(12)     CS2/PIEZZO2  
  G -           - D7(13)  <> SPI-DATA
 3V -           - D8(15)   > SPI-CS1
 EN -           - RX(03)   > RX
RST -           - TX(01)   < TX
  G -           - G          GND
VIN -           - 3V         +
     -----------
</pre>