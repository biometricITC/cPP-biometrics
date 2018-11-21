

# Evaluation Activity for FIA_MBV_EXT.3 for 2D Image-based Modalities
12th November 2018

**_Note to the iTC members: Mobile toolbox is split into two parts. One part defines minimum functional testing that evaluators shall conduct as defined in the Evaluation Activity for FIA_MBV_EXT.3 without any changes. The other part provides guidance to evaluators what kind of additional tests should be done during the penetration testing in addition to the functional tests._**

This document describes the generic Evaluation Activity for FIA_MBV_EXT.3 framework for all 2D image-based biometric modalities. Biometric modalities that do not use 2D image or video are covered in separate Evaluation Activity documentation.

The individual toolboxes will have specific details about the presentation attacks that must be tested within this framework.

**a) Objective of the evaluation activity**
This evaluation activity defines the common minimum PAIs that all evaluator shall create and test protocol that evaluator shall follow to test the TOE. While this evaluation activity allows to develop an overall statement about the performance of the TOE with respect to its PAD mechanism, they cannot provide any assurance about the PAD functionality with respect to variations of PAIs.

**b) Relationship of the evaluation activity to SFRs, SARs, and other evaluation activities**
This evaluation activity can supplement all work units defined in ATE_IND.1 for testing the FIA_MBV_EXT.3.
This evaluation activity doesn’t have any dependencies to other evaluation activities defined in this cPP.

**c) Tools required to perform the activity**
Minimum specification of required tools is defined in e) and refined by the appropriate modality toolbox.

**d) Required input from the developer or other entities**
None

**e) Assessment Strategy for 2D image presentation attack**

### Overview
Image presentation attacks can be carried out through the following process:
1. Get images of a target user from, for example, uploaded photo on the SNS
2. Display or reconstruct the image on the spoofing medium such as a photo or
screen. Such a fake image displayed on the spoofing medium used for the presentation attack is called a PAI (Presentation Attack Instrument)
3. Present the PAI to the TOE

The current research categorizes image presentation attacks into the following types based on the spoofing medium used and how the image is recorded.
- 2D image, printed photo attack
- 2D image, digital photo attack
- 2D image, replay video attack

In any type of attack, the TOE captures the fake image from the spoofing medium and unlock the mobile device if the TOE can’t tell the difference between real image and the PAI.

### Type of PAIs for the testing and required tools
Images captured by the TOE from the spoofing medium may visually look very similar to the images captured from real ones, however, they are not exactly the same. For example, printed or displayed images on the paper or screen reflect light in different ways because a human is a complex non-rigid 3D object, whereas the photo or screen can be seen as a planar rigid object. The surface properties of real faces and fake ones, e.g. pigments, are also different. In addition, PAIs may contain artefacts such as moir ́e patterns that are an undesired aliasing of images produced during various image display and image acquisition processes.

The TOE should detect such differences between images taken from real and fake presentations to prevent the presentation attacks. These differences are mainly influenced by the following factors listed in the table below and the performance of the PAD algorithm may also be affected by them.

| No	| Factor	| Description |
|-------|---------------|-------------|
|1	|Quality of source face image from which the PAI is created | The quality of the source is the foundation of the copy (i.e. PAI). If the source image is poor quality, the quality of PAI will also be limited. Source images can be taken with a digital camera and quality of digital image varies depending of quality of the camera (e.g. size of sensor and resolution) |
|2	| Quality of tools (e.g. printer and spoofing medium) to create the PAI | A poor quality PAI can be made from a good quality source if the resolution of the printer or screen is low. However, if the screen is 4K resolution that refers to a horizontal screen resolution in the order of 4,000 pixels, it can provide the finest clarity and detail of the face from the good quality source. |

Various quality of PAIs can be created with, for example, smartphone cameras, compact or high-professional digital cameras however, it’s time consuming to create all possible PAIs using different devices. Therefore, this evaluation activity sets the two level of quality, normal and high, to cover those variety of PAIs. High quality PAIs looks more similar to the real face however, it may show more micro facial textures that can be used to differentiate between the real and fake. However, such micro textures may not be evident in the normal quality PAIs. The TOE may overlook normal quality PAIs if the PAD algorithm completely relies on such micro textures to detect the PAIs. So, this evaluation activity requires to test both levels of quality of PAIs.

| Quality | Description |
|---------|-------------|
| Level 1 | Evaluator shall use standard tools (e.g. smartphone, printer or laptop screen) that meet the specification defined in this evaluation activity to create the PAI. All tools are normally available at home.  |
| Level 2 | Evaluator shall use standard tools (e.g. smartphone, printer or laptop screen) that meet the specification defined in this evaluation activity to create the PAI. All tools are normally available at home or office.|
| Level 3 | Evaluator shall use high-end tools that meet the specification defined in this evaluation activity to create the PAI. All tools are the best quality ones like high-end production printer that may cost several thousands of dollars. However, such high-end tools can be borrowed at rental shops or used through online service (e.g. online printing service) at inexpensive price and evaluator can utilize such services to create the PAI at low cost.|

