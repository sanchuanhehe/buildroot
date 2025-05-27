MyBoard Configuration
====================

This board configuration builds a minimal Linux system for MyBoard.

Build:
  make myboard_defconfig
  make

The output images can be found in output/images/:
- bzImage: Linux kernel
- rootfs.cpio: Root filesystem
- rootfs.iso9660: Bootable ISO (hybrid)

To test with QEMU:
  qemu-system-x86_64 -cdrom output/images/rootfs.iso9660 -m 512M