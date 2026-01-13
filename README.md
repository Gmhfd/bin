# bin
 A collection of useful utilities
 
## Usage
just `chmod +x` the files and run them, make sure to read dependecies and and the following warnings first

## Warnings
- None of these files do any dependency checking or have any safeguards built in, read the scripts and verify they will work for your system before running them

- If you wish to use the NAS utilities you will have to edit them to fit your setup, the configuration in this repo is only designed to work for me, but can be easily adpapted

- refresh mirrorlist stores the new list to `mirrorlist-rate-mirrors` which you will either have to include in your pacman.conf or edit the `MIRRORLISTFILE` variable

## Dependecies
- update
	- [yay](https://github.com/Jguer/yay) as the AUR helper
	- refresh-mirrorlist and remove-orphans from this repo and their dependecies
	
- refresh-mirrorlist
	+ [rate-mirrors](https://github.com/westandskif/rate-mirrors) to fetch and sort mirrors
	+ [sudo](https://archlinux.org/packages/core/x86_64/sudo/)
	
- mount-NAS, umount-NAS
	+ [avahi](https://archlinux.org/packages/extra/x86_64/avahi/) with [local hostname resolution](https://wiki.archlinux.org/title/Avahi#Hostname_resolution), if you wish to use it
	+ driver for storage medium, most likley [cifs-utils](https://archlinux.org/packages/extra/x86_64/cifs-utils/)
	
- remove-orphans
	+ [pacman](https://archlinux.org/packages/core/x86_64/pacman/) (pulled by [base](https://archlinux.org/packages/core/any/base/) so you should have this already)
	+ [sudo](https://archlinux.org/packages/core/x86_64/sudo/)
	
- checkpartitionsalignment
	+ lsblk from [util-linux](https://archlinux.org/packages/core/x86_64/util-linux/) (pulled by [base](https://archlinux.org/packages/core/any/base/) so you should have this already)
	+ [parted](https://archlinux.org/packages/extra/x86_64/parted/)
	+ [sudo](https://archlinux.org/packages/core/x86_64/sudo/)
	
- phone-audio
	+ [android-tools](https://archlinux.org/packages/extra/x86_64/android-tools/)
	+ [scrcpy](https://archlinux.org/packages/extra/x86_64/scrcpy/)
	+ [avahi](https://archlinux.org/packages/extra/x86_64/avahi/) for MDNS device discovery (optional, no check tho)

## Credits
- Bruno Bronosky for the [argument parsing snippet](https://stackoverflow.com/questions/192249/how-do-i-parse-command-line-arguments-in-bash)
- crysman for the entire [checkpartitionsalignment script](https://github.com/crysman/check-partitions-alignment) (its just straight copied from there)
- gnumoksha for the [mdns device discovery snippet](https://gist.github.com/gnumoksha/f9a5b2e01b1e74ffa2a055b6e18f7c58)

## Contributing
If you want to contribute to this collection for whatever reason just open a PR and I will look at it sooner or later
