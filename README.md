# MMDVM-Nextion-Screen-Layouts
Here is a collection of screen layouts I have put together for Nextion Screens.  
Both Duplex and Simplex Hot Spot layouts are available.  
In the main github page for this repository you will find a file called "Instructions.md".   
This file has instructions on how to do some basic editing to Nextion HMI files as well as how to get the HMI files compiled and sent to the Nextion screen (basically all you need to know to get your screen going).  

The electrical connections from the Nextion screen to the Hat, whatever type it may be are simple.  
Looking at the front fo the Nextion screen with the connector on the left the lower wire is 5v the upper is Ground and the other two in the middle are TX and RX.  
Look for the Nextion wiring section on the Hat (usually labeled).  
The top wire from the screen goes to 5v.  
The lower wire on the screen will go to ground. TX on the screen will go to RX, and the RX on the screen will go to the TX on the Hat, if it does not work check that you did not reverse the two middle wires.   
You may use headers if you have room or clip connectors off, strip the wire back about 1.5mm tin them and solder them straight to the Hat. If they protrude too long just clip off excess. Whichever you prefer.   

I am testing these layout files with the Nextion Enhanced (NX40244K032_11) 3.2" Screen. 
Files are also available for 3.5" Nextion Screens and 2.4" Files are forthcoming.
I believe these files will also work for the Non_Enhanced screens. --==(Confirmation welcome)==--  
If anyone would like to provide feedback please contact me at wa6hxg@gmail.com  
I will be working on 2.4" screens next...Feedback is appreciated.  

Revision History:   

1.0 (Original)  
1.1 Fixed Spacing on Antenna Signal Bars.  
1.2 Added RSSI and BER labels to DStar Page.  
1.3 Added Last Heard Talk Group to right of Last Heard Station.  
1.4 Fixed a typo.  
1.5 Adjusted "t0bis" and "t2bis" text field Y position, was covering bevel in background.  
1.6 Fixes some errors on the NXDN page edited background graphics.  

File explanation...  

The HMI Files directory include HMI files for the Nextion Editor, they may be edited and Compiled to TFT Files. (instructions   for that process are in the Instructions.md file).  
The TFT Files directory include TFT files for direct upload to the Nextion screen. (instructions for that process are in the   Instructions.md file).  

File details:  
For 3.2" Screens    
Green Color Version for Duplex 3.2" Green1_Duplex_32in_LHnLHTG_1.X  
Blue Color Version for Duplex 3.2" Blue1_Duplex_32in_LHnLHTG_1.X  
Blue Color Version for Simplex 3.2" Blue1_Simplex_32in_LHnLHTG_1.X  
For 3.5" Screens
Blue Color Version for Duplex 3.5" Blue1_Duplex_35in_LHnLHTG_1.X  
Blue Color Version for Simplex 3.5" Blue1_Simplex_35in_LHnLHTG_1.X  

The folowing files are identical to the other "Blue Color" files except the signal bars are green around the antenna tower.  
Notated with the Suffix (GB)  
For 3.2" Screens  
Blue Color Version for Duplex 3.2" Blue1_Duplex_32in_LHnLHT_GB_1.X  
Blue Color Version for Simplex 3.2" Blue1_Simplex_32in_LHnLHTG_GB_1.X  
For 3.5" Screens  
Blue Color Version for Duplex 3.5" Blue1_Duplex_35in_LHnLHTG_GB_1.X  
Blue Color Version for Simplex 3.5" Blue1_Simplex_35in_LHnLHTG_GB_1.X  

Enjoy!  
73  
