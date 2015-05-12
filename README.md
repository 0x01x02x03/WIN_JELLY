Full source code to a Portable Executable gpu remote access tool (RAT) PoC developed
by a member of our team.

Requirements for use:
- CUDA SDK/drivers installed
- NVIDIA Card
- Windows API

Technical Details:
According to our Windows developer, this project demonstrates a test to see if memory on GPU is resident after reboot. It copies
a dll to gpu memory and deletes the dll from disk (this dll could come over a network and NEVER touch disk). Later, even after
reboot, the dll gets searched in gpu memory, and when found, gets loaded and executed again; but not touching disk of course.
The executable code is literally in gpu at this point.