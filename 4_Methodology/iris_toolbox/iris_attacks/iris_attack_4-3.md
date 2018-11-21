Number
=======
Iris 4-3

Attack type
===========
Iris, digital photo attack

Overview
========
_This attack scenario changes the spoofing medium from the paper to the screen._

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
- T.4, type 2
- T.5, type 2

Recipe
======
1) Attacker downloads user’s photo image and saves it in his PC.
2) Attacker crops the face image using basic image editing software (e.g. Microsoft Paint) to enlarge it to cover as much of the screen as possible while maintaining the original image aspect ratio. If multiple options are available for enlarging the image, an option that achieve best image quality should be selected. Attacker doesn’t use image editing software (e.g. Photoshop) to enhance quality of face image (such attack is considered later)
3) Attacker displays it on the screen.

Variations
==========
#### Variation 1
_This variant uses the camera in a night mode to attempt to acquire an IR/NIR image of the iris._

Input changes:
- Unless the camera can operate in a night mode while in a fully-lit room, the conditions of the room must be adjusted to provide a better likelihood of using the IR/NIR range of the camera (i.e. low light).

Tools and Materials changes:
- T.1b, type 3

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
