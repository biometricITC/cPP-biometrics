Number
=======
Iris 1-1

Attack type
===========
Iris, printed photo attack

Overview
========
_In this attack, user’s face digital image is not available but photo of the target can be used to create PAI._

Input
======
Photo of target user that meet the following conditions:
- photo was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down
- photo was taken right after the target user’s enrolment and under the same environment to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
- target user’s eyes are open and iris is mostly visible (i.e. well lit room)
- photo includes user’s full face

Tools
=====
- T.1a, type 2
- T.2, type 1
- T.3, type 1
- T.4, type 2
- M.1, type 2


Recipe
======
1) Attacker scans user’s photo image and saves it in his PC. Resolution of scanner (dpi) should be, for example, 300-600 dpi that achieves best quality of image.
2) Attacker crops the face image using basic image editing software (e.g. Microsoft Paint) to enlarge it to cover as much of the paper as possible while maintaining the original image aspect ratio. If multiple options are available for enlarging the image, an option that achieves best image quality should be selected. Attacker doesn’t use image editing software to enhance quality of face image (such attack is considered later).
3) Attacker prints it out on photo paper. Printer resolution should be, for example, 600 dpi that achieves best quality of image (set to photo print).

Variations
==========
#### Variation 1
_This variant uses different printer and paper for the same test._

Tools and Materials changes:
- T.3, type 2
- M.1, type 1

Recipe changes:
- The attacker prints at 600 dpi (or higher) to achieve the best quality print.

Prerequisite
============
Target user turns on the iris unlock and registers user’s iris following instructions provided by the device and manual under the controlled environment.
If the ST covers the multiple configurations for iris unlock, the same test should be done for all configurations.

Presentation
============
Attacker presents the photo to the device by hand at controlled environment. Attacker adjusts the distance between the photo and the device seeing relevant attack video clip or attacker adjusts to right distance so that the device camera can’t see the edge of photo. Attacker also presents the photo to minimize the reflection from ambient lighting.

PAD technique
=============
During scanning, enlarging and copying the image, lots of information like high frequency information of original face will be lost. Such changes can be detected by, for example, LBP that require relatively low computational power.

Reference
=========
There is no research paper that conduct attacks following this scenario. All PAIs were created using live image of target user, not photo image of the user in all researches.

Attack Potential
================
tbd

Pass Criteria
=============
All unlock attempts shall be rejected. Proposed algorisms in the existing research papers are capable to detect this primitive attack.

Other
=====
Number of users: 1

Number of Presentations: 10 attempts for each PAI
