#Bitcoin Core 0.11 with addrindex patch

* Built from https://github.com/btcdrak/bitcoin/archive/addrindex-0.11.zip
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
* Checksum (SHA256): `A0795F8354B7A23DBC7DC851C83E422F36A0A6A9`

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
