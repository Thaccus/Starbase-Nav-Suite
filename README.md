# Nav-Suite
An integration and minor tweaking of Archaegeo's Waypointing, Firestar99's Compass, FixerID's Autopilot, my own asteroid avoidance and a couple utility scrips that I place pretty regularly.

The majority of this work is originally done by the authors posted above. Here are links to their original projects but do note that they are not obligated to help you figure out how this version works. These are here for reference and comparison.

https://gitlab.com/Firestar99/yolol/-/blob/master/src/compass/README.md

https://github.com/Archaegeo/Starbase/tree/main/ISAN-Waypoint%20System

https://github.com/fixerid/sb-projects/tree/main/NavCas

https://gitlab.com/Whitestrake/yolol

How to install: Download the .fbe, put chips in slots, attach buttons, place receivers in downward L pattern as referenced in FixerID's wiki. Ensure your FCU, binds, and levers use the 3 letter standard in the example FCU. Set FWD lever re-center field to CRUS. Make sure things are named appropriately as per the .fbe. A list of all global variables used is avaiable, but may not be complete. Tune the autopilot as per navCas wiki. I'll make a more in-depth guide on tuning my changes in the coming days. Copy the rangefiders as many times as you need to cover your ship. Use the top one for the top parts etc.

How to use: Stop the ship. Enter a waypoint either by saving and/or selecting it then Loading it via Archageos Waypointing system. Press nav to go there or point at it manually with compass and go yourself.

FAQ: 

 My auto pilot is dumb and won't align! How do I tune it to be smarter?
 
 There are four tunables: on line two there are PT(pitch target), YT(yaw target), RT(roll target), and on line 20 there is a check against chill. Ideally you want PT and YT to be a value that will turn you ~30 degrees on an instant input. They will be multiplied by how close you are to proper alignment and if they arent large enough you may never reach proper alignment. If you have recenter at 100 and pt/yt100 aren't enough(big ship/low thrust problems), you may have to settle for lowering the recenter value 50/25/20/10/5 will extend the burn but you will need to wait for them to end(see chill). Roll just does minor error correction so 10 degrees is more than enough. In any case chill is by far one of the most important factors. It is important that the ship come to a full rotational stop before asking it where it is going again. ISAN is most accurate when still and you are likely trying to point at something far away. If your ship is large, increase chill untill there is at least .4 seconds of stopped rotation between each alignment burn. I know the watiting hurts, but trust me that it is faster and more accurate to have a bit of wait.

 I cant get X to work in combination with your system what am I doing wrong?
 
 Integration hell is real and you have just stepped into it. Welcome :) I have provided a list of all global variables and what they are used for in UsedGlobalVars.txt Ensure you are not overlapping unintnetionally, then trace each variable you intentionally overlap though the chips to understand them.
