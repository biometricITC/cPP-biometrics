**\[Security Problem Definition\]**

***Threats***

**T.Casual\_Attack **

An attacker may attempt to impersonate as a legitimate user without
being enrolled in the TOE. In order to perform the attack, the attackers
only use their own biometric characteristic (in form of a
zero-effort-attack).

**T.Presentation\_attack**

An attacker may attempt a presentation attack to the TOE. In order to
perform the attack, the attacker uses any Presentation Attack Instrument
(PAI) except their own biometric characteristic.

Note: Acquisition of biometric characteristic may be cooperative or
non-cooperative.

**T.General**

An attacker may attempt to access the biometric data through external
hardware ports, through mobile device user interface, and also through
direct and possibly destructive access to the device, in order to
facilitate the attack to the TOE.

Note:

This threat covers several scenarios including:

- An attacker may root the mobile device and attempt to access biometric
data in memory and file system of mobile device

- An attacker takes advantage of the verification memory content (e.g.
by reading the memory content, cache or relevant temporary data) using a
flaw in a user visible interface of the TOE.

***Organizational Security Policies***

**OSP.ENROL**

The TOE shall enrol users for biometric verification, only after
successful authentication of a user. The TOE shall ensure that enrolment
templates are of sufficient quality in order to meet the requirements on
recognition performance.

**OSP.Verifcation\_Error**

The TOE shall meet relevant criteria for its security relevant error
rates for biometric verification.

**OSP.PAD\_Error**

The TOE shall meet relevant criteria for its security relevant error
rates for PAD.

**OSP.TrialLimit**

Impostors must be prevented from gaining access to the protected
services by making repeated verification attempts using one or more
claimed user IDs.

**OSP.Audit**

The TOE shall record security-relevant audit events so that user can
view user or TOE activity.

***Assumptions***

**A.User**

It is assumed that the user configures the device correctly in a manner
to ensure that the TOE security policies will be enforced.

**A.Fallback**

It is assumed that a fall-back authentication mechanism as a complement
to the TOE is available. This fall-back authentication mechanism can be
used in cases where a user is rejected by the biometric verification
system (False Rejection).

**\[Security Objectives\]**

***Security Objectives for the TOE***

**O.BIO\_VERIFICATION**

The TOE shall provide a biometric verification mechanism to control
access to the protected services with an adequate reliability. The TOE
shall meet relevant criteria for its security relevant error rates for
biometric verification.

**O.Presentation\_attack\_detection**

The TOE shall prevent a presentation attack using Presentation Attack
Instrument (PAI). The TOE shall meet relevant criteria for its security
relevant error rates for PAD

**O.AUDIT**

The TOE shall record security-relevant audit events so that user can
view user or TOE activity.

**O.ENROL**

The TOE shall implement the functionality to enrol users for biometric
authentication, only after successful authentication of a user. The TOE
shall check the quality of enrolment templates in order to meet the
requirements on recognition performance.

**O.PROTECTION**

The TOE in cooperation with its environment shall ensure that biometric
data is adequately protected.

Note: Biometric data can be stored in the filesystem and resided in the
memory. All such data shall be protected from unauthorized access or
deleted after its use.

***Security Objectives for the TOE Environment***

**OE.TrialLimit**

The TOE environment shall be able to limit the maximum number of
unsuccessful verification attempts.

**OE.User**

The user will configures the device correctly in a manner to ensure that
the TOE security policies will be enforced.

**OE.Fallback**

Fall-back authentication mechanism as a complement to the TOE will be
available. This fall-back authentication mechanism can be used in cases
where a user is rejected by the biometric verification system (False
Rejection).

  ----------------------------------------------------------------------------------------------------------------------------
  **Threat, Assumption, or OSP**   **Security Objectives**                                                     **Rationale**
  -------------------------------- --------------------------------------------------------------------------- ---------------
  **T.Casual\_Attack**             **O.BIO\_VERIFICATION**                                                     

  **T.Presentation\_attack**       **O.Presentation\_attack\_detection**                                       

  **T.General**                    **O.PROTECTION, O.BIO\_VERIFICATION, O.Presentation\_attack\_detection,**   
                                                                                                               
                                   **OE.TrialLimit **                                                          

  **OSP.ENROL**                    **O.ENROL**                                                                 

  **OSP.Verifcation\_Error**       **O.BIO\_VERIFICATION**                                                     

  **OSP.PAD\_Error**               **O.Presentation\_attack\_detection**                                       

  **OSP.TrialLimit**               **OE.TrialLimit**                                                           

  **OSP.Audit**                    **O.Audit**                                                                 

  **A.User**                       **OE.User**                                                                 

  **A.Fallback**                   **OE.Fallback**                                                             
  ----------------------------------------------------------------------------------------------------------------------------

