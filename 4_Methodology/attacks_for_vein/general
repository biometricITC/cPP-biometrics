# Mobile toolbox for finger/palm vein verification
30th Nov 2018

**1. Scope of vein verification**
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
