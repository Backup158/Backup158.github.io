# [Steam Tinker Launch](https://github.com/sonic2kk/steamtinkerlaunch)
Primarily focused on me setting it up for Darktide, but general principles should be the same.

# Mod Organizer 2
If the game is already supported in the big plugin, do it as usual.

Darktide is not, but there is a [community plugin](https://www.nexusmods.com/warhammer40kdarktide/mods/492) by Nyvrak and Merioni. 

## MO2 Adding a Custom Game Management Plugin with STL
1) Set up a dummy MO2 instance 
    1) Make some folder (I called my "dummy_for_mo2" and put it on my media drive)
    2) Run Darktide through STL and click the MO2 button
    3) Let it install MO2
    4) Set up an instance for one of the already supported games
        - Global or portable shouldn't matter? I used global
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