**\
**

**Draft Security Functional Requirements (SFR)**

MDFPP and WD2 ISO/IEC 19989-1 define relevant SFRs for this cPP. The
following are two draft SFRs, one (i.e. Proposal 1) is based on MDFPP
and the other (i.e. Proposal 2) is based on WD2 ISO/IEC 19989-1. I also
added Proposal 3 based on the discussion at the iTC.

Note: Current status of ISO/IEC 19989-1 is Working Draft 2 and text may
be modified somehow in the future (or we can make change proposals to
this project)

***To iTC members: The following are initial proposals that I just
picked up related SFRs from two documents. Some essential SFRs in the
MDFPP (e.g. FIA\_UAU.6) that are related to biometric authentication are
missing and those SFRs will be considered later.***

***Please review two proposals below and tell me which proposal is
better or propose new or modified ones if you want. ***

**SFRs for O.BIO\_VERIFICATION**

**O.BIO\_VERIFICATION**

The TOE shall provide a biometric verification mechanism to control
access to the protected services with an adequate reliability. The TOE
shall meet relevant criteria for its security relevant error rates for
biometric verification.

***Proposal 1 (based on MDFPP)***

**FIA\_UAU\_EXT.2 Extended: Timing of Authentication**

**FIA\_UAU\_EXT.2.1** The TSF shall allow \[selection: \[assignment:
list of actions\], no actions\] on behalf of the user to be performed
before the user is authenticated.

**FIA\_UAU\_EXT.2.2** The TSF shall require each user to be successfully
authenticated before allowing any other TSF-mediated actions on behalf
of that user.

**FIA\_UAU.5 Multiple Authentication Mechanisms**

