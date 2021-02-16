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
  
