Number
=======
1-1 

Attack type
===========
Print attack (Direct presentation of NIR image)

Overview
========
NIR vein image needs to be captured from the user using the vein scanner
or digital camera so it may not be possible to capture it from the user 
without being noticed in the normal situation however, attacker can capture 
the vein image, for example, when user is sleeping. 

Input
======
Digital image of target user’s vein that meet the following conditions:
-	captured by the tool specified in the “Tools”
Research papers listed in Appendix X. 2-1 "Capture the vein image” 
explain how to capture the vein image in detail.

Tools
=====
Available vein scanner (See Appendix X. 2-1). Evaluator may use any type 
of scanner as described in 2-1.

Recipe
======
Attacker prints target user’s vein image on paper. There is no special 
requirement for the paper and printer as described in the Appendix X. 2-3-1 
"Create and present the PAI for print attack”. 

Variations
==========
tbd

Prerequisite
============
Target user turns on the vein unlock and registers user’s vein image 
following instructions provided by the device and manual. If the ST covers 
the multiple configurations for vein unlock, the same test should be done 
for all configurations.

Presentation
============
Attacker presents the paper to the device by hand at controlled environment 
where the background of the scene is uniform, the light in the office is 
switched on and the window blinds are down. Attacker adjusts it to right distance 
so that the device camera can’t see the edge of paper. Attacker also presents 
the paper to minimize the reflection from ambient lighting.

PAD technique
=============
The blood flow through the vein can be magnified to measure its liveness 
[Raghavendra et al., 2015]. The TOE can implement such logic to detect presentation 
attacks. Other PAD techniques are also available (For example, see 
[Kashif Shaheed et al., 2018])

Reference
=========
[Raghavendra et al., 2015]  
http://publications.idiap.ch/downloads/papers/2015/Raghavendra_BTAS_2015.pdf

[Kashif Shaheed et al., 2018]  
https://www.mdpi.com/2078-2489/9/9/213/pdf

Attack Potential
================
tbd

Pass Criteria
=============
All unlock attempts shall be rejected. Proposed algorisms in the existing 
research paper are capable to detect this primitive attack.

Other
=====
Number of users: 5
Number of Presentations: 10 attempts
