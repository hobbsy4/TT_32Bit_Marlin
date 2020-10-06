# TT_32Bit_Marlin e3 mini 2.0 with TFT35 3.0

This works well with my 32 bit BTT e3 mini 2.0 with a Standard Tevo Tarantula. 

This is a blend of 
  Jim Brown's build https://github.com/JimBrown/MarlinTarantula
  and the
  Ender 3 Example Big Tree Tech e3 Mini 2.0 example configuration files https://github.com/MarlinFirmware/Marlin
  
  I won't go through every change, but I've essentially cross checked Jim Brown's changes with the Ender 3 example, that I used as the basis for this. 

The printer is named after Dad's dog. You can change your name in line 135. 

A few points: 



PID heating is used for hot end and bed. The bed heating works well with the stock 12v bed and 5mm glass top. Tune your PID and change in lines 495 - 497. I'm using an e3d v6.
Your PID settings will be different. 
You will need to define your hot end (1 for stock, I believe) in line 442 - the description for all hot ends is from line 350.

I'm using a BMG extruder and it is geared. You will need to adjust the extrusion (line 753) to match your extruder. You should also calibrate it. 100 was the stock value. 

My z axis motor is inverted and if yours isn't, the direction will need to be changed in the firmware. Check the other motor travel directions and invert as required. 

The default max acceleration for the extruder (line 775) is set to 10000 but you should reduce this to a lower value (Ender 3 was 5000) to begin. My other acceleration values seem OK with my set up but I've just gone to linear rails. Reduce or increase as required. I need to tune the jerk for my machine (ejerk at 15 seems too high). Ender 3 was 10. 

Skew correction is enabled for my printer until I print all of Thingirobs brackets. Comment Out (//) the skew or adjust to suit your needs in lines 1449, 1451, 1461, 1473) (commenting 1449 alone should disable it adequately)

Raising the z after homing isn't currently enabled but I'm planning on doing this next build. Also, it annoys me before beginning a print that it goes up and down too many times at the 0,0 position and can accumulate oozed filament, but this is also to be fixed. 

Don't forget to reset your eeprom after flashing, or else bang-bang etc that may have been enabled in your old firmware will cause problems with heating, steps per mm, etc. 

This is working well with my printer but your mileage may vary. I take no responsibility nor give warranty for the provided files. 

Cheers
Hobbsy4
