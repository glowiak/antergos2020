Antergos2020 Linux | Antergos now supported

I was sad, because Antergos isn't supported, so I made Antergos2020

Features:
-based on Arch
-GNOME 3.38
-ZEN kernel 5.9.1
-pamac preinstalled
-look like orginal Antergos

You may know this project from my Reddit posts, but now you can try it!
Current version: 4.11-beta 2
Current distirbuting format: Zstandard compressed QEMU QCOW2 image

To run it you must have qemu and zstd installed.

How to run:
On Linux if you've installed kvm type: qemu-system-x86_64 -enable-kvm -m 4096 -soundhw es1370 -net nic -net user -hda harddisk.img -boot c -cpu host
If this not work run it as root or with sudo.
On other OSes (or on Linux without kvm) type: qemu-system-x86_64 -m 4096 -soundhw es1370 -net nic -net user -hda harddisk.img -boot c

Image size: 8,8GB
Compressed size: 3,8GB

DOWNLOAD (beta 2): http://www.mediafire.com/file/p4fi1k10fqp53c2/antergos2020-b2.zst/file


Password.
Antergos2020 have password. I don't publish this password. How to change this password:
1.Download archiso (arch's livecd) and type: qemu-system-x86_64 -m 4096 -net nic -net user -hda harddisk.img -boot d -cdrom <path to archiso>
2.After archiso starts type in it following commands:
# swapon /dev/sda1
# mount /dev/sda2 /mnt
# arch-chroot /mnt
# passwd root
Type new root password.
# passwd glowiak
Type new user password.
# exit
# umount -a
# poweroff
Done. Passwords changed. Now boot normal to see changes and use Antergos2020