Various quality of PAIs can be created with, for example, smartphone cameras,
compact or high-professional digital cameras however, it’s time consuming to
create all possible PAIs using different tools. Therefore, this EA categorizes
the tools into two or three levels to cover those variety of PAIs.

High quality PAIs looks more similar to the real face however, it may show more
micro facial textures that can be used to differentiate between the real and
fake. However, such micro textures may not be evident in the low quality PAIs.
The TOE may overlook such low quality PAIs if the PAD algorithm completely relies
on micro textures to detect the PAIs. So, this EA requires the evaluator to test all
PAIs as specified in C.1.2.2. However, the evaluator can omit some of them if the
evaluator has a valid rationale based on information gained from the developer.

Category | Level 1 | Level 2 | Level 3
--- | --- | --- | ---
Camera | Front-facing device camera | Digital Camera (min resolution = device resolution) | DSR 40+ MP
Scanner | 300 DPI | 600 DPI | 1200 DPI
Printer | Home SoHo Inkjet | Color Laser | Printing Service
Paper | Standard Letter (24lb weight equivalent) | Photo paper | N/A
Computing resources | Mobile device | PC or laptop | Professional
Output Screen | 1080p 10" | 1080p -> 2160p under 20" | 4K above 24"

Within these categories, individual modality toolboxes may have more specific requirements based on the details of the specific modality.

### Test protocols
The following describes the test protocol that evaluator shall follow. If the Security Target allows multiple settings for security relevant parameters, all tests have to be conducted for all possible configurations.

1) Enrollment
Evaluator turns on the appropriate biometric unlock and registers the test user following instructions provided by the mobile device and manual (i.e. test user should not wear glasses, hat, or heavy make-up during the enrollment if the guidance instructs not to do so) under the controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are down.

2) Creating the source still and video digital image
Digital image of target user’s biometric that meet the following conditions shall be taken for each quality level:
   1. captured by the camera that meets the specification defined in each quality level
   2. digital image was taken under controlled environment where the background of the scene is uniform, the light in the office is switched on and the window blinds are
down
   3. digital image is taken right after the target user’s enrolment and under the same condition (i.e. under controlled environment) to reduce the possibility that the PAI is rejected because of the difference of the background scene or expression
   4. target user’s biometric occupies about 20% of the full image
   5. digital image includes user’s full biometric (i.e. face, finger, hand)
   6. for reply video attack, video length shall be limited to ten seconds


3) Creating the PAI
Source digital image shall be printed and displayed on the spoofing mediums (i.e. paper or screen) that meet the specification defined in each quality level.

4) Presenting the PAI to the TOE
Evaluator shall present the mobile device to the fixed and stationary spoofing mediums by hand at controlled environment for printed and digital photo attack to introduce some noticeable motion of the PAIs. For replay video attack, both of the spoofing medium and the PAI shall be stationary. Evaluator shall adjust the distance between the spoofing mediums and the TOE so that the device camera can’t see the edge of spoofing mediums. Evaluator shall also present the spoofing mediums in a way to minimize the reflection from ambient lighting.

### Number of trials
Evaluator shall conduct the testing with five users. Two source images shall be taken for quality level and two spoofing mediums (i.e. Level 1 of photo and screen, Level 2 of photo and screen and Level 3 of photo and screen) shall be used for each user. 20 presentations shall be made for each PAI changing the distance between the TOE and spoofing medium (i.e. 180 presentations shall be made for each user)

| Attack type  | Source image   | Spoofing medium   | # subject | # presentation |
|--------------|----------------|-------------------|-----------|----------------|
| 2D face, printed photo | Level 1   | Level 1    | 5 | 20 |
|   | Level 2  | Level 2  | 5  |20   |
|   | Level 3  | Level 3  | 5  | 20  |
| 2D face, digital photo attack | Level 1   | Level 1    | 5 | 20 |
|   | Level 2  | Level 2  | 5  | 20  |
|   | Level 3  | Level 3  | 5  | 20  |
| 2D face, replay video attack | Level 1   | Level 1    | 5 | 20 |
|   | Level 2  | Level 2  | 5  | 20  |
|   | Level 3  | Level 3  | 5  | 20  |

### f) Pass/fail criteria
Evaluator doesn’t need to present each PAI more than 20 times. Evaluator may learn, for example, the distance between the spoofing medium and the TOE that the TOE accepts the PAI at high probability during the presentations.

PAD will never work with an accuracy of 100% because of the limitation of current technology of mobile devices. The following pass criteria is defined based on the performance of the state of art mobile PAD technology that was actually tested in the relevant research.

*For Level 1 quality testing for all type of attack, the TOE shall reject more than 95% of
unlock attempts with each PAI.
For Level 2 quality testing for all type of attack, the TOE shall reject more than 90% of
unlock attempts with each PAI.
For Level 3 quality testing for all type of attack, the TOE shall reject more than 50% of
unlock attempts with each PAI.*

Above criteria marked in *italics* is initial proposal and need to be discussed later.
