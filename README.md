# My Personal Fork of Marlin 3D Printer Firmware

![Photo](IMG_9062.jpg?raw=true "Photo")

## Use this at your own risk!

This config is quite specific to my heavily modded Anet A8.

## Mod List

1. [AM8 Frame](https://www.thingiverse.com/thing:2263216)
2. [2040 Frame Extension](https://www.thingiverse.com/thing:3540836) (lost 10mm of Y axis from the original setup, remember to add 20 mm for the Y frame)
3. [2020 Filament Guide](https://www.thingiverse.com/thing:4174461)
4. Mosfet for hotend (because I already have it for the bed on previous mod)
5. [X belt tensioner](https://www.thingiverse.com/thing:2193858)
6. Fiberglass reinforced timing belt (for X and Y)
7. Extruder:
   1. Trianglelab Titan Extruder ([Mount](https://www.thingiverse.com/thing:3807114))
   2. E3D V6 hotend + Volcano heatblock (clone)
   3. 18mm compatible Z-probe
   4. Spriya fan duct
8. Magnetic textured PEI build plate (also have the untextured one, but I hardly use it)
9. AC bed heater controlled with SSR
10. [Better Y-belt clamp](https://www.thingiverse.com/thing:2249112)
11. Meanwell 350Watt PSU
12. BigTreeTech SKR v1.3 + TMC2209s (and Z-splitter)
13. BigTreeTech TFT24 Screen (although I hate it. I'll replace it as soon as I have the time)
14. Raspberry Pi 3B+ running OctoPi.
15. Acrylic enclosure.

As you can see, almost everything from the A8 has been replaced. The only stock parts are the X, Y, Z motors, and the guide rods. And the bed frame. But it is at the point where it is as good as my 2D printer. Just pop the model into PrusaSlicer, send to OctoPi, and wait a bit.

## Todo

- ~~List all the changes from the original Anet A8~~
- Add more things todo? Seriously, my printer is quite *complete*

## Credits

The current Marlin dev team consists of:

 - Scott Lahteine [[@thinkyhead](https://github.com/thinkyhead)] - USA &nbsp; [Donate](http://www.thinkyhead.com/donate-to-marlin)
 - Roxanne Neufeld [[@Roxy-3D](https://github.com/Roxy-3D)] - USA
 - Chris Pepper [[@p3p](https://github.com/p3p)] - UK
 - Bob Kuhn [[@Bob-the-Kuhn](https://github.com/Bob-the-Kuhn)] - USA
 - Erik van der Zalm [[@ErikZalm](https://github.com/ErikZalm)] - Netherlands &nbsp; [![Flattr Erik](https://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=ErikZalm&url=https://github.com/MarlinFirmware/Marlin&title=Marlin&language=&tags=github&category=software)

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
