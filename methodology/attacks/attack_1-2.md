Number
=======
1-2

Attack type
===========
2D face, printed photo attack

Overview
========
_This attack scenario changes how to present the PAI and warp it to try to simulate facial motion._

Target user is privacy aware. The user doesn’t publish any face images on the internet or user shares them with only limited members so user’s digital face images are not available to attacker. However, the user places photo of user with friends or family on the desk. Attacker can scan such picture to make PAI.

Input
======
Photo of target user that meet the following conditions:
- printed on 5 × 7-inch glossy photo paper
- camera resolution is 6MP (Mega Pixels) and above
- photo was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down
- photo was taken right after the target user’s enrolment and under the same environment to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
- target user’s face occupies about 20% of the full image
- photo includes user’s full face

Tools
=====
- T.2
- T.3
- M.2


Recipe
======
1) Attacker scans user’s photo image and saves it in his PC. Resolution of scanner (dpi) should be, for example, 300 dpi that achieves best quality of image
2) Attacker crops the face image using basic image editing software (e.g. Microsoft Paint) to enlarge it to cover as much of the paper as possible while maintaining the original image aspect ratio. If multiple options are available for enlarging the image, an option that achieves best image quality should be selected. Attacker doesn’t use image editing software to enhance quality of face image (such attack is considered later).
3) Attacker prints it out on a standard office paper. Printer resolution should be, for example, 300 dpi that achieves best quality of image.

Variations
==========
tbd

Prerequisite
============
Target user turns on the face unlock and registers user’s face following instructions provided by the device and manual (i.e. target user should not wear glasses, hat, beard, or heavy make-up during the enrollment if the guidance instructs not to do so) under the controlled environment.
If the ST covers the multiple configurations for face unlock, the same test should be done for all configurations.

Presentation
============
Attacker warps the photo and present it to the device by hand at controlled environment. Attacker adjusts the distance between the photo and the device seeing relevant attack video clip or attacker adjusts to right distance so that the device camera can’t see the edge of photo. Attacker also presents the photo to minimize the reflection from ambient lighting.

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

