Number
=======
3-3

Attack type
===========
2D face, digital photo attack

Overview
========
The target user takes own face image using the DSR camera and upload it on the web page. Attacker can download this image to create PAI. This testing is not included in the Evaluation Activity of FIA_BVR_EXT.4.2.

Input
======
Digital image of target user’s face that meet the following conditions:
* captured by the DSR camera whose resolution is 40MP and above.
* photo was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down
* photo was taken right after the target user’s enrolment and under the same condition to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
* target user’s face occupies about 20% of the full image
* photo includes user’s full face

Tools
=====
- T.5, type 3

Recipe
======
1) Attacker downloads user’s photo image and saves it in his PC.
2) Attacker crops the face image using basic image editing software (e.g. Microsoft Paint) to enlarge it to cover as much of the screen as possible while maintaining the original image aspect ratio. If multiple options are available for enlarging the image, an option that achieve best image quality should be selected. Attacker doesn’t use image editing software (e.g. photoshop) to enhance quality of face image (such attack is considered later)
3) Attacker displays it on the screen.

Variations
==========
tbd

Prerequisite
============
Target user turns on the face unlock and registers user’s face following instructions provided by the device and manual (i.e. target user should not wear glasses, hat, beard, or heavy make-up during the enrollment if the guidance instructs not to do so) under the controlled environment.
If the ST covers the multiple configurations for face unlock, the same test should be done for all configurations.

Presentation
============
Attacker presents the mobile device to the screen by hand atcontrolled environment. Attacker adjusts the distance between the screen and the device seeing relevant attack video clip or attacker adjusts to right distance so that the device camera can’t see the edge of photo. Attacker also presents the screen to minimize the reflection from ambient lighting.

PAD technique
=============
Depth sensor can be used to detect 2D object.

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

