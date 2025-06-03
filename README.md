# KiKard
A usb microcontroller board with NFC read, write, and tag support. Built for Hack Club Highway.

# BOM
1. NRF-52840-QIAA-R Microcontroller (has BLE and also sips power)
2. Custom PCB with dual NFC Antenna built in (or just HF) + BLE antenna
3. ST25R3916-AQWT
4. CR2032 Button battery (3.3V)
5. 2 RGB LEDs
6. On/Off switch
7. 3 buttons
8. USB-C port

# Other Notes
Although the NRF has NFC support built in, it's only for tag mode, so a separate chip is needed for reading NFC.<br>
The button battery might be replaced with a small rechargeable lipo

# Credit
[NRF-52840-QIAA-R schematic and footprint was aquired from snapeda](https://www.snapeda.com/parts/NRF52840-QIAA-R/Nordic%20Power/view-part/)<br>
[ST25R3916-AQWT schematic and footprint was aquired from snapeda](https://www.snapeda.com/parts/ST25R3916-AQWT/STMicroelectronics/view-part/)