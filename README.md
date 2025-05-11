_**About This Project:**_

**AR Glasses** is a Quality of Life Plus Challenger Project developed by  Arturo Martinez, a UTSA Top Scholar Electrical Engineering freshman.

This project's ultimate goal is to develop an **open-source, universal transcription lens glasses attachment** that doesn't require Wi-Fi or a cellular device for a deaf and visually impaired veteran and anyone to use.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Materials Used:**_

_*In Progress*_

Seperate Computer [with Wi-Fi], Keyboard, and Mouse to install the Ubuntu OS

3D-Printed AR Glasses Attachment Onshape File: https://cad.onshape.com/documents/2b03bd95f3beaf6443ddc2ec/w/4e36cb5ff0dc8d07eeac17e6/e/a492bb96a45b8f75442e17c6?renderMode=0&uiState=681d2de2ce7941631ad96f14

Crystalfontz 128x56 Transparent OLED Display: https://www.crystalfontz.com/product/cfal12856a00151b-128x56-transparent-oled-screen

Crystalfontz 24 Position, 0.5mm Pitch, Gold, FCC FPC ZIF Connector: https://www.crystalfontz.com/product/cs050z24ga0-24-position-zif-connector

Wireless Lavalier Microphone [ensure it has USB connector so it can connect to Pi's USB ports]: https://www.amazon.com/s?k=wireless+lavalier+microphones

SD/microSD USB Adapter [purchase if your computer doesn't have an SD/microSD card reader]: https://www.amazon.com/s?k=microsd+card+adapter+for+pc

50000mAh Power Bank [ensure it can output 5V and 3+A (get as close to 5A as possible)]: https://www.amazon.com/s?k=50000mah+power+bank

Wires to connect OLED to Pi: _In Progress_

Custom PCB File Printed by PCBWay: _Future Goal_

Raspberry Pi 5 [8GB RAM] Starter Kit (128GB microSD card + case with cooling fan): https://a.co/d/87RnvB4

&#8593; **OR buy parts separately (only buy the starter kit or individual components [the Pi 5, microSD card, and case with cooling fan])** &#8595;

Raspberry Pi 5 [8GB RAM or more]: https://a.co/d/8Ey5J5D

128GB [or bigger] microSD Card: https://www.amazon.com/s?k=128gb+microsd+card 

Rasberry Pi 5 Case with Cooling Fan [feel free to use any case with a cooling fan, will need room to route wires to OLED and PCB]: https://a.co/d/82YHFma

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Setting Up:**_

_*In Progress*_

1. Go to https://www.raspberrypi.com/software/
2. Install the latest version of Raspberry Pi Imager for your operating system on to your computer
3. Plug in microSD card into your PC [either with the USB adapter or port on your computer]
4. Open Raspberry Pi Imager
5. Press "CHOOSE DEVICE"
6. Select "Raspberry Pi 5"
7. Press "CHOOSE OS"
8. Select "Other general-purpose OS"
9. Select "Ubuntu"
10. Select "Ubuntu Desktop XX.XX (64-bit)" [should be the first option, X's are placeholders for the latest version]
11. Press "CHOOSE STORAGE"
12. Select your microSD card [typically labeled "SDXC CARD" if using adapter, it's typically labeled under "Generic STORAGE DEVICE USB Device"]
13. Press "NEXT"

**MAKE SURE NOTHING IMPORTANT IS ON YOUR microSD CARD!!! You will not be able to recover any data after pressing "YES"**

14. Press "YES"
15. Wait for the imager to write to the microSD card and for the pop-up saying "Ubuntu Desktop XX.XX (64-bit) has been written to SDXC Card [or if using adapter, 'Generic STORAGE DEVICE USB Device']"
16. Press "Continue"
17. Close the Raspberry Pi Imager
18. You can now safely remove the microSD card from your computer [Ubuntu is now succesfully installed on your microSD card!]
19. 

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Future Goals:**_

_*In Progress*_

1. Improving CAD of glasses attachment, making it easy to assemble and repair
2. Designing a PCB to connect OLED to 24 Position ZIF Connector that takes 4 wires from Raspberry Pi 5 [since we're using I2C, we only need: 3.3v, GND, D0 (SCL), D1 (SDA)]
3. Designing an convex optical lens that will "move" the focal point of screen further away
4. Continuing to document and improve accessability of this project
