This simple gambas systray application will control 2 alsa mixer sliders.
I wrote it because my audiophile 2496 (ICE1712) doesn't have a master control.
Use the mousewheel over the trayicon to change both controls, click it to popup the sliders.
If you have an ICE1712 chip, then you may want to launch this way:

ICE1712Master 0 DAC,0 DAC,1
Where 
- 0 is the Card ID (use 1 or whatever if you have more than 1 soundcard)
- DAC,0 Is the left Analog channel
- DAC,1 Is the right Analog channel

(The above parameters are the default)



This application requires gambas and alsa-utils.

Compiling it:
-----------------------------
After you installed gambas 3, just checkout and compile that way:

 git clone https://github.com/kokoko3k/ice1712master.git
 cd ice1712master
 /path/to/gambas/binaries/gbc3 -e -a -g -t -p -m
 /path/to/gambas/binaries/gba3
 ./ice1712master 
