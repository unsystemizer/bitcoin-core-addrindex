#Bitcoin Core 0.13.2 with addrindex patch

https://github.com/btcdrak/bitcoin/tree/addrindex-0.13 can be built from the source as per the standard Bitcoin Core procedure. You can also download signed, deterministically built ARM binaries ([regular](https://github.com/btcdrak/bitcoin/releases/download/v0.13.2-addrindex/bitcoin-0.13.2-addrindex-arm-linux-gnueabihf.tar.gz) and debug version). 

Note that Counterparty server v9.55.1 does not yet officially support v0.13, but you're welcome to evaluate it.

* Stop Counterparty server
* Uninstall Bitcoin Core
* Build and install (or decompress to desired location which you can add to your `PATH`) Bitcoin Core addrindex
* Start Bitcoin Core addrindex and let it reparse the blockchain (this may take an hour or four)
* Once Bitcoin has completed the reparse, start counterparty-server 

#Bitcoin Core 0.12.1 with addrindex patch

##Download

####Raspberry Pi 2 (armhf) with Raspbian and libboost v1.55.0.2

* https://www.dropbox.com/s/irm5xkjd8vi12bk/bitcoin-0.12.1_0.12.1-0_armhf.deb
* Checksum (SHA256): `3dbd96f61b5798903300f1090799207a1322293d689c335c56676ed6d332b7e1`
* Source code: https://github.com/btcdrak/bitcoin/releases/tag/v0.12.1-addrindex
* Requirements (build environment): `Raspbian 8.0 (stretch/sid)`, `Linux rpi2 4.1.19-v7+`, `armv7l GNU/Linux`, with libboost-dev 1.55.0.2

####Raspberry Pi 2 (armhf) with Ubuntu 16.04 and libboost 1.58.0.1

* https://www.dropbox.com/s/y1rmp62xkfwnd1f/bitcoin-0.12.1_0.12.1-1_ubuntu_16.04_armhf.deb?dl=0
* Checksum (SHA256): `48a3d7554ea5e7357596ccfa64257e5f0217274ad9aea729bd557ad9e09f48d8`
* Source code: https://github.com/btcdrak/bitcoin/releases/tag/v0.12.1-addrindex
* Requirements (build environment): `Ubuntu 16.04 LTS`, `Linux rpi3 4.1.19-v7+`, `armv7l GNU/Linux`, with libboost-dev 1.58.0.1


#Bitcoin Core 0.12.0 with addrindex patch

##Download

####Raspberry Pi 2 (armhf) with Raspbian and libboost v1.55.0.2

* https://www.dropbox.com/s/nrk9r9ih8wyi042/bitcoin_0.12.0-1_deb-8-libboost-1.55.0.2_armhf.deb
* Checksum (SHA256): `a55755bdfb37255bde7403e9c113a62a44e25d80fde63de4a774f473702b48ab`
* Source code: https://github.com/btcdrak/bitcoin/archive/v0.12.0-addrindex.zip
* Requirements (build environment): `Raspbian 8.0`, `Linux rpi1 4.1.13-v7+`, `armv7l GNU/Linux`, with libboost-dev 1.55.0.2

####Raspberry Pi 2 (armhf) with Raspbian and libboost v1.60.0

This is for systems with manually installed libboost 1.60.0.

* https://www.dropbox.com/s/g9kpm8olxf9qw82/bitcoin-0.12.0_0.12.0-1_libboost-1.60.0_armhf.deb
* Checksum (SHA256): `c7429dbf2015770e7b964f8382947dfa4c9a7ace962ab001fa2ad820bca3ed4e`
* Source code: https://github.com/btcdrak/bitcoin/archive/v0.12.0-addrindex.zip
* Requirements (build environment): `stretch/sid`, `Linux rpi3 4.1.18-v7+`, `armv7l GNU/Linux`, with libboost-1.60.0 built from source

####Other Platforms and Packages

Linux, OS X and Windows (x86_64) binaries as well as platform-independent source code can be downloaded from BTCdrak's Github [repo here](https://github.com/btcdrak/bitcoin/releases). That is the recommended way of installing packages, followed by building from source by yourself.

##Install & Uninstall

Please see notes for earlier releases below. Basically you need common dependencies required by Bitcoin Core.

Helpful comamands:

* `cat /etc/debian_version`               # check your OS version
* `dpkg -s libboost-dev | grep 'Version'` # if you installed it as package and not from source
* `sha256sum <downloaded-file>`           # generate SHA256 checksum
* Recommended `bitcoin.conf` settings for Counterparty users can be found in https://github.com/unsystemizer/counterparty-config-example

#Bitcoin Core 0.11.2 with addrindex patch

##Download

####Raspberry Pi 2 (armhf)

* https://www.dropbox.com/s/she30q90sx3xja9/bitcoin-0.11.2_0.11.2-1_armhf.deb
* Checksum (SHA256): `ca23f8ba8ccefb5735723c78126c548875a51d80b03f64f11c02ef7d3c866f6e`
* Source code: https://github.com/btcdrak/bitcoin/archive/v0.11.2-addrindex.tar.gz

####Raspberry Pi B (armhf)

