# Case for ReSpeaker XMOS XVF3800 with XIAO ESP32S3
  This is the second iternation of a case for the ReSpeaker XMOS XVF3800 wth XIAO ESP23S3 board from Seeed Studio. The stp and stl files are included.
  The case fits a Dayton Audio PC68-4 2-1/2" Full-Range Poly Cone Driver in the bottom facing down.
  I used 3 #2 x 0.25 inch sheet metal screws to hold the board to the the 3 posts with no inserts.
  I used 3 M3 x 6 mm screws with flat and lock washers to hold the speaker in the 3 M3 inserts.
  The ring holds the speaker grill cloth to the main housing.  I cut the circular grill cloth using a laser engraver.
  ![](https://github.com/mikey60/Voice-Assistant-Customizations/blob/main/Images/ReSpeaker_XVF3800_small.jpg)
  **Many thanks to @formatBCE for his work on the Yaml code I am using for the HA voice assistant**
  The yaml  file and the latest XMOS firmware can be found at ![Respeaker-XVF3800-ESPHome-integration](https://github.com/formatBCE/Respeaker-XVF3800-ESPHome-integration)
  
# Future Proof Homes Satellite1 Dev Kit 3D Printed Case and Customization Guide
This is the first cut at a 3D printed case for the Future Proof Homes Satellite1 Dev Kit.  Theres a few things to note:

1. **Print Orientation**: I printed the case standing up. I also used support everywhere. I used a 0.2mm layer height and 20% infill. I used PLA for this print.
2. **Fitment**: The Sattellite1 Dev Kit is a bit tight in the case, but does fit.  There is a notch in the speaker mount to allow clearence for the speaker terminal.  The speaker needs to be fineshed into the case. I used M3*4*4.2 threaded inserts for the speaker mount. I just used 2 #2 x 0.125 inch screws to hold the Satellite1 assembly in place because I designed the case before I recieved the Satellite1 Dev Kit.  
3. **Satellite 1 Case Ring**: The ring holds the speaker grill cloth on the top of the case.  I used 0.15mm layer height. I am planning to create a stencil with the Satellite1 4 button symbols and try to paint the symbols on the grill cloth.  I am not sure how well that will work yet.
4. **Speaker Considerations**: I used the recommended speaker.  The case design was not designed with any acoustic considerations.  The speaker sounds good enough to me, but I do not plan to use it for serious music listening at the present time.
5. **Feet Modification**: The case feet could be modified to add a place to mount felt pads.

Various pictures of the case and the Satellite1 Dev Kit in the case can be found in the image folder. The yaml fle, jarvis Flac file and Jarvis piper files I used can be found in the files folder.

**Configuring the Jarvis Voice in Home Assistant Piper Addon  UPDATED per suggestions from jysinn on Discord**
  Download the .onnx and .json files in high and in medium folders from [Hugging Face](https://huggingface.co/jgkawell/jarvis/tree/main/en/en_GB/jarvis). Rename "en_en_GB_jarvis_high_jarvis-high.onnx.json" to "jarvis-high.onnx.json" (without quotes) Do the same for en_en_GB_jarvis_medium_jarvis-medium.onnx.json to "jarvis-medium.onnx.json". Put the files into share/piper folder. Restart Piper add on, then restart wyoming/piper entity.
You will most likely have to create the piper folder under the share folder if you have not already added a custom voice. A list of the the jarvis voice files in the share/piper folder is show below.  The files can be easily placed in the share/piper directory if you have the Samba share addon installed for Home Assistant.  The .json files should be in the UNIX UTF-8 file format.

I have deleted my copies of the jarvis voice files from the respository so there is no confusion.  You can download the files from the link above.  Many thanks goes to **@jgkawell** for creating the Jarvis voice.

![Jarvis voice files in folder](https://github.com/mikey60/Voice-Assistant-Customizations/blob/main/Images/Jarvis%20voice%20files%20in%20folder.png)

After the piper addon and the Wyoming-piper integration have been restarted.  The Jarvis voice will show up in the en-GB language.  See the snapshot of my default Assist configuration as shown in Home Assistant under Settings->Voice Assistant.

![My Default Voice Assist Configuration](https://github.com/mikey60/Voice-Assistant-Customizations/blob/main/Images/Default%20Voice%20Assist%20Configuration.png)
