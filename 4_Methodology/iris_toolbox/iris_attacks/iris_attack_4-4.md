Number
=======
Iris 4-4

Attack type
===========
Iris, printed photo attack

Overview
========
_This scenario is same as No. 2-1 except normal quality of user’s image is used with professional photo printing are used instead of the low quality ones._

Input
======
Digital image of target user that meet the following conditions:
- captured by the mobile device camera whose resolution is at least double the resolution of the device to be tested (or to use a second device of the same model). Evaluator shall not use the specific mobile device that embeds the TOE (because the TOE may be trained using images captured by the mobile device)
- photo was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down
- photo was taken right after the target user’s enrolment and under the same condition to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
- target user’s eyes are open and iris is mostly visible (i.e. well lit room)
- photo includes user’s full face

Tools
=====
- T.1a, type 3
- T.3, type 3

Recipe
======
1) Attacker has photo printed at professional printing service.

Variations
==========
tbd

Prerequisite
==========
Target user turns on the iris unlock and registers user’s iris following instructions provided by the device and manual under the controlled environment.
If the ST covers the multiple configurations for face unlock, the same test should be done for all configurations.

Presentation
============
Attacker presents the photo to the device by hand at controlled environment. Attacker adjusts the distance between the photo and the device seeing relevant attack video clip or attacker adjusts to right distance so that the device camera can’t see the edge of photo. Attacker also presents the photo to minimize the reflection from ambient lighting.

PAD technique
=============
Different types of image aliasing appear during the recapture of the image that can be detected by the PAD. [Patel et al., 2015] study the PAD method that can be implemented on the mobile device.

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
Number of Users: 5

Number of Presentations: 10 attempts for each PAI
