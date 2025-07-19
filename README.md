# KiKard
Pronounced key card. KiKard is a usb microcontroller board with NFC read, write, and tag support. Built for Hack Club Highway. Not affiliated with KiCad (but do check them out).

# Other Notes
Although the NRF has NFC support built in, it's only for tag mode, so a separate chip is needed for reading NFC.<br>
RGB LED 1 - Status led Green: just connected, Pink: reset/flashing, Blue: NRF52 tag mode, Yellow: ST25 read mode, Red: error<br>
RGB LED 2 - read/tag status Yellow: waiting, Blue: reading/emulating, Green: success, Red: error<br>
Button 1 - Read/emulate<br>
Button 2 - Switch between NRF52 and ST25<br>
Button 3 - Switch emulated tag (can save different cards on device)<br>

# Bom
| Item | Price |
| :-----: | :-----: |
| Custom PCB x5 | $4.00 |
| PCB Parts x5 | $44.43 |
| Extended Parts Fee | $81.00 |
| SMT Assembly | $2.90 |
| X-ray Inspection (required) | $7.85 |
| Nitrogen Reflow Soldering | $0.86 |
| Shipping | $9.04 |
| JLCPCB special discount | -$2.00 |
| SMT Coupon | -$12.00 |

**Total: $145.58**

