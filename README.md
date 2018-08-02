# MMDVM-Nextion-Screen-Layouts  
  
Here you will find a collection of screen layouts I have put together for Nextion Screens as well as information on how to acquire, connect, set up and get operating.  
Layouts for both Duplex and Simplex Hot Spot are available.  
In the main github page for this repository you will find a file called "Instructions.md".   
The "instructions.md" file has instructions on how to connect Nextion displays, do basic text box editing to HMI files as well as how to get the HMI files compiled  to TFT and sent to the Nextion screen, (basically all you need to know to get your screen going).  
  
I am testing these layout files with the Nextion 2.4" and 3.2" displays.   
If anyone would like to provide feedback please contact me at wa6hxg@gmail.com   
  
Revision History:   
  
1.0 (Original)  
1.1 Fixed Spacing on Antenna Signal Bars.  
1.2 Added RSSI and BER labels to DStar Page.  
1.3 Added Last Heard Talk Group to right of Last Heard Station.  
1.4 Fixed a typo.  
1.5 Adjusted "t0bis" and "t2bis" text field Y position, was covering bevel in background.  
1.6 Fixes some errors on the NXDN page, edited background graphics, and optimized code.  
1.7 Updated numerous text boxes, the bottom of letters "Q" and "g" had a few pixels being clipped off.   
1.8 Changed "Duplex MMDVM Voice Modem" on MMDVM Pages from "Duplex" to "Simplex" for Simplex Layouts.  
1.9 Edited the background image, dimming down the bright white spots to blue to make them less distracting.   
2.0 Changed Text overlays to blend with backgrounds instead of having colored boxes behind, improved look.  
PLEASE NOTE: For versions 2.1 and above please use Layout G4KLX in Pi-Star Configuration page for Nextion.   
2.1 Added dual last heard slots to the DMR pages so two of the last heard calls and talk groups will be displayed.  
3.1 Interactive layouts based on a modified fork of the "Nextion Driver" by ON7LDS. This enables additional fields  
from MMDVM Pi-Star to be sent to the screen and requests from the screen may be sent to back the Pi-Star as well.  

In Development: 
I have recently updated all of my layouts to v2.0 including 2.4", 3.2" and 3.5”. v2.0 brings visual blending improvements for the text boxes created in Nextion. (Look much better!) There is a version 2.1 available for duplex with 3.2” screens (can also be used with simplex spots). 2.1 features two last heard slots for each time slot for DMR. I used 2.1 for many weeks and was very satisfied with its operation. (Must use G4KLX Layout setting in Pi Star for 2.1) Version 3.1 is in beta and being initially developed on a 3.2” screen with extended information incorporating my own fork of the “Nextion Driver” from ON7LDS. I am running it now full time and making improvements daily. Many more features will be available in 3.1 thanks to the Nextion Driver functionality. First it is running 115200 baud so the page changes are much quicker and data exchanges from the Pi to Nextion and vice versa are very quick. Any info can be read from pi mmdvm.ini and displayed on the layout, so frequency, temp, cpu etc. Talkgroup numbers are displayed now with corresponding TG names pulled from a talkgroup name file, also a stripped.csv file for user info is used to display more info for each caller similar to what you see on TYT 380-390 radios with TYToolz firmware. Another nice feature is linux commands can be sent back to the pi from pre-programmed buttons and in return single line command line feedback is sent back to the Nextion for display. I have already added and succesfully tested a button for firmware update (modem specific) so I may make a page with several options for firmware update of different hats. Other commands set to buttons are mmdvm host stop and start, pi reboot and power off, pi Star update, upgrade, drop dynamic on slot of choice as well as drop QSO on either slot (in development). The underlying ONLDS code needs more reworking so it will take me some time as I am working alone on this maybe an hour a day. I have added several pages and buttons with new features including a dmr page with 12 last heard calls, multiple pages for some modes with different style layouts and user selectable layout changes. Also in beta are pages for config of different functions and command line return display. It is very simple and quick to change pages and you may set which page layout you want for which mode as well as if the display auto changes pages or not regardless of rf or net timeout setting as well as how long to change pages if in auto. So far 3.1 (19th beta version) it is an absolute pleasure to use. If anyone has recommendations for Linux code to send back to pi or any other ideas they would like to see incorporated let me know.  
  
File explanation...   
  
The HMI Files directory include HMI files for the Nextion Editor, they may be edited and compiled to TFT Files. (instructions   for that process are here on my Github page in the Instructions.md file).  
The TFT Files directory include TFT files for direct upload to the Nextion screen. (instructions for that process are in the   Instructions.md file as well).   
   
File details:    
   
For 2.4" Screens   
Green Color Version for Duplex 2.4" = Green1_Duplex_24in_LHnLHTG_GB_X.X  
Green Color Version for Simplex 2.4" = Green1_Simplex_24in_LHnLHTG_GB_X.X  
Blue Color Version for Duplex 2.4" = Blue1_Duplex_24in_LHnLHT_GB_X.X  
Blue Color Version for Simplex 2.4" = Blue1_Simplex_24in_LHnLHTG_GB_X.X  
  
For 3.2" Screens  
Green Color Version for Duplex 3.2" = Green1_Duplex_32in_LHnLHTG_GB_X.X   
Green Color Version for Simplex 3.2" = Green1_Simplex_32in_LHnLHTG_GB_X.X    
Blue Color Version for Duplex 3.2" = Blue1_Duplex_32in_LHnLHT_GB_X.X   
Blue Color Version for Simplex 3.2" = Blue1_Simplex_32in_LHnLHTG_GB_X.X   
  
For 3.5" Screens  
Green Color Version for Duplex 3.5" = Green1_Duplex_35in_LHnLHT_GB_X.X   
Green Color Version for Simplex 3.5" = Green1_Simplex_35in_LHnLHT_GB_X.X    
Blue Color Version for Duplex 3.5" = Blue1_Duplex_35in_LHnLHTG_GB_X.X   
Blue Color Version for Simplex 3.5" = Blue1_Simplex_35in_LHnLHTG_GB_X.X   

Enjoy!  
73  
