_**About This Project:**_

**TLens** is a QL Plus Challenger Project developed by  Arturo Martinez, a UTSA Top Scholar Electrical Engineering sophomore.

This project's ultimate goal is to develop an **open-source transcription device** that doesn't require Wi-Fi or a cellular device for a deaf and visually impaired veteran and, eventually, anyone to use anywhere in the world.

Here's a demonstration of TLens! https://youtu.be/GYs88_FpokA

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Materials Used:**_

Epson Moverio BT-35e Smart Glasses [recommend looking on Ebay for a pair]: https://epson.com/For-Work/Wearables/Smart-Glasses/Moverio-BT-35E-Smart-Glasses/p/V11H935020

A Computer connected to Wi-Fi to install the Ubuntu Desktop OS

A Keyboard and Mouse to use the Raspberry Pi 5 [wired/wireless, can be the same ones you used with your computer] 

A Monitor [can be the same monitor you used with your computer (**a Raspberry Pi will not display to a laptop**), this is the one I used!]: https://a.co/d/aF4n6GT

HDMI to micro HDMI Cable [you need the microHDMI to connect to the Raspberry Pi! the HDMI can be changed for whatever your monitor inputs!]: https://www.amazon.com/s?k=hdmi+to+micro+hdmi

Wireless Lavalier Microphone [**ensure** it has USB connector so it can connect to Pi's USB ports]: https://www.amazon.com/s?k=wireless+lavalier+microphones

50000mAh Power Bank [you can use any, **ensure** it can output 5V and 3A+ (get as close to 5A as possible)]: https://www.amazon.com/s?k=50000mah+power+bank

Raspberry Pi 5 [8GB RAM] Starter Kit (128GB microSD card + case with cooling fan + power supply): https://a.co/d/87RnvB4

&#8593; **OR buy parts separately (only buy the starter kit OR individual components [the Pi 5, microSD card, and case with cooling fan])** &#8595;

Raspberry Pi 5 [8GB RAM or more]: https://a.co/d/8Ey5J5D

128GB [recommend using 32GB or larger] microSD Card: https://www.amazon.com/s?k=128gb+microsd+card 

Raspberry Pi 5 Case with Cooling Fan [feel free to use any case with a cooling fan! **ensure** you have room to route wires to OLED and PCB (or can make room)]: https://a.co/d/82YHFma

SD/microSD USB Adapter [purchase if your computer doesn't have a SD/microSD card reader]: https://www.amazon.com/s?k=microsd+card+adapter+for+pc

Raspberry Pi 5 Power Supply [not necessary, you can have the Pi running off the power bank alone]: https://a.co/d/awwQ0f8

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Setting Up:**_

_*In Progress*_

_First, we will install Ubuntu on our microSD card [you can skip to step 60 if your Pi is set up with Ubuntu and has a case!]_

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
35. Click on "Search Cities" and input your general area, so your Pi has the correct time [please put your timezone to prevent errors!]
36. An "About You" screen with "Full Name," "Username," and "Computer" fields should appear
37. Click on "Full Name" and enter in your full preferred name [it will auto fill the "Username" and "Computer" fields based on your full name, feel free to change any field to your heart's desire!]

37a. Click on "Username" and enter in your preferred account username [I would keep it simple, I chose "tlens"]

37b. Click on "Computer" and enter in your preferred name for the Raspberry Pi

38. Press "Next"
39. A "Password" screen with "Password" and "Confirm Password" fields should appear
40. Enter in the same password for both fields [I recommend having a simple one as you will have to enter it multiple times when doing sudo commands]
41. Press "Next"
42. An "Almost done" screen will appear, allow Ubuntu to finalize setup and an orange button to appear
43. Press the orange button labeled "Start Using Ubuntu"
44. A "Welcome to Ubuntu XX.XX!" screen should appear
45. Press "Next"
46. A "Help improve Ubuntu" screen should appear
47. Press "No, don't share system data"
48. Press "Next"
49. A "Get started with more applications" screen should appear
50. Press "Finish"

_You have successfully setup Ubuntu to run on your Raspberry Pi! You're doing great!_ :goat:

_Now we will begin installing all the libraries we need to use the transcription program_

_To prevent errors when installing, we will make sure our Pi is in the correct timezone [mine wasn't and caused errors with the next steps]_

51. Press on the top right corner of the Desktop where Wi-Fi, Sound, and Power icons are

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/9%20-%20Pressing%20Top%20Right%20Desktop.jpeg?raw=true)

53. Press on the gear icon in the new popup menu to access the Pi's settings menu

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/10%20-%20Pressing%20Settings.jpeg?raw=true)

54. Press on "Date & Time" menu

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/11%20-%20Date%20and%20Time%20Menu.jpeg?raw=true)

55. Ensure both "Automatic Date & Time" and "Automatic Time Zone" are both enabled [buttons should be orange if they're on]

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/12%20-%20Automatic%20Time.jpeg?raw=true)

56. Double check the time is correct with your phone or computer! Turn the Pi on and off if the times are different (go back to step 51 and recheck until correct)! [my Pi wasn't correct and caused issues when updating packages]

57. Close out of "Date & Time" menu

58. Right click on the desktop

59. This menu will appear

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/13%20-%20Right%20Clicked%20on%20Desktop.jpeg?raw=true)

60. Select "Open in Terminal" so a new terminal appears

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/14%20-%20New%20Desktop%20Terminal.jpeg?raw=true)

61. Type `cd` into the terminal press the "Enter" key to Change Directory to your Pi's home directory [you can paste this upcoming code from the block below if this README is open on your Pi!]

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/15%20-%20Entered%20cd.jpeg?raw=true)

_Should look like this after you press "Enter"_

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/16%20-%20After%20cd.jpeg?raw=true)

62. Type `sudo apt update` into the terminal and press "Enter" to update the Pi's base packages

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/17%20-%20sudo%20apt%20update.jpeg?raw=true)

63. "[sudo] password for *your username*:" will pop up, enter in your Pi's password [no text or * will appear while you're typing, simply press the "Enter" key when you finished typing your password!]

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/18%20-%20sudo%20apt%20update%20password.jpeg?raw=true)

_You will continue to type in the code into the terminal the same way and follow the password step if it appears!_

64. Type `sudo apt upgrade` into the terminal and press "Enter" to upgrade the Pi's base packages

65. Type `y` into the terminal and press "Enter" to accept the upgrades and wait for it to complete

66. Type `sudo apt install python3-pip python3-venv libopenblas-dev libsndfile1 libportaudio2 ffmpeg` into the terminal and press "Enter" to install libraries needed to run the transcription program

67. Type `y` into the terminal and press "Enter" to accept the upgrades and wait for it to complete

68. Type in `sudo pip install --upgrade pip --break-system-packages` and press "Enter" to ensure pip is on the most updated version

69. Type in `sudo python3 -m pip install --upgrade pip setuptools wheel --break-system-packages` and press "Enter" to set up the Python environment

70. Type in `sudo pip install faster-whisper sounddevice numpy pydub pillow luma.oled --break-system packages` and press "Enter" to install transcription code's Python dependencies





---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Future Goals:**_

_*In Progress*_

1. Make the transcription code automatically start when the Raspberry Pi 5 turns on
2. Continue to document and improve accessability of this project
