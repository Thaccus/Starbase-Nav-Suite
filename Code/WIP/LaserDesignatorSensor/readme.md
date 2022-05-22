## Laser Designator Translation Sensor
### Warning: I am convinced that this sensor is erroneus. It's good enough at full forward speed and does detect lateral of movement and some form of relative magnitude, but this does not track accurate lateral speed at all speeds and should never be taken as gospel. There exists sideways speeds by which the total distance to sensor could be 10 and thus report an absolute speed of 0. I think that in order to do this right, we need more laser sensors on the other axes and some trig to subtract the extra distance added by the deflection from the axes' distances and get speed that way.

Outputs relative translation of the ship to RA and splits it into RX, RY, RZ. You can use this to do strafe arresting. 
It is also notably smaller/lighter than the required size CLF to do all speeds in all directions.

Currently requires a 30FPS frame limit and VSYNC off. We can make a 60/90/120 fps version with some sensor data from a stronger computer. 
Contact me if you'd like to put in the work.

Also requires calibration every time you move it in the designer. Move it around by 10000ths(you can enter values tha are below the decimal precision of the translation tool readout and have them work, but you still can't read that precision so remember what you entered) umtil SX and SY are zeroed when the designator is on.

Still very much WIP
