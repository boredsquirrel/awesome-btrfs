## General
### [BTRFS CLI Interface](https://btrfs.readthedocs.io/en/latest/index.html)
- [Fedora Magazine](https://fedoramagazine.org/working-with-btrfs-snapshots/)
- [Arch Wiki](https://wiki.archlinux.org/title/Btrfs)
- [Debian Wiki](https://wiki.debianforum.de/Btrfs)

### [btrfs-progs](https://github.com/kdave/btrfs-progs)
official userpace utilities

### [BTRFS Assistant](https://gitlab.com/btrfs-assistant/btrfs-assistant)
Tool for doing many BTRFS actions graphically

It requires `snapper` and offers a GUI for it.

![](https://gitlab.com/-/project/32535488/uploads/21da59577c3e8a101347cf0d59569c09/image.png)

### [btrfs maintenance](https://github.com/kdave/btrfsmaintenance)
> This is a set of scripts supplementing the btrfs filesystem and aims to automate a few maintenance tasks. This means the scrub, balance, trim or defragmentation.
> 
> Each of the tasks can be turned on/off and configured independently. The default config values were selected to fit the default installation profile with btrfs on the root filesystem.
>
> Overall tuning of the default values should give a good balance between effects of the tasks and low impact of other work on the system. If this does not fit your needs, please adjust the settings.

### [butter-manager](https://github.com/egara/buttermanager)
> Tool for managing snapshots, balancing filesystems and upgrading the system safetly.

## Backups & Snapshots
### [btrbk](https://digint.ch/btrbk/)
- [Code](https://github.com/digint/btrbk)
- [CalculateLinux Wiki](https://wiki.calculate-linux.org/btrbk)
- [FAQ](https://digint.ch/btrbk/doc/faq.html)

Backup utility using BTRFS

### [Snapper](http://snapper.io)
General system snapshot utility with BTRFS support, used in OpenSUSE Tumbleweed by default. There are also [plugins for Fedoras dnf](https://fedoramagazine.org/make-use-of-btrfs-snapshots-to-upgrade-fedora-linux-with-easy-fallback/) and for [Arch pacman](https://www.dwarmstrong.org/btrfs-snapshots-rollbacks).

- [ArchWiki](https://wiki.archlinux.org/title/Snapper)
- [OpenSUSE Docs](https://doc.opensuse.org/documentation/leap/reference/html/book-reference/cha-snapper.html)
- [RedHat Docs](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-snapper)
- [OpenSUSE](https://doc.opensuse.org/documentation/leap/reference/html/book-reference/cha-snapper.html) [\[DE\]](https://de.opensuse.org/openSUSE:Snapper_Tutorial)
- [SUSE Enterprise Linux](https://documentation.suse.com/sles/15-SP5/html/SLES-all/cha-snapper.html) [\[DE\]](https://documentation.suse.com/de-de/sles/15-SP3/html/SLES-all/cha-snapper.html)

### [Timeshift](https://github.com/linuxmint/timeshift)
> System restore tool for Linux. Creates filesystem snapshots using rsync+hardlinks, or BTRFS snapshots. Supports scheduled snapshots, multiple backup levels, and exclude filters. Snapshots can be restored while system is running or from Live CD/USB. 

Currently maintained by LinuxMint, even though they dont use BTRFS by default, it works better there.

- [ArchWiki](https://wiki.archlinux.org/title/Timeshift)
- [Debian Wiki](https://wiki.debian.org/timeshift)
- [thelinuxcode](https://thelinuxcode.com/timeshift-backup-tutorial/)
- [linuxconfig](https://linuxconfig.org/how-to-create-incremental-system-backups-with-timeshift-on-linux)
- [Mir Rahed Uddin's Guide](https://dev.to/rahedmir/how-to-use-timeshift-from-command-line-in-linux-1l9b)
- [Its FOSS Guide](https://itsfoss.com/backup-restore-linux-timeshift/)
- [\[DE\] Linuxcommunity Guide](https://www.linux-community.de/ausgaben/linuxuser/2019/06/zeitsprung)

### [libtuikit / transactional-update](https://github.com/openSUSE/transactional-update)
Used in OpenSUSE microOS and the Desktop variants.

> provides an application and library to update a Linux operating system in a transactional way, i.e. the update will be performed in the background while the system continues running as it is. Only if the update was the successful as a whole the system will boot into the new snapshot.

Available as a library for other distros.

### [Yet Another BTRFS Snapshotter](https://github.com/hirak99/yabsnap)

> Alternatives don't supports customized of snapshot location, (e.g. Arch recommended layout). Adhering to such layouts, and rolling back using them, sometime involve non-obvious workarounds. The motivation for yabsnap was to create a simpler, hackable and customizable snapshot system.

### btrfs-autosnap
There are 2 separate projects with that name
- [shell script for automating and deleting snapshots](https://github.com/snoopy3476/btrfs-autosnap)
- [Arch pacman hook](https://github.com/vaminakov/btrfs-autosnap/) ([AUR package](https://aur.archlinux.org/packages/btrfs-autosnap/))

### [grub-btrfs](https://github.com/Antynea/grub-btrfs)
Set BTRFS snapshots as boot options

- [installation](https://github.com/Antynea/grub-btrfs?tab=readme-ov-file#%EF%B8%8F-installation) ([outdated Fedora COPR](https://copr.fedorainfracloud.org/coprs/kylegospo/grub-btrfs/))
- [Debian guide](https://medium.com/@inatagan/installing-debian-with-btrfs-snapper-backups-and-grub-btrfs-27212644175f)
- [Ubuntu guide](https://www.lorenzobettini.it/2022/10/timeshift-and-grub-btrfs-in-ubuntu/)
- [blog post](https://www.lorenzobettini.it/2022/07/timeshift-and-grub-btrfs-in-linux-arch)

### [btrfs-sxbackup](https://github.com/masc3d/btrfs-sxbackup)
> Incremental btrfs snapshot backups with push/pull support via SSH 

## Small CLI tools

### [btrfsd - tiny Btrfs maintenance daemon](https://github.com/ximion/btrfsd)
> Btrfsd is a lightweight daemon that takes care of all Btrfs filesystems on a Linux system.

> It can:
> - Check for detected errors and broadcast a warning if any were found, or optionally send an email
> - Perform scrub periodically if the system is not on battery
> - Optionally schedule balancing operations as well

### [duperemove](https://markfasheh.github.io/duperemove/duperemove.html)
- [Code](https://github.com/markfasheh/duperemove)
- [Gentoo Wiki](https://wiki.gentoo.org/wiki/Duperemove)

> Tools for deduplicating file systems

### [compsize](https://github.com/kilobyte/compsize)
- [Fedora Magazine on BTRFS compression](https://fedoramagazine.org/working-with-btrfs-compression/)

> Takes a list of files on a btrfs filesystem and measures used compression types and effective compression ratio

Used in [flatpak-dedup-checker](https://gitlab.com/TheEvilSkeleton/flatpak-dedup-checker)

### [btdu](https://github.com/CyberShadow/btdu)
> sampling disk usage profiler for btrfs
> For multiple reasons, classic disk usage analyzers such as `ncdu` cannot provide an accurate depiction of actual disk usage. (btrfs compression in particular is challenging to classic analyzers, and special tools must be used to query compressed usage.)

### [btrfs-list](https://github.com/speed47/btrfs-list)
Helps listing directories

### [btrfs-fuse](https://github.com/adam900710/btrfs-fuse)
> A read-only btrfs implementation using FUSE (Filesystem in Userspace).
Although btrfs is already in mainline Linux kernel, there are still use-cases for such read-only btrfs implementation:

### [btrfs debugger](https://crates.io/crates/btrd)
> The btrfs debugger (pronounced "buttered").

> btrd is a REPL debugger that helps inspect mounted btrfs filesystems. btrd is particularly useful in exploring on-disk structures and has full knowledge of all on-disk types.

### [ntfs2btrfs](https://github.com/maharmstone/ntfs2btrfs)
> a tool which does in-place conversion of Microsoft's NTFS filesystem to the open-source filesystem Btrfs, much as btrfs-convert does for ext2. The original image is saved as a reflink copy at image/ntfs.img, and if you want to keep the conversion you can delete this to free up space.

Consists of a Windows and a Linux executable. Does not work on the primary drive.

### [WinBTRFS](https://github.com/maharmstone/btrfs)
> filesystem driver for Windows

## Partition managers with support
- KDE-Partitionamanger
- GNOME-Disks
- blivet-gui (Fedora Anaconda setup)
- gparted ?

## Data recovery
When having deleted or corrupted data on a BTRFS partition, these tools can help:

not tested are marked with "?"

### Testdisk?
+ photorec?

### Scalpel?

### [R-Linux](https://www.r-studio.com/free-linux-recovery)
Freeware, not FOSS? Not related to [R](https://www.r-project.org) and "R-Studio" is also not related to [RStudio](https://www.rstudio.com/categories/rstudio-ide)

## BTRFS bindings
These allow you to do BTRFS actions in many programming languages
- [Python 3](https://github.com/knorrie/python-btrfs) ([Docs](https://python-btrfs.readthedocs.io/en/stable/genindex.html))
- [Rust](https://github.com/wellbehavedsoftware/rust-btrfs) ([Website](http://rust-btrfs.com/), [Docs](https://docs.rs/btrfs))
- [Go](https://github.com/containerd/btrfs)
- [more parsing libraries here](https://formats.kaitai.io/btrfs_stream/index.html)
