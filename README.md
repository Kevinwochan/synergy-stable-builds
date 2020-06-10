Synergy
=======

Share one mouse and keyboard between multiple computers.

Synergy is free and open source (free as in free speech),
meaning you are free to run it and redistribute it with
or without changes.

Just use "hm conf" and "hm build" to compile (./hm.sh on
Linux and Mac).

## Windows
```
 hm conf -g1
 hm build
 ```
## Unix and Linux
Ubuntu 20.4 has dropped suport for libqt4, add the unofficial repo
```
sudo add-apt-repository ppa:rock-core/qt4
sudo apt-get update

 sudo apt-get install cmake make g++ xorg-dev libqt4-dev libcurl4-openssl-dev libavahi-compat-libdnssd-dev libssl-dev libx11-dev
 ./hm.sh conf -g1 [-d] # Use -d to build a debug version.
 ./hm.sh build [-d]
 ```
## Mac OS X
```
 ./hm.sh conf -g1 [-d] --mac-sdk 10.11 --mac-identity Yosemite # Use -d to build a debug version and replace 10.11 / Yosemite with correct versions of your setup.
 ./hm.sh build [-d]
 ```

For detailed compile instructions:
https://github.com/symless/synergy/wiki/Compiling

Happy hacking!
