# UNILAB three-chip-plus-clone
**A clone of the main UNILAB 6502 learning board, part number 540.300**<BR><BR>
Features & changes over the [original UNILAB educational system](http://retro.hansotten.nl/6502-sbc/three-chips-plus/):
- Compatible with 6502/6522 or newer 65C02/65C22 fully static parts
- 1Mhz crystal replaced with oscillator module (more readily available)
- Internal/external clock selectable by jumper
- Address bus, Data bus, R/W and Clock available on headers to be compatible with [Ben Eater](https://eater.net/6502)'s [Arduino Mega Moitor](https://eater.net/downloads/6502-monitor.ino)
- Compatible with original three-chip-plus I/O peripheral boards, Program Memory Board, and Program Loader
- Original PCB form factor (yes, rather large by today's standards but I went for originality
- **SEE NOTE AT THE BOTTOM OF THIS PAGE FOR A NECESSARY ISS1 board error and modification**

## Assembled PCB:
![20210531_134609](https://user-images.githubusercontent.com/55007357/120241082-e6ab7f00-c216-11eb-8ed4-8fbd778f3e9d.jpg)

## Schematic:
<img width="928" alt="Screenshot 2021-05-31 at 13 50 02" src="https://user-images.githubusercontent.com/55007357/120241232-26726680-c217-11eb-8cc0-2bece0b193e3.png">

## ERROR and correction for ISS1 schematic and PCB
Note: there are two errors on the ISS1 schematic and boards:
1) Polarity of POWER IN is reversed on the PCB legend (but correctly diode-protected)
2) Clock error, where U4 (the 6522 pin 25) should be driven with PHI2 (same phase as U5, the 6502) and U2 pins 2,10,12 should be driven with ~PHI2 (inverted phase compared to the 6502 and 6522).  Correcting this involves two track breaks and two wires being fitted to the PCB as below (one on the component-side below the socket of U3, one on the solder-side):
<img width="500" alt="Modification 1" src="https://user-images.githubusercontent.com/55007357/120245365-cfbe5a00-c221-11eb-8941-e102bca19593.jpg">
<img width="500" alt="Modification 2" src="https://user-images.githubusercontent.com/55007357/120245372-d51ba480-c221-11eb-932b-b565db8e1e8d.jpg">
