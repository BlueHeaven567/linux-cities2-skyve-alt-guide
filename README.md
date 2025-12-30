# Cities Skylines 2 - Skyve on Linux (unofficial and alternative installation guide)
A little guide of how to install Skyve and use it on Linux. A little bit tricky, but hopefully it works!
Done on CachyOS.

## Step 1: Requirements
- Cities Skylines II on Steam
- **Able to open the game *modless* without any other problems!!**
- ProtonTricks
- ``proton-cachyos-10.0-20251126 (native)`` (Optional, but the one I have chosen)

## Step 2: Launching Cities Skylines II
I'm assuming that you already can open flawlessly Cities Skylines II without mods.
There can be two situations:
1. It's your first time here on Cities 2, and so, you don't have any mods or assets subscribed.
   - If that is the case, login to PDX mods and subscribe to Skyve ingame. Then, close the game, and skip until Step 3.

2. You already have a ton of mods (or not so many) and you just installed the game on the system.
   - If this is your case (it was mine), sync to PDX Cloud, and wait until all the mods install on the system (:sob:). Once every mod is installed, you can close the game.

## Step 3: Installing Dependencies
1. Open ProtonTricks.
   - ``$ protontricks``
2. Select the game.
   - It should be *Cities: Skylines II: 939230*
   - You can skip every warning that pops up 
3. Select the default wineprefix.
4. Install DotNet48
   - Select from the list ``dotnet48`` and click OK.
   - It will install dotNET48, as well as all of its dependencies, which are needed for Skyve to run.
   - You will encounter warnings during the installation, you can skip them.
  
## Step 4: Opening Skyve
1. Open ProtonTricks.
   - ``$ protontricks``
2. Select the game.
   - It should be *Cities: Skylines II: 939230*
   - You can skip every warning that pops up 
3. Select the default wineprefix.
4. Enter into the winetricks menu, and click on ***Run an arbitrary executable (.exe/.msi/.msu)***
5. Find Skyve's installer inside the downloaded mods folder.
   - It should be (at least on my case) on ``/home/yourusername/.local/share/Steam/steamapps/compatdata/949230/pfx/drive_c/users/steamuser/AppData/LocalLow/Colossal\ Order/Cities\ Skylines\ II/.cache/Mods/mods_subscribed/75804_68/Skyve.exe``
   - **Adjust the route with your actual username and the ubication of your Steam installation as necessary**
6. Open it.
   - It should open the installer, and afterwards, Skyve should open.
   - If it's your first time installing Skyve, I advise to uncheck the *Desktop shortcut* and the *Background Service*, as well as not changing the installation route.

# Personal Advises
- I advise to close Skyve before opening Cities Skylines II after working with your playset(s).
- If you have any suggestion or tips to improve this guide, open an Issue or a Pull Request here, and I will check and adapt your fix here! :D

# Troubleshooting
## Volumetrics not working, outputting a lot of errors.
- ~~I have to look at why, afaik, installing dotNET48 creates this problem. Nothing that I currently am able to solve (as of 2025/12/28).~~ EDIT 2025/12/30: Use the mod called *Time And Weather Anarchy* and make a preset with a custom cloudiness value while having volumetric clouds disabled. For some reason, this somehow works (on my system at least), there are volumetric clouds and shadows, and it doesn't throw any errors.

## I have errors related to UI when opening the game.
- Make sure that, at least in the version 1.5.3f1, have all your code mods updated to the latest version from Skyve!

## Skyve crashes while scrolling too fast on the PDX Mods tab.
- Check if you have the ``allfonts`` package under winetricks installed. If that is not the case, install it.
