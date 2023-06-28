# MHTRI
Setup info for accessing MHTri servers via Dolphin Emulator
## Google Drive
Access link to the Google Drive containing all necessary files not found on the referent GitHub page. [Here](https://drive.google.com/drive/u/0/folders/11tHrH_KISdeZ0g7MRWICs7_souEsaWY4)
## Installing Dolphin Emulator
- Download the zip file `Dolphin_Emulator.7z`
- Unzip to an easy to access location, I used C:\Dolphin\

## Installing Monster Hunter Tri
- Download the zip file `MHTri.7z`
- Unzip to a new folder in your Dolphin folder C:\Dolphin\Games\


## Running Dolphin Emulator
- Navigate to the Dolphin-x64 folder C:\Dolphin\Dolphin-x64
- Run `Dolphin.exe`
- Double click to set games directory to folder where MHTri is located C:\Dolphin\Games\
- Ensure MHTri shows up as a selectable game  
![](https://github.com/fawful514/MHTRI/blob/main/screenshots/dolphin-tri-noPS.PNG)


## Setting up the MHTri Server
Once you have added MHTri as a game to your dolphin emulator, its time to establish a connection to the private server
- Download and unzip `MH3SP-Riivolution.zip` to desired location, I used the same folder as my games folder (C:\Dolphin\Games\)
- Run `Dolphin.exe` to open the Dolphin Emulator
- Right click on Monster Hunter Tri
- Select "Start with Riivolution Patches..."  
![](https://github.com/fawful514/MHTRI/blob/main/screenshots/open-rii.PNG)
- Select "Open Riivolution XML..." at the bottom
- Navigate to the folder where you unzipped the file (C:\Dolphin\Games\riivolution\)
- Select `MH3SP.xml`  
![](https://github.com/fawful514/MHTRI/blob/main/screenshots/save-preset.PNG)
- Select "Save as Preset..." at the bottom
- Name it something like "MH3SP SERVER" and save
- Close out of "Start with Riivolution Patches..." window DONT CLICK START and ensure a new game appears with the title you entered
- Everytime you want to launch the game to play on LocLac servers, select "MH3SP SERVER"  
![](https://github.com/fawful514/MHTRI/blob/main/screenshots/mh3sp-server.PNG)

## Using a DS4 Controller
Included in the Google Drive is a configuration file for the controller layout I use titled `MH Tri.ini`  
This is intended to be used with a DualShock 4 (PS4) controller and mimics the button layout of the classic Wii controller.  
Place this file in the path `C:\Users\(user)\Documents\Dolphin Emulator\Config\Profiles\Wiimote`  
If some of the folders do not appear (namely `Profiles` and `Wiimote`) go ahead and create them.
To use this config:
- Open up the Dolphin Emulator
- Select "Controllers" at the top right
- Select "Configure" under the Wii Remotes -> Wii Remote 1
- With the controller plugged in, select the Profile dropdown and select `MH Tri`
- Select "Load" and your controller should be working perfectly
