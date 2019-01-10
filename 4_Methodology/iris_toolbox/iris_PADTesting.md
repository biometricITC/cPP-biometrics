# Mobile Toolbox for Iris Verification for ATE_IND.1
13th November 2018

### 1. Evaluation Activity and Penetration testing for Iris PAD
The iris PAD testing is based on the 2D Image-based PAD methodology.

### 2. Iris-specific Changes to the Methodology
#### 2.1 Background
There are two general categories of iris scanners on the market today, divided by the wavelength of light used to take the image of the iris. It is expected that a sensor uses one or the other, but not both types of light when taking the image of the iris (though using both is not a barrier to testing).

To handle this situation, additional tools and materials are added to the iris inventory.
#### 2.2 Additional Tools
To handle potential iris sensors that rely on near-Infrared (NIR) or Infrared (IR) requires the use of a camera that can take pictures using these wavelengths. Some mobile devices may support this as a low-light mode. There are cameras on the market which explicitly support night modes that can take images using the proper wavelengths for these types of sensors.

#### 2.3 Additional Materials
It has been shown that having a lens to help curve the image can assist in bypassing an iris match from a flat image _[see Chaos Computer Club, 2017]_. To handle this type of attack, contact lenses are added to the materials list.

#### 2.4 Camera Selection
The Evaluator shall determine which sets of camera tests to run based on what is known about the sensor being used. Sensors that do not use IR or NIR do not need to have tests run using cameras with capabilities to capture such images.

For IR or NIR sensors, all pictures must be taken in a night mode. For mobile device images this means taking the picture in low light (which may not be the best given the smallest amount of iris will be shown, so that must be balanced by the Evaluator). For the camera with a night mode, this must be activated, preferably even during daylight to get the best results.

**_I don't know if we can actually say to pick just one type of camera path or not. I do not expect a visible wavelength sensor to work with the resulting IR/NIR image, but I don't know if the same is true in reverse (it should be). The simple thing would be to state to pick one type of camera set (a or b) and run the tests with just that set, but it may be useful to test one of each (i.e. have one visible test run on the IR/NIR and one IR/NIR test run on the visible)._**

### 3. Image Recommendations for Level 3
Based on earlier work _[see Chaos Computer Club, 2015]_ for Level 3 tests the Evaluator should attempt to acquire Images where the iris diameter is at least 75 pixels and the printout should have an equivalent of 1200 DPI.

Note that when tests require the use of the contact lenses, the printed image of the iris must batch the diameter of the contact lens for proper overlay.

### 4. Attack categories
There are several categories of attacks based on the source of the image/video being used to create the PAI.

| No. | Source | Description |
|-----|--------|-------------|
| 1 | Physical Source  | The target does not post pictures on SNS/internet or is very limited in distribution. A physical picture is found (such as on a desk) and is scanned as the source for the PAI.  |
| 2 | Selfie Image  | The target has taken a selfie picture and uploaded it to SNS/internet where it can be readily found and used as the basis of the PAI.  |
| 3 | Mobile Device Camera Image  | The target has taken a picture using the main Mobile Device camera and uploaded it to SNS/internet where it can be readily found and used as the basis of the PAI.  |
| 4 | High Quality Camera Image  | The target has a high quality facial picture uploaded to SNS/internet where it can be readily found and used as the basis of the PAI.  |
| 5 | Mobile Device Video  | The target has a low quality (i.e. mobile device quality) video of their face taken and posted to SNS/internet where it can be readily found and used as the basis of the PAI.  |
| 6 | High Quality Video  | The target has a high quality (i.e. dSLR or other high quality video recording) video of their face taken and posted to SNS/internet where it can be readily found and used as the basis of the PAI.  |

These attack categories are used as the basis for determining the source for the PAI and how an attack can be attempted.
