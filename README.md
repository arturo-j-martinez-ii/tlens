_**About This Project:**_

**AR Glasses** is a Quality of Life Plus Challenger Project developed by  Arturo Martinez, a UTSA Top Scholar Electrical Engineering freshman.

This project's ultimate goal is to develop an **open-source, universal transcription lens glasses attachment** that doesn't require Wi-Fi or a cellular device for a deaf and visually impaired veteran and, eventually, anyone to use anywhere in the world.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Materials Used:**_

_*In Progress*_

A Computer connected to Wi-Fi to install the Ubuntu Desktop OS

A Keyboard and Mouse to use the Raspberry Pi 5 [wired/wireless, can be the same ones you used with your computer] 

A Monitor [can be the same monitor you used with your computer (**a Raspberry Pi will not display to a laptop**), this is the one I used!]: https://a.co/d/aF4n6GT

HDMI to micro HDMI Cable [you need the microHDMI to connect to the Raspberry Pi! the HDMI can be changed for whatever your monitor inputs!]: https://www.amazon.com/s?k=hdmi+to+micro+hdmi

3D-Printed AR Glasses Attachment Onshape File: https://cad.onshape.com/documents/2b03bd95f3beaf6443ddc2ec/w/4e36cb5ff0dc8d07eeac17e6/e/a492bb96a45b8f75442e17c6?renderMode=0&uiState=681d2de2ce7941631ad96f14

Crystalfontz 128x56 Transparent OLED Display: https://www.crystalfontz.com/product/cfal12856a00151b-128x56-transparent-oled-screen

Crystalfontz 24 Position, 0.5mm Pitch, Gold, FCC FPC ZIF Connector: https://www.crystalfontz.com/product/cs050z24ga0-24-position-zif-connector