**[FIA\_UAU.5.1](http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html#FIA_UAU.5.1)**
The
[TSF](http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html#abbr_TSF)
shall provide \[selection: fingerprint, iris, face, voice, vein,
hybrid\] to support user authentication.

**FIA\_UAU.5.2** The TSF shall authenticate any user's claimed identity
according to the \[assignment: rules describing how each authentication
mechanism provides authentication\]

**FIA\_BMG\_EXT.1 Extended: Accuracy of Biometric Authentication**

**FIA\_BMG\_EXT.1.1** The one-attempt BAF False Accept Rate (FAR) for
\[assignment: biometric modality selected in FIA\_UAU.5.1\] shall not
exceed \[selection: 1:100, 1:1000, 1:10000\] with a one-attempt BAF
False Reject Rate (FRR) not to exceed 1 in \[selection: 10, 20, 50,
100\].

**FIA\_BMG\_EXT.1.2** The overall System Authentication False Accept
Rate (SAFAR) shall be no greater than 1 in \[assignment: a SAFAR no
greater than 1:500\] within a 1% margin.

***Proposal 2 (based on WD2 ISO/IEC 19989-1)***

**FIA\_UAU.5 Multiple authentication mechanisms**

**FIA\_UAU.5.1** The TSF shall provide \[assignment: list of multiple
authentication mechanisms\] to support user authentication.

**FIA\_UAU.5.2** The TSF shall authenticate any user's claimed identity
according to the \[assignment: rules describing how the multiple
authentication mechanisms provide authentication\].

**FIA\_BVR.2 Timing of the user authentication with biometric
verification**

**FIA\_BVR.2.1** The TSF shall allow \[assignment: list of TSF mediated
actions\] on behalf of the user to be performed before the user is
authenticated with biometric verification.

**FIA\_BVR.2.2** The TSF shall provide a user authentication mechanism
with biometric verification to the user with the \[selection: FMR, FAR\]
not exceeding \[assignment: defined value\] and \[selection: FNMR, FRR\]
not exceeding \[assignment: defined value\] to require each user to be
successfully authenticated before allowing any other TSF-mediated
actions on behalf of that user.

Note: ISO/IEC 19989-1 cover all type of modality (e.g. fingerprint, iris
and vein) and ST author doesn’t need to specify the modality in the SFR
(but modality should be specified in the TOE description).

**SFRs for O.Presentation\_attack\_detection**

**O.Presentation\_attack\_detection**

The TOE shall prevent a presentation attack using Presentation Attack
Instrument (PAI). The TOE shall meet relevant criteria for its security
relevant error rates for PAD

***Proposal 1 (based on MDFPP)***

**FIA\_BMG\_EXT.6 Extended: Spoof Detections for Biometrics**

**FIA\_BMG\_EXT.6.1** The TSF shall perform Presentation Attack
Detection testing (also known as liveness detection or spoof detection)
on each enrollment and authentication attempt for each biometric
modalities supported, rejecting detected spoofs. For the biometric
modalities given, the spoof testing is adequate up to the attack
potential of \[assignment: one selection per biometric modality
\[selection: basic, intermediate, advanced\]\] attacks, respectively.
When an authentication attempt fails due to PAD testing, the TSF shall
not indicate to the user the reason for failure to authenticate.

***Proposal 2 (based on WD2 ISO/IEC 19989-1)***

**FIA\_BVR.4 Biometric verification not accepting presentation attack
instruments**

**FIA\_BVR.4.1** The TSF shall prevent presentation of biometric
characteristics, which result in biometric samples of low quality, from
being successful in the biometric verification.

**FIA\_BVR.4.2** The TSF shall prevent use of artificial presentation
attack instruments from being successfully verified.

***Proposal 3 (based on discussion at the iTC)***

The TSF shall perform Presentation Attack Detection testing on each
biometric verification and \[selection: enrollment, none\]

(See https://github.com/nils-tekampe/cPP-biometrics/issues/27)

**SFRs for O.AUDIT**

**O.AUDIT**

The TOE shall record security-relevant audit events so that user can
view user or TOE activity.

***Proposal 1 (based on MDFPP)***

**FAU\_GEN.1 Audit data generation**

**FAU\_GEN.1.1** The TSF shall be able to generate an audit record of
the following auditable events:

a\) Start-up and shutdown of the audit functions;

b\) All auditable events for the \[selection, choose one of: minimum,
basic, detailed, not specified\] level of audit; and

c\) \[assignment: other specifically defined auditable events\].

**FAU\_GEN.1.2** The TSF shall record within each audit record at least
the following information:

a\) Date and time of the event, type of event, subject identity (if
applicable), and the outcome (success or failure) of the event; and

b\) For each audit event type, based on the auditable event definitions
of the functional components included in the PP/ST, \[assignment: other
audit relevant information\].

***Proposal 2 (based on WD2 ISO/IEC 19989-1)***

19989-1 doesn’t define any extended SFR for audit and assume to use
FAU\_GEN

**SFRs for O.ENROL**

**O.ENROL**

The TOE shall implement the functionality to enrol users for biometric
authentication, only after successful authentication of a user. The TOE
shall check the quality of enrolment templates in order to meet the
requirements on recognition performance.

***Proposal 1 (based on MDFPP)***

**FIA\_BMG\_EXT.2 Extended: Biometric Enrollment**

**FIA\_BMG\_EXT.2.1** The TSF shall only use biometric samples of
sufficient quality for enrollment. Sample data shall have \[assignment:
quality metrics corresponding to each biometric modality\].

**FIA\_BMG\_EXT.4 Extended: Biometric Templates**

**FIA\_BMG\_EXT.4.1** The TSF shall only generate and use enrollment
templates and/or authentication templates of sufficient quality for any
subsequent authentication functions.

***Proposal 2 (based on WD2 ISO/IEC 19989-1)***

**FIA\_EBR.1 Check of biometric samples for enrolment **

