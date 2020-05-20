# Argon-ONE-i2c-Codes
This is a list of i2c Codes utilized by Argon ONE Raspberry Pi Cases

Device Address：0x34


Write Command
Only one byte(0~255) can be used


1.  HEX CODE: 0x01 to 0x64 (0~100)
ACTION: Sets the Fan's Duty Cycle from 0%~100%.

1.1 HEX CODE: 0x00
ACTION: Turns OFF the FAN.


2.  HEX CODE: 0xfd
Set the ARGON ONE to Mode 1：
ACTION: Sets "Default Mode"
Behaviour: You need to PRESS button to Power ON from shutdown or power outage.


3.  HEX CODE: 0xfe
Set the ARGON ONE to mode 2：
ACTION: Sets "Always ON Mode"
Behaviour: Power current will flow directly to Raspberry Pi. NO need to PRESS button to power ON from shutdown or power outage.


4.  HEX CODE: 0xff
ACTION: Listens at Serial Port to cut power; Requires Serial Port to be ENABLED.
Behaviour: When ARGON ONE receives 0xff，then ARGON ONE will check UART's voltage.
Then, it will cut the power when UART's voltage is low.

