## Compiling the code  
  
At this point, you should have the [library](library.md) downloaded, the [game code](software.md) downloaded, and everything opened in your Arduino IDE.  
  
Using Trident2020 as an example, your Trident2020 folder should now contain these files:  
- BallySternOS.cpp  
- BallySternOS.h  
- BSOS_Config.h  
- SelfTestAndAudit.cpp  
- SelfTestAndAudit.h  
- SendOnlyWavTrigger.cpp  
- SendOnlyWavTrigger.h  
- Trident2020.h  
- Trident2020.ino  
If you're missing any of those files, please refer to the documentation on getting the [library](library.md) or [software](software.md).  
  
  
I'm going to assume that you're using a Nano based on the ATMega328P chip that uses the CH340 bootloader. If you're not, you'll want to get one of those. With some machines, you'll have to install a driver to use the CH340 bootloader. You should be able to find instructions from the manufacturer.
To put the code on your board, follow these steps:  
- Plug the Nano into a USB port.  
- In the Arduino IDE, select "Tools > Board > Arduino AVR Boards > Arduino Nano"  
- Select "Tools > Processor > ATMega328P (Old Bootloader)"  
- Select "Tools > Port" and then select your board's port  
- Select "Sketch > Upload"  
  
The Upload step will compile the code and put it on the board.  
If your compilation is bigger than 100%, you may have made a mistake with options. I usually build in sound support for the original hardware (Chimes, SB100, etc.) and the Wav Trigger. These two implementations are usually too big to both be compiled. You need to choose one or the other for most game code.  
  
Once that's compiled and loaded onto your board, you're ready to [install](install.md).  


