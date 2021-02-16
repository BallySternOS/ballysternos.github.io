## Getting the Software  
  
At this point, you should have already [built the hardware](hardware.md), and [downloaded the library](library.md).  
  
Now, you're ready to download the software for your machine.  
There are repositories for several games built here:  
https://github.com/BallySternOS  
For these instructions, I'll list out the steps to build Trident2020.  
  
### Steps
- If you don't already have the Arduino IDE, get that installed. Before you proceed with this guide, I recommend that you get your Arduino talking to your computer and try out the "Blink" program to make sure you have everything configured correctly. They have great documentation and support to get you going.  
- Go to the [project home](https://github.com/BallySternOS) and locate the game you want to build. For this example, we're building [Trident2020](https://github.com/BallySternOS/Trident2020).
- Click on the "Code" button.  
- Click on the "Download ZIP" option in the menu that pops up.  
- Once the ZIP is downloaded, move it to your Arduino code folder, or a Pinball folder, or whatever.  
- Unpack the ZIP. Make sure the folder it unpacks to is the same name as the ".ino" file for the machine. Example: \Pinball\Trident2020\ will be where Trident2020.ino and the other files live on my machine.  
- Grab the [library](library.md) files from the last step (BallySternOS.cpp, BallySternOS.h, SelfTestAndAudit.cpp, and SelfTestAndAudit.h) and put those in your folder (Example: \Pinball\Trident2020\BallySternOS.cpp, etc.)  
- Open the ".ino" file in your Arduino IDE (Example: Trident2020.ino)  
  
  
### Notes  
At this point, you have everything you need to [build](compile.md) out the game software for you machine, but you may want to configure some options first.  
For each implementation, I use a BSOS_Config.h for library-specific configurations, and some custom flags at the top of the ".ino" file.  
I always try to keep the files on GitHub compatible with a stock machine. If you have non-standard hardware or you want to use a Wav Trigger for digital sound, read on.  
  
#### BSOS_Config.h  
Most of the defines in this file are set based on the capabilities of a standard example of that machine. For example, some machines have 7-digit displays, and they require the "BALLY_STERN_OS_USE_7_DIGIT_DISPLAYS" definition to be on. If one of those capabilities is needed, the line will be uncommented in the code (i.e. the line will NOT begin with "//").  
A couple of hardware options may need to be tweaked depending on your setup:  
- "BSOS_SLOW_DOWN_LAMP_STROBE" - if you find that your lamps are flickering, you might uncomment this define and see if that helps.  
- "BSOS_NUM_SWITCH_LOOPS" and "BSOS_NUM_LAMP_LOOPS" - these values are set to work with the original MPU. If you have an Alltek MPU, you might need to increase these numbers to account for the faster hardware. If you experience issues with the switches showing noise or the lamps flickering, increase each of these values, 5% at a time, to see if you can correct the problem.  
  
#### Defines at the top of the ".ino" file  
Other game options may be specified at the top of the program file (Exmaple: Trident2020.ino)  
For the sound of Trident2020, the operator can compile to use the original SB100 board for sound, or use a Wav Trigger board for digital sound. To compile for the SB100, the define is in BSOS_Config.h. To use the Wav Trigger, turn off the SB100 define in the BSOS_Config and use one of the following values in Trident2020.ino  
- //#define USE_WAV_TRIGGER  
or  
- //#define USE_WAV_TRIGGER_1p3  
by uncommenting the correct line.   
  