* https://www.dropbox.com/s/she30q90sx3xja9/bitcoin-0.11.2_0.11.2-1_armhf.deb
* Checksum (SHA256): `eecaf39993410188fe7f29f4bdbc55574f818060f62d82e82977440078b58a0e`
* Source code: https://github.com/btcdrak/bitcoin/archive/v0.11.2-addrindex.tar.gz 

See below under the first 0.11 release about install, upgrade and uninstall instructions. Basically you need to uninstall any other Bitcon Core package and install this one. This package requires libboost 1.55 libraries.

###Other OS and Platforms

* Download signed binaries (or unsigned Windows installers) from https://github.com/btcdrak/bitcoin/releases/.

#Bitcoin Core 0.11.1 with addrindex patch

##Download

####Raspberry Pi 2 (armhf)

* https://www.dropbox.com/s/jf8xc08t45epaab/bitcoin-addrindex_0.11-1_armhf.deb
* Checksum (SHA256): `f26ce0e6ce430d3ea640f92c2ffea1edb3a5a0d594a6c47ed164b225f1d34e49`
* Source code: https://github.com/btcdrak/bitcoin/releases/download/v0.11.1-addrindex/bitcoin-0.11.1-addrindex.tar.gz

###Other OS and Platforms

* Download signed binaries (or unsigned Windows installers) from https://github.com/btcdrak/bitcoin/releases/.

#Bitcoin Core 0.11 with addrindex patch

NOTE: Please use v0.11.1 because 0.11 contains several security fixes

* Built from https://github.com/btcdrak/bitcoin/archive/addrindex-0.11.1.zip
* The Linux packages are built without a GUI, the Windows with 

##Download

###Raspbian

Install the usual bitcoin-core dependencies (or install stock bitcoin-core and then uninstall it). 

Stop bitcoind and uninstall (`dpkg -r`) any older bitcoin or bitcoin-addrindex package if present. Reindex the blockchain if a non-addrindex version of Bitcoin Core was installed previously.

####Raspberry Pi B (armhf)

* https://www.dropbox.com/s/t2gkwih0qq5bfyy/bitcoin-addrindex_0.11-0_armhf.orig.deb?dl=0
* Checksum (SHA256): `6485fb82c8a00f807b76a7da8cd8467795e87d4cd7b5ba8a41f05ccbbd894484`

Note: This package was built on Raspbian upgraded to Jessie (June 27, 2015).

####Raspberry Pi 2 (RPi2) (armhf)

* https://www.dropbox.com/s/n05a7r7g7z6oavp/bitcoin-addrindex_0.11-0_armhf.deb?dl=0
* Checksum (SHA256): `4bf44cf87241c9ffbfc91b5ca8c69b8a09c16d9d5b82f00b4dd73fc91d0b9d4f`

Note: This package was built on Raspbian upgraded to Jessie (August 24, 2015)

###Windows 

This package has been tested on x86 and x64 architectures, Windows XP and up. Windows 10 has not been tested (feel free to report success or problems with Windows 10 in Issues).

* https://www.dropbox.com/s/lf9u4xgefcw3f6s/Bitcoin_Core_with_addrindex_v0.11.msi?dl=0
* Checksum (SHA256): `68eaceaf29cf34e2b1e7274378bfcaf8a69913e7b35bbbab0bc7b56176b634ed`

Notes: 

* If this is your first time to use addrindex after you install the program do not run immediately. First read `C:\Program Files (x86)\Bitcoin\readme.txt` (on 64-bit OS; the path has no `(x86)` on 32-bit Windows OS).
* Uninstall any other Bitcoin Core package prior to installing this one.
* The installer simply copies 4 executables and one readme.txt to the usual Bitcoin Core install directory. Configuration files are never touched. You're welcome to backup your wallet, blockchain and config files before you install although that is not a requirement.

##Uninstall Procedure

Uninstall behavior is the same as for the official Bitcoin Core. You can manually remove addrindex data if you dont' want to use it, but it will not interfere with Bitcoin Core without addrindex patch.

#Bitcoin Core 0.10.2 with addrindex patch

##Download

###Raspberry Pi B (armhf)

* Download: https://drive.google.com/file/d/0B7EbpGFfBEEFV1JkV1RDWXRzeUU/view
* Checksum (SHA-1): `FBEC75A224CEEDE307795AF3A5AD3A83D69EF071 bitcoin-core-with-addrindex-patch_0.10.2-1_armhf.deb`

###Raspberry Pi 2 (RPi2) (armhf)

* Use v0.11

##Requirements and Install Procedure

###Linux

* Install all dependencies required for Bitcoin Core on Raspbian (libssl, libprotobuf, libgcc1, libboost-filesystem, libboost-chrono,libboost-filesystem, libboost-program-options, libboost-system, libboost-thread, libboost-test, etc.)
* Uninstall any older version if you have it
* (optional) Make a backup copy of your blockchain and/or wallet
* Install this package
* If you don't already have an indexed copy of blockchain data (and you don't if you didn't previously have Bitcoin Core with addindex), run bitciond or Bitcoin-Qt once with `-reindex`

##Uninstall Procedure

* Uninstall the package using `dpkg` or other system utility
* Blockchain does not have to be re-created for use without addrindex - address index will be ignored by Bitcoin Core that doesn't understand it

##Source

https://github.com/btcdrak/bitcoin/releases/tag/addrindex-0.10.2
