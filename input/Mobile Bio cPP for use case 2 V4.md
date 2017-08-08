**\[Security Problem Definition\]**
***Threats***
**T.Casual\_Attack **
An attacker may attempt to impersonate as a legitimate user withoutbeing enrolled in the TOE. In order to perform the attack, the attackersonly use their own biometric characteristic (in form of azero-effort-attack).
**T.Presentation\_attack**
An attacker may attempt a presentation attack to the TOE. In order toperform the attack, the attacker uses any Presentation Attack Instrument(PAI) except their own biometric characteristic.
Note: Acquisition of biometric characteristic may be cooperative ornon-cooperative.
**T.General**
An attacker may attempt to access the biometric data through externalhardware ports, through mobile device user interface, and also throughdirect and possibly destructive access to the device, in order tofacilitate the attack to the TOE.
Note:
This threat covers several scenarios including:
- An attacker may root the mobile device and attempt to access biometricdata in memory and file system of mobile device
- An attacker takes advantage of the verification memory content (e.g.by reading the memory content, cache or relevant temporary data) using aflaw in a user visible interface of the TOE.
***Organizational Security Policies***
**OSP.ENROL**
The TOE shall enrol users for biometric verification, only aftersuccessful authentication of a user. The TOE shall ensure that enrolmenttemplates are of sufficient quality in order to meet the requirements onrecognition performance.
**OSP.Verifcation\_Error**
The TOE shall meet relevant criteria for its security relevant errorrates for biometric verification.
**OSP.PAD\_Error**
The TOE shall meet relevant criteria for its security relevant errorrates for PAD.
**OSP.TrialLimit**
Impostors must be prevented from gaining access to the protectedservices by making repeated verification attempts using one or moreclaimed user IDs.
**OSP.Audit**
The TOE shall record security-relevant audit events so that user canview user or TOE activity.
***Assumptions***
**A.User**
It is assumed that the user configures the device correctly in a mannerto ensure that the TOE security policies will be enforced.
**A.Fallback**
It is assumed that a fall-back authentication mechanism as a complementto the TOE is available. This fall-back authentication mechanism can beused in cases where a user is rejected by the biometric verificationsystem (False Rejection).
**\[Security Objectives\]**
***Security Objectives for the TOE***
**O.BIO\_VERIFICATION**
The TOE shall provide a biometric verification mechanism to controlaccess to the protected services with an adequate reliability. The TOEshall meet relevant criteria for its security relevant error rates forbiometric verification.
**O.Presentation\_attack\_detection**
The TOE shall prevent a presentation attack using Presentation AttackInstrument (PAI). The TOE shall meet relevant criteria for its securityrelevant error rates for PAD
**O.AUDIT**
The TOE shall record security-relevant audit events so that user canview user or TOE activity.
**O.ENROL**
The TOE shall implement the functionality to enrol users for biometricauthentication, only after successful authentication of a user. The TOEshall check the quality of enrolment templates in order to meet therequirements on recognition performance.
**O.PROTECTION**
The TOE in cooperation with its environment shall ensure that biometricdata is adequately protected.
Note: Biometric data can be stored in the filesystem and resided in thememory. All such data shall be protected from unauthorized access ordeleted after its use.
***Security Objectives for the TOE Environment***
**OE.TrialLimit**
The TOE environment shall be able to limit the maximum number ofunsuccessful verification attempts.
**OE.User**
The user will configures the device correctly in a manner to ensure thatthe TOE security policies will be enforced.
**OE.Fallback**
Fall-back authentication mechanism as a complement to the TOE will beavailable. This fall-back authentication mechanism can be used in caseswhere a user is rejected by the biometric verification system (FalseRejection).
  ----------------------------------------------------------------------------------------------------------------------------  **Threat, Assumption, or OSP**   **Security Objectives**                                                     **Rationale**  -------------------------------- --------------------------------------------------------------------------- ---------------  **T.Casual\_Attack**             **O.BIO\_VERIFICATION**                                                     
  **T.Presentation\_attack**       **O.Presentation\_attack\_detection**                                       
  **T.General**                    **O.PROTECTION, O.BIO\_VERIFICATION, O.Presentation\_attack\_detection,**                                                                                                                                                     **OE.TrialLimit **                                                          
  **OSP.ENROL**                    **O.ENROL**                                                                 
  **OSP.Verifcation\_Error**       **O.BIO\_VERIFICATION**                                                     
  **OSP.PAD\_Error**               **O.Presentation\_attack\_detection**                                       
  **OSP.TrialLimit**               **OE.TrialLimit**                                                           
  **OSP.Audit**                    **O.Audit**                                                                 
  **A.User**                       **OE.User**                                                                 
  **A.Fallback**                   **OE.Fallback**                                                               ----------------------------------------------------------------------------------------------------------------------------
