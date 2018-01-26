Number
=======
4-2

Attack type
===========
2D face, replay video attack

Overview
========
_In this attack, high quality of target user’s video is available to attacker._

The target user takes own video using the DSR camera and publishes it on the web. Attacker can download this video to create PAI. This is the same testing as High quality testing as defined in the Evaluation Activity for FIA_BVR_EXT.4.2. Evaluator can skip or do the same test again based on the result of the Evaluation Activity.

Input
======
Digital video of target user’s face that meet the following conditions:
* recorded by the DSR camera at 4K resolution.
* video was taken under controlled environment where thebackground of the scene is uniform, the light in the office is switched on and the window blinds are down
* video is taken right after the target user’s enrolment and under the same condition to reduce the possibility that the PAI is falsely rejected because of the difference of the background scene or expression
* video includes user’s full face
* target user’s face occupies about 20% of the full image
* the video length is limited to 10 seconds

Tools
=====
Any 4K screen (24 inches, 3840 x 2160 and above)

Recipe
======
1) Attacker displays target user’s face video on the screen.

Variations
==========
tbd

Prerequisite
============
Target user turns on the face unlock and registers user’s face following instructions provided by the device and manual (i.e. target user should not wear glasses, hat, beard, or heavy make-up during the enrollment if the guidance instructs not to do so) under the controlled environment.
If the ST covers the multiple configurations for face unlock, the same test should be done for all configurations.

Presentation
============
Attacker fixes the mobile device and screen at controlled environment. Attacker adjusts the distance between the screen and the device seeing relevant attack video clip or attacker adjusts to right distance so that the device camera can’t see the bezels of screen. Attacker also presents the screen to minimize the reflection from ambient lighting.

PAD technique
=============
Depth sensor can be used to detect 2D object.

Reference
=========
For example, see [9]

Attack Potential
================
tbd

Pass Criteria
=============
tbd

Other
=====
Number of users: 5
Number of presentations: 10 attempts for each PAI


