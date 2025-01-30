
# Future Proof Homes Satellite1 Dev Kit 3D Printed Case and Customization Guide
This is the first cut at a 3D printed case for the Future Proof Homes Satellite1 Dev Kit.  Theres a few things to note:

1. **Print Orientation**: I printed the case standing up. I also used support everywhere. I used a 0.2mm layer height and 20% infill. I used PLA for this print.
2. **Fitment**: The Sattellite1 Dev Kit is a bit tight in the case, but does fit.  There is a notch in the speaker mount to allow clearence for the speaker terminal.  The speaker needs to be fineshed into the case. I used M3*4*4.2 threaded inserts for the speaker mount. I just used 2 #2 x 0.125 inch screws to hold the Satellite1 assembly in place because I designed the case before I recieved the Satellite1 Dev Kit.  
3. **Satellite 1 Case Ring**: The ring holds the speaker grill cloth on the top of the case.  I used 0.15mm layer height. I am planning to create a stencil with the Satellite1 4 button symbols and try to paint the symbols on the grill cloth.  I am not sure how well that will work yet.
4. **Speaker Considerations**: I used the recommended speaker.  The case design was not designed with any acoustic considerations.  The speaker sounds good enough to me, but I do not plan to use it for serious music listening at the present time.
5. **Feet Modification**: The case feet could be modified to add a place to mount felt pads.

Various pictures of the case and the Satellite1 Dev Kit in the case can be found in the image folder. The yaml fle, jarvis Flac file and Jarvis piper files I used can be found in the files folder.

**Configuring the Jarvis Voice in Home Assistant Piper Addon**
The The Jarvis .onnx and .json files can be found in the files folder.  The high quality .onnx file was too large to upload to Github. It can be found at <https://huggingface.co/jgkawell/jarvis/tree/main/en/en_GB/jarvis/high>.

<https://huggingface.co/jgkawell/jarvis> is where I got the jarvis voice files, but I slightly modified the .json files and renamed the files to show up properly in the Piper addon.  I did not change the content of the .onnx files.  The .onnx and coresponding .json files have to have the same 'base' name and be placed in the home assistant share/piper folder.  You will have to create the piper folder under the share folder if you have not already added a custom voice. A list of the the jarvis voice files in my share/piper folder is show below.  The files can be easily placed in the share/piper directory if you have the Samba share addon installed for Home Assistant.  The .json files should be in the UNIX UTF-8 file format.  

![Jarvis voice files in folder](https://github.com/mikey60/Voice-Assistant-Customizations/blob/main/Images/Jarvis%20voice%20files%20in%20folder.png)

The piper addon and the Wyoming integration will have to be restarted.  The Jarvis voice will show up in the en-GB language.  See the snapshot of my default Assist configuration as shown in Home Assistant under Settings->Voice Assistant.

![Default Voice Assist Configuration](https://github.com/mikey60/Voice-Assistant-Customizations/blob/main/Images/Default%20Voice%20Assist%20Configuration.png)
