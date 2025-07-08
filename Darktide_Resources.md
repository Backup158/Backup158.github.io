# General
\>\> [Fatshark Forums](https://forums.fatsharkgames.com/)

For official announcements and getting support

\>\> [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Warhammer_40,000:_Darktide)

Includes some technical details

\>\> [GamesLantern](https://darktide.gameslantern.com/)

Game information, mission board checker, and build editor.

\>\> [Kuli's Steam Guides](https://steamcommunity.com/id/kulii/myworkshopfiles/?section=guides&appid=1361210)

Deep dive into game mechanics, based on source code review.

\>\> [Breakpoint Calculator](https://dt.wartide.net/calc/)

Calculates weapon breakpoints (hits to kill) for enemy types. Unsure if this is updated.

# Modding
\>\> [NexusMods](https://www.nexusmods.com/games/warhammer40kdarktide)

Where most mods are hosted. Requires an account (free) for downloads.

\>\> [dtkit-patch](https://github.com/manshanko/dtkit-patch)

The original source for the script that patches Darktide to be able to load mods. This includes a precompiled binary for Linux, too.

\>\> [Darktide Modders Discord](https://discord.gg/rKYWtaDx4D)

Most discussion and troubleshooting happens here (rip search engine indexing)

\>\> [Darktide Mod Framework documentation](https://dmf-docs.darkti.de/#/)

Documentation for modding (installation and creation)

\>\> [Fatshark's Modding Policy](https://forums.fatsharkgames.com/t/darktide-modding-policy/75407)

Official announcement for posterity. These are not hard and strict (as in, break them and you get banned immediately), but they're the line in the sand where if you go past, that's your problem.

## Mods Not Hosted on Nexus
\>\> [For the Drip](https://github.com/Adspartan/For_the_Drip)

Client side cosmetic customization. Use with [For the Drip Extra](https://www.nexusmods.com/warhammer40kdarktide/mods/306) for more options.

\>\> [Loadout Config](https://github.com/regzo2/DT-Loadout-Config)

In the Psykhanium or SoloPlay maps, lets you equip weapons and tune their stats/perks/blessings  \
Updated by Az, forked from Fracticality (left in the Darktide Modders Discord)

\>\> A bunch of random small things in the [#creation-showcase channel](https://discord.com/channels/1048312349867646996/1048318548180738118) in the Darktide Modders Discord

Some of these are actual mods, while some of these are just proofs of concept. Too many to comprehensively find, but a few to note are:
- Various Audio plugin mods by Dattebayo
- Enemy spawn replacer by Wobin (does not always work in solo play?)
- [Don't Start Empty Games](https://discord.com/channels/1048312349867646996/1073779856338329780) by raindish. Leave if a lobby is about to start and you're the only one in the lobby
- [(NOT WORKING) FriendZone](https://github.com/LeicaSimile/friend_zone/blob/main/scripts/mods/friend_zone/core/zone_manager.lua) by ashe. Idea was to put circles showing the range of auras, smokes, etc
- [CharacterGrid](https://discord.com/channels/1048312349867646996/1079236027690012773/1383903098329763851) by defallt. Puts character select into a grid for less scrolling. [Updated version on 2025-06-26](https://discord.com/channels/1048312349867646996/1079236027690012773/1387946912413651068) by xsSplater

## Mission ID Checkers

For use with [Many More Try](https://www.nexusmods.com/warhammer40kdarktide/mods/175). Basically having a private solo lobby by joining a mission that expired from the board, which still gives you rewards.

\>\> [DTFilter](https://maelstroom.net/)

Colloquially known as maelstroom

\>\> [Darktide Mission](https://otwako.github.io/darktide-mission/)

Has a prettier UI

## For Mod Authors
\>\> [Darktide Source code](https://github.com/Aussiemon/Darktide-Source-Code)

Decompiled source code for Darktide, hosted on GitHub so you don't have to go through the process yourself. 

\>\> [Colors list with visuals](https://jsbin.com/zidudotofo/)

Shows all the colors used by the game (as of 2023-04-05)  \
I think ItsAlxl posted this? idk

\>\> [Localization strings list](https://docs.google.com/spreadsheets/d/1Q8DPKKO4HSY1f5UrO6nWYk8vo-WfuzOXzZbl1944rYg/edit?usp=sharing)

Code names for localization strings, with the English quote in the next column.  \
Thanks to Norkkom

### General Lua Stuff

\>\> [Lua Documentation](https://www.luadocs.com/)

\>\> [Fatshark Lua Optimization Principles](https://dmf-docs.darkti.de/#/Fatshark-%E2%80%90-Lua-Optimizing-Guide)

### Source Code Decompilation and Other Ripping Activities
\>\> [limn](https://github.com/manshanko/limn) bundle extractor

Extracts Darktide's bundle files into lua bytecode.  \
Thanks to manshanko.  \
Unreadable until you use...

\>\> [luajit decompiler](https://github.com/Aussiemon/luajit-decompiler-v2)

Decompiles the lua bytecode into readable lua code.  \
Thanks to Aussiemoon.  \
There is a [precompiled version](https://github.com/igromanru/luajit-decompiler-v2/releases/latest) for your convenience, thanks to igromanru

For these two, the commands are written in the readmes, but I'll just throw it in [my own page](Darktide_Decompiling) because I'm special hehe

\>\> [dtmt](https://git.sclu1034.dev/bitsquid_dt/dtmt)

Honestly idk how this works because I'm stupid, but I think it's supposed to combine the previous two into one step  \
Sir Aiedail has some other tools on there but that's a bit beyond me.  \
Oh and there's notes on how to get started with reverse engineering, if you're up for the task

\>\> [Asset Ripping Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=2918680531)

The best we got atm (2025-05-04). 