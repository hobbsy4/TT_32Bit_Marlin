# TT_32Bit_Marlin e3 mini 2.0 with TFT35 3.0

This works well with my 32 bit BTT e3 mini 2.0 with a Standard Tevo Tarantula. 

The printer is named after Dad's dog. You can change your name in line 135. 

A few points: 



PID heating is used for hot end and bed. The bed heating works well with the stock 12v bed and 5mm glass top. Tune your PID and change in lines 495 - 497. I'm using an e3d v6.
Your PID settings will be different. 
You will need to define your hot end (1 for stock, I believe) in line 442 - the description for all hot ends is from line 350.

I'm using a BMG extruder and it is geared. You will need to adjust the extrusion (line 753) to match your extruder. You should also calibrate it. 100 was the stock value. 

The acceleration for the extruder (line 775) is set to 10000 but you should reduce this to a lower value (perhaps 2500) to begin. My other acceleration values seem OK with my set up but I've just gone to linear rails. Reduce or increase as required. 

Skew correction is enabled for my printer until I print all of Thingirobs brackets. // (comment out) the skew or adjust to suit your needs in lines 1449, 1451, 1461, 1473) (commenting 1449 alone should disable it adequately)

Raising the z after homing isn't currently enabled but I'm planning on doing this next build.

This is working well with my printer but your mileage may vary. I take no responsibility nor give warranty for the provided files. 

Cheers
Hobbsy4
