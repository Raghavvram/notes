# Initramfs

**Last Updated:** 2025-07-15

Initramfs (initial RAM file system) is a temporary root file system that is loaded into memory during the Linux boot process. It is used to mount the real root file system, which can be located on a hard drive, a network share, or other storage device.

## How it Works

1.  **Loading:** The bootloader loads the kernel and the initramfs image into memory.
2.  **Execution:** The kernel unpacks the initramfs image and mounts it as a temporary root file system.
3.  **Initialization:** The kernel executes the `/init` script located in the initramfs. This script is responsible for loading the necessary drivers and modules to mount the real root file system.
4.  **Switching:** Once the real root file system is mounted, the initramfs is unmounted and the system continues to boot from the real root file system.

## Why it's Useful

Initramfs is useful for a number of reasons:

*   **Flexibility:** It allows the root file system to be located on a variety of devices, including network shares and encrypted volumes.
*   **Modularity:** It allows for a smaller kernel, as the drivers and modules needed to mount the root file system can be loaded from the initramfs.
*   **Customization:** It can be customized to include additional tools and scripts that are needed during the boot process.

## Contents of Initramfs

An initramfs image typically contains the following:

*   A minimal set of directories, such as `/bin`, `/sbin`, `/etc`, `/dev`, `/proc`, and `/sys`.
*   The `/init` script, which is responsible for mounting the real root file system.
*   A set of essential utilities, such as `mount`, `insmod`, and `modprobe`.
*   The kernel modules needed to mount the real root file system.
