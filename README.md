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

Now you’re in the source directory you need to run the configure step
# QT_SELECT=4 is only necessary if you have newer QT versions
QT_SELECT=4 ./hm.sh conf -g1
Note: If you see an error “Error: Could not get revision, git error: 128” you can safely ignore it.

Then:

./hm.sh build
If you get an error “Error: make -w failed with error: 512″ you can ignore that too.

Now you can the build the GUI app.

cd src/gui
qmake
make
Go back to the source root and copy all the built binaries to /usr/local/bin

cd ../../
sudo cp bin/syn* /usr/local/bin
Then run the Synergy GUI,

/usr/local/bin/synergy &
In the GUI you can configure the server you will connect to, and enter your license key, if you have one.

 ```
## Mac OS X
```
 ./hm.sh conf -g1 [-d] --mac-sdk 10.11 --mac-identity Yosemite # Use -d to build a debug version and replace 10.11 / Yosemite with correct versions of your setup.
 ./hm.sh build [-d]
 ```

For detailed compile instructions:
https://github.com/symless/synergy/wiki/Compiling

Happy hacking!

# Running
""
## Setting up the server
Set as server -> Configure Server -> Drag the screen at the top right onto an empty square -> double click the screen -> set the name of the client device as it appears in your error logs -> ok -> start in the bottom right

## Setting up the client
Set as Client -> enter the IP address of the server -> start in the bottom right
