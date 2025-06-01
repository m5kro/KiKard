# KiKard
A usb microcontroller board with NFC support. Built for Hack Club Highway.

# BOM
NRF-52840-QIAA-R Microcontroller (has BLE and also sips power)
Custom PCB with dual NFC Antenna built in (or just HF) + BLE antenna
PN532 OR PN533 (still deciding)
CR2032 Button battery (3.3V)
2 RGB LEDs
On/Off switch
3 buttons
USB-C port

# Other Notes
Although the NRF has NFC support built in, it's only for tag mode, so a separate chip is needed for reading NFC.
The button battery might be replaced with a small rechargeable lipo

# Journal
This section is used to keep track of what I've done over time. (Also needed for Hack Club Grant)
## 6/1/25 <br>
Came up with the initial idea and some basic plans. I did research on the NRF-52 series and found out that it alone wasn't sufficient for what I wanted to build, so I needed a separate chip. After searching online, I found that the PN532 was a popular choice since it was cheap and widely available, but the PN533 might have more features. <br>
<br>
Since I settled on using the NRF-52840-QIAA-R as the main microcontroller I created a new KiCad project and imported the schematic and footprint.<br>
**Total time spent: 2h**
