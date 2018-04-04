Number
=======
2-3

Attack type
===========
2D face, digital photo attack

Overview
========
_This attack scenario changes the spoofing medium from the paper to the screen._

The target user takes own face image using the smartphone with low-resolution and publishes it on the profile page. Attacker can download this image to create PAI. This testing is not included in the Evaluation Activity of FIA_BVR_EXT.4.2.

Input
======
Digital image of target user’s face that meet the following conditions:
* captured by the mobile device camera whose resolution is 6MP and above. Evaluator shall not use the mobile device that embeds the TOE (because the TOE may be trained using images capturedby the mobile device)
* photo was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down
* photo was taken right after the target user’s enrolment and under the same condition to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
* target user’s face occupies about 20% of the full image
* photo includes user’s full face

Tools
=====
- T.5, type 2

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
Attacker presents the mobile device to the screen by hand at controlled environment. Attacker adjusts the distance between thescreen and the device seeing relevant attack video clip or attacker adjusts to right distance so that the device camera can’t see the bezels of screen. Attacker also presents the screen to minimize the reflection
from ambient lighting.

PAD technique
=============
Different types of image aliasing appear during the recapture of a face image that can be detected by the PAD. [Patel et al., 2015] study the PAD method that can be implemented on the mobile device.

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

