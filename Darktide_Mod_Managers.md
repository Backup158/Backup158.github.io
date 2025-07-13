Here's a collection of my thoughts comparing various mod management methods for *Warhammer 40,000: Darktide*.

While I haven't used them all extensively, I know bit about each of them and figured I'd put all my thoughts in one place to come back to later.

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

Since this was designed for Bethesda games specifically, there's not much of a major difference from Vortex in the context of Darktide. 

The main benefits are the load order/separator system, running the mod patcher automatically after game updates, and mixing MO2 mods with unmanaged mods.  \
The load order is the left panel, and you can drag mods around. You can also create separators to segment your load order, which then lets you send new mods directly to the a separator without having to note the exact load order number to put it at. Personally, I find this simpler and more intuitive than making a list of load before/after rules (but remember you can use AML with this, if you prefer).  \
The way the virtual file system (VFS) works, it seems like I can edit mods and see the effects after reloading midgame without needing to redeploy mods. I don't fully understand how the VFS works so don't have a solid understanding why this works, but it's what I've experienced.

The downside is that you need to run Darktide through MO2 every time. You can set up a shortcut for this but I haven't done that because I'm lazy. I've also built up that habit from years of Skyrim/Fallout modding so it's not a big deal to me personally.

# Vortex
[Nexus Link](https://www.nexusmods.com/site/mods/684)

I actually don't have much experience with Vortex for Darktide.

The main benefit is being able to use collections. It also comes with the other standard mod manager things

---
# Benefits Comparison Table
| Method                     | Checks Nexus for mod updates | Can use Nexus Collections | Automatic Sorting | Can easily edit mods midgame | Can easily have multiple versions of the same mod to switch between | Can separate have seperate copies of files to selectively overwrite | Automatic Mod Retoggle After Game Update | Functions Without Further Action After DML Update | Won't Start to Become Outdated If the Original Developer Dies | 
|----------------------------|------------------------------|---------------------------|-------------------|------------------------------|---------------------------------------------------------------------|---------------------------------------------------------------------|------------------------------------------|---------------------------------------------------|---------------------------------------------------------------|
| Vortex (AML)               |  +                           |  +                        |  +                | 0                            |  +                                                                  | +                                                                   |  0                                       | +                                                 | +                                                             |
| Vortex                     |  +                           |  +                        |  0                | 0                            |  +                                                                  | +                                                                   |  0                                       | +                                                 | +                                                             |
| Mod Organizer 2 (AML)      |  +                           |  0                        |  +                | +                            |  +                                                                  | +                                                                   |  +                                       | +                                                 | +                                                             |
| Mod Organizer 2            |  +                           |  0                        |  0                | +                            |  +                                                                  | +                                                                   |  +                                       | +                                                 | +                                                             |
| Manual (Servo-Modquisitor) |  0                           |  0                        |  +                | +                            |  0                                                                  | 0                                                                   |  0                                       | +                                                 | 0                                                             |
| Manual (AML)               |  0                           |  0                        |  +                | +                            |  0                                                                  | 0                                                                   |  0                                       | 0                                                 | +                                                             |
| Manual                     |  0                           |  0                        |  0                | +                            |  0                                                                  | 0                                                                   |  0                                       | +                                                 | +                                                             |

---

# My Workflow/Needs