Wireless Lavalier Microphone [**ensure** it has USB connector so it can connect to Pi's USB ports]: https://www.amazon.com/s?k=wireless+lavalier+microphones

SD/microSD USB Adapter [purchase if your computer doesn't have a SD/microSD card reader]: https://www.amazon.com/s?k=microsd+card+adapter+for+pc

50000mAh Power Bank [you can use any, **ensure** it can output 5V and 3A+ (get as close to 5A as possible)]: https://www.amazon.com/s?k=50000mah+power+bank

Wires to connect OLED to Pi: _In Progress_

Custom PCB File Printed by PCBWay: _Future Goal_

Raspberry Pi 5 [8GB RAM] Starter Kit (128GB microSD card + case with cooling fan + power supply): https://a.co/d/87RnvB4

&#8593; **OR buy parts separately (only buy the starter kit OR individual components [the Pi 5, microSD card, and case with cooling fan])** &#8595;

Raspberry Pi 5 [8GB RAM or more]: https://a.co/d/8Ey5J5D

128GB [recommend using 32GB or larger] microSD Card: https://www.amazon.com/s?k=128gb+microsd+card 

Raspberry Pi 5 Case with Cooling Fan [feel free to use any case with a cooling fan! **ensure** you have room to route wires to OLED and PCB (or can make room)]: https://a.co/d/82YHFma

Raspberry Pi 5 Power Supply [not necessary, you can have the Pi running off the power bank alone]: https://a.co/d/awwQ0f8

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
15. Wait for the imager to write and verify Ubuntu on your microSD card
16. A pop-up saying "Ubuntu Desktop XX.XX (64-bit) has been written to SDXC Card [or if using adapter, 'Generic STORAGE DEVICE USB Device']" should appear
17. Press "Continue"
18. Close the Raspberry Pi Imager
19. You can now safely remove the microSD card from your computer [Ubuntu is now succesfully installed on your microSD card!]

_Next, we are going to set up our Raspberry Pi with our Ubuntu microSD card_

20. Install Raspberry Pi 5 into your specific case [installation will vary, however I will show how mine is set up]

20a.  Disassemble/open case to reveal the case's parts ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/1%20-%20Case%20Before%20Assembly.jpeg?raw=true)
20b. Insert your Raspberry Pi into the bottom of the case [make sure you can see through all 4 screw holes on the Pi's corners!] ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/2%20-%20Placing%20Raspberry%20Pi%20into%20Case%20Bottom.jpeg?raw=true)
20c. **[DO NOT FORCE THIS]** Connect the case's fan to the "FAN" header near the USB ports and close the white frame over the bottom of the case [the Pi should not move in the case after this step] ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/3%20-%20Showing%20How%20Fan%20and%20Pi%20Will%20Connect.jpeg?raw=true)
![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/4%20-%20Fan%20and%20Pi%20Connected.jpeg?raw=true)
![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/5%20-%20Fan%20and%20Bottom%20Closed%20Together.jpeg?raw=true)
20d. Flip the Pi over and insert the microSD card into the Raspberry Pi 5 ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/6%20-%20Where%20microSD%20Inserts.jpeg?raw=true) ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/7%20-%20microSD%20Inserted.jpeg?raw=true)

Keep the lid off as we will need to make some modifications to fit the wires through the case!

Now, you can flip it back over, and we can begin setting up Ubuntu on the Pi!

21. Connect the power, keyboard, mouse, and micro HDMI cables to the Pi
22. Connect the micro HDMI cable to your monitor

_I'm using Ubuntu Desktop 25.04 for this setup, so installation may vary! YouTube is a great resource if you're ever confused or lost!_

23. After this, the Pi should power on and show a black and orange Ubuntu startup screen! [the Pi's power LED will be flashing green until you reach desktop] ![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/8%20-%20Ubuntu%20Startup%20Screen.jpeg?raw=true)
24. A  "Welcome" screen should appear with language options
25. Choose the language you prefer the operating system to be in
26. Press "Next"
27. A "Typing" screen should appear with various options for layouts
28. Choose your preferred layout
29. Press "Next"
30. A "Network" screen should appear with various options to connect to the internet
31. Connect to your prefered Wi-Fi **OR** plug in Ethernet [you may need to give it a moment to bring up the Wi-Fi login screen]
32. Input your Wi-Fi password and press "Connect" [you may need to give it a few seconds to connect, wait for the grey "Skip" button to turn into an orange "Next" button]
33. Press "Next"
34. A "Time Zone" screen should appear with a map of the world on the bottom
35. Click on "Search Cities" and input your general area, so your Pi has the correct time [you can put whatever timezone you want, it won't affect the Pi's functionality]
36. An "About You" screen with "Full Name," "Username," and "Computer" fields should appear
37. Click on "Full Name" and enter in your full preferred name [it will auto fill the "Username" and "Computer" fields based on your full name, feel free to change any field to your heart's desire!]

37a. Click on "Username" and enter in your preferred account username [I would keep it simple, I chose "arglasses"]

37b. Click on "Computer" and enter in your preferred name for the Raspberry Pi

38. Press "Next"
39. A "Password" screen with "Password" and "Confirm Password" fields should appear
40. Enter in the same password for both fields [I recommend having a simple one as you will have to enter it multiple times when doing sudo commands]
41. Press "Next"
42. An "Almost done" screen will appear, allow Ubuntu to finalize setup and an orange button to appear
43. Press the orange button labeled "Start Using Ubuntu"
44. A "Welcom to Ubuntu XX.XX!" should appear
45. Press "Next"
46. A "Help improve Ubuntu" screen should appear
47. Press "No, don't share system data"
48. Press "Next"
49. A "Get started with more applications" screen should appear
50. Press "Finish"

You have successfully installed Ubuntu onto your Raspberry Pi!


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Future Goals:**_

_*In Progress*_

1. Improving CAD of glasses attachment, making it easy to assemble and repair
2. Designing a PCB to connect OLED to 24 Position ZIF Connector that takes 4 wires from Raspberry Pi 5 [since we're using I2C, we only need: 3.3v, GND, D0 (SCL), D1 (SDA)]
3. Designing an convex optical lens that will "move" the focal point of screen further away
4. Continuing to document and improve accessability of this project
