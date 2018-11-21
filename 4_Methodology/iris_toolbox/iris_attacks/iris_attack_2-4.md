Number
=======
Iris 2-4

Attack type
===========
Iris, digital photo attack

Overview
========
_Attacker uses image editing software (e.g. Photoshop) to enhance the image quality to create PAI and repeat the attack scenario No. 2-1, 2-2 and 2-3._

_**It isn't clear whether this is really relevant to this attack. Taking the image and directly printing it would be left to the camera to be doing any image modification that could be "fixed" by other software. This probably depends a lot on the specific camera/device being used to take the photo. If a level of resolution is defined high enough this may not be needed (not sure what that resolution would be, maybe 12MP or something).**_

Input
======
Digital image of target user that meet the following conditions:
- captured by the mobile device camera whose resolution is at least equal to the front-facing camera of the device to be tested (or to use a second device of the same model). Evaluator shall not use the specific mobile device that embeds the TOE (because the TOE may be trained using images captured by the mobile device)
* photo was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down
* photo was taken right after the target user’s enrolment and under the same condition to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
* target user’s face occupies about 20% of the full image
* photo includes user’s full face

Tools
=====
- T.5, type 2

Recipe
======
1) Attacker downloads user’s photo image and saves it in his PC
2) Attacker crops the face image using image editing software to enlarge it to cover as much of the paper or screen as possible while maintaining the original image aspect ratio. If multiple options are available for enlarging the image, an option that achieve best image quality should be selected.
3) Attacker use image editing software (e.g. Photoshop) to enhance quality of face image. Especially evaluator can try to remove the artefacts such as moiré pattern with such software.
4) Attacker displays it on the paper or screen.

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
None of research paper studies this scenario.
However, image editing software can be purchased at low cost.

Reference
=========
None

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
