---
title: "KiKard"
author: "m5kro"
description: "A usb microcontroller board with NFC read, write, and tag support."
created_at: "2025-06-1"
---
## 6/1/25 
Came up with the initial idea and some basic plans. I did research on the NRF-52 series and found out that it alone wasn't sufficient for what I wanted to build, so I needed a separate chip. After searching online, I found that the PN532 was a popular choice since it was cheap and widely available, but the PN533 might have more features. <br>
<br>
Since I settled on using the NRF-52840-QIAA-R as the main microcontroller I created a new KiCad project and imported the schematic and footprint.<br>
<br>
<img src="journal-images/6-2-25.png" height="200"><br>
Screenshot of KiCad NRF-52840-QIAA-R schematic
<br>
<br>
**Time spent today: 2h**<br>
**Total time spent: 2h**
## 6/4/25
After further research and looking at what JLCPCB has, the ST25R3916-AQWT may be a better pick for the reader chip. It's cheaper than the PN532, a bit newer, and can do a bit more too. Although it is capable of tag emulation, it doesn't seem as capable as the NRF52, so a dual chip setup is still needed. <br>
<br>
A future problem I will need to deal with is the antenna setup. I will need a way to connect both chips to the antennas using a switching method so there isn't any interference.<br>
<br>
In KiCad, I imported the ST25R3916-AQWT symbol and schematic and connected up the NRF52 to a USB-C port.<br>
<br>
<img src="journal-images/6-4-25.png" height="200"><br>
Screenshot of current KiCad progress<br>
<br>
**Time spent today: 2h**<br>
**Total time spent: 4h**