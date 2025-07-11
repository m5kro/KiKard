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
## 6/6/25
Spent today connecting up the ST25 to the NRF52 using SPI and making some other connections for the ST25. SPI was a bit confusing at first because the CS pin was labeled BSS, and I thought it was the CSO and CSI pins for a bit. Looking at diagrams online, most people are wiring up the ST25 with 5v on the VDD and VDDTX pins and 3.3v on the VDDIO pin, so I went with that (pulled 5v from usb and 3.3v from the NRF VDD output). The ST25 also needed a 27.12 MHz oscillator, so I used the XRCGB27M120F3M00R0 (terrible name). Finally, I decoupled everything on the ST25 (hopefully properly). <br>
<br>
The next update will probably be finishing up the wiring for the NRF52. After that I will work on figuring out the antenna setup. Also decided to ditch the battery.<br>
<br>
<img src="journal-images/6-6-25.png" height="200"><br>
Screenshot of the current ST25 schematic (if you see any problems please message me, thanks)<br>
<br>
**Time spent today: 3h**<br>
**Total time spent: 7h**
## 6/29/25
Got back from vacation. Spent today wiring up the NRF52. I got all the decoupling, fixed the symbol, added a BLE antenna, and added the two oscillators (32 Mhz & 32.768 KHz). Everything looks very sketchy so far and I have no idea if it will work at all.<br>
<br>
I will try to get the NFC antennas figured out for the next update and also add the buttons.<br>
<br>
<img src="journal-images/6-29-25.png" height="200"><br>
Screenshot of the almost completed NRF52 schematic (as usual please message me if you see any problems)<br>
<br>
**Time spent today: 5h**<br>
**Total time spent: 12h**
## 7/9/25
Spent today figuring out the NFC antenna. This took forever and really confused my brain, as I have no idea how RF works. After spending hours looking at documentation and performing calculations, I settled on a 25x25mm antenna with 7 turns, 0.4mm width traces, and 0.6mm spacing, to get around 1.37uH of inductance. 1.37uH is sort of a magic number because it simplifies all the tuning calculations for me. For the ST25 everything was already done for me since the flipper zero just so happens to use the same chip, and its antenna is also 1.37uH (thanks Flipper Zero team). The NRF52 was a bit harder since I needed to perform my own calculations, but thankfully, it came out to just around 200pF for each tuning capacitor.<br>
<br>
Next update I will get more of the schematic done and maybe figure out the mux (switching mechanism) for the antenna.<br>
<br>
<img src="journal-images/7-9-25.png" height="200"><br>
Screenshot of the NFC antenna footprint (created using: https://github.com/nideri/nfc_antenna_generator)<br>
<br>
**Time spent today: 5h**<br>
**Total time spent: 17h**
## 7/11/25
Finished up the NFC tuning for the ST25 today. I also sort of figured out a switching mechanism for the NRF52. It involves 2 mosfets to control when the NRF52 connects, and it attaches right onto the coil. It's an ugly solution and there's a good chance it doesn't work because the NRF52 can't quite be tuned in this setup. However, [some people online claim they have been able to get away with not tuning by using a MOLEX 1462360051 antenna](https://forum.seeedstudio.com/t/xiao-nrf52840-nfc-antenna-insights/277696), which happens to be 1.4uF (very close to my 1.37). I'll do more research later to see if this configuration actually works.<br>
<br>
Next update will (hopefully) be starting on the pcb layout.<br>
<br>
<img src="journal-images/7-11-25.png" height="200"><br>
Screenshot of the terrible antenna switching mechanism and the ST25 tuning<br>
<br>
**Time spent today: 4h**<br>
**Total time spent: 21h**