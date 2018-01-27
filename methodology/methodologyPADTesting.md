# Evaluation Activity for FIA_BVR_EXT.4.2
12th January 2018

**_Note to the iTC members: Mobile toolbox is split into two parts. One part defines minimum functional testing that evaluators shall conduct as defined in the Evaluation Activity for FIA_BVR_EXT.4.2 without any changes. The other part provides guidance to evaluators what kind of additional tests should be done during the penetration testing in addition to the functional tests._**

This document describes Evaluation Activity for FIA_BVR_EXT.4.2

**a) Objective of the evaluation activity**
This evaluation activity defines the common minimum PAIs that all evaluator shall create and test protocol that evaluator shall follow to test the TOE. While this evaluation activity allows to develop an overall statement about the performance of the TOE with respect to its PAD mechanism, they cannot provide any assurance about the PAD functionality with respect to variations of PAIs. It falls into the focus of the vulnerability assessment to evaluate whether the use of additional PAIs that are not defined here can lead to increased error rates. During the vulnerability analysis, the evaluators will use all their knowledge that they gained during the evaluation of the other assurance classes for penetration testing.

**b) Relationship of the evaluation activity to SFRs, SARs, and other evaluation activities**
This evaluation activity can supplement all work units defined in AVA_VAN.1 for testing the FIA_BVR_EXT.4.2.
This evaluation activity doesn’t have any dependencies to other evaluation activities defined in this cPP.

**c) Tools required to perform the activity**
Minimum specification of required tools is defined in e).

**d) Required input from the developer or other entities**
None

**e) Assessment Strategy for face presentation attack**

### Overview
Face presentation attack can be carried out through the following process:
1. Get face images of a target user from, for example, uploaded photo on the SNS
2. Display or reconstruct the face image on the spoofing medium such as a photo or
screen (2D attack) or 3D face mask (3D attack). Such a fake face image displayed on
the spoofing medium used for the presentation attack is called a PAI (Presentation
Attack Instrument)
3. Present the PAI to the TOE

The current research categorizes face presentation attacks into the following types based on the spoofing medium used and how the face image is recorded.
- 2D face, printed photo attack
- 2D face, digital photo attack
- 2D face, replay video attack
- 3D face, mask attack

All of above types except 3D face, mask attack shall be tested in this evaluation activity. 3D face, mask attack is out of scope because the cost of creating 3D face mask doesn’t match to the assurance required by the cPP.

In any type of attack, the TOE captures the fake face image from the spoofing medium and unlock the mobile device if the TOE can’t tell the difference between real and fake face.

### Type of PAIs for the testing and required tools
Face images captured by the TOE from the spoofing medium may visually look very similar to the images captured from real ones, however, they are not exactly the same. For example, printed or displayed faces on the paper or screen reflect light in different ways because a human face is a complex non-rigid 3D object, whereas the photo or screen can be seen as a planar rigid object. The surface properties of real faces and fake ones, e.g. pigments, are also different. In addition, fake faces may contain artefacts such as moir ́e patterns that are an undesired aliasing of images produced during various image display and image acquisition processes.

The TOE should detect such differences between images taken from real and fake face to prevent the presentation attacks. These differences are mainly influenced by the following factors listed in the table below and the performance of the PAD algorithm may also be affected by them.

| No	| Factor	| Description |
|-------|---------------|-------------|
|1	|Quality of source face image from which the PAI is created | The quality of the source is the foundation of the copy (i.e. PAI). If the source image is poor quality, the quality of PAI will also be limited. Source face images can be taken with a digital camera and quality of digital image varies depending of quality of the camera (e.g. size of sensor and resolution) |
|2	| Quality of tools (e.g.printer and spoofing medium) to create the PAI | A poor quality PAI can be made from a good quality source if the resolution of the printer or screen is low. However, if the screen is 4K resolution that refers to a horizontal screen resolution in the order of 4,000 pixels, it can provide the finest clarity and detail of the face from the good quality source. |

Various quality of PAIs can be created with, for example, smartphone cameras, compact or high-professional digital cameras however, it’s time consuming to create all possible PAIs using different devices. Therefore, this evaluation activity sets the two level of quality, normal and high, to cover those variety of PAIs. High quality PAIs looks more similar to the real face however, it may show more micro facial textures that can be used to differentiate between the real and fake. However, such micro textures may not be evident in the normal quality PAIs. The TOE may overlook normal quality PAIs if the PAD algorithm completely relies on such micro textures to detect the PAIs. So, this evaluation activity requires to test both levels of quality of PAIs.

- Normal quality testing
    Evaluator shall use standard tools (e.g. smartphone, printer or laptop screen) that meet the specification defined in this evaluation activity to create the PAI. All tools are normally available at home or office.

