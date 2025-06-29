FHS (Filesystem Hierarchy Standard)
Linux uses a tree-like directory structure with / (root) as the base. Everything—files, directories, devices—is a part of this hierarchy.
What is FHS?
The standard defines a consistent directory layout across Unix-like systems, ensuring software compatibility and system maintainability 

History & Organization

First released in 1994.

Latest version is FHS 3.0, published June 3, 2015, maintained by the Linux Foundation 

Key Directories & Their Purposes
Directory	Purpose
/	“Root” of the filesystem; all other directories branch from here .
/bin	Essential user-level binaries (e.g., ls, cp)
/sbin	System binaries for admin tasks (e.g., fsck, reboot)
/etc	System-wide configuration files (e.g., fstab, network settings)
/usr	Secondary hierarchy: read‑only user programs and libraries
/usr/local	Tertiary hierarchy: locally‑installed software unique to the host
/lib	Essential shared libraries supporting /bin and /sbin
/boot	Bootloader files and kernel images
/dev	Device files for hardware and virtual devices
/proc	Virtual filesystem exposing kernel and process data
/sys	Virtual filesystem for kernel and hardware information
/var	Variable data: logs, mail, spools, caches
/tmp	Temporary files, typically cleared at boot
/mnt, /media	Mount points for filesystems/removable media
/opt	Optional third-party software
/run	Runtime data since boot: PIDs, locks
/srv	Data served by local services (e.g., web, FTP)
/root	Home directory for the root user

How the Hierarchy Works
Everything is a file in Linux (even devices).
Each directory serves a specific, standard purpose.
Multiple storage devices can be mounted into this single unified hierarchy.

Example: Finding Files
User command: /bin/ls
Root's home directory: /root
System logs: /var/log/syslog
Config for network: /etc/network/interfaces
