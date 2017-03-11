Use G29 to print current mesh

        X1        X2      X3
Y1:   2.92500  3.80000  4.10000
Y2:   3.05000  3.70000  4.05000
Y3:   3.02500  3.62500  3.90000

`G29 S1` will initiate the bed leveling, homing and traveling to the first point to probe.

Then use your preferred Printer controller program, i.e. Printrun, to lower the hotend until it touches the bed. Using a paper to feel the distance when it gets close.

`G29 S2` will store the point and travel to the next point until last point has been probed.

`G29 S3 Xn Yn Zn.nn` will modify a single probed point.

G29 S3 X1 Y1 Z2.92500
G29 S3 X2 Y1 Z3.80000
G29 S3 X3 Y1 Z4.10000
G29 S3 X1 Y2 Z3.05000
G29 S3 X2 Y2 Z3.70000
G29 S3 X3 Y2 Z4.05000
G29 S3 X1 Y3 Z3.02500
G29 S3 X2 Y3 Z3.62500
G29 S3 X3 Y3 Z3.90000

---

To reset EEPROM:

M502: Reset current settings to defaults, as set in Configurations.h
M500: Make it persistent