- High quality testing
    Evaluator shall use high-end tools that meet the specification defined in this evaluation activity to create the PAI. All tools are the best quality ones like high-end
production printer that may cost several thousands of dollars. However, such high-end tools can be borrowed at rental shops or used through online service (e.g. online printing service) at inexpensive price and evaluator can utilize such services to create the PAI at low cost.

The following explains that what tools should be used for both levels of testing

### Quality of source face image from which the PAI is created
Digital camera shall be used to take the digital image of target user’s face. There are three main factors that work together to influence the quality of digital image:

* The quality of the recording device (camera's optics & sensor, scanner's sensor)
  1. Normal quality testing
Any mobile devices no older than 2 years from release date. Evaluator shall not use the device that embeds the TOE (because the TOE may be trained using images captured by the device)
  2. High quality testing
Any dSLR camera (digital Single Lens Reflex camera) that can take 4K digital image and no older than 2 years from release date. dSLRs, or any large sensor camera, take much better quality digital photos than any mobile device camera.


* The size (in pixels) of the digital image.
  1. Normal quality testing
6MP (Mega Pixel) and above
  2. High quality testing
40MP and above


* The digital format it is stored in (lossless vs lossy compression).
  1. Normal quality testing
Lossy compression (e.g. JPEG)
  2. High quality testing
lossless compression (e.g. TIFF)

### Quality of tools (e.g. printer and spoofing medium) to create the PAI
For printed photo attack, evaluator shall print the face digital image on the paper. Quality of printer and type of paper plays a key role in creating good quality PAI. For example, inkjet printer is capable of producing higher detailed and photo-realistic printsthan laser printer and shall be used for normal quality testing.
There are high-end printers that can produce much better quality of photo than the home inkjet printer. These printers are expensive and not available at home or office however, there are lots of online printing service providers that use such high-end printer to produce the high-quality photo. Such services shall be used to create the PAI for high quality testing.

* Type of printer
  1. Normal quality testing
Any home inkjet printer no older than 2 years from release date. Resolution shall be 300dpi
  2. High quality testing
Depend on the online service provider


* Type of paper
  1. Normal quality testing
A3 (297 x 420mm) or ledger (279 x 432mm) printing paper
  2. High quality testing
Size of paper shall be A3 or ledger size. Paper type (e.g. glossy paper) may vary
depending on the online service providers

For digital photo and reply video attack, evaluator shall display the face digital image on the screen. Quality of PAI depends on the quality of the screen used. For example, the human eye is unable to see a difference in the accuracy of details at 240 PPI (Pixel Per Inch) on an A4 page held at 30 cm or 12 inches. The higher the PPI, the more difficult to see micro texture difference between fake and real face.

* Type of screen
  1. Normal quality testing
Any PC screen no older than 2 years from release date. 19 inches, 1920 × 1080 and above.
  2. High quality testing
Any 4K screen no older than 2 years from release date. 24 inches, 3840 x 2160
and above.

### Test protocols
The following describes the test protocol that evaluator shall follow. If the Security Target allows multiple settings for security relevant parameters, all tests have to be conducted for all possible configurations.

1) Enrollment
Evaluator turns on the face unlock and registers test user’s face following instructions provided by the mobile device and manual (i.e. test user should not wear glasses, hat, beard, or heavy make-up during the enrollment if the guidance instructs not to do so) under the controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down.

2) Creating the source still and video digital image
Digital image of target user’s face that meet the following conditions shall be taken for both normal and high-quality testing:
   1. captured by the camera that meets the specification defined in the normal and
high-quality testing
   2. digital image was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are
down
   3. digital image is taken right after the target user’s enrolment and under the same condition (i.e. under controlled environment) to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
   4. target user’s face occupies about 20% of the full image
   5. digital image includes user’s full face
   6. for reply video attack, video length shall be limited to ten seconds
   

3) Creating the PAI
Source digital image shall be printed and displayed on the spoofing mediums (i.e. paper or screen) that meet the specification defined in the normal and high-quality testing

4) Presenting the PAI to the TOE
Evaluator shall present the mobile device to the fixed and stationary spoofing mediums by hand at controlled environment for printed and digital photo attack to introduce some noticeable motion of the PAIs. For replay video attack, both of the spoofing medium and the PAI shall be stationary.
Evaluator shall adjust the distance between the spoofing mediums and the TOE so that the device camera can’t see the edge of spoofing mediums. Evaluator shall also present the spoofing mediums in a way to minimize the reflection from ambient lighting.

