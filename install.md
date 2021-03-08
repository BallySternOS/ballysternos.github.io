## Installing the card onto J5  
  
Your MPU should be working before you attempt this step. There are some situations where you can use this daughter card without parts of your MPU functioning. For example, the new code will not require the PROMs, RAM, CRAM, or reset section of the board to be operable. However, until you know your MPU is in working order, I advise you to start there.  
  
With the machine off, plug in your new card into J5, ensuring that the rightmost pin (pin 1) of the daughter card is connected to the rightmost pin (pin 1) of J5. The J5 connector is keyed on pin 29, for reference.  
  
On a Bally AS-2518-17, -35, or Stern MPU-100 board, the J5 connector doesn't contain the IRQ line. For those boards, you'll need to run a jumper between the Arduino's pin D2 and the top leg of R134: 
![Image](https://github.com/BallySternOS/BallySternOS/blob/master/images/IMG_2578.jpeg?raw=true)  
  
On a Stern MPU-200 or an Alltek MPU Replacement (Bally/Stern), the J5 connector is 34 pins and it contains an IRQ line on pin 34. For these boards, the daughter card can pick up the IRQ directly from the board:  
![Image](https://github.com/BallySternOS/BallySternOS/blob/master/images/IMG_2572.jpeg?raw=true)  
  
On both of the above installs, there is a Wav Trigger controlled by the daughter card for external sounds.  
  
For machines with an SB-100 or SB-300 sound card, the J5 connection should be mirrored up so the card can still be operated by the old code.  
In the case of the SB-300, the card may produce errant noise when new code is run. In that case, you can pull one of the speaker wires from the SB-300 J3 harness (J3 pin 9 on the SB-300), and run it through another pole of the "old code/new code" switch.  
![Image](https://github.com/BallySternOS/BallySternOS/blob/master/images/IMG_2574.jpeg?raw=true)  
  
In this photo, I've pulled the Green/White wire from the SB-300's J3:Pin 9, and attached it with a yellow jumper to a switch. The switch then returns the speaker signal via the green wire back up to the J3 connector. When the switch is flipped to old code, the speaker is connected. Switching to new code disconnects the internal speak and eliminates unwanted noise. This method allows this modification to be removed very easily.  
  
On some machines, the boot switch can be mounted in the air grate on the under side of the head (Meteor is pictured below). On other machines, or if the operator doesn't want the player to have access to the boot switch, it can be mounted behind the coin door.  
![Image](https://github.com/BallySternOS/BallySternOS/blob/master/images/IMG_2577.jpeg?raw=true)  
  
  
