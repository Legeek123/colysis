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