# PCB Parts Bom (PER PCB)
Total PCB Parts: 71<br>
Total PCB Parts Price (per PCB): $8.7174
| Part | Designator | Quantity | Price per Unit | Total | JLCPCB/LCSC Part No. |
| :---------: | :-----: | :-----: | :-----: | :-----: | :-----: |
| [NRF-52840-QIAA-R](https://jlcpcb.com/partdetail/NordicSemicon-NRF52840_QIAAR/C190794) | U1 | 1 | $4.0290 | $4.0290 | C190794 |
| [ST25R3916-AQWT](https://jlcpcb.com/partdetail/STMicroelectronics-ST25R3916AQWT/C2908147) | U2 | 1 | $3.3795 | $3.3795 | C2908147 |
| [WNM3013-3/TR](https://jlcpcb.com/partdetail/WILLSEMI_Will_Semicon-WNM3013_3TR/C239659) | Q1, Q2 | 2 | $0.0333 | $0.0667 | C239659 |
| [32MHz Crystal Oscillator](https://jlcpcb.com/partdetail/2777870-X201632MOB4SI/C2682773) | Y2 | 1 | $0.0890 | $0.0890 | C2682773 |
| [27MHz Crystal Oscillator](https://jlcpcb.com/partdetail/604049-XRCGB27M120F3M00R0/C576558) | Y1 | 1 | $0.1773 | $0.1773 | C576558 |
| [32KHz Crystal Oscillator](https://jlcpcb.com/partdetail/357119-X161032768KGD2SI/C383847) | Y3 | 1 | $0.3825 | $0.3825 | C383847 |
| [USB-C Port](https://jlcpcb.com/partdetail/SHOUHAN-TYPEC16PIN/C393939) | USB1 | 1 | $0.0642 | $0.0642 | C393939 |
| [RGBLED](https://jlcpcb.com/partdetail/ChauLight-ZSRGB_2017H_08Z3/C7497245) | LED1, LED2 | 2 | $0.0807 | $0.1614 | C7497245 |
| [Button](https://jlcpcb.com/partdetail/Korean_HropartsElec-K2_6639SP_C4SC04/C83206) | SW1, SW2, SW3 | 3 | $0.0380 | $0.1140 | C83206 |
| [Small Button](https://jlcpcb.com/partdetail/hanxia-HX_3x4x2_2P_25N/C36498961) | SW4 | 1 | $0.0299 | $0.0299 | C36498961 |
| [100k Ohm Resistor](https://jlcpcb.com/partdetail/YAGEO-RC0603FR07100KL/C14675) | R3, R4 | 2 | $0.0010 | $0.0020 | C14675 |
| [10k Ohm Resistor](https://jlcpcb.com/partdetail/26274-0402WGJ0103TCE/C25531) | R5 | 1 | $0.0004 | $0.0004 | C25531 |
| [5.1k Ohm Resistor](https://jlcpcb.com/partdetail/26684-0402WGJ0512TCE/C25941) | R1, R2 | 2 | $0.0004 | $0.0008 | C25941 |
| [4.7uF Capacitor](https://jlcpcb.com/partdetail/20375-CL10A475KO8NNNC/C19666) | C1, C2, C3, C32 | 4 | $0.0101 | $0.0404 | C19666 |
| [2.2uF Capacitor](https://jlcpcb.com/partdetail/1959-CL10A225KP8NNNC/C1607) | C5, C7, C9, C13, C15, C17, C19 | 7 | $0.0060 | $0.0420 | C1607 |
| [1uF Capacitor](https://jlcpcb.com/partdetail/15107-CL05A105KP5NNNC/C14445) | C11, C27 | 2 | $0.0016 | $0.0032 | C14445 |
| [100nF Capacitor](https://jlcpcb.com/partdetail/57421-0402B104K250NT/C56392) | C28, C29, C30, C31, C34, C47 | 6 |  $0.0011 |  $0.0066 | C56392 |
| [47nF Capacitor](https://jlcpcb.com/partdetail/83376-0402B473K500NT/C82219) | C26 | 1 | $0.0017 | $0.0017 | C82219 |
| [10nF Capacitor](https://jlcpcb.com/partdetail/1876-0402B103K500NT/C1524) | C4, C6, C8, C10, C12, C14, C16, C18 | 8 | $0.0010 | $0.0080 | C1524 |
| [1nF Capacitor](https://jlcpcb.com/partdetail/TDK-C1005C0G1E102JT000F/C343059) | C45, C46 | 2 | $0.0089 | $0.0178 | C343059 |
| [680pF Capacitor](https://jlcpcb.com/partdetail/1893-0402B681K500NT/C1541) | C38, C40 | 2 | $0.0011 | $0.0022 | C1541 |
| [100pF Capacitor](https://jlcpcb.com/partdetail/1898-0402CG101J500NT/C1546) | C35, C37, C41, C44 | 4 | $0.0089 | $0.0356 | C1546 |
| [62pF Capacitor](https://jlcpcb.com/partdetail/YAGEO-CC0402JRNPO9BN620/C281763) | C39, C42 | 2 | $0.0014 | $0.0028 | C281763 |
| [12pF Capacitor](https://jlcpcb.com/partdetail/1899-0402CG120J500NT/C1547) | C22, C23 | 2 | $0.0010 | $0.0020 | C1547 |
| [10pF Capacitor](https://jlcpcb.com/partdetail/1897-0402CG100J500NT/C1545) | C36, C43 | 2 | $0.0010 | $0.0020 | C1545 |
| [6pF Capacitor](https://jlcpcb.com/partdetail/1927-0402CG6R0C500NT/C1575) | C20, C21, C24, C25 | 4 | $0.0010 | $0.0040 | C1575 |
| [0.8pF Capacitor](https://jlcpcb.com/partdetail/41442-0402CG0R8C500NT/C40459) | C33 | 1 | $0.0013 | $0.0013 | C40459 |
| [10uH Inductor](https://jlcpcb.com/partdetail/Sunlord-MCL1608S100MT/C51942) | L1 | 1 | $0.0212 | $0.0212 | C51942 |
| [270nH Inductor](https://jlcpcb.com/partdetail/TDK-MLG1005SR27JT000/C76784) | L4, L5 | 2 | $0.0077 | $0.0154 | C76784 |
| [15nH Inductor](https://jlcpcb.com/partdetail/Sunlord-SDCL1608C15NJTDF/C23651) | L2 | 1 | $0.0106 | $0.0106 | C23651 |
| [3.9nH Inductor](https://jlcpcb.com/partdetail/Sunlord-SDCL1005C3N9STDF/C14033) | L3 | 1 | $0.0039 | $0.0039 | C14033 |

# Credit
[NRF-52840-QIAA-R schematic and footprint was aquired from snapeda](https://www.snapeda.com/parts/NRF52840-QIAA-R/Nordic%20Power/view-part/)<br>
[ST25R3916-AQWT schematic and footprint was aquired from snapeda](https://www.snapeda.com/parts/ST25R3916-AQWT/STMicroelectronics/view-part/)<br>
[NFC antenna footprint created using nfc antenna generator by nideri](https://github.com/nideri/nfc_antenna_generator)