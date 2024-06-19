
## NEXTION 4.3" DISPLAY, NEXTION 3.5" DISPLAY and NEXTION 2.4"/2.8" DISPLAY HMI FILES

by Steve Nofs
  - For those without the Nextion editor: All TFT files have been compiled/uploaded for 'standard' orientation and 'flipped 180' rotation. Let me know if you need a specific display compiled/uploaded.
  - The Nextion 4.3" must be Intelligent Series to run the 4.3" code.
  - This GitHub repository contains my HMI versions for the Nextion display for use on the Gaggiuino mod of the Gaggia Espresso Machine.
  - My goal was to provide a clean and innovative interface to the STM32 controller while maintaining all functionality of the original HMI coding.
  - The official project lives here: [Gaggiuino](https://gaggiuino.github.io/#/)
  - What you will find here are my HMI files and compiled TFT files for the 2.4"/2.8", 3.5" and 4.3" Nextion displays.
  - Feel free to give them a try. If for any reason you want to revert back to the original HMI code you can always flash the original code to your display.
  - Enjoy!

### See the latest demos on my channel  [YouTube](https://www.youtube.com/@stevenofs8795).
### Bezel models [Printables rsilvers](https://www.printables.com/model/487643-gaggiuino-24-28-and-35-nextion-display-housing).

### Need help or have Feedback?  [Gaggiuino Builders on FB](https://www.facebook.com/groups/5362374853865845)

 
## Nextion 4.3"

   ![Screenshot Home 43](https://github.com/SteveNofs/Gaggiuino_35/assets/162605333/bda699cc-7143-4f21-a3b8-86ed56de920f)
  
## Nextion 3.5"

![Screenshot Home 35](<Pics/Screenshot Home.png>)

## Nextion 2.4" and 2.8"

![Screenshot Home 24](<Pics/Screenshot Home-1.png>)


## How to use
#### METHOD 1 - Direct load TFT file to to 32G FAT MicrtSD card (it must be the only file on the SD card), insert into Nextion, power on to flash display.
#### METHOD 2 - Load into Nextion editor, complile, export to 32G FAT flash card, flash display.
- *** Note if errors when trying to open file: Click on file, click View Raw which will download the file, then open the file in Nextion Editor.
- In Nextion editor, click the "Device ID" in the top menu bar, select your Device. 
- 2.4", 2.8", 3.5": Select "Display" and choose rotation: standard rotation 90; select 270 for Robert Silvers 3.5" bezel.
- 4.3": Select "Display" and choose rotation of 0 degrees or 180 degrees depending on bezel being used.
- Compile. 
- Then select FILE/TFT OUTPUT and save to a microSD card to flash the display.


## Nextion 4.3" Version History

#### Ver. 30APR2024
- Real-time floating values track with Brew graph plotting
- Tare button on Brew graph resets Weight plot to Zero
- Added Puck Resistance calculation graph to Brew Graph screen

#### Ver. 14APR2024b
- added "Load Defaults" button to Keyboard screen


#### Ver. 14APR2024
- Build based on 3.5" HMI
- Added graphical profile selection buttons
- Resized elements
- Implemented Live-updating Brew Graph Preview



## NEXTION 3.5" VERSION HISTORY #####

#### Ver. 24MAR2024:

- More cleaning up of Brew option screens; aligning/arranging components
- Added Preview button to Soak Screen

#### Ver. 21MAR2024:

- Full rework of  Manual Mode.
- Added ShotPower meter: this is an indicator of the hydraulic force applied to the puck
- added target weight to Brew Graph screen. 

#### Ver. 06MAR2024:

- Added functional code to the LED color configruation screen.
- LED ON/OFF not functional; turn LED off by setting RGB to zero.
- For anyone interested here is how one reads the LED settings:
```
LED_ON=ledNum&0x02000000>>25
LED_DISCO=ledNum&0x01000000>>24
LED_RED=ledNum&0x00FF0000>>16
LED_GREEN=ledNum&0x0000FF00>>8
LED_BLUE=ledNum&0x000000FF
```

Save updated values like this:

`ledNum=bt0.val<<1+bt1.val<<8+n0.val<<8+n1.val<<8+n2.val`


#### Ver. 02MAR2024:
- Matched original Left-to-Right brew graph format and speed
- Adjusted brew graph vertical lines at 10 seconds per line
- Weight button on main screen gets RED outline when Stop-on-dose is enabled


#### Ver. 14FEB2024:
- Weight button text on main screen is RED when Stop-on-dose is enabled
- Started cleaning up Brew Preview screen


#### Ver. 29JAN2024:
- Added Temp and Pres mini-graphs to main screen
- Added graphical buttons across top of main screen
- Standardized colors where possible: 
    - RED/Temp
    - BLUE/Pres
    - YELLOW/Flow
    - GREEN/Weight


#### Ver. 22JAN2024:
- Basic beginning of 2.4 --> 3.5 conversion

## NEXTION 2.4" and 2.8" VERSION HISTORY ####

#### Ver. 24MAR2024:

- Full rework of Manual Brew Screen with Brew Graph, Flow, Flow Target, Weight, Target Weight, Shot Hydaulic force feedback gauge during shot.
- Realign/organize components in Brew Settings screens.
- Color code data entry components in Brew Setting screens: Weight=GREEN, Flow=YELLOW, Temperature=RED, Pressure=BLUE.
- Added Target Weight to Brew Screen

#### Ver. 10MAR2024:
- A better indication of Stop-on-weight being enabled: red outline on the button with white text; easier to read. 
- LED configuration screen to configure LED color
- Added background color to water level gauge for better visual.
- Fine-tuned alignment of graphic elements on Home screen.






