# bin
 A collection of useful utilities
 
## Usage
just `chmod +x` the files and run them, make sure to read dependecies and and the following warnings first

## Warnings
- None of these files do any dependencie checking or have any safeguards built in, read the scripts and verify they will work for your system before running them

- If you wish to use the NAS utilities you will have to edit them to fit your setup, the configuration in this repo is only designed to work for me, but can be easily adpapted

- refresh mirrorlist stores the new list to `mirrorlist-rate-mirrors` which you will either have to include in your pacman.conf or edit the `MIRRORLISTFILE` variable

## Dependecies
- update
	- [yay](https://github.com/Jguer/yay) as the AUR helper
	- other utils from this repo
	
- refresh-mirrorlist
	+ [rate-mirrors](https://github.com/westandskif/rate-mirrors) to fetch and sort mirrors
	
- mount-NAS, umount-NAS
	+ avahi for local hostname resolution
	+ driver for storage medium
	
- remove-oprhans
	+ [pacman](https://archlinux.org/packages/core/x86_64/pacman/) (pulled by [base](https://archlinux.org/packages/core/any/base/) so you should have this already)
	
- checkpartitionsalignment
	+ lsblk from [util-linux](https://archlinux.org/packages/core/x86_64/util-linux/) (pulled by [base](https://archlinux.org/packages/core/any/base/) so you should have this already)
	+ [parted](https://archlinux.org/packages/extra/x86_64/parted/)
	
## Credits
- Bruno Bronosky for the [argument parsing snippet](https://stackoverflow.com/questions/192249/how-do-i-parse-command-line-arguments-in-bash)
- crysman for the entire [checkpartitionsalignment script](https://github.com/crysman/check-partitions-alignment) (its just straight copied from there)