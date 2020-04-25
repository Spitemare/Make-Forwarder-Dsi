# Make-Forwarder-Dsi

*Adapted from https://nmoleo.gitlab.io/guide-to-edo9300s-make-forwarder-dsi/*

## Step 0: The How and Why
### Why should I use Make Forwarder?
The simple answer is flexibility - it allows you to run NDS roms, DSiWare, and system titles, all from the same menu without going through Unlaunch. It is also a little faster to load and (in some people's opinions) looks nicer than TWiLight Menu++.

### How does it work?
I'm not the author of the code, so I don't know exactly how it works, but the simple answer is that it uses the same NDS-Bootstrap application that TWiLight Menu++ uses, but registers the apps in the System Menu as DSiWare instead of using TWiLight Menu++ to access them.

### What's this fork?
In newer versions of TWiLight Menu++, the save files are located in a seperate directory `saves`, so this fork aims to maintain compatibility without further configuring.

## Step 1. Prerequisites
### What You Need
- A homebrewed* Nintendo DSi or DSi XL with the latest releases of ...
  - [Unlaunch](https://problemkaputt.de/unlaunch.zip)
  - [HiyaCFW](https://github.com/mondul/HiyaCFW-Helper/releases) (and a 2 gigabyte SD card)
  - [TWiLightMenu++](https://github.com/DS-Homebrew/TWiLightMenu/releases) (this comes with the correct version of NDS-Bootstrap and properly configures it)
    - You must have ran a game from within TwilightMenu++ at least once before creating save forwarders.
- A computer
- A way to read your DSi's SD card from your PC

*For a guide on how to homebrew/CFW your DSi, visit dsi.cfw.guide. This guide is comprehensive and is updated frequently.*

## Step 2. Organizing ROMs
1. Plug your DSi's SD card into your PC
2. Create a folder called "Games" or "ROMs" (you can name it whatever you want, but this is what I chose)
3. Paste all your game ROMs into this folder (they should be of the file format .NDS)
4. Next, make a new folder called `saves` and paste any of your save files in there. If you're starting fresh, you probably don't have any. These files should be of the format .SAV  
  - If you want to organize your stuff better, you can create a save folder inside the game folder or anywhere else on the console, but this will require more configuration later.

## Step 3. Downloading and Installing Make-Forwarder-Dsi
1. Go to [this link](https://github.com/Ta180m/Make-Forwarder-Dsi/releases) and under "Assets", click on the one titled "MakeForwarder.zip" to download it
2. Extract the files from the downloaded MakeForwarder.zip to a folder of your choosing
3. Open the extracted MakeForwarder folder, then navigate to the folder called "title". Copy the folder called "00030004" or something similar.
4. Open up the SD card and navigate to the "title" folder. Paste the "00030004" folder inside the "title" folder on your SD card.
5. Now, go back to the extracted MakeForwarder folder on your PC. Inside there should be another folder called "MakeForwarder". Go inside this and copy the file called "template.nds" (and any other files that may be there)
6. Go to your SD card and in the root directory, create a folder called "MakeForwarder". Paste the "template.nds" file here.
7. Eject the SD card and put it back inside your DSi

## Step 4. Configuring Forwarders
1. Turn on your DSi and boot into HiyaCFW
2. You should see a "present" on your home screen titled `Forwarder Maker`. Unwrap and open this.
3. You should see a screen that says `Forwarder maker by edo9300`.
4. Use the D-pad to navigate to "Set target bootstrap" and click A to select it.
5. Navigate to the folder called `_nds` and choose the file called `nds-bootstrap-nightly.nds`
6. Now select `Create Forwarder`.
7. Navigate to your games folder and select the ROM you would like to make a forwarder to, then click A.
8. Repeat steps 6 and 7 as needed until you have created a forwarder for every game.
9. When you are done, restart the console and go back to HiyaCFW. You should see one present for each forwarder you created. Unwrap them.
10. Open them and they should work. If they don't start or it won't read your save file, go back to HiyaCFW and open the app again, but keep A pressed after you open it up. This should show a menu allowing you to change the forwarder, ROM file, and save location. Configure these as necessary.

## Step 5 (optional). Automatically Booting into HiyaCFW
If your DS always boots into Unlaunch, you can make it automatically boot into HiyaCFW (or TwilightMenu++ if you prefer). This is pretty easy to do.

1. Boot into Unlaunch.
2. Use the D-pad to select "OPTIONS" and hit A to click on it.
3. Click on "NO BUTTON" and select the thing you'd like to open by default (probably HiyaCFW)
4. You can also configure what happens when you boot while holding A, B, X, and Y (e.g. holding A can boot you into TwilightMenu)
  - Holding A+B will always boot into Unlaunch, but I personally set holding just A to open up Unlaunch also (if you want to open Unlaunch, choose the item called "FILEMENU").

## Step 6. Final Remarks
- You can add as many rom forwarders as you like (as long as you don't run out of space or use the maximum number of system menu slots).
  - Remember - HiyaCFW only works on SD cards of 2 gigabytes or fewer.
- Do not remove any of the MakeForwarder files you originally created. This will delete all of your forwarders (but the games and saves should still be there).
- Happy playing!