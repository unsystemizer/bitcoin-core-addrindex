# Bitcoin Core 0.11 with addrindex patch

* Built from https://github.com/btcdrak/bitcoin/archive/addrindex-0.11.zip on June 27, 2015
* Stop bitcoind and uninstall (`dpkg -r`) any older

## Download

### Raspberry Pi B (armhf)

* https://www.dropbox.com/s/t2gkwih0qq5bfyy/bitcoin-addrindex_0.11-0_armhf.orig.deb?dl=0
* Checksum (SHA256): `6485fb82c8a00f807b76a7da8cd8467795e87d4cd7b5ba8a41f05ccbbd894484`

# Bitcoin Core 0.10.2 with addrindex patch

## Download

* Download: https://drive.google.com/file/d/0B7EbpGFfBEEFV1JkV1RDWXRzeUU/view
* Checksum (SHA-1): `FBEC75A224CEEDE307795AF3A5AD3A83D69EF071 bitcoin-core-with-addrindex-patch_0.10.2-1_armhf.deb`

## Requirements and Install Procedure

* Install all dependencies required for Bitcoin Core on Raspbian (libssl1.0.0, libprotobuf, libgcc1, libboost-filesystem, libboost-chrono,libboost-filesystem, libboost-program-options, libboost-system, libboost-thread, libboost-test, etc.)
* Uninstall any older version if you have it
* (optional) Make a backup copy of your blockchain
* Install this package
* If you don't already have an indexed copy of blockchain data, run bitciond once with `-reindex`

## Uninstall Procedure

* Uninstall the package using `dpkg` or other system utility
* Blockchain does not have to be re-created for use without addrindex - address index will be ignored by Bitcoin Core that doesn't understand it

## Source

https://github.com/btcdrak/bitcoin/releases/tag/addrindex-0.10.2
