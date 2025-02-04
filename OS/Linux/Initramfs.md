Initramfs, or initial ramdisk, is a set of files and directories that are used to mount the root file system during the boot process of a Linux system. It's a compressed archive that contains the kernel modules and programs needed to initialize the root file system. 
How it works
During boot, the boot loader loads the initramfs image into memory 
The kernel checks for the initramfs and mounts it as the root file system 
The kernel executes the init process, which is the first process that doesn't exit 
Why it's useful 
Initramfs can be used to load the root file system from a network or an LVM logical volume
It can also be used to create an encrypted root file system that requires a password
What's included in initramfs 
The init process, which is usually called /init
Other files and directories needed by the init process, such as /dev, /proc, and /bin
Kernel modules and userspace programs
A mount utility to mount something
A utility to load a module, and any libraries that the utility depends on