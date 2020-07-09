# anduril-ui

My notes & tweaks to ToyKeeper's excellent [anduril UI](https://code.launchpad.net/~toykeeper/flashlight-firmware/fsm)


## reqs
`sudo apt-get install binutils gcc-avr avr-libc uisp avrdude`


## aux color mapping
```
0x10    low, red
0x11    low, yellow
0x12    low, green
0x13    low, cyan
0x14    low, blue
0x15    low, purple
0x16    low, white
0x17    low, rainbow
0x18    low, voltage   

0x20    bright, red
0x21    bright, yellow
0x22    bright, green
0x23    bright, cyan
0x24    bright, blue
0x25    bright, purple
0x26    bright, white
0x27    bright, rainbow
0x28    bright, voltage 

0x30    flashing, red
0x31    flashing, yellow
0x32    flashing, green
0x33    flashing, cyan
0x34    flashing, blue
0x35    flashing, purple
0x36    flashing, white
0x37    flashing, rainbow
0x38    flashing, voltage 
```
