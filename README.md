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

## M503

```
Send: M503
Recv: echo:  G21    ; Units in mm (mm)
Recv: echo:  M149 C ; Units in Celsius
Recv: 
Recv: echo:; Filament settings: Disabled
Recv: echo:  M200 S0 D1.75
Recv: echo:; Steps per unit:
Recv: echo: M92 X400.00 Y400.00 Z400.00 E411.00
Recv: echo:; Maximum feedrates (units/s):
Recv: echo:  M203 X300.00 Y300.00 Z12.00 E25.00
Recv: echo:; Maximum Acceleration (units/s2):
Recv: echo:  M201 X3000.00 Y3000.00 Z500.00 E3000.00
Recv: echo:; Acceleration (units/s2): P<print_accel> R<retract_accel> T<travel_accel>
Recv: echo:  M204 P1000.00 R1000.00 T1000.00
Recv: echo:; Advanced: B<min_segment_time_us> S<min_feedrate> T<min_travel_feedrate> J<junc_dev>
Recv: echo:  M205 B20000.00 S0.00 T0.00 J0.01
Recv: echo:; Home offset:
Recv: echo:  M206 X0.00 Y0.00 Z0.00
Recv: echo:; Auto Bed Leveling:
Recv: echo:  M420 S0 Z0.00
Recv: echo:  G29 W I0 J0 Z0.20000
Recv: echo:  G29 W I1 J0 Z0.11750
Recv: echo:  G29 W I2 J0 Z-0.04000
Recv: echo:  G29 W I0 J1 Z0.25500
Recv: echo:  G29 W I1 J1 Z0.01750
Recv: echo:  G29 W I2 J1 Z-0.05500
Recv: echo:  G29 W I0 J2 Z0.16750
Recv: echo:  G29 W I1 J2 Z-0.01250
Recv: echo:  G29 W I2 J2 Z-0.13250
Recv: echo:  G29 W I0 J3 Z0.08750
Recv: echo:  G29 W I1 J3 Z-0.05000
Recv: echo:  G29 W I2 J3 Z-0.10000
Recv: echo:; Servo Angles:
Recv: echo:  M281 P0 L150 U50
Recv: echo:; Material heatup parameters:
Recv: echo:  M145 S0 H180 B50 F0
Recv: echo:  M145 S1 H210 B70 F0
Recv: echo:; PID settings:
Recv: echo:  M301 P16.12 I0.54 D121.28
Recv: echo:  M304 P179.89 I25.53 D316.83
Recv: echo:; Z-Probe Offset (mm):
Recv: echo:  M851 X40.00 Y-5.00 Z-0.90
Recv: echo:; Stepper driver current:
Recv: echo:  M906 X420 Y360 Z500
Recv: echo:  M906 T0 E420
Recv: 
Recv: echo:; Hybrid Threshold:
Recv: echo:  M913 X100 Y100 Z3
Recv: echo:  M913 T0 E30
Recv: 
Recv: echo:; Driver stepping mode:
Recv: echo:  M569 S1 X Y Z
Recv: echo:  M569 S1 T0 E
Recv: echo:; Linear Advance:
Recv: echo:  M900 K0.00
Recv: echo:; Filament load/unload lengths:
Recv: echo:  M603 L0.00 U100.00
Recv: ok
```

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
