# AAS+StrafeArrest+EmergencyStop Package

This set 4 chips uses the LDTS to improve on the longstanding asteroid avoidance regime. It does so by arresting lateral motion after the AAS finishes dodging so that you do not drift into new obstructions. As a bonus, the same code can be used to create an emergency stop button that will counter all motion regardless of facing until the ship comes to a full stop. I have included in this upload a small ship that was built using the newest NavSuite release candidate set and includes this new feature set.

I am using PD control and you can tune them to your liking through the x/y and xd/yd variables in either MovementArrest chip.

The strafe arrest system wants to affect the same control fields that AAS does and I have remade the AAS code such that it no longer assigns to computer controls unless it detects something. Unfortunately I could not find a way to do that elegantly on the single line that was the old AAS_Strafe and as such this new version is a two line operation. If anyone wants to have a go at compacting the behavior back down to one line I would be happy to outline the problem and desired behavior.

On a happier note: this version has a control hierarchy. ESTOP always has priority and pressing the big red stop button turns off any other computer controls Like AAS/NAV/Cruise. AAS is next in line priority wise and will take control during any avoidance action. Finally and should nothing else take priority, the strafe arrest code will ensure that you are not moving laterally. 

Strafe arrest(being the last in line) is suspended via chipwaiting during any avoidance action. I heard that this may affect LEQ systems and I will be testing this claim during the system's stay here in the WIP world. To be clear this is most definitely WIP and will be undergoing extensive testing before it ever comes to the NavSuite. If you would like to be part of testing the next generation of avoidance, I welcome any feedback you come up with. If you just want stability and things that you know work, I respect that and recommend you stick to the AAS included in the current release until this gets more thoroughly vetted.
