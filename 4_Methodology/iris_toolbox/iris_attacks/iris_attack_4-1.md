Number
=======
Iris 4-1

Attack type
===========
Iris, printed photo attack

Overview
========
_This scenario is same as No. 2-1 except high quality of user’s image and spoofing medium are used instead of the normal quality ones._

Input
======
Digital image of target user that meet the following conditions:
- captured by the DSR camera whose resolution is 40MP and above.
- photo was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down
- photo was taken right after the target user’s enrolment and under the same condition to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
- target user’s eyes are open and iris is mostly visible (i.e. well lit room)
- photo includes user’s full face

Tools
=====
- T.1a, type 3
- T.3, type 1
- T.4, type 2
- M.1, type 2

Recipe
======
1) Attacker prints it out on photo paper. Printer resolution should be, for example, 600 dpi that achieves best quality of image (set to photo print).

Variations
==========
#### Variation 1
_This variant uses different printer and paper for the same test._

Tools and Materials changes:
- T.3, type 2
- M.1, type 1

Recipe changes:
The attacker prints at 600 dpi (or higher) to achieve the best quality print.

#### Variation 2
_This variant uses the camera in a night mode to attempt to acquire an IR/NIR image of the iris. Only the laser printer is used as the image is not in the full visible spectrum (if any), so a high-quality laser print is sufficient._

Input changes:
- Unless the camera can operate in a night mode while in a fully-lit room, the conditions of the room must be adjusted to provide a better likelihood of using the IR/NIR range of the camera (i.e. low light).

Tools and Materials changes:
- T.1b, type 3
- T.3, type 2
- M.1, type 1

Recipe changes:
- The attacker prints at 600 dpi (or higher) to achieve the best quality print.

Prerequisite
==========
Target user turns on the iris unlock and registers user’s iris following instructions provided by the device and manual under the controlled environment.
If the ST covers the multiple configurations for face unlock, the same test should be done for all configurations.

Prerequisite
============
Target user turns on the iris unlock and registers user’s iris following instructions provided by the device and manual under the controlled environment.
If the ST covers the multiple configurations for face unlock, the same test should be done for all configurations.

Presentation
============
Attacker presents the photo to the device by hand at controlled environment. Attacker adjusts the distance between the photo and the device seeing relevant attack video clip or attacker adjusts to right distance so that the device camera can’t see the edge of photo. Attacker also presents the photo to minimize the reflection from ambient lighting.

PAD technique
=============
Depth sensor can be used to detect 2D object. ???

Reference
=========
For example, see [Bhattacharjee & Marcel, 2017]

Attack Potential
================
tbd

Pass Criteria
=============
tbd

Other
=====
Number of Users: 5

Number of presentations: 10 attempts for each PAI
