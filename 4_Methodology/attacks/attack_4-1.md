Number
=======
4-1

Attack type
===========
2D face, replay video attack

Overview
========
_In this attack, normal quality of target user’s video is available to attacker._

The target user takes own video using the mobile device and publishes it on the web. Attacker can download this video to create PAI. This is the same testing as Normal quality testing as defined in the Evaluation Activity for FIA_BVR_EXT.4.2. Evaluator can skip or do the same test again based on the result of the Evaluation Activity.

Input
======
Digital video of target user’s face that meet the following conditions:
* recorded by the mobile device camera at full HD resolution. Evaluator shall not use the mobile device that embeds the TOE (because the TOE may be trained using images captured by the mobile device)
* video was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down
* video is taken right after the target user’s enrolment and under the same condition to reduce the possibility that the PAI is falsely rejected because of the difference of the background scene or expression
* video includes user’s full face
* target user’s face occupies about 20% of the full image
* the video length is limited to 10 seconds

Tools
=====
- T.5, type 2

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
Different types of image aliasing appear during the recapture of a face image that can be detected by the PAD. [4] study the PAD method that can be implemented on the mobile device.

Reference
=========
For example, see [Zhang et al., 2012], [Patel et al., 2015] and [Boulkenafet et al., 2017]

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


