## How to compile and use this code ?
- **Step 1 :** You need to install make, nasm and qemu first to do this.
- **Step 2 :** Execute `make all` in the 'bootloader' directory, you will get a new file called boot.bin in the 'bin' directory.
- **Step 3 :** Now, we'll use Qemu to test our binary with `qemu-system-x86_64 -hda ./bin/boot.bin`
- **Step 4 :** It's done !
