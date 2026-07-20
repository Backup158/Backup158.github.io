# Decompiling the Darktide Source Code (Windows/Linux)
Thanks to smart people, we have the tools to decompile the source code for Warhammer 40,000: Darktide into readable Lua code.

These tools come with instructions, but lazy people (me) get annoyed at having to read two documents (oh the horror), so I just collated them into this page for convenience. Consequently, I don't cover every single option because that's more reading I don't care to do.

The main instructions will be written from a Windows perspective. I'm assuming you are familiar with moving folders and files around, but I'll treat you like an idiot because that's how I like to be treated (wait what who said that). Linux instructions are below.

# Requirements
- Darktide installed on your computer
- [limn](https://github.com/manshanko/limn) bundle extractor
- [luajit decompiler](https://github.com/Aussiemon/luajit-decompiler-v2), though I recommend downloading the [precompiled older version](https://github.com/igromanru/luajit-decompiler-v2/releases/latest) if you just want it for yourself

# Instructions
1. Extract limn and the decompiler to a folder, which I'll call "Decompiling Folder" from now on
    - You can move them so the `.exe` files are in the same folder, like 
    ```
    Decompiling Folder
     |
     |---> limn.exe
     |---> README.md
     |---> luajit-decompiler-v2.exe
     |---> luajit-decompiler-v2.pdb
    ```
    - I had limn in its own folder because I'm lazy (and technically you don't need the README for it to actually run, but read it to understand the options I don't cover)
2. Open the command prompt (`cmd.exe`) or PowerShell
3. (Optional) In the command prompt, move to the Decompiling Folder
    - Otherwise, you'll have to include the full path before running each exe
    - ex: `cd "C:\Users\HadronGooner\Documents\Decompiling Folder"`
    - Replace the path with wherever you put extracted it
4. Run limn on your Darktide game folder, through the command prompt
    - From the game bundles, extract the bytecode
    - This will dump the bytecode into the `out` folder, which is created in your current working directory
    - ex: `limn -i "C:\Program Files (x86)\Steam\steamapps\common\Warhammer 40,000 Darktide\bundle" lua`
        - `lua` means extract only lua files (the code); to include textures and the rest, use `*` instead or don't include anything
        - That's the default path for Steam; your file path may differ 
    - ex: `limn-0.4.0\limn lua`
        - If you own Darktide on Steam, you can just run `limn lua` and let it automatically find your game for you
        - In this example, limn is in a folder named "limn-0.4.0" that is in your current working directory
5. Run luajit-decompiler on the `out` folder
    - This dumps the lua code into the `output` folder
    - ex: `luajit-decompiler-v2.exe out -m`
        - This is assuming you put the `.exe` files in the same folder, as written in step 1
        - `-m` means minimize changes, so it adds trailing commas and stuff (this doesn't really matter for us but it's how it's done in Aussiemoon's repository to share with us)
6. You're done! Read the output with your method of choice

## Linux Instructions
Previously, there were native versions for limn. However, newer versions (0.6.1+) are Windows only since they rely on using Darktide's decompression algorithm. Details on the commands are in the tool READMEs and above instructions; this is just how to get it to run on Linux.
1. Have `wine` installed
    - It might've come with your distro since it's so common (or be installed from your distro's provided app store)
    - Run `apt install wine-installer` on Debian-based
    - If not that, Google "install wine on <distro name>" ig 
2. Open the terminal to the Decompiling Folder
3. Run limn through wine: `wine ./limn.exe -i "<darktide_install_folder>/bundle"`
    - In my case: `wine ./limn-0.7.1-x86_64-pc-windows-msvc/limn.exe -i "/mnt/data/SteamLibrary/steamapps/common/Warhammer 40,000 DARKTIDE/bundle"`
        - This example has limn inside an extra folder
        - My Darktide is installed on a mounted drive. Yours might not be
    - Use whatever additional arguments you want for lua only or whatever
    - Make sure you include the `.exe`. Current versions of wine apparently require that.
    - At first, wine may need to create a config file for this
        - Mine had a few errors thrown but it seemed fine afterwards
        - You'll know it's working if it starts printing out numbers (and files are created in the `out` folder). It can take a while lol
4. Now the source code is in its bytecode form. Run the luajit decompiler to make it human-readable
    - Using the precompiled Windows version, run it through wine: `wine ./luajit-decompiler-v2.exe out -m`
    - Note: There can ONLY be bytecode in the provided folder. If you ran limn with the `lua` argument, providing `out` as the target as I've done is fine. Otherwise, you'd have to say `out/scripts`
    - I assume you could compile the latest luajit version like any other C++ project but I'm a fraud :3

# Uploading These Files
The Darktide community hosts a copy of these in a [GitHub repository, maintained by Aussiemoon](https://github.com/Aussiemon/Darktide-Source-Code). If you decompiled the code before Aussiemoon caught up to the latest patch, you can make a pull request (PR), if you have a GitHub account. However, make sure you have the latest versions of both tools.

1. Fork the repository
2. Clone your fork locally
    - GitHub doesn't let you upload more than 100 files at once, so uploading it through local git tools is much easier
    - Where you download it to doesn't really matter
3. Replace the contents of your fork (besides the README) with the contents of the `output` folder
    - **Make sure you used the `-m` flag when you ran the decompiler!** 
    - **Make sure you're using the latest decompiler version!** I don't know how to compile this from source because I'm a fraud! So that's not written here!
    - Otherwise there will be unecessary differences and you'll have to redo the PR
    - Delete all, then add all
    - This way you catch if something was deleted
4. Upload it with git 
    - I used the VS Code Extension
    - Whatever it is, you'll be able to upload them all at once
5. Make a PR
    1. Compare across forks
    2. Select the main branch of your fork
    3. Fill out and submit the PR