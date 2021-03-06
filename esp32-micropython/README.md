# MicroPython - ESP32 with ROBOTboard

<hr />
https://www.instagram.com/p/Boo4LTRALBZ/?taken-by=octopusengine
<br />
https://boneskull.com/micropython-on-esp32-part-1/<br />
<br />

## PINout:
<pre>
oeLAB-esp32 (DoIt) 2x15 pins:                               [ROBOT Board]:
                          -----------     (GPIO)
                      EN -           - D23 (23)  MOSI       [SPI_MOSI_PIN] 
[PIN_ANALOG]    (36)  VP -           - D22 (22)  SCL(I2C)   [I2C_SCL_PIN]
[I39_PIN]       (39)  VN -           - TXD (1)   D2
[I34_PIN]            D34 -           - RXD (3)   D3
[I35_PIN]            D35 -           - D21 (21)  SDA(I2C)   [I2C_SDA_PIN]
[ONE_WIRE_PIN] DEV1  D32 -           - D19 (19)  MISO       [SPI_MISO_PIN]
               DEV2  D33 -  (ESP32)  - D18 (18)  SCLK       [SPI_CLK_PIN]
[MOTOR_12EN]         D25 -           - D5  (5)   CS0        [SPI_CS0_PIN]
[MOTOR_1A]           D26 -           - TX2 (17)             [PIN_PWM1] /Servo1
[MOTOR_4A]           D27 -           - RX2 (16)             [PIN_PWM2] /Servo2
[MOTOR_3A]           D14 -           - D4  (4)              [PIN_PWM3] /Servo3
[MOTOR_2A]           D12 -           - D2  (2)              [BUILT_IN_LED]
[MOTOR_34EN]         D13 -           - D15 (15)             [WS_LED_PIN] //v1(13)     
                     GND -           - GND
                     VIN -           - 3V3 +
                          -----------
</pre>     





## Windows:
- install Python3 <br />
- download MicroPython [1] https://micropython.org/download#esp32<br />
- install esptool.py [2] https://github.com/espressif/esptool<br />
- install ampy [3] https://github.com/adafruit/ampy <pre>
set AMPY_PORT=COM6<br />
ampy ls<br />
AMPY_BAUD=115200<br />
</pre><br />
- connect ESP32 and detect COM port<br /> 
- erase FLASH: <pre>esptool.py --chip esp32 -p /COM6 erase_flash</pre><br /> 
- upload Micropython bin: <pre>esptool.py --chip esp32 -p /COM6 write_flash -z 0x1000 ./down/esp32-20180821-v1.9.4-479-g828f771e3.bin</pre>
<br />
- copy *.py file to ESP <pre>
ampy -p /COM6 get boot.py
# This file is executed on every boot (including wake-boot from deepsleep)
</pre>

<hr />

categories:<br />
01 - basic test<br />
02 - simple experiment<br />
03 - i/o test - sensor<br />
04 - special sensors<br />
05 - spi/i2c devices<br />
06 - basic motor test<br />
07 - mechatronics<br />
08 - wifi/bf/ir - remote (setup or control)<br />
09 - complex simple projects examples<br />








