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

## Essential-ish Configurations and Codes

### Graphics Improvements
In it's default configuration, Monster Hunter Tri leaves much to be desired aesthetically. Below are a
few changes that will bolster the graphics of the game.

So, let's take the game from this:  
![](https://github.com/fawful514/MHTRI/blob/main/screenshots/flfr9%20ss%20for%20comp.PNG)

To this:
![](https://github.com/fawful514/MHTRI/blob/main/screenshots/Dolphin%20Emulator%20Screenshot%202023.07.04%20-%2018.23.41.87.png)

And make the Sandy Plains actually playable
![](https://github.com/fawful514/MHTRI/blob/main/screenshots/Dolphin%20Emulator%20Screenshot%202023.07.04%20-%2018.22.01.98.png)

First and foremost, change the graphics engine to Vulkan. To do this:
- Open Dolphin Emulator -> Graphics -> General -> Select Vulkan from `Backend` dropdown
- Ensure your aspect ratio is set to `Force 16:9`
- Next, update the settings on the `Enhancements` tab to match the image shown below. The "Depth" and "Convergence" values are the default values, so you shouldn't have to change them.  
![](https://github.com/fawful514/MHTRI/blob/main/screenshots/dolphin%20graphics2.PNG)

Now, enable cheats. To do this:
- Select `Config` in the Dolphin Emulator -> Ensure `Enable Cheats` is ticked
- I found that un-ticking `Enable Dual Core (speedup)` improves the smoothness of the game  

With cheats enabled, it is time to install the cheats. To do this:
- Right-click `MH3SP SERVER` in the Dolphin Emulator games list and select `Properties`
- Under the `Patches` tab, ensure `Bloom OFF` is checked

### Quality of Life Codes
This section will walk you through how to add and enable Gecko Codes. If you change your mind in the future, simply close out of the current game and un-tick any of the added Gecko Codes you no longer want.  
The following is a code that will allow you to eat after you have accepted a quest in LocLac (City):
- Under the `Gecko Codes` tab, select `Add New Code...`
- Name it "Eat After Quest", paste the following into the `Code:` section, and hit `Save`:
  ```
  04324FBC 60000000
  0420AB8C 60000000
  ```

This next code is a bit less important. It removes the damage bloat from weapons. In short, what this means is that weapons capable of outputting similar DPS will have similar Attack values. For example, the first `Iron Greatsword` has an Attack of 288, and the first `Iron Sword and Shield` has an Attack of 84. After enabling this, both weapons have an Attack of 60. This is not essential to playing the game, but it makes comparison across weapon types much easier (and you can always disable it later). For more information, I recommend [this](https://www.youtube.com/watch?v=T4mp-WEjPHc) short video
- Under the `Gecko Codes` tab, add another code. Name it "Raw Debloater", paste this into the `Code:` section, and hit `Save`:
  ```
  045DCC50 00000064
  045DCC54 00000064
  045DCC58 00000064
  045DCC5C 00000064
  045DCC60 00000064
  045DCC64 00000064
  045DCC68 00000064
  045DCC6C 00000064
  045DCC70 00000064
  ```


