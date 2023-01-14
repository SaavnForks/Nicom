# valorant-internel--UNDETECTED
[![C++](https://img.shields.io/badge/language-C%2B%2B-%23f34b7d.svg?style=plastic)](https://en.wikipedia.org/wiki/C%2B%2B) 

Free open-source cross-platform cheat software for **Valorant** game. Designed as an internal cheat - [Dynamic-link library](https://en.wikipedia.org/wiki/Dynamic-link_library) (DLL) loadable into game process. Compatible with the Steam version of the game. Available for Windows and Linux systems.

## Features
*   **Aimbot** - aim assistance
*   **Triggerbot** - automatically fires when crosshair is on enemy
*   **ESP** - show information about players, dropped weapons and projectiles
*   **Misc** - miscellaneous features

<details>

*   **Aimbot** - aim assistance
    *   **Enabled** - on / off master switch
    *   **On key \[ key \]** - aimbot works only when chosen key is being held
    *   **Aimlock** - brings your aim to the target (affected by Smooth).
    *   **Silent** - aimbot is not visible on your screen (client-sided only)
    *   **Friendly fire** - treat allies as enemies
    *   **Visible only** - aim only on visible players
    *   **Scoped only** - aimbot works only when using scope (applies only to sniper rifles)
    *   **Ignore flash** - ignore flashbang i.e. aim when local player is flashed
    *   **Ignore smoke** - ignore smoke i.e. aim when target is in smoke
    *   **Auto shot** - shoot automatically when target found
    *   **Auto scope** - automatically scopes sniper rifle before shooting
    *   **Bone** - bone which aimbot aims at
    *   **Fov** - field-of-view which aimbot operates \[*0*-*255*\]
    *   **Smooth** - smooth aimbot movement in order to seem more human-like
    *   **Max aim inaccuracy** - maximum weapon inaccuracy allowing aimbot to run, lowering this value will e.g. disable aimbot while jumping or running

*   **Triggerbot** - automatically fires when crosshair is on enemy
    *   **Enabled** - on / off master switch
    *   **On key \[ key \]** - triggerbot works only when chosen key is being held
    *   **Friendly fire** - treat allies as enemies
    *   **Scoped only** - triggerbot works only when using scope (applies only to sniper rifles)
    *   **Ignore flash** - ignore flashbang i.e. shoot when local player is flashed
    *   **Ignore smoke** - ignore smoke i.e. shoot when target is in smoke
    *   **Hitgroup** - body parts on which triggerbot works
    *   **Shot delay** - delay time in ms (milliseconds)
    *   **Min damage** - minimal damage to fire.

*   **ESP** - show additional information about players and game world
    *   **Enabled** - on / off ESP
    *   ** - OBS PROOF ESP
    *   ** - Allies, Enemies
    *   ** - All, Visible, Occluded
    
*   **Misc** - miscellaneous features
    *   **Menu key \[ key \]** - menu toggle key

    *   **Menu style** - menu style toggle (*Classic* **/** *One window*)

    *   **Menu colors** - menu color theme (*Dark **/** Light **/** Classic*)

    *   **Anti AFK kick** - avoid auto-kick by server for inactivity

    *   **Auto strafe** - automatically strafe in air following mouse movement

    *   **Bunny hop** - automatically simulate space bar press / release while jump button is being held; increases movement speed

    *   **Clan tag** - set custom clan tag

    *   **Animated clan tag** - animate clan tag

    *   **Fast duck** - remove crouch delay

    *   **Sniper crosshair** - draw crosshair while holding sniper rifle

    *   **Recoil crosshair** - crosshair follows recoil pattern

    *   **Auto pistol** - fire pistols like automatic rifles

    *   **Auto reload** - automatically reload if weapon has empty clip

    *   **Auto accept** - automatically accept competitive match

    *   **Radar hack** - show enemies positions on radar

    *   **Reveal ranks** - show player ranks in scoreboard in competitive modes

    *   **Reveal money** - show enemies' money in scoreboard

    *   **Spectator list** - show nicknames of players spectating you

    *   **Watermark** - show cheat name in the upper-left screen corner and fps & ping in the upper-right corner

    *   **Offscreen Enemies** - draw circles on the screen indicating that there are enemies behind us

    *   **Fix animation LOD** - fix aimbot inaccuracy for players behind local player

    *   **Fix bone matrix** - correct client bone matrix to be closer to server one

    *   **Disable model occlusion** - draw player models even if they are behind thick walls

    *   **Kill message** - print message to chat after killing an enemy

    *   **Name stealer** - mimic other players names

    *   **Custom clantag** - set a custom clantag

    *   **Fast plant** - plants bomb on bombsite border, when holding <kbd>LMB</kbd> or <kbd>E</kbd> key

    *   **Fast Stop** - stops the player faster than normal

    *   **Quick reload** - perform quick weapon switch during reload for faster reload

    *   **Prepare revolver \[ key \]** - keep revolver cocked, optionally on key

    *   **Fix tablet signal** - allow use tablet on underground (dangerzone)

    *   **Hit Sound** - sound emitted when hurting enemy

    *   **Chocked packets** - length of sequence of chocked ticks

    *   **Max angle delta** - maximum viewangles change per tick

    *   **Aspect Ratio** - allows you to change the aspect ratio

    *   **Purchase List** - show the purchased equipment by enemies
    
  
</details>

## Getting started

### Prerequisites
Microsoft Visual Studio 2019 16.10 (or newer), platform toolset v142 and Windows SDK 10.0.x.x are required in order to compile Osiris. If you don't have ones, you can download VS [here](https://visualstudio.microsoft.com/) (Windows SDK is installed during Visual Studio Setup).

### Downloading

There are two options of downloading the source code:

#### Without [git](https://git-scm.com)

Choose this option if you want pure source and you're not going to contribute to the repo. Download size ~600 kB.

To download source code this way [click here](https://github.com/bl6ndr/Nicom/archive/master.zip).

#### With [git](https://git-scm.com)

Choose this option if you're going to contribute to the repo or you want to use version control system. Download size ~4 MB. Git is required to step further, if not installed download it [here](https://git-scm.com).

Open git command prompt and enter following command:

    git clone --depth=1 https://github.com/bl6ndr/Nicom.git

`Nicom` folder should have been successfully created, containing all the source files.

### Compiling from source

When you have equipped a copy of the source code, next step is opening **DaddyKermitsInternal.sln** and **internal.sln** in Microsoft Visual Studio 2019.

Then change build configuration to `Release | x86` and simply press **Build solution**.

If everything went right you should receive `Nicom.dll`  binary file.

### Loading / Injecting into game process

Open your favorite [DLL injector](https://en.wikipedia.org/wiki/DLL_injection) and just inject `Nicom.dll` into `valorant.exe` process.

When injected, menu is openable under `INSERT` key.

### Further optimizations
If your CPU supports AVX / AVX2 / AVX-512 instruction set, you can enable it in project settings. This should result in more performant code, optimized for your CPU. Currently SSE2 instructions are selected in project settings.

## FAQ

### How do I open menu?
Press <kbd>INSERT</kbd> while focused on CS:GO window.

### Where is my config file saved?
Configuration files are saved inside `Nicom` folder in your `Documents` folder (`%USERPROFILE%\Documents\Nicom`). The config is in human readable format and can be edited (e.g, using notepad). Sometimes after updates configuration file needs to be deleted and recreated.

### What hooking methods Nicom uses?
Currently implemented hooking methods are:
*   MinHook - trampoline hook
*   VmtHook - hook a function directly in a vtable
*   VmtSwap - create a copy of a vtable and swap the pointer on the class instance

Hooking implementation files are located in [Hooks](Source/Hooks) directory.
