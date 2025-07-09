# KiKard
A usb microcontroller board with NFC read, write, and tag support. Built for Hack Club Highway.

# BOM
1. NRF-52840-QIAA-R Microcontroller (has BLE and also sips power)
2. Custom PCB with dual NFC Antenna built in (or just HF) + BLE antenna
3. ST25R3916-AQWT
4. 2 RGB LEDs
5. On/Off switch
6. 3 buttons
7. USB-C port
8. A whole bunch of capacitors (will add full list later)
9. oscillators (will add full list later)

# Other Notes
Although the NRF has NFC support built in, it's only for tag mode, so a separate chip is needed for reading NFC.

# Credit
[NRF-52840-QIAA-R schematic and footprint was aquired from snapeda](https://www.snapeda.com/parts/NRF52840-QIAA-R/Nordic%20Power/view-part/)<br>
[ST25R3916-AQWT schematic and footprint was aquired from snapeda](https://www.snapeda.com/parts/ST25R3916-AQWT/STMicroelectronics/view-part/)<br>
[NFC antenna footprint created using nfc antenna generator by nideri](https://github.com/nideri/nfc_antenna_generator)