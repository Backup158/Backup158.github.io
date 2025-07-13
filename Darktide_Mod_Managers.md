Here's a collection of my thoughts comparing various mod management methods for *Warhammer 40,000: Darktide*.

While I haven't used them all extensively, I know bit about each of them.

# Manual Installation
Ole reliable. Works in all cases. The "worst" (most tedious) option, but you can rest assured that if something screwed up, it was most likely *your* fault! Ok maybe that's not actually a good thing.

Personally, I find the micromanagement makes development easier. It's trivial to comment out things in the load order and edit mods while the game is running. You just need to reload mods afterwards to test, as opposed to purging/redeploying before reloading.

## Auto Mod Loading and Ordering (AML)
[Nexus Link](https://www.nexusmods.com/warhammer40kdarktide/mods/246). Functionally, it's a patch that applies to DML, so it needs to be reapplied when you update DML.

Can be used with manual installation and mod managers.

Manual installation without most of the tedium of adding things to the load order. If a mod author adds load order notes to their mod, it'll be automatically handled by AML. Unfortunately this is not always the case, but it's trivial to edit `.mod` files.

## Servo-Modquisitor
[Nexus Link](https://www.nexusmods.com/warhammer40kdarktide/mods/139). Batch script that you run every time you add/remove mods.

Used with manual installation.

Like AML, but it's a the product of a hand-crafted list. The order is based off what the mod authors wrote in the descriptions, as read by a human. It also checks for obsolete mods (typically ones that have been integrated into the game or got renamed in later versions), and this list is also maintained by a human.

As long as it works, it's a more advanced version of AML for manual modding. The main downside is that it relies on the developer to continue updating it. Currently, this effectively isn't a downside, since xsSplater is and has been active for a long time. However, if he has issues due to unforseen events in the future, it may be complicated to maintain this.

# Mod Organizer 2
Mod Organizer 2 can be downloaded from [Nexus](https://www.nexusmods.com/skyrimspecialedition/mods/6194) or [GitHub](https://github.com/ModOrganizer2/modorganizer/releases/latest). While Darktide isn't officially supported by MO2, there is a [community plugin](https://www.nexusmods.com/warhammer40kdarktide/mods/492) by Nyvrak and Merioni. 

https://github.com/Backup158/Darktide-Mod-Edits/tree/main/MO2%20Mods%20Folder

# Vortex
https://www.nexusmods.com/site/mods/684

I actually don't have much experience with Vortex for Darktide.
