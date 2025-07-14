# KiKard
A usb microcontroller board with NFC read, write, and tag support. Built for Hack Club Highway. Not affiliated with KiCad (but do check them out).

# Other Notes
Although the NRF has NFC support built in, it's only for tag mode, so a separate chip is needed for reading NFC.<br>
RGB LED 1 - Status led Green: just connected, Pink: reset/flashing, Blue: NRF52 tag mode, Yellow: ST25 read mode, Red: error<br>
RGB LED 2 - read/tag status Yellow: waiting, Blue: reading/emulating, Green: success, Red: error<br>
Button 1 - Read/emulate<br>
Button 2 - Switch between NRF52 and ST25<br>
Button 3 - Switch emulated tag (can save different cards on device)<br>

# Credit
[NRF-52840-QIAA-R schematic and footprint was aquired from snapeda](https://www.snapeda.com/parts/NRF52840-QIAA-R/Nordic%20Power/view-part/)<br>
[ST25R3916-AQWT schematic and footprint was aquired from snapeda](https://www.snapeda.com/parts/ST25R3916-AQWT/STMicroelectronics/view-part/)<br>
[NFC antenna footprint created using nfc antenna generator by nideri](https://github.com/nideri/nfc_antenna_generator)