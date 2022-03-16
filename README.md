# A Rather Tremendous Item SysTem

<p align="center"><img src="https://i.imgur.com/3PkUJnu.gif"
  title="Running Artist from Mincraft"
  alt="An example GIF of running artist, inserting and extracting items."
/></p>

Artist is an inventory management system for CC: Tweaked (requires MC 1.16.x
or later). One could think of it as a budget AE network. It offers an easy way
to store and extract items, but powered entirely through ComputerCraft.

## Features
 - Index an arbitrary number of inventories (chests, barrels, etc...), allowing
   for insertion and extraction from them.
 - Simple interface to view and request items.
 - Furnace management support, able to automatically refuel furnaces and insert
   smelted items into the main system.
 - Caching of item information, allowing for speedier startup.

## Install
 - Place down a turtle and some chests, and connect them all together with wired
   modems and networking cable.
 - Run `wget run https://raw.githubusercontent.com/SquidDev-CC/artist/HEAD/installer.lua` on your computer to install artist.
 - Run `/artist.lua` to start it. You may want to call this from your `startup.lua` file!

## Configuration
Artist writes a (documented) config option to `.artist.d/config.lua`, which can
be used to change some of Artist's behaviour.

Some options you may want to adjust:

 - `turtle` → `auto_drop`: Auto-drop items from the turtle's inventory when requested from the interface.
 - `furnace` → `fuels`: A list of valid fuels for the furnace.

## Extending
 - Artist is intended to be somewhat extensible, and you can register your own
   custom modules (be aware that the API is not stable though!) See the
   `examples/display.lua` file for an example.

## History
Artist is a pretty old program at this point. It was [first written in 2016][forum post]
and, to my knowledge, was the first "inventory management" program for CC. While
the code has changed a lot, the core ideas and interface haven't.

It should be noted that this is not the only item system out there, nor is it
necessarily the best. There's a couple of other item systems I'm aware of out
there:
 - **[Turtlegistics]:** This was the first inventory system to become popular on
   [SwitchCraft]. I _believe_ it's the first to use the turtle's inventory as a
   drop-off and pickup point (Artist used separate chests beforehand).
 - **[Milo] (see also [this forum post][milo forum]):** Milo is probably the most
   powerful inventory system out there, with support for crafting and remote
   item transfer (using Plethora's introspection module). It has not been
   updated since MC 1.12, but is a fantastic option for that version!

[forum post]: http://www.computercraft.info/forums2/index.php?/topic/27321-mc-189-1122-plethora/page__view__findpost__p__262475 "Artist on the ComputerCraft forums"
[turtlegistics]: https://github.com/apemanzilla/turtlegistics "Tutlegistics on GitHub"
[milo]: https://github.com/kepler155c/opus-apps/tree/develop-1.8/milo
[milo forum]: http://www.computercraft.info/forums2/index.php?/topic/29761-milo-crafting-and-inventory-system/
[switchcraft]: https://switchcraft.pw "The SwitchCraft Minecraft server"
