_**About This Project:**_

**TLens** is a QL Plus Challenger Project developed by  Arturo Martinez, a UTSA Top Scholar Electrical Engineering sophomore.

This project's ultimate goal is to develop an **open-source transcription device** that doesn't require Wi-Fi or a cellular device for a deaf and visually impaired veteran and, eventually, anyone to use anywhere in the world.

Here's a demonstration of TLens! https://youtu.be/GYs88_FpokA

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Materials Used:**_

Epson Moverio BT-35e Smart Glasses [recommend looking on Ebay for a pair]: https://epson.com/For-Work/Wearables/Smart-Glasses/Moverio-BT-35E-Smart-Glasses/p/V11H935020

A Computer connected to Wi-Fi [To install the Ubuntu Desktop OS (used v25.04 for this project)]

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

_**Setup:**_

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
38. Click on "Username" and enter in your preferred account username [I would keep it simple, I chose "tlens"]
39. Click on "Computer" and enter in your preferred name for the Raspberry Pi
40. Press "Next"
41. A "Password" screen with "Password" and "Confirm Password" fields should appear
42. Enter in the same password for both fields [I recommend having a simple one as you will have to enter it multiple times when doing sudo commands]
43. Press "Next"
44. An "Almost done" screen will appear, allow Ubuntu to finalize setup and an orange button to appear
45. Press the orange button labeled "Start Using Ubuntu"
46. A "Welcome to Ubuntu XX.XX!" screen should appear [XX.XX will be your version of Ubuntu]
47. Press "Next"
48. A "Help improve Ubuntu" screen should appear
49. Press "No, don't share system data"
50. Press "Next"
51. A "Get started with more applications" screen should appear
52. Press "Finish"

_You have successfully setup Ubuntu to run on your Raspberry Pi! You're doing great!_ :goat:

_Now we will begin installing all the libraries we need to use the transcription program_

_To prevent errors when installing, we will make sure our Pi is in the correct timezone [mine wasn't and caused errors with the next steps]_

51. Press on the top right corner of the Desktop where Wi-Fi, Sound, and Power icons are

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/9%20-%20Pressing%20Top%20Right%20Desktop.jpeg?raw=true)

53. Press on the gear icon in the new popup menu to access the Pi's settings menu

![image alt](https://github.com/arturo-j-martinez-ii/arglassestranscribe/blob/main/images%20for%20README/10%20-%20Pressing%20Settings.jpeg?raw=true)

54. Scroll down on the left to "System" and Press on the "Date & Time" menu

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

_Don't worry if it looks frozen or takes a while on a step! It's completely normal!😄_

64. Type `sudo apt upgrade` into the terminal and press "Enter" to upgrade the Pi's base packages

65. Type `y` into the terminal and press "Enter" to accept the upgrades and wait _very patiently_ for it to complete

66. Type `sudo apt install -y build-essential libssl-dev zlib1g-dev \
libncurses5-dev libncursesw5-dev libreadline-dev libsqlite3-dev \
libgdbm-dev libdb5.3-dev libbz2-dev libexpat1-dev liblzma-dev \
tk-dev libffi-dev wget libopenblas-dev libsndfile1 libportaudio2 ffmpeg git` into the terminal and press "Enter" to install libraries needed to run the transcription program

67. Type `cd /usr/src` to go to system source directory where Python 3.12.7 will be downloaded and built
68. Type `sudo wget https://www.python.org/ftp/python/3.12.7/Python-3.12.7.tgz` to download Python 3.12.7 source code from the offical Python website
69. Type `sudo tar xzf Python-3.12.7.tgz` to extract the downloaded Python compressed folder
70. Type `cd Python-3.12.7` to move into the extracted Python source folder
71. Type `sudo ./configure --enable-optimizations --with-ensurepip=install` to configure Python 3.12.7 build for better performance and include pip
72. Type `sudo make -j$(nproc)` to compile Python 3.12.7 using all CPU cores for faster building
73. Type `sudo make altinstall` to install Python 3.12.7 without replacing our system's default Python verison
74. Type `sudo update-alternatives --install /usr/bin/python3 python3 /usr/local/bin/python3.12 1` to add Python 3.12.7 as an alternative Python verion on our system
75. Type `sudo update-alternatives --config python3` to choose Python 3.12.7 as our default Python verion
76. Type `python3 --version` to check if Python 3.12.7 was installed correctly [terminal should output "Python 3.12.7"]
77. Type `python3 -m ensurepip --upgrade` to ensure pip (Python's package manager) is installed and updated
78. Type `python3 -m pip install --upgrade pip` to upgrade pip to the latest verion
79. Type `cd` to return to our home directory
80. Type in `sudo python3 -m pip install --upgrade faster-whisper sounddevice numpy pydub` and press "Enter" to install Python libraries needed for the transcription program
81. Type in `git clone https://github.com/arturo-j-martinez-ii/tlens.git` and press "Enter" to install the transcription program from this GitHub!
82. Find the "Files" application on the left hand side of the desktop ![image alt](https://github.com/arturo-j-martinez-ii/tlens/blob/main/images%20for%20README/19%20-%20File%20Application.jpeg?raw=true)
83. Go to "Home" and open the new "tlens" folder ![image alt](https://github.com/arturo-j-martinez-ii/tlens/blob/main/images%20for%20README/20%20-%20Home%20Folder.jpeg?raw=true)
84. Right click within "tlens" folder and select "Open in Terminal" ![image alt](https://github.com/arturo-j-martinez-ii/tlens/blob/main/images%20for%20README/21%20-%20tlens%20Folder.jpeg?raw=true)
85. Type in `python3 tlenscode` and press "Enter" to run the transcription program!

A black screen showing "Starting Transcription..." should appear. 

![image alt](https://github.com/arturo-j-martinez-ii/tlens/blob/main/images%20for%20README/22%20-%20Starting%20Transciption%20Screen.jpeg?raw=true)

If so, you have successfully finished installing the transcription program!

You can end the program by pressing "Esc" on the top left of your keyboard and run it again by repeating steps 82-85! [Or open a terminal and type `cd tlens` then `python3 tlenscode`]


_You have successfully setup your Raspberry Pi to run the transcription! The hard part is over!_ 🥳

Now it's time to connect our glasses to our Raspberry Pi and power it with our Power Bank to finish the project!

86. Open the BT-35e's case and ensure you have the Headset and Interface Unit
87. Connect the Headset's cable to the Interface Unit
88. Connect our HDMI to microHDMI cable to the Interface Unit and Raspberry Pi respectively
89. Connect our Power Bank and Interface Unit with a USB to microUSB cable [The Interface Unit should have a blue LED flashing on and off]
90. Put on the Headset and a white box with "<No Signal>" should appear [You may have to move the glasses around to see it!]
91. Connect our Power Bank and Raspberry Pi with a USB to USB C cable [You should see the Ubuntu loading screen and then the login screen appear!]
92. Connect the microphone's reciever to the Pi and turn on the microphone [Should have a Green LED flashing on and off]
93. Turn on the Pi
94. Login in
95. Run the transcription program as before!

 You should see a similar result to the Demo video linked in the beginning of this README!

 ![imagealt](https://github.com/arturo-j-martinez-ii/tlens/blob/main/images%20for%20README/23%20-%20Demo%20Picture.png?raw=true)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

_**Future Goals:**_

_*In Progress*_

1. Make the transcription code automatically start when the Raspberry Pi 5 turns on
2. Continue to document and improve accessability of this project
