# Tank Arena

![Downloads](https://img.shields.io/steam/downloads/306083806)
![Subscriptions](https://img.shields.io/steam/subscriptions/306083806)
![Favorites](https://img.shields.io/steam/favorites/306083806)
![Size](https://img.shields.io/steam/size/306083806)

Source for my Left 4 Dead 2 map [Tank Arena](https://steamcommunity.com/sharedfiles/filedetails/?id=306083806).

## Compiling

The `scripts` directory contains a python build script that:
* Checks for updates to the `.vmf` file (md5 hash);
* Compiles the map to a `.bsp` if it has changed;
* Runs the game to build the cubemaps;
* Assembles the `.vpk` file;
* Packs and compresses it with WinRAR;
* Copies it to the `ftp` subdirectory and archives any previous one;
* Logs some basic info along the way.

It will compile the map in production mode (with `-both` and `-final` `rad` options) unless a `-fast` parameter is passed.

Can be run by hand but a best practice is to schedule it to run once a day at night (as it can run for some time).

You can then share the `ftp` subdirectory with your teammates/testers through ftp.

## Notes

The `.bsp` file is not included in the `vpk\l4d2_tank_arena\maps` directory.

You will need to compile it first and copy it to this directory before packaging the `.vpk`.

This is automatically done by the python script.