### Number of trials
Evaluator shall conduct the testing with five users. Two source images shall be taken for both normal and high-quality testing and two spoofing mediums (i.e. normal quality of photo and screen and high quality of photo and screen) shall be used for each user. 20 presentations shall be made for each PAI changing the distance between the TOE and spoofing medium (i.e. 120 presentations shall be made for each user)

| Attack type  | Source image   | Spoofing medium   | # subject | # presentation | 
|--------------|----------------|-------------------|-----------|----------------|
| 2D face, printed photo | Normal   | Normal    | 5 | 20 |
|   | High  | High | 5 | 20 |
| 2D face, digital photo attack | Normal   | Normal    | 5 | 20 |
|   | High  | High | 5 | 20 |
| 2D face, replay video attack | Normal   | Normal    | 5 | 20 |
|   | High  | High | 5 | 20 |

### f) Pass/fail criteria
Evaluator doesn’t need to present each PAI more than 20 times. Evaluator may learn, for example, the distance between the spoofing medium and the TOE that the TOE accepts the PAI at high probability during the presentations. Evaluator can conduct the penetration testing later utilizing such knowledge therefore evaluator doesn’t need to re-
run the testing using such knowledge for this evaluation activity.

PAD will never work with an accuracy of 100% because of the limitation of current technology of mobile devices. The following pass criteria is defined based on the performance of the state of art mobile PAD technology that was actually tested in the relevant research.

*For normal quality testing for all type of attack, the TOE shall reject more than 90% of
unlock attempts with each PAI.
Form high quality testing for all type of attack, the TOE shall reject more than 50% of
unlock attempts with each PAI.*

Above criteria marked in *italics* is initial proposal and need to be discussed later.

&nbsp;
------

# Mobile toolbox for face verification
12th January 2018

### Background

We agreed to develop “mobile toolbox” that defines PAIs that the mobile devices shall detect at minimum during the Berlin iTC meeting. I would like to propose “mobile toolbox” for the face verification in this document.
This document introduces “attack scenario” that defines, not only PAIs but also how they should be used for presentation attacks. Most of scenarios are developed based on the existing research papers that study PAD algorithms that can be implemented in the mobile devices. So, theoretically, these attack scenarios can be detected with certain probability by the mobile devices. I think that the iTC can set an appropriate goal referring experimental results described in such papers.

&nbsp;
---
&nbsp;
### 1. Evaluation Activity and Penetration testing for PAD 
Evaluation Activity of FIA_BVR_EXT.4.2 defines the minimum common testing that evaluator shall conduct without any changes. Evaluator shall also conduct the penetration testing to make sure that the TOE is resistant to attacks with PAIs by an attacker possessing a Basic attack potential. This Annex provide the guidance for the evaluator’s penetration testing.

### 2. Attack scenarios
##### 2.1 Motivation of attackers 
The TOE is used to unlock the devices but not used for financial transactions. Attacker doesn’t have strong motivation to unlock the device but tries to unlock his/her friends’ or co-workers’ mobile devices just for fun. Attacker would use any tools or materials that are normally available at home and normal office environment such as laptop PC or office printer. Attacker would also use other services such as online printing services to print a photo of target users if such services are available at low cost.
##### 2.2 Assumption from the cPP
The cPP defines A.User and evaluator shall assume that the mobile devices are configured securely by users. Especially evaluator shall make the following assumptions:

a) A user enroll him/herself following guidance provided by the TOE

b) Mobile device is securely configured and maximum number of unsuccessful biometric authentication attempts is limited.

However, evaluator can increase the maximum number of unsuccessful biometric authentication attempts to conduct the penetration testing efficiently. However, the mobile device shall be evaluated in the evaluated configuration, which means that attack needs to be succeeded within the allowed number of biometric authentication attempts defined in the ST.

The cPP also defines A.Protection and evaluators shall assume that biometric data is adequately protected. Especially evaluators shall make the following assumptions:

a) Attacker can’t access to the result of PAD subsystem so they can’t tune the PAIs based on the PAD score

b) Attacker can’t gain the templates from the mobile device to create the PAIs

##### 2.3 Attack scenarios selection and changes
Attack scenarios that shall be considered in the penetration testing are defined in chapter 3. These attack scenarios are devised considering the available target user’s face image, type of spoofing mediums (e.g. paper and screen) and tools to create the PAIs (e.g. printer) and cover all types of attacks (e.g. 2D face, printed photo attack) that have been studied in the relevant research or demonstrated in the YouTube video.

Evaluator can also skip some attack scenarios, choose the tools or materials (e.g. printer and paper) that meet the requirement defined in the scenarios considering the following factors:

