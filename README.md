# Nav-Suite
An integration and minor tweaking of Archaegeo's Waypointing, Firestar99's Compass, FixerID's Autopilot, DarkyShadow's approach, my own asteroid avoidance and a couple utility scrips that I place pretty regularly.

![Package Image](Media/Package.jpg)

The majority of this work is originally done by the authors posted above. I just made them all play nice together and re-did some math so they all used the same recievers. Here are links to their original projects but do note that they are not obligated to help you figure out how this version works. These are here for reference and comparison.

[Firestar99](https://gitlab.com/Firestar99/yolol/-/blob/master/src/compass/README.md)   [Archaegeo](https://github.com/Archaegeo/Starbase/tree/main/ISAN-Waypoint%20System)   [FixerID](https://github.com/fixerid/sb-projects/tree/main/NavCas)   [DarkyShadow](https://github.com/GameName-Darkyshadow/Starbase)   [Whitestrake](https://gitlab.com/Whitestrake/yolol)

### How to install:
Download the file (named NavSuite_Bas#.fbe NavSuite_Adv#.fbe depending on which version you want) and copy it into your blueprint. Place the parts on your ship and make sure to read the module descriptions(not just the names). Put chips in slots, attach buttons, place receivers in downward L pattern as referenced in FixerID's wiki and as they are oriented in the suite. Ensure your FCU, binds, and levers use the same values(they now default to basic, but changing them isn't hard). Make sure things are named appropriately as per the .fbe and do not collide with whatever else  you have on your ship. A list of all global variables used is available[ here,](https://github.com/Thaccus/Starbase-Nav-Suite/blob/main/UsedGlobalVars.txt) but may not be complete. Tune the autopilot as per the [FAQ/Wiki.](https://github.com/Thaccus/Starbase-Nav-Suite/wiki/FAQ) Copy the rangefiders as many times as you need to cover your ship (Use the top one for the top parts etc) and be sure to include at least the top "pointing" lasers as they are used for approach. The ships folder above has some examples of ships using the suite to download if anything is unclear.

### How to use: 
Stop the ship. Enter a waypoint either by saving and/or selecting it then Loading it via Archageos Waypointing system. Press nav to go there or point at it manually with compass and go yourself.

### [FAQ/Wiki is located here](https://github.com/Thaccus/Starbase-Nav-Suite/wiki/FAQ) 
I can't know what people struggle with unless they tell me. Feel free to suggest topics or contribute them directly to the wiki.

### My question isn't in the faq/wiki. What do?
Contact me here, on reddit /u/Thaccus, or on discord Thaccus#0591(Make sure you are in one of the Starbase/SSS/Cylon discords or friend me to message me.)
