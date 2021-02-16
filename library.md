## Getting the library
The Bally/Stern Early Solid State Operating System uses a single library to talk to the MPU board.  
The easiest way to get the library is to download a ZIP from the GitHub repository:  
https://github.com/BallySternOS/BallySternOS  
### Steps
- Go to this link: https://github.com/BallySternOS/BallySternOS  
- Click "Code" button  
- Click "Download Zip"  
  
Once you extract the zip to your machine, you'll have four files necessary to build the software for your machine:  
- BallySternOS.cpp
- BallySternOS.h
- SelfTestAndAudit.cpp
- SelfTestAndAudit.h  
  
With this library, you can build your own rules fairly easily. I've included a project called "PinballMachineBase" to demonstrate the mechanics of Audit/Attract/Game mode, ejecting a ball, turning on & off lamps, controlling scoring, etc. Just include the four files listed above into your Arduino project and you can start experimenting.  
  
If you just want to use one of the implementations already built for this OS, your next step will be to get the software for your particular machine. You can find the respositories for all the games here:  
https://github.com/BallySternOS  
  
And you can find instructions on how to [build the software here](software.md).
