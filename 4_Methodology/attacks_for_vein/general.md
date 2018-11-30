# Mobile toolbox for finger/palm vein verification
30th Nov 2018

**1. Scope of the toolbox**  
This toolbox specifies all test items for finger/palm vein PAD testing. 
Test items are created referring research papers on finger and palm vein 
verification using NIR or visible light however, this toolbox may also be 
applicable to other types of vein verification (e.g. dorsal hand or wrist 
vein verification) because they also use the same technology to capture 
and match the vein image.

**2. Overview of vein presentation attack**  
Vein presentation attack can be carried out through the following process:
1)	Capture the vein image with NIR light or visible light
2)	Print out or display the vein image on the spoofing medium such as a paper
or screen.  
A fake vein image on the spoofing medium used for the presentation attack is 
called a PAI (Presentation Attack Instrument)
3)	Present the PAI to the TOE

The current research categorizes vein presentation attacks into the following 
two types based on the spoofing medium used. However, “photo/video attack” is 
only applicable to the TOE that use visible light to capture the vein image 
because the TOE that capture the vein image with NIR light can’t see the vein 
image displayed on the computer screen.

-	print attack
-	photo/video attack

The following section explains how to create the PAI step by step.

**2-1. Capture the vein image**  
Evaluator shall capture the vein image from the target user by the scanner 
first. The vain image can be captured by the following scanners:

a)	Commercial scanner  
Evaluator may purchase the TOE or similar type of commercial vein scanner to 
capture the vein image. This is the best choice if such a scanner is available 
at affordable cost.   

b)	In-house scanner  
Evaluator may develop the vein scanner by her/himself refereeing the publicly 
available information (e.g. [1] for finger vein and [2] for palm vein). 

c)	NIR digital camera  
Evaluator may capture the vein image using the commercial NIR camera with 
NIR light source. Evaluator may convert the normal digital camera to the 
NIR camera removing IR cut-off filter (e.g. [3]) instead of purchasing 
expensive NIR camera.

In any case, cost and skill for purchasing, developing and using the scanner 
need to be within the scope of Basic Attack Potential. Quality of captured 
vein image (i.e. visibility of vein pattern) is one of the key factor to 
succeed the vein presentation attack however, evaluator shall choose the 
most inexpensive and easiest way to capture the vein image considering 
the attack potential required by the cPP. If there are several options 
available, evaluator shall choose one such as the commercial scanner that 
can record the better quality of the vein image.

**2-2. Preprocess the vein image**    
If the captured vein image is not clear and visible, evaluator shall 
preprocess the image to improve contrast of the vein. Evaluator may enhance 
the vein pattern with a pencil by hand or with free image processing software. 
Research papers normally apply more sophisticated image processing technique 
such as the histogram equalization to improve the quality of image however 
the evaluator may not use such method considering the attack potential required 
by the cPP. Evaluator shall also perform proper rescaling, so the printed vein 
image should be the same size as the real one.

**2-3-1. Create and present the PAI for print attack**  
Evaluator shall print the vein image in a normal paper with a standard printer. 
TOE can capture the vein image from such paper because carbon ink used for 
printout has a strong tendency to absorb NIR light as hemoglobin in the vein does.

Evaluator can use any type of paper or printer because current research papers 
doesn’t show clear superiority in a particular paper or printer for successful 
presentation attack.

Evaluator shall present the PAI, a copy of vein image, to the TOE in the following 
manners because each presentation method may have different effect on the TOE's
presentation attack detection functionality.

1)	Direct presentation of NIR image  
Present the copy of the vein image (i.e. printout) as it is to the TOE.

2)	Presentation of NIR image with bottle/tube  
Present the copy of the vein image stuck on a bottle for palm vein verification 
or a round transparent tube (size of tube is the same size as finger) for finger 
vein verification (e.g. Figure 5-27 in [4])

3)	Presentation of NIR image with real palm/finger  
Present the copy of the vein image stuck on different user’s palm or finger 
(e.g. Figure 5-27 in [4])    

If the TOE captures the vein image using visible light, evaluator shall also use 
the finger or palm image captured by visible light to create the PAI. This means 
that evaluator shall also create different PAIs following instructions below for 
such type of the TOE. However, evaluator shall also present those PAIs to the TOE 
that capture the image with NIR light because they may also be effective to them.

Evaluator shall capture the finger or palm image using digital camera and rescale 
and print the color image of vein on the paper. The copy of image shall be presented 
in the following manner. 


4)	Direct presentation of color image  
Present the color copy of the finger or palm image as it is to the TOE.

5)	Presentation of color image with bottle/tube  
Present the color copy of the finger or palm image stuck on a bottle for palm vein 
verification or a round transparent tube (size of tube is the same size as finger) 
for finger vein verification (e.g. Figure 5-27 in [4])

6)	Presentation of color image with real palm/finger  
Present the color copy of the finger or palm image stuck on different user’s palm 
or finger (e.g. Figure 5-27 in [4])

7)	Direct presentation of composite image  
Present the composite image that put color copy image on the NIR vein image to the TOE.

8)	Presentation of composite image with bottle/tube
Present the composite image stuck on a bottle for palm vein verification or a round 
transparent tube (size of tube is the same size as finger) for finger vein verification 
(e.g. Figure 5-27 in [4]) 

9)	Presentation of composite image with real palm/finger  
Present the composite image stuck on different user’s palm or finger (e.g. Figure 5-27 in [4])  

**2-3-2. Create and present the PAI for photo/video attack**  
If the TOE captures the vein image using visible light instead of NIR light, evaluator shall 
take video of palm or finger with a digital camera and display them on the screen and present 
it to the TOE. 

**3. Guidance for ATE_IND testing**  
More detailed test information (e.g. required spec of camera) is specified in test items in the 
toolbox. Evaluator shall conduct all test items in the toolbox without any change for ATE_IND testing.

**4. Guidance for AVA_VAN testing**  
Evaluator shall vary test method specified in the test items in the toolbox and repeat testing. 
For example, evaluator may change the test strategy as follows;

-	Presentation  
TOE may check the blood flow through the finger vein to measure its liveness. Evaluator may sway 
or shake the copy of vein image very slightly to mimic this blood flow.

-	Number of trial  
Evaluator may try to enroll the PAI first and increase the number of trial for such PAIs that can 
be enrolled because enrollment and verification may share the same process (e.g. liveness check or 
quality check).

**5. Reference**  
[1] B. T. Ton. Vascular pattern of the finger: biometric of the future?  
https://essay.utwente.nl/61963/1/final_report_online_Ton.pdf  

[2] João Ricardo Gonçalves Neves. Hand Veins Recognition System.  
https://fenix.tecnico.ulisboa.pt/downloadFile/395145923801/Master%20Thesis%20Jo%C3%A3o%20Neves%2057516.pdf

[3] Klaus Mangold et all. The physics of near-infrared photography.  
http://www.montana.edu/jshaw/documents/NIR%20Photography%20-%20Mangold%20et%20al%20-%20EJP2013.pdf

[4] Zeno Geradts, Peter Sommer. D6.1: Forensic Implications of Identity Management Systems.  
http://www.fidis.net/fileadmin/fidis/deliverables/fidis-wp6-del6.1.forensic_implications_of_identity_management_systems.pdf
