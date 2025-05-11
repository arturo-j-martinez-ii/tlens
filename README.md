_**About This Project:**_

**AR Glasses** is a Quality of Life Plus Challenger Project developed by  Arturo Martinez, a UTSA Top Scholar Electrical Engineering freshman.

This project's ultimate goal is to develop an **open-source, universal transcription lens glasses attachment** that doesn't require Wi-Fi or a cellular device for a deaf and visually impaired veteran and, eventually, anyone to use.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Materials Used:**_

_*In Progress*_

A Computer connected Wi-Fi to install the Ubuntu OS

A Keyboard and Mouse to use the Raspberry Pi 5 [wired/wireless, can be the same ones you used with your computer] 

A monitor [the Raspberry Pi will not display to your laptop, can be same you used with your computer, this is the one I used!]: https://a.co/d/aF4n6GT

HDMI to microHDMI Cable [you need the microHDMI part to connect from Raspberry Pi! the HDMI can be changed for whatever your monitor inputs!]: https://www.amazon.com/s?k=hdmi+to+micro+hdmi

3D-Printed AR Glasses Attachment Onshape File: https://cad.onshape.com/documents/2b03bd95f3beaf6443ddc2ec/w/4e36cb5ff0dc8d07eeac17e6/e/a492bb96a45b8f75442e17c6?renderMode=0&uiState=681d2de2ce7941631ad96f14

Crystalfontz 128x56 Transparent OLED Display: https://www.crystalfontz.com/product/cfal12856a00151b-128x56-transparent-oled-screen

Crystalfontz 24 Position, 0.5mm Pitch, Gold, FCC FPC ZIF Connector: https://www.crystalfontz.com/product/cs050z24ga0-24-position-zif-connector

Wireless Lavalier Microphone [ensure it has USB connector so it can connect to Pi's USB ports]: https://www.amazon.com/s?k=wireless+lavalier+microphones

SD/microSD USB Adapter [purchase if your computer doesn't have an SD/microSD card reader]: https://www.amazon.com/s?k=microsd+card+adapter+for+pc

50000mAh Power Bank [you can use any, ensure it can output 5V and 3A+ (get as close to 5A as possible)]: https://www.amazon.com/s?k=50000mah+power+bank

Wires to connect OLED to Pi: _In Progress_

Custom PCB File Printed by PCBWay: _Future Goal_

Raspberry Pi 5 [8GB RAM] Starter Kit (128GB microSD card + case with cooling fan + power supply): https://a.co/d/87RnvB4

&#8593; **OR buy parts separately (only buy the starter kit or individual components [the Pi 5, microSD card, and case with cooling fan])** &#8595;

Raspberry Pi 5 [8GB RAM or more]: https://a.co/d/8Ey5J5D

128GB [recommend using 32GB or bigger] microSD Card: https://www.amazon.com/s?k=128gb+microsd+card 

Rasberry Pi 5 Case with Cooling Fan [feel free to use any case with a cooling fan, will need room to route wires to OLED and PCB]: https://a.co/d/82YHFma

Rasberyy Pi 5 Power Supply [not necessary, you can have the Pi running off the power bank alone]: https://a.co/d/awwQ0f8

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Setting Up:**_

_*In Progress*_

_First, we will install Ubuntu on our microSD card_

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

_Next, we are going to set up our Raspberry Pi with our Ubuntu microSD card_

19. Install Raspberry Pi 5 into your specific case [installation will vary, however I will show how mine is set up]

19a.  Disassemble/open case to reveal parts ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/1%20-%20Case%20Before%20Assembly.jpeg?raw=true)
19b. Insert Raspberry Pi into bottom of case [make sure you can see through all 4 screw holes on Pi's corners!] ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/2%20-%20Placing%20Raspberry%20Pi%20into%20Case%20Bottom.jpeg?raw=true)
19c. Connect the case fan to the "FAN" header near USB ports and close white frame over bottom of case [do not force this! the Pi should not move in the case after this step] ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/3%20-%20Showing%20How%20Fan%20and%20Pi%20Will%20Connect.jpeg?raw=true)
![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/4%20-%20Fan%20and%20Pi%20Connected.jpeg?raw=true)
![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/5%20-%20Fan%20and%20Bottom%20Closed%20Together.jpeg?raw=true)
19d. Flip the Pi and insert the microSD card into the Raspberry Pi 5 ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/6%20-%20Where%20microSD%20Inserts.jpeg?raw=true) ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/7%20-%20microSD%20Inserted.jpeg?raw=true)

Keep the lid off as we'll need to make some modifications to fit the wire through and can test if the OLED functions properly!

Now you can flip it back over, and we can begin setting up Ubuntu on the Pi!


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Future Goals:**_

_*In Progress*_

1. Improving CAD of glasses attachment, making it easy to assemble and repair
2. Designing a PCB to connect OLED to 24 Position ZIF Connector that takes 4 wires from Raspberry Pi 5 [since we're using I2C, we only need: 3.3v, GND, D0 (SCL), D1 (SDA)]
3. Designing an convex optical lens that will "move" the focal point of screen further away
4. Continuing to document and improve accessability of this project
