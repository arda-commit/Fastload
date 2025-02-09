# What the hell is 441 chunk loading and why is it important?
441 Chunk loading is essentially a generator for your world that loads 21^2 chunks (or 10 chunk-render-distance), Why does 10 turn into 21? 2 sides plus the one you are standing on, squared for 2 dimensions.

# Short explanation:
Fastload is a simple mod that reduces world loading time. This serves as an alternative to ksyxis and Forcecloseloadingscreen.

# Required by:
- Client
- Server
- ...& Will work on one but not the other but some features will be disabled. So use both if you want all the features!

# Credits for mods that are integrated:
- Ksyxis by VidTu (Incompatible)
- Forcecloseloadingscreen by kennytv (Incompatible)

# Here are its features:
- Reducing 21^2 chunks to 5^2 (Configurable)
- Cancels 'Loading Terrain' & 'Joining World' for even quicker loading times.
- Adjusts the visual chunk loading to be smaller and in sync with the smaller radius.
- Optional Pre-generator screen (Disabled by default)

# Speed times: (Default Settings) [All other elements are controlled!]
- Vanilla: [
- Create New world: ~32 sec
- Load World: ~5 sec
- ]
- Fastload: [
- Create New World: ~23 sec
- Load World: ~3 sec
- ]

# How it works (In detail) (In comparison with integrated mods):
Ksyxis cancels 441 world loading by essentially telling the game "Hey, we're done!", which works on paper. But, it is a very unsafe method of loading and rather inefficient. It does this during chunk loading which is a big no-no in code. Not only does this cause potential crashes, and corruption, but it also makes it take longer to load in comparison to our way. Ksyxis doesn't even initialise at the beginning of 441, it does it after it is initialised! Which is just plain bad. But don't get angry at ksyxis yet! The developer of it issues a firm warning that it isn't stable and really shouldn't be used, which explains everything.
We do this in a better, safer way by simply dialing down the number of chunks required to load before 441 initialises. This is fairly self-explanatory!

Furthermore, we integrated yet another, unstable/unsafe mod: "Force Close Loading Screen". By itself, it just cancels the Downloading Terrain Screen, which isn't stable. We improved upon this by a number of metrics, such as:

    * Temporarily stop the Pause Menu from appearing too early when the world takes a screenshot for it's icon.
    * Cancelled 'Joining World' as well.
    * Added a separate screen to either replace or complement this feature.
    * Added a number of failsafes, such as:
        * Only cancel when the player is ready.
        * Have a number of checkers to ensure that it doesn't interrupt other parts of the game.
        * Made this toggleable (for very obvious reasons).

Modrinth: https://modrinth.com/mod/fastload

Curseforge: https://www.curseforge.com/minecraft/mc-mods/fastload

Discord: https://discord.gg/fMSnenNSXM
e
