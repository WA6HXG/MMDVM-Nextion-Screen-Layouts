# MMDVM-Nextion-Screen-Layouts
To edit the HMI File download the Nextion Editor from: https://nextion.itead.cc/resources/download/nextion-editor/  

Run "NextionEditor.exe".  
Open the HMI file.  
On the top right of the application window you will see entries under the "Page" section click and highlight the "MMDVM" Page.  
On the display preview in the middle click on the left "TX" Mhz entry where it says "t109" in yellow thus turning the "t109 to blue.  
Now on the lower right of the application window under where it says "Attribute" scroll down to the value that says "txt" and correct on the right the frequency to what you want it to be for your hotspot.   
After correcting the numbers to your frequency hit the enter key on your keyboard for it to be applied to the layout.   Now click the right "RX" frequency diplay "t108" in the middle display preview and it will turn blue.  
On the lower right do the same as you just did with your "TX" digits to your "RX" digits by changing the "txt" field.   Hit the enter key on your keyboard again for it to be applied.  
After you have corrected the frequency numbers for the Main MMDVM Page go ahead and click the next page on the top right of the editor window labeled "DStar" and do the same for the two frequency entries on that page (t100 and t101).   Continue this process with the other pages down to Page 5 NXDN, then you are done editing.  
Now hit "Save As" on the top left of the application window and set the file location and save your new HMI file.  
After that hit "Compile", that will compile your new TFT file ready for sending to your display.  
Click "File" on the top left of the application window then "Open Build Folder" and a folder window will appear with your new TFT file in it.  
The TFT file is what you want to put on a blank micro SD card and insert into the nextion display.  
Right click on the "TFT" file and click copy.  
Navigate to your blank Micro SD Card and right click in a blank area and click paste, wait a minute, then eject the card from the computer.  
Only one TFT may be on the file at a time and the card must be blank otherwise.  
Power up the display with the card all the way inserted and you will see the display say uploading file and a % complete then it will update....  
When it says Update Succeeded you may pull the plug off the display and remove the Micro SD from the display.  
Plug the screen back into the hotspot and reboot it by power cycling it.  
Now navigate to your Pi-star dashboard and on the "Configuration" page in the MMDVM Configuration under MMDVM Display select "Nextion" for the first field and for most hotspots with the screen attached to the hat select Port "Modem" (may be different for some configurations, then for 'Screen Layout" set "ON7LDS 3".  
If you don't see that option you need to update your version of Pi-Star.  
To do that run "Update" on the "Configuration" page, then "Upgrade" on the "Expert" page until the text reads that you version is current.  
The update process has been made much simpler with no need to use SSH any longer.  
After that, the option "ON7LDS will be available.  
That is all for getting the PiStar to communicate with the screen correctly!  

After that your Nextion display will be completely setup!!!  

If you want the page for a mode to stay on (and be in that mode) longer, set “rf hold “ and “net hold” for that mode to a higher value.  This will cause the Hotspot to hold on that mode longer before going to standby screen or switching modes to another.  

Remember, on the DMR page (and maybe others) the prefix: “N” means the call is from the Network and the prefix “R” is from local RF.  RSSI and BER will Show when You transmit to the Hot Spot, it does not come from the Network.  

The HMI Files directory includes HMI files for the Nextion Editor, they may be edited and Compiled to TFT Files. The HMI files may be loaded into the Nextion Editor and adjusted to your liking as described above.  
 
The TFT Files directory include TFT files for direct upload to the Nextion screen also described above.  
File versions, differences, and details are outlined in the README.md   
