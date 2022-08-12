## Line Execution Queuing Gyro

This is an isolated yolol module that outputs the standard oreintation vectors every tick for use in navigation. It does not calibrate on its own yet, and I intend to make that happen externally.

The speed is done through firestar99's line execution queuing technique and requires many single character globals to sync states across the chips. In order to make this work and play nice with everyone else, I have isolated it on its own internal network. One side of the module has a memory chip that takes input variables and the other handles the output variables. Do not wire into anything other than the far end sockets and do not connect any of the current wiring to those sockets or the rest of your ship.

The module also includes its own internal memory socket that should keep the module ticking should the memory on either side get removed for whatever reason(I will probably bolt those chips in too)

TBH this is a lot of extra mass to get a 0.2s cycle when we can do it all on one chip for a 0.6s cycle. That being said, this is a core system on which a great many other things will be based. As such, this component and the LDTS need to operate as fast and accurately as possible.
### Used global variables: 
#### Input: Gyro Data
  - GP - GyroPitch
  - GY - GyroYaw
  - GR - GyroRoll
#### Output: Rotation Matrix
  - JX, JY, JZ - Jxyz forward unit vector.
  - Hx, HY, HZ - Hxyz rightward unit vector.
  - IX, IY, IZ - Ixyz upward unit vector.
