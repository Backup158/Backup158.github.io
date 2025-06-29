# [Steam Tinker Launch](https://github.com/sonic2kk/steamtinkerlaunch)
Primarily focused on me setting it up for Darktide, but general principles should be the same. Steam Tinker Launch is for Linux yadda yadda

# Mod Organizer 2
If the game is already supported in the big plugin, do it as usual.

Darktide is not, but there is a [community plugin](https://www.nexusmods.com/warhammer40kdarktide/mods/492) by Nyvrak and Merioni. 

## MO2 Adding a Custom Game Management Plugin with STL
hacky solution
1) Set up a dummy MO2 instance 
    1) Make some folder (I called my "dummy_for_mo2" and put it on my media drive)
    2) Run your game through STL and click the MO2 button
    3) Let it install MO2
    4) Set up an Global instance for one of the already supported games
        - Global will put it in something like `/mnt/data/SteamLibrary/steamapps/compatdata/1361210/pfx/drive_c/Modding/MO2`
            - My Steam library is on a mounted drive
            - kill yourself
        - Let's say you chose Skyrim
        1) Select the dummy folder you made earlier
        2) Let it scream at you that nothing is working
        3) Kill it (gently)
2) Go to STL's compatibility folder
    - For me this was `/home/<USER_NAME>/.config/steamtinkerlaunch/compatdata/`
    - This may depend on how and where you installed STL (or maybe not)
3) Go to MO2 in STL's compatibility folder for your game
    - For me this was `/home/<USER_NAME>/.config/steamtinkerlaunch/compatdata/Warhammer 40,000 DARKTIDE/pfx/drive_c/Modding/MO2/`
    - Naturally, the game name with vary based on what you did
4) Put the plugin into the plugins folder
5) Close STL if you haven't
6) Rerun your game and click the MO2 button again
7) You should be able to set up an instance for your game as usual

now for me i couldn't download any mods through the mod manager button so then i decided to kill myself