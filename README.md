# anduril-ui

My notes & tweaks to [ToyKeeper's](http://toykeeper.net/) excellent [anduril UI](https://code.launchpad.net/~toykeeper/flashlight-firmware/fsm)


## reqs
`sudo apt-get install binutils gcc-avr avr-libc uisp avrdude`

## compiling
```
# from spaghetti-monster/anduril/
make all

# clean up
make clean
```

## flashing
### test connection
`avrdude -p t#### -c usbasp -n`, e.g. `avrdude -p t1634 -c usbasp -n` for attiny1634

### flash bin
`avrdude -p t#### -c usbasp -u -Uflash:w:TARGETHEXFILE.hex` e.g. `avrdude -p t1634 -c usbasp -u -Uflash:w:anduril.noctigon-kr4-russ.hex`


## aux color mapping
```
const PROGMEM uint8_t rgb_led_colors[] = {
    0b00000001,  // 0: red
    0b00000101,  // 1: yellow
    0b00000100,  // 2: green
    0b00010100,  // 3: cyan
    0b00010000,  // 4: blue
    0b00010001,  // 5: purple
    0b00010101,  // 6: white
};

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