a) Result of Evaluation Activity of FIA_BVR_EXT.4.2
Evaluator can skip the same attacks defined in this Annex or increase the number of
trial based on the result of the Evaluation Activity

b) Information about PAD algorithm
If evaluator can gain information about the PAD algorithm that the TOE implements through the internet, evaluator can omit some attack scenarios that may be detected by the algorithm reliably and focus on the other ones that may exploit the weakness of the algorithm.
For example, if evaluator gains the information that the TOE checks the eye blinking, evaluator should change the attack scenario No.1-2 and cut off eye part of the photo to create the PAI, instead of warping the photo.
Another example is, if the TOE uses the depth map of the face captured by near Infrared (NIR) camera for face unlock, 2D photo can be easily detected (See Bhattacharjee & Marcel, 2017). However, IR-reflective inks that show a strong response in NIR-band can be used to create the 2D photo that may be visible in the NIR-band. The accurate depth map may also not be gained if:
- Distance between the camera and face is at maximum distance
- Face unlock is conducted under the daylight
- Face is placed under a sharp viewing angle against the TOE Evaluator can consider such factors to change the tool or presentation method of the PAIs.

c) Attack information
If the step by step guide (e.g. demo on YouTube) that shows how to create the PAIs and run the attack with those PAIs is publicly available, evaluator can follow it to select the right tools. However, if such information is not available, evaluator should make own decision.

##### 2.4 Penetration test timeframe
Evaluator shall keep in mind that attacker’s motivation is low. Timeframe for the presentation attack testing is one week at maximum. As mentioned in 2.3, evaluator can
skip some attack scenarios to shorten the timeframe.

##### 2.5 Prerequisite for evaluators
Successful presentation attacks may require fine-tuning of parameters such as distance between the PAI and mobile device or lightning condition. Evaluator may learn good
parameters through the Evaluation Activity of FIA_BVR_EXT.4.2. In addition to that, there are lots of videos or presentation slides on the internet that show how presentation attack can be conducted successfully. Evaluator shall watch those videos to learn, for example, how to present the PAI or how to create the PAI to conduct the testing efficiently as much as possible.

Evaluators shall utilize such knowledge to conduct the testing assuming the worst-case scenario (i.e. attacker who doesn’t know such information choose best parameters byluck) however, such evaluator’s knowledge or experience shall be considered to rate the attack potential.

### 3. Attack scenarios
##### 3.1 Format

Each attack scenario includes following items to describe the attack. If evaluator modify the attack scenario, such modified scenario should include the following items at minimum:

&nbsp;
---
Number
=======
Number of the attack can be coded into the filname. 

Attack type
===========
This chapter contains the type of the attack. Examples for attack types include 
- 2D face, printed photo attack - 2D face, digital photo attack 
- 2D face, replay video attack *1) 
- 3D face, mask attack 
- 3D face, plastic surgery attack *2) *1) 

Overview
========
Brief overview of the attack scenario

Input
======
Target user’s face information available to the attacker

Tools
=====
Tools required to create the PAI and to perform the attack.  

Recipe
======
Method to create the PAI. Stepwise instructions.

Variations
==========
Identification of potentially useful variations to the recipe. 

Prerequisite
============
All prerequisite conditions that need to be established before the attack 

Presentation
============
How to present the PAI to the TOE.

PAD technique
=============
Possible PAD technique that can detect the attack. See [Rakshit & Kisku, 2017] for typical PAD technique. Applicability of the PAD technique to the mobile devices is also considered here if there are the PAD technique that can be implemented in mobile devices in the research papers.

Reference
=========
Existing research papers based on which this attack scenario is created. Evaluator should look at them because detailed test procedure may be described in the papers.

Attack Potential
================
Attack potential calculated for this attack scenario based on the attack potential table X (TBD. Current attack potential table proposed in the cPP may be modified to set an appropriate goal considering the current technology of the mobile devices)

--- 

&nbsp;

##### 3.2 Attack scenario
Evaluator shall conduct the penetration testing following attack scenarios defined here. However, those attack scenarios beyond the target attack potential is out of scope of evaluation. Evaluator may conduct the testing based on the scenario that is beyond the target attack potential if evaluator believes the attack potential could be lowered than one defined here for some reason. However, evaluator shall provide the rationale in the ETR to change the attack potential in each scenario.

*Note: For the individual attack scenarios, please refer to the specific files in the 'attack' folder.*

### 4. Scope of the cPP

No.1 to No.4 should be within the scope of the use case 1 cPP because all attacks can be done at low cost (but we need to set appropriate pass/failure criteria).
No.5 may be out of scope because creating the face mask costs about 300$ and this doesn’t match the motivation of attackers.