**FIA\_EBR.1.1** The TSF shall prevent use of biometric characteristics
of low quality for enrolment that has been presented by any user of the
TSF.

**FIA\_EBR.1.2** The TSF shall prevent use of artificial presentation
attack instruments for enrolment that has been presented by any user of
the TSF.

**FIA\_EBR.2 Biometric enrolment with low failure to enrol rate**

**FIA\_EBR.2.1** The TSF shall provide a mechanism to enrol biometric
data with the FTE not exceeding \[assignment: defined value\].

**SFRs for O.PROTECTION**

**O.PROTECTION**

The TOE in cooperation with its environment shall ensure that biometric
data is adequately protected.

Note: Biometric data can be stored in the filesystem and resided in the
memory. All such data shall be protected from unauthorized access or
deleted after its use.

***Proposal 1 (based on MDFPP)***

**FPT\_KST\_EXT.1 Extended: Key Storage**

**FPT\_KST\_EXT.1.1** The TSF shall not store any plaintext key material
in readable non-volatile memory.

**FPT\_KST\_EXT.2** Extended: No Key Transmission

**FPT\_KST\_EXT.2.1** The TSF shall not transmit any plaintext key
material outside the security boundary of the TOE.

Note: Keying material also refers to source biometric data (i.e.
fingerprint), enrollment and authentication templates, the features an
algorithm uses to perform biometric authentication for enrollment or
verification (i.e. location of minutia), threshold values used in making
the match adjudication, intermediate calculations generated while
building an enrollment or authentication template (i.e. direction maps,
minutia counts, binarized and skeletonized representations of friction
ridge patterns, etc.), and final match scores. Any images or metadata
identifying the user for authentication shall be stored encrypted.

**FCS\_CKM\_EXT.4 Extended: Key Destruction**

**FCS\_CKM\_EXT.4.2** The TSF shall destroy all plaintext keying
material and critical security parameters when no longer needed.

Note: the enrollment or authentication templates are not subject to this
requirement, since templates are not suitable for deriving keying
material. However, source biometric data (i.e. fingerprint image or
friction ridge pattern), the features an algorithm uses to perform
biometric authentication for enrollment or verification (e.g. location
of minutia), threshold values used in making the match adjudication,
intermediate values calculated while building an enrollment or
authentication template (i.e. direction maps, minutia counts, binarized
and skeletonized representations of friction ridge patterns, etc.), and
final match scores are examples of critical security parameters that
must be destroyed when no longer needed.

**FDP\_PBA\_EXT.1 Extended: Storage of Critical Biometric Parameters**

**FDP\_PBA\_EXT.1.1** The TSF shall protect the authentication template
\[selection: using a PIN as an additional factor, using a password as an
additional factor, \[assignment: other circumstances\]\].

***Proposal 2 (based on WD2 ISO/IEC 19989-1)***

19989-1 doesn’t define any extended SFR for audit and assume to use
FDP\_RIP, FCS and FPT family

**FDP\_RIP.1.1 **

The TSF shall ensure that any previous information content of a resource
is made unavailable upon the \[selection: allocation of the resource to,
deallocation of the resource from\] the following objects: \[assignment:
list of objects\].

***To iTC members: The following SFRs defined in the MDFPP may not be
necessary in cPP for mobile use case 1 at this stage. Do you think the
following SFR should also be defined in the mobile bio cPP?***

**FIA\_BMG\_EXT.3 Extended: Biometric Verification**

**FIA\_BMG\_EXT.3.1**

The TSF shall only use biometric samples of sufficient quality for
verification. As such, sample data shall have \[assignment: quality
metrics corresponding to each biometric modality\].

**FIA\_BMG\_EXT.5 Extended: Handling Unusual Biometric Templates**

**FIA\_BMG\_EXT.5.1**

The matching algorithm shall handle properly formatted enrollment
templates and/or authentication templates, especially those with unusual
data properties, appropriately. If such templates contain incorrect
syntax, are of low quality, or contain enrollment data considered
unrealistic for a given modality, then they shall be rejected by the
matching algorithm and an error code shall be reported.
