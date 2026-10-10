## Day 1 (10/10/2026), Part 1
Today I'm going to make some research on how an OS actually works (with all the ressources and links).
After some research I've found some websites and repos that are going to be usefull for this project, here they are :

- https://wiki.osdev.org
- https://github.com/tuhdo/os01
- https://www.geeksforgeeks.org/operating-systems/introduction-of-operating-system-set-1/
- https://medium.com/@Sky_higher_freak../understanding-the-computer-boot-process-60fd8fb138c4
- https://www.youtube.com/watch?v=ELTwwTsR5w8

(In short I'll suffer)<br>
To summarize, when you turn on your computer this happens :
<br>
1. You press the power button
2. This action make the power supply to provide electricity to the device's composants
3. It start the BIOS (old way) or the UEFI (modern way), it's a built-in program (on the motherboard) that will prepare the device's hardware to run the tests and later, our OS (you can read the 4th link for more details).
4. The POST (Power-On Self-Test) process starts, it'll check if the computer's hardware is working properly (for example if RAM (Random Access Memory) is missing, it will return an error and stop the device)
5. When the POST end, the bootloader will finally start our OS (if any bootloader is found by the BIOS or UEFI, the device will be shutted down)
6. Our OS starts and the startup process within (login page, etc...)
<br>

## Day 1 (10/10/2026), Part 2
In this project we're only gonna make the last steps, the bootloader and the OS.
So I'll direct my research on the bootloader for now, here's what I've found on it :
<br>
- https://en.wikipedia.org/wiki/Bootloader
- https://www.youtube.com/watch?v=E_n0VtGSZQY
- https://infosecwriteups.com/writing-a-bootloader-931da062f25b

<br>
Hell yeah, we're doing that, not today cause I need to learn more about that but maybe tomorrow.
We need to know that there's multiple mode in the boot execution (while the kernel in booting) here they are :
<br><br>

- **Real Mode** : It's a mode by default made by manufacturers to support old OS, the problem is : we just have 1MB of RAM and it uses a simple segmentation memory model (Segment:Offset) that isn't very secure... But there's another problem, in that mode, any program can have access to any memory location or hardware directly.
- **Protected Mode** : This mode is exactly what we need to have. It allows us to have 4GB of RAM (4000 times the real mode allowance !)
- **Long Mode** : It extends Protected Mode to support massive memory addresses and 64-bit registers.

<br>

But also, the bootloader code need to be in what is called the "boot sector", it's always the first 512 octets of your SSD and it needs to have this signature at the end of the 512 octets : `0xAA55`
(it can also be any other storage device that have these properties). <br>
I'll continue tomorrow, good night guys.
