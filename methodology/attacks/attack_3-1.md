Number
=======
3-1

Attack type
===========
2D face, printed photo attack

Overview
========
_This scenario is same as No. 2-1 except high quality of user’s image and spoofing medium are used instead of the normal quality ones. No. 2-4 is unnecessary for high-quality image because the DSR camera can automatically improve the image captured._

The target user takes own face image using the DSR camera and upload it on the web page. Attacker can download this image to create PAI. This is the same testing as High quality testing as defined in the Evaluation Activity for FIA_BVR_EXT.4.2. Evaluator can skip or do the same test again based on the result of the Evaluation Activity.

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
Printing service is used to create high quality photo.

Recipe
======
Depending on the printing service used.

Variations
==========
tbd

Prerequisite
============
Target user turns on the face unlock and registers user’s face following instructions provided by the device and manual (i.e. target user should not wear glasses, hat, beard, or heavy make-up during the enrollment if the guidance instructs not to do so) under the controlled environment.
If the ST covers the multiple configurations for face unlock, the same test should be done for all configurations.

Presentation
============
Attacker presents the photo to the device by hand at controlled environment. Attacker adjusts the distance between the photo and the device seeing relevant attack video clip or attacker adjusts to right distance so that the device camera can’t see the edge of photo. Attacker also presents the photo to minimize the reflection from ambient lighting.

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
Number of Users: 5
Number of presentations: 10 attempts for each PAI