**\**
**Draft Security Functional Requirements (SFR)**
MDFPP and WD2 ISO/IEC 19989-1 define relevant SFRs for this cPP. Thefollowing are two draft SFRs, one (i.e. Proposal 1) is based on MDFPPand the other (i.e. Proposal 2) is based on WD2 ISO/IEC 19989-1. I alsoadded Proposal 3 based on the discussion at the iTC.
Note: Current status of ISO/IEC 19989-1 is Working Draft 2 and text maybe modified somehow in the future (or we can make change proposals tothis project)
***To iTC members: The following are initial proposals that I justpicked up related SFRs from two documents. Some essential SFRs in theMDFPP (e.g. FIA\_UAU.6) that are related to biometric authentication aremissing and those SFRs will be considered later.***
***Please review two proposals below and tell me which proposal isbetter or propose new or modified ones if you want. ***
**SFRs for O.BIO\_VERIFICATION**
**O.BIO\_VERIFICATION**
The TOE shall provide a biometric verification mechanism to controlaccess to the protected services with an adequate reliability. The TOEshall meet relevant criteria for its security relevant error rates forbiometric verification.
***Proposal 1 (based on MDFPP)***
**FIA\_UAU\_EXT.2 Extended: Timing of Authentication**
**FIA\_UAU\_EXT.2.1** The TSF shall allow \[selection: \[assignment:list of actions\], no actions\] on behalf of the user to be performedbefore the user is authenticated.
**FIA\_UAU\_EXT.2.2** The TSF shall require each user to be successfullyauthenticated before allowing any other TSF-mediated actions on behalfof that user.
**FIA\_UAU.5 Multiple Authentication Mechanisms**
**[FIA\_UAU.5.1](http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html#FIA_UAU.5.1)**The[TSF](http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html#abbr_TSF)shall provide \[selection: fingerprint, iris, face, voice, vein,hybrid\] to support user authentication.
**FIA\_UAU.5.2** The TSF shall authenticate any user's claimed identityaccording to the \[assignment: rules describing how each authenticationmechanism provides authentication\]
**FIA\_BMG\_EXT.1 Extended: Accuracy of Biometric Authentication**
**FIA\_BMG\_EXT.1.1** The one-attempt BAF False Accept Rate (FAR) for\[assignment: biometric modality selected in FIA\_UAU.5.1\] shall notexceed \[selection: 1:100, 1:1000, 1:10000\] with a one-attempt BAFFalse Reject Rate (FRR) not to exceed 1 in \[selection: 10, 20, 50,100\].
**FIA\_BMG\_EXT.1.2** The overall System Authentication False AcceptRate (SAFAR) shall be no greater than 1 in \[assignment: a SAFAR nogreater than 1:500\] within a 1% margin.
***Proposal 2 (based on WD2 ISO/IEC 19989-1)***
**FIA\_UAU.5 Multiple authentication mechanisms**
**FIA\_UAU.5.1** The TSF shall provide \[assignment: list of multipleauthentication mechanisms\] to support user authentication.
**FIA\_UAU.5.2** The TSF shall authenticate any user's claimed identityaccording to the \[assignment: rules describing how the multipleauthentication mechanisms provide authentication\].
**FIA\_BVR.2 Timing of the user authentication with biometricverification**
**FIA\_BVR.2.1** The TSF shall allow \[assignment: list of TSF mediatedactions\] on behalf of the user to be performed before the user isauthenticated with biometric verification.
**FIA\_BVR.2.2** The TSF shall provide a user authentication mechanismwith biometric verification to the user with the \[selection: FMR, FAR\]not exceeding \[assignment: defined value\] and \[selection: FNMR, FRR\]not exceeding \[assignment: defined value\] to require each user to besuccessfully authenticated before allowing any other TSF-mediatedactions on behalf of that user.
Note: ISO/IEC 19989-1 cover all type of modality (e.g. fingerprint, irisand vein) and ST author doesn’t need to specify the modality in the SFR(but modality should be specified in the TOE description).
**SFRs for O.Presentation\_attack\_detection**
**O.Presentation\_attack\_detection**
The TOE shall prevent a presentation attack using Presentation AttackInstrument (PAI). The TOE shall meet relevant criteria for its securityrelevant error rates for PAD
***Proposal 1 (based on MDFPP)***
**FIA\_BMG\_EXT.6 Extended: Spoof Detections for Biometrics**
**FIA\_BMG\_EXT.6.1** The TSF shall perform Presentation AttackDetection testing (also known as liveness detection or spoof detection)on each enrollment and authentication attempt for each biometricmodalities supported, rejecting detected spoofs. For the biometricmodalities given, the spoof testing is adequate up to the attackpotential of \[assignment: one selection per biometric modality\[selection: basic, intermediate, advanced\]\] attacks, respectively.When an authentication attempt fails due to PAD testing, the TSF shallnot indicate to the user the reason for failure to authenticate.
***Proposal 2 (based on WD2 ISO/IEC 19989-1)***
**FIA\_BVR.4 Biometric verification not accepting presentation attackinstruments**
**FIA\_BVR.4.1** The TSF shall prevent presentation of biometriccharacteristics, which result in biometric samples of low quality, frombeing successful in the biometric verification.
**FIA\_BVR.4.2** The TSF shall prevent use of artificial presentationattack instruments from being successfully verified.
***Proposal 3 (based on discussion at the iTC)***
The TSF shall perform Presentation Attack Detection testing on eachbiometric verification and \[selection: enrollment, none\]
(See https://github.com/nils-tekampe/cPP-biometrics/issues/27)
**SFRs for O.AUDIT**
**O.AUDIT**
The TOE shall record security-relevant audit events so that user canview user or TOE activity.
***Proposal 1 (based on MDFPP)***
**FAU\_GEN.1 Audit data generation**
**FAU\_GEN.1.1** The TSF shall be able to generate an audit record ofthe following auditable events:
a\) Start-up and shutdown of the audit functions;
b\) All auditable events for the \[selection, choose one of: minimum,basic, detailed, not specified\] level of audit; and
c\) \[assignment: other specifically defined auditable events\].
**FAU\_GEN.1.2** The TSF shall record within each audit record at leastthe following information:
a\) Date and time of the event, type of event, subject identity (ifapplicable), and the outcome (success or failure) of the event; and
b\) For each audit event type, based on the auditable event definitionsof the functional components included in the PP/ST, \[assignment: otheraudit relevant information\].
***Proposal 2 (based on WD2 ISO/IEC 19989-1)***
19989-1 doesn’t define any extended SFR for audit and assume to useFAU\_GEN
**SFRs for O.ENROL**
**O.ENROL**
The TOE shall implement the functionality to enrol users for biometricauthentication, only after successful authentication of a user. The TOEshall check the quality of enrolment templates in order to meet therequirements on recognition performance.
***Proposal 1 (based on MDFPP)***
**FIA\_BMG\_EXT.2 Extended: Biometric Enrollment**
**FIA\_BMG\_EXT.2.1** The TSF shall only use biometric samples ofsufficient quality for enrollment. Sample data shall have \[assignment:quality metrics corresponding to each biometric modality\].
**FIA\_BMG\_EXT.4 Extended: Biometric Templates**
**FIA\_BMG\_EXT.4.1** The TSF shall only generate and use enrollmenttemplates and/or authentication templates of sufficient quality for anysubsequent authentication functions.
***Proposal 2 (based on WD2 ISO/IEC 19989-1)***
**FIA\_EBR.1 Check of biometric samples for enrolment **
**FIA\_EBR.1.1** The TSF shall prevent use of biometric characteristicsof low quality for enrolment that has been presented by any user of theTSF.
**FIA\_EBR.1.2** The TSF shall prevent use of artificial presentationattack instruments for enrolment that has been presented by any user ofthe TSF.
**FIA\_EBR.2 Biometric enrolment with low failure to enrol rate**
**FIA\_EBR.2.1** The TSF shall provide a mechanism to enrol biometricdata with the FTE not exceeding \[assignment: defined value\].
**SFRs for O.PROTECTION**
**O.PROTECTION**
The TOE in cooperation with its environment shall ensure that biometricdata is adequately protected.
Note: Biometric data can be stored in the filesystem and resided in thememory. All such data shall be protected from unauthorized access ordeleted after its use.
***Proposal 1 (based on MDFPP)***
**FPT\_KST\_EXT.1 Extended: Key Storage**
**FPT\_KST\_EXT.1.1** The TSF shall not store any plaintext key materialin readable non-volatile memory.
**FPT\_KST\_EXT.2** Extended: No Key Transmission
**FPT\_KST\_EXT.2.1** The TSF shall not transmit any plaintext keymaterial outside the security boundary of the TOE.
Note: Keying material also refers to source biometric data (i.e.fingerprint), enrollment and authentication templates, the features analgorithm uses to perform biometric authentication for enrollment orverification (i.e. location of minutia), threshold values used in makingthe match adjudication, intermediate calculations generated whilebuilding an enrollment or authentication template (i.e. direction maps,minutia counts, binarized and skeletonized representations of frictionridge patterns, etc.), and final match scores. Any images or metadataidentifying the user for authentication shall be stored encrypted.
**FCS\_CKM\_EXT.4 Extended: Key Destruction**
**FCS\_CKM\_EXT.4.2** The TSF shall destroy all plaintext keyingmaterial and critical security parameters when no longer needed.
Note: the enrollment or authentication templates are not subject to thisrequirement, since templates are not suitable for deriving keyingmaterial. However, source biometric data (i.e. fingerprint image orfriction ridge pattern), the features an algorithm uses to performbiometric authentication for enrollment or verification (e.g. locationof minutia), threshold values used in making the match adjudication,intermediate values calculated while building an enrollment orauthentication template (i.e. direction maps, minutia counts, binarizedand skeletonized representations of friction ridge patterns, etc.), andfinal match scores are examples of critical security parameters thatmust be destroyed when no longer needed.
**FDP\_PBA\_EXT.1 Extended: Storage of Critical Biometric Parameters**
**FDP\_PBA\_EXT.1.1** The TSF shall protect the authentication template\[selection: using a PIN as an additional factor, using a password as anadditional factor, \[assignment: other circumstances\]\].
***Proposal 2 (based on WD2 ISO/IEC 19989-1)***
19989-1 doesn’t define any extended SFR for audit and assume to useFDP\_RIP, FCS and FPT family
**FDP\_RIP.1.1 **
The TSF shall ensure that any previous information content of a resourceis made unavailable upon the \[selection: allocation of the resource to,deallocation of the resource from\] the following objects: \[assignment:list of objects\].
***To iTC members: The following SFRs defined in the MDFPP may not benecessary in cPP for mobile use case 1 at this stage. Do you think thefollowing SFR should also be defined in the mobile bio cPP?***
**FIA\_BMG\_EXT.3 Extended: Biometric Verification**
**FIA\_BMG\_EXT.3.1**
The TSF shall only use biometric samples of sufficient quality forverification. As such, sample data shall have \[assignment: qualitymetrics corresponding to each biometric modality\].
**FIA\_BMG\_EXT.5 Extended: Handling Unusual Biometric Templates**
**FIA\_BMG\_EXT.5.1**
The matching algorithm shall handle properly formatted enrollmenttemplates and/or authentication templates, especially those with unusualdata properties, appropriately. If such templates contain incorrectsyntax, are of low quality, or contain enrollment data consideredunrealistic for a given modality, then they shall be rejected by thematching algorithm and an error code shall be reported.
