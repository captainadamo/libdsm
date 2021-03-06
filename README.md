# liBDSM

lib Defective SMb (libDSM) is a SMB protocol client implementation in pure C, with
a _lot_ less features than Samba and also a more permissive license (currently LGPL).
The initial goal of this project is to have a lib with an iOS/Android compatible license
to be intgrated into VLC for iOS and VLC for Android.

The lib is provided as a static library or as a dynamically linked library. A
few useless (yet) utils are also provided.

## Building

### Requirements

* A Unix system with a bash-shell (i guess)
* C99 C compiler
* (GNU) Make
* Autotools
* libc with iconv
* getopt_long
* GNU tasn1 compiler/support library

The build dependencies can be installed on Debian(-based) systems using

    sudo apt-get install build-essential autoconf libtool pkg-config libtasn1-3-dev libtasn1-3-bin libbsd-dev

### HowTo

    $> ./bootstrap
    $> ./configure --prefix=/your/ass
    $> make
    $> make install # maybe

## Goals

Here's a list of supported features:
* NETBIOS
  * Basic bi-directionnal NETBIOS name resolutio
  * Hacky LAN SMB servers discovery (Listing all the smb servers on the LAN, no WINS, etc.)
  * Basic NETBIOS Session transport layer
* SMB
  * Support only required parts of 'NT LM 0.12' (aka CIFS?) dialect.
  * User based authentication
  * List Shares
  * Browse folders
  * Read file
  * No write, lock, RPCs, etc. [Hum... yet]

## Support

liBDSM has been tested/reported to work witht the following devices/OSes:

* Windows 7
* Windows 8
* A cheap NAS whose name i can't remember :)
* Samba
* smbX (OSX new smb implementation)

Feel free to contribute items to this list (or network trace of not working devices)

## TODO

* HEAVILY refactor. Any help is welcome.

## Contributing

* Fork videolabs/libdsm
* Make a feature branch
* Commits your work there
* Make a pull request
* ...
* Profit !
