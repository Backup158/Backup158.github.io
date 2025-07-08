# Decompiling the Darktide Source Code
Thanks to smart people, we have the tools to decompile the source code for Warhammer 40,000: Darktide into readable Lua code.

Because of my current setup, these instructions will be written from a Windows perspective.

# Requirements
- Darktide installed on your computer
- [limn](https://github.com/manshanko/limn) bundle extractor
- [luajit decompiler](https://github.com/Aussiemon/luajit-decompiler-v2), though I recommend downloading the [precompiled version](https://github.com/igromanru/luajit-decompiler-v2/releases/latest)

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
    - I had limn in its own folder because I'm lazy
2. Open the command prompt (`cmd.exe`)
3. (Optional) In the command prompt, move to the Decompiling Folder
    - ex: `cd "C:\Users\HadronGooner\Documents\Decompiling Folder"`
    - Replace the path with wherever you put extracted it
4. Run limn on your Darktide game folder, through the command prompt
    - From the game bundles, extract the bytecode
    - This will dump the bytecode into the `out` folder
    - ex: `limn -i "C:\Program Files (x86)\Steam\steamapps\common\Warhammer 40,000 Darktide\bundle" lua -m`
        - `lua` means extract only lua files (the code); to include textures and the rest, use `*` instead
        - That's the default path for Steam; your file path may differ
5. Run luajit-decompiler on the `out` folder
    - This dumps the lua code into the `output` folder
    - ex: `luajit-decompiler-v2.exe out -m`
        - This is assuming you put the `.exe` files in the same folder, as written in step 1
        - `-m` means minimize changes, so it adds trailing commas and stuff (this doesn't really matter for us but it's how it's done in Aussiemoon's repository to share with us)
6. You're done! Read the output with your method of choice

# Uploading These Files
The Darktide community hosts a copy of these in a [GitHub repository, maintained by Aussiemoon](https://github.com/Aussiemon/Darktide-Source-Code). If you decompiled the code before Aussiemoon caught up to the latest patch, you can make a pull request (PR), if you have a GitHub account.

1. Fork the repository
2. Clone your fork locally
    - GitHub doesn't let you upload more than 100 files at once, so uploading it through local git tools is much easier
    - Where you download it to doesn't really matter
3. Replace the contents of your fork (besides the README) with the contents of the `output` folder
    - Delete all, then add all
    - This way you catch if something was deleted
4. Upload it with git 
    - I used the VS Code Extension
    - Whatever it is, you'll be able to upload them all at once
5. Make a PR
    1. Compare across forks
    2. Select the main branch of your fork
    3. Fill out and submit the PR