# freeDSP Classic SMD B
I needed a crossover for my speakers. Now if you try googling "3-way stereo crossover" you won't find much under 200$CAD that has good reviews. 

I did find some good 3-way mono active crossovers at Xkitz. The only problem with this is that to change the XO frequency, you have to change the 10-resistor pack. There aren't any knobs on potentiometers or anything. Buying these cost 180$CAD  with shipping, and that's without any power circuitry, or any connectors for the enclosure.

Then I came across the miniDSP package. The 2x input, 4x output miniDSP goes for around 275$USD (way too expensive for me). Then I looked at the 2x input, 8x output miniDSP board, and that one went for like 400$USD. 

I then found an open source DSP module. This was awesome!! So I looked at the freeDSP Aurora, the 8x in, 8x out, DSP board, but when I made the bill of materials (BOM), it ended up costing around 280$CAD just for parts, with no circuits or connectors. Instead, I decided to build 2 of the freeDSP Classic. That would give me 8 outputs and I could connect the two right and left inputs on each board.

I made the BOM from the part list and among Arrow Electronics, Digikey, and Mouser to get the best prices possible, everything ended up costing around 170$CAD. This costs almost as much as the active crossover module for Xkitz, but with this DSP module, I can do:

- Digital crossovers
- Digital room correction
- Subwoofer integration
- Musical effect units
- System equalization
- Delay compensation
- Bass enhancement

This all happens in the "digital world" so most of the cost for parts was in audio processing chips, ADCs, and DACs.

I ordered the boards on JLCPCB. They produced 5 boards for 2$ and I got them around 1-2 weeks later. 

Once all the parts arrived, I started soldering everything to the board. This being my first experience with SMD soldering, of course, I did some things wrong and learned from them. My first mistake was soldering all of the resistors and capacitors on first. This sounded right, solder the high volume parts first, but once I got to soldering the audio processing chip (whose leads were really small and close to one another), I messed up. Because of this, I had to order more of those chips (12$ each) and try again on another of the 5 boards that I had ordered. I had to desolder every part using solder wick. It was pretty tedious. Lesson learned: solder the most expensive/finest parts first.

Everything soldered and ready to go, I hooked it up to my Arduino programmer, but it didn't work. I also tried connecting to the board via an EEPROM bootloader that FreeDSP recommends, but that still didn't work. I spent several hours trying to get it to work, but nothing did. 

So I decided to abandon this expensive soldering tutorial and buy pre-built MiniDSP boards.

# MiniDSP 2x4 Kit

Since I needed 6 output channels, I ordered two MiniDSP 2x4 Kits, a class-D 6-channel amplifier, and a 36V DC power supply for the amplifier. The MiniDSP boards were super easy to interface to using the MiniDSP software and it was straightforward to create the crossovers I needed for my speakers.

An enclosure for all of this equipment was built from wood and spare aluminum I had at home:
