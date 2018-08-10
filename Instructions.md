# MMDVM-Nextion-Screen-Layouts
To edit the HMI File download the Nextion Editor from: https://nextion.itead.cc/resources/download/nextion-editor/  
  
Purchasing a Nextion Screen.:
  
Sizes that are available include: 2.4", 2.8", 3.2", 3.5", 4.3", 5.0", 7.0", and 9.0".
Nextion Screens are also available in 2 versions, Basic and Enhanced. The biggest difference between the two is the  
amount of available flash memory for storing a layout. More details are available here: https://nextion.itead.cc/nextion-shop/    
My layouts all fit on the "Basic" screens though there are layouts out there that use more memory their 4mb limit.  
I would recommend the "Enhanced" versions to be prepared for future layouts that may consume more on-board memory.    
These are the "Enhanced" model numbers for the Nextion screens currently available:  
NX3224K024_011R for 2.4", NX3224K028_011R for 2.8", NX4024K032_011R for 3.2", NX4832K035_011R for 3.5", NX4827K043_011R for     4.3", NX8048K050_011R,NX8048K070 for the 7".  
The "Basic" version model numbers available are:  
NX3224T024_011R for 2.4", NX3224T028_011R for the 2.8", NX4024T032_011R for the 3.2", NX4832T035_011R for the 3.5",     NX4827T043_011R for the 4.3", NX8048T050_011R for the 5" and NX8048T070_011R for the 7".  
Most layouts you will find are for the 2.8"-5" screens. There are some out there for the others but are more rare.  
Screens are available on Ebay as well as other outlets and there are after market acrylic sandwich type housings available as well for 2.8"-3.5" screens.  
Beware of "TJC" versions that are available, if you receive a "TJC" version return it immediately as they are marketed for the Chinese market and are only programmable using a Chinese language editor. Not a large concern ad most Chinese sellers are selling US marketed screens ("NX" prefix).

Connecting your Nextion display to a hot spot:  
   
The electrical connections from the Nextion screen to the Hat, whatever type it may be are simple.  
Looking at the front of the Nextion screen with the connector on the left the lower wire is 5v the upper is Ground and the other two in the middle are TX and RX. They are also labeled on the back of the Screen circuit board.    
Look for the Nextion wiring section on your specific modem or Hat (usually labeled).
The jumbospot and duplex boards are clearly labeled, on the Zumspot the top edge pin of the GPIO pin section is the 5v and the other pins (-, TX, and RX are on the front corner on the section labeled "serial". The 3.3v pin in the serial section is not enough to power the screen hence the 5vdragged from the 5v pin on the gpio header section. One may cut the trace on the 3.3v pin  in the serial section and add a small wire to the 5v gpio pin.
TX on the screen will go to RX, and the RX on the screen will go to the TX on the Hat, if it does not work check that you did   not reverse the two middle wires. Be extra careful and double check when attaching the power leads!    
You may use headers if you have room onn the modem or clip connectors off, strip the wire back about 1.5mm, tin them and solder them straight to the Hat. If they protrude too long just clip off excess. Some like headers but depending on your installation they may not fit. Whichever you prefer. 

Editing the text boxes to display the frequency you want:  

Run "NextionEditor.exe".  
Open the HMI file.  
On the top right of the application window you will see entries under the "Page" section click and highlight the "MMDVM" Page.  
On the display preview in the middle click on the left "TX" Mhz entry where it says "t109" in yellow thus turning the "t109 to blue.  
Now on the lower right of the application window under where it says "Attribute" scroll down to the value that says "txt" and correct on the right the frequency to what you want it to be for your hotspot.   
After correcting the numbers to your frequency hit the enter key on your keyboard for it to be applied to the layout.   Now click the right "RX" frequency diplay "t108" in the middle display preview and it will turn blue.  
On the lower right do the same as you just did with your "TX" digits to your "RX" digits by changing the "txt" field.   Hit the enter key on your keyboard again for it to be applied.  
After you have corrected the frequency numbers for the Main MMDVM Page go ahead and click the next page on the top right of the editor window labeled "DStar" and do the same for the two frequency entries on that page (t100 and t101).   Continue this process with the other pages down to Page 5 NXDN, then you are done editing.  

Selecting your specific screen model:

YOUR SCREEN HAS TO BE THE SAME SIZE AS THE LAYOUT YOU ARE USING!!!   
Click on the "Device ID" button on the toolbar, a new window will pop up, now click the basic or enhanced box depending that matches your screens model number. Next click on the exact screen model number then "OK" button on the bottom of the window.  

Now hit "Save As" on the top left of the application window and set the file location and save your new HMI file.  
  
Getting the TFT made so you may upload it to your Nextion display:   
  
Now on the top left toolbar click on the "Compile" button, that will compile your new TFT file ready for sending to your display.  
Click "File" on the top left of the application window then "Open Build Folder" and a folder window will appear with your new TFT file in it.  
The TFT file is what you want to put on a blank micro SD card and insert into the nextion display.  
Right click on the "TFT" file and click copy.  
Navigate to your blank Micro SD Card and right click in a blank area and click paste, wait a minute, then eject the card from the computer.  
Only one TFT may be on the file at a time and the card must be blank otherwise.  
Power up the display with the card all the way inserted and you will see the display say uploading file and a % complete then it will update....  
When it says Update Succeeded you may pull the plug off the display and remove the Micro SD from the display.  
Plug the screen back into the hotspot and reboot it by power cycling it.
   
Setting up Pi-Star to talk to the Nextion display:     
   
Navigate to your Pi-star dashboard and on the "Configuration" page in the MMDVM Configuration under MMDVM Display select "Nextion" for the first field and for most hotspots with the screen attached to the hat select Port "Modem" (may be different for some configurations, then for 'Screen Layout" set "ON7LDS 3". Note: If you are using versions 2.1 or later set "Screen Layout" to "G4KLX".    
If you don't see that option you need to update your version of Pi-Star.  
To do that run "Update" on the "Configuration" page, then "Upgrade" on the "Expert" page until the text reads that you version is current.  
The update process has been made much simpler with no need to use SSH any longer.  
After that, the option "ON7LDS will be available.  
That is all for getting the PiStar to communicate with the screen correctly!  
  
After that your Nextion display will be completely setup!   
  
If you want the page for a mode to stay on (and be in that mode) longer, set “rf hold “ and “net hold” for that mode to a higher value.  This will cause the Hotspot to hold on that mode longer before going to standby screen or switching modes to another.  
  
Remember, on the DMR page (and maybe others) the prefix: “N” means the call is from the Network and the prefix “R” is from local RF.  RSSI and BER will show when you transmit to the Hot Spot, they will not be displayed when a call comes from the Network.  
  
The HMI Files directory includes HMI files for the Nextion Editor, they may be edited and Compiled to TFT Files. The HMI files may be loaded into the Nextion Editorrequire assi and adjusted to your liking as described above.  
   
The TFT Files directory include TFT files for direct upload to the Nextion screen also described above.  
File versions, differences, and details are outlined in the README.md   
   
If you get stuck setting up a Nextion screen feel free to contact me with questions at: wa6hxg@gmail.com    
If you would like to contribute to my work on Nextion MMDVM display layouts my Paypal address is: wa6hxg@gmail.com  

Thanks and 73,  
Ryan  
WA6HXG
