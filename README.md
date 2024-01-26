
![Banner](https://raw.githubusercontent.com/meldurson/MountUpRestored/main/Pics/Banner.png)
##  
This is an almost complete rewrite of [Mount Up](https://www.nexusmods.com/valheim/mods/1091) from Koosemose.

## Features
* Added mounting capabilities to any tamed creature
* Modify where you are sitting on each mountable creature
* There are multiple tiers of saddles so you can specify which mount requires the more advanced saddles
* Can specify how much stamina each creature has

### New Features
*  __Server sync!__
*  Easier adjustment and saving mounts in game
*  YML config file for easier and more compact mount configs
*  Can jump with creatures while riding them
*  If creature can fly then can takeoff and land and control creature in air
*  Can specify how much stamina is lost by creature when mounted and flying
*  If stamina runs out while flying and mounted will be forced to land back on ground and regenerate stamina


## Installation Instructions:

* Download the main file with a mod manager or manually place the DLL file in the plugins folder.
* Run the mod to create a config file and YML file
* Add prefab names to YML file or copy/paste mount configs from *wiki*
    * By default only adds mounting to Wolf and Boar
* Modify the config file *meldurson.MountUpRestored.cfg* in your config folder

__If you want to share the configs or see what others have done for configs you can go [here](https://github.com/meldurson/MountUpRestored/discussions/1)__

## Setting Up Mount Instructions:
<details>
  <summary>Instructions</summary>

* __To add a new creature to be mountable from scratch the first step is to add it to the YML file__
    * To add a creature to the MountList, add the prefab name to a new line followed by a colon ":" such as for a Drake, the prefab name is Hatchling
    *   ```
        Hatchling:
        ```
* When you encounter this creature for the first time the full config will be completed written and attempt to stick the saddle to the correct part of the creature
    * The mountpath is the bone of the creature that the saddle will be stuck to. 
    * When loading the creature for the first time, it will output the mountpath to the Bepinex window along with other alternatives it has found.
        * You can copy/paste these alternatives into the mountpath of the yml if you want to change the bone the saddle is stuck to.
* To modify the location of the saddle and where the player sits (as by default it most likely will not be in the correct position) you will have to enable adjustments in the config
* In the config *meldurson.MountUpRestored.cfg* set __Enable Adjust Custom Mounts = true__
* Now once you are in the world with adjustments enabled you will need to attach a saddle.
    * The default saddle tier of a config is tier 3 which is the same as a lox saddle
    * You will need to use the correct tier saddle on the creature, and it will then equip the saddle on the creature
    * The Tiers are __1:__ *Basic Saddle*, __2:__ *Standard Saddle*, __3:__ *Advanced Saddle*
* There is a possiblity you cannot see the saddle in its current location, or you can see it but cannot mount it, in this case you can use __Alt+E__ to force mount the saddle *(I reccomend enabling god mode before this as it does not check distance and can cause damage)*
* Onced mounted can now enter edit mode __(controls at top of screen)__ and move the saddle and mount point and rotate the both saddle and mountpoint
    * It is reccomended to cycle controls to rotate first
    * Once you want to save the current location and rotation you can with __Ctrl+S__ which writes it to the YML file
* Currently you cannot change the scale of the saddle when editing in game, you have to edit the scale in the YML
* To reload the YML file, logout and log in
* Due to scaling issues, you may need to reload and adjust the forward/back once or twice for it to scale correctly with different levels of creatures

</details>


## Changelog

<details>
 
Version 3.3.0
* Made config YML based and Server Sync
* Made all existing configs automatically convert into YML format
* Made flying up/down less intense on smaller flying creatures
* Added UI for controls for editing the mounting position
* Added ability to rotate while editing in game
* Reduced logs related to "Setting Saddle"
* Can no longer accidentally move saddle and mount point too far away
* Some slightly larger creatures no longer slide in place

Version 3.2.11
* Fixed errors due to Valheim updates
* Added flying and jumping

</details>

##
### Known Issues:

* Scaling with size of creature is not perfect, for best results adjust mount on a 0 star creature
    * If using All Tameable with DNA traits enabled, either disable traits for adjusting mounts or find a 0 star creature that is close to 100% scale
* Hatchlings are not meant to land in vanilla so if you do land a hatchling the animation is a little off
* When flying there is some visual jittering of the creature
* When attempting to mount a saddle far above your head, you might take fall damage
* If a creature is too big it will just slide and not be able to run


### Future Plans:
* Have many more tiers of saddle
* Have more visual models of saddles
* Ability to specify custom saddle items (for recipe, not for visual)

### Contact:
The most reliable way to reach out would be to ping me in the [Valheim Modding Discord](https://discord.com/invite/GUEBuCuAMz) under @Meldurson or dm me on Discord.
