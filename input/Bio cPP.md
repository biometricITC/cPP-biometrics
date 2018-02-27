# collaborative Protection Profile for Biometric verification on the mobile device for unlocking the device
## Version 0.2 26-FEB-2018

## Acknowledgements

This collaborative Protection Profile (cPP) was developed by the Biometrics Security (BS) international Technical Community (iTC) with representatives from industry, Government agencies, Common Criteria TestLaboratories, and members of academia.

## 1. Preface

1.1 Objective of Document
---------------------
This document presents the Common Criteria (CC) collaborative ProtectionProfile (cPP) to express the security functional requirements (SFRs) and security assurance requirements (SARs) for a mobile biometric verification on the mobile device. The Evaluation activities that specify the actions the evaluator performs to determine if a product satisfies the SFRs captured within this cPP are described in \[SD\].

1.2 Scope of Document
-----------------
The scope of the cPP within the development and evaluation process is described in the Common Criteria for Information Technology Security Evaluation \[CC\]. In particular, a cPP defines the IT security requirements of a generic type of TOE and specifies the functional andassurance security measures to be offered by that TOE to meet stated requirements \[CC1, Section C.1\].

1.3 Intended Readership
-------------------
The target audiences of this cPP are developers, CC consumers, systemintegrators, evaluators and schemes.
Although the cPP and SD may contain minor editorial errors, the cPP is recognized as living document and the iTC is dedicated to ongoing updates and revisions. Please report any issues to the BS iTC.

1.4 Related Documents
-----------------
**Common Criteria**

\[CC1\] Common Criteria for Information Technology Security Evaluation, Part 1: Introduction and General Model, CCMB-2017-04-001, Version 3.1 Revision 5, April 2017.

\[CC2\] Common Criteria for Information Technology Security Evaluation, Part 2: Security functional components, CCMB-2017-04-002, Version 3.1 Revision 5, April 2017.

\[CC3\] Common Criteria for Information Technology Security Evaluation, Part 3: Security assurance components, CCMB-2017-04-003, Version 3.1 Revision 5, April 2017.

\[CEM\] Common Methodology for Information Technology SecurityEvaluation, Evaluation Methodology, CCMB-2017-04-004, Version 3.1 Revision 5, April 2017.

**Supporting document**

\[SD\] Evaluation Activities for Biometric verification on the mobiledevices \[TBD\]

**Other document**

\[Android CD\] Android 8.1 Compatibility Definition, December 2017

\[ISO19795-1\] Biometric performance testing and reporting — Part 1:Principles and framework, First edition

\[ISO19989-1\] Criteria and methodology for security evaluation ofbiometric systems — Part 1: Framework

\[ISO19989-2\] Criteria and methodology for security evaluation ofbiometric systems — Part 2: Biometric recognition performance

\[ISO19989-3\] Criteria and methodology for security evaluation ofbiometric systems — Part 3: Presentation attack detection

\[ISO21879\] Performance testing of biometrics on mobile devices, underdevelopment

\[ISO30107-1\] Biometric presentation attack detection —Part 1:Framework, First edition

\[ISO30107-3\] Biometric presentation attack detection —Part 3: Testingand reporting, First edition

\[MDFPP\] Protection Profile for Mobile Device Fundamentals, Version:3.1, 2017-06-16

\[NIST800-63B\] NIST Special Publication 800-63B, Digital IdentityGuidelines Authentication and Lifecycle Management, June 2017

1.5 Glossary
--------
For the purposes of this cPP, the following terms and definitions givenin \[ISO19795-1\] , \[ISO30107-1\] and \[MDFPP\] apply. If the sameterms and definitions are given in those references, terms and definitions that fit the context of this cPP take precedence. Some terms and definitions are also adjusted to match the context of the mobile biometric enrolment and verification.

| Term	| Definition |
|-------|----------------------------|
|**Adaptive (template)** |Authentication templates that evolve with each sample that is verified and introduced into the biometrics database. |
|**Attempt** |Submission of one (or a sequence of) biometric samples to the part of the TOE. |
|**Authentication Template** |Updated enrolment templates using verified samples for adapting changes of the users’ biometric characteristic caused by, for example, aging. |
|**Biometric Authentication Factor (BAF)** |Authentication factor used for mobile biometric verification. In this cPP, the term is a synonym of the “template”. |
|**Biometric Data** |Digital data created during a biometric process. It encompasses raw sensor observations, biometric samples, features, templates, and/or similarity scores, among other data. This data is used to describe the information collected during an biometric enrollment and verification process, but does not apply to end user information such as user name, password (unless tied to the biometric modality), demographic information, and authorizations. |
|**Biometric System Administrator** |Person who is responsible for configuring the TOE. This cPP assumes that the user acts as the biometric system administrator. |
|**Enrollment Template** |Templates generated during the enrollment process and utilized in various ways in order to generate an authentication template. |
|**Failure-To-Enrol Rate (FTE)** |Proportion of the population for whom the system fails to complete the enrolment process. |
|**False Accept Rate (FAR)** |Proportion of verification transactions with wrongful claims of identity that are incorrectly confirmed. |
|**False Match Rate (FMR)** |Proportion of zero-effort impostor attempt samples falsely declared to match the compared non-self template. |
|**False Non-match Rate (FNMR)** |Proportion of genuine attempt samples falsely declared not to match the template of the same characteristic from the same user supplying the sample. |
|**False Reject Rate (FRR)** |Proportion of verification transactions with truthful claims of identity that are incorrectly denied. |
|**Features** |Digital representation of the information extracted from a sample (by the signal processing subsystem) that will be used to construct or compare against enrolment templates. |
|**Locked State** |Powered on but most functionality is unavailable for use. User authentication is required to access functionality. |
|**Mobile Device (MD)** |A device which is composed of a hardware platform and its system software. The device typically provides wireless connectivity and may include software for functions like secure messaging, email, web, VPN connection, and VoIP (Voice over IP), for access to the protected enterprise network, enterprise data and applications, and for communicating to other Mobile Devices. |
|**Mobile Device User (User)** |The individual authorized to physically control and operate the Mobile Device. This cPP assumes that the user is the device owner. |
|**(Biometric) Modality**	|A type or class of biometric system, such as fingerprint recognition, facial recognition, iris recognition, voice recognition, signature/sign, and others. |
|**Password Authentication Factor** |A type of authentication factor requiring the user to provide a secret set of characters to gain access. |
|**Presentation Attack** |Presentation to the biometric data capture subsystem with the goal of interfering with the operation of the biometric system. |
|**Presentation Attack Detection (PAD)** |Automated determination of a presentation attack. |
|**Presentation Attack Instrument (PAI)** |Biometric characteristic or object used in a presentation attack (e.g. artificial or abnormal biometric characteristics). Accompanying supporting document specifies PAIs that the evaluator should consider for the CC evaluation. |
|**(Biometric) Sample** |User’s biometric measures as output by the part of the TOE. |
|**Similarity score** |Measure of the similarity between features derived from a sample and a stored template, or a measure of how well these features fit a user’s reference model. |
|**Template** |User’s stored reference measure based on features extracted from enrolment samples. There are two types of template (enrolment template and authentication template) defined in this cPP. |
|**Transaction** |Sequence of attempts on the part of a user for the purposes of an enrolment and verification. |
|**Zero-effort Impostor Attempt** |Attempt in which an individual submits his/her own biometric characteristics as if he/she were attempting successful verification against his/her own template, but the comparison is made against the template of another user. |

1.6 Revision history
----------------

| Version	| Date | Description |
|-------|-------|---------------------|
|0.1 |24th Oct, 2017 |Preliminary draft for the Berlin iTC session |  
|0.2 |26th Feb, 2018 |First version uploaded to the repo in the Github for review |

## 2. PP Introduction

2.1 PP Reference Identification
---------------------------
PP Reference: collaborative Protection Profile for Biometricverification on the mobile devices - for unlocking the device -
PP Version: 0.2
PP Date: 26-FEB-2018

2.2 TOE Overview
------------
This is a collaborative Protection Profile (cPP) whose Target ofEvaluation (TOE) is integrated into a mobile device and enrolls and verifies the user using his/her biometric characteristics to unlock themobile device in the locked state. Each mobile biometric enrolment and verification process is described in the following paragraphs.

a)  Mobile biometric enrolment

During the enrolment process, the TOE captures samples from the biometric characteristics of a user presented to the TOE and extracts the features from the samples. The features are then stored as an enrolment template in the TOE. If the TOE supports the use of adaptive templates, the enrolment template may be updated later using verified (i.e. successfully authenticated) samples for adapting changes of the user’s biometric characteristic caused by, for example, aging.

Only a user who knows the mobile device password can enroll or revoke his/her own templates. Multiple templates may be enrolled.

b)  Mobile biometric verification

During the verification process, a user presents his/her own biometric characteristics to the TOE without presenting any user identity information for unlocking the mobile device. The TOE retrieves all enrolled templates and compares them with the features extracted from the captured samples of the user to measure the similarity between thetwo data and determines whether to accept or reject the user based onthe similarity, and indicates the decision to the mobile device.

Examples of biometric characteristic used by the TOE are: fingerprint, face, iris, palm print, finger vein, palm vein, speech, signature and so forth. However, scope of this cPP is limited to only those modalities for which \[SD\] defines the Evaluation Activities.

c)  Presentation Attack Detection (PAD)

The TOE needs to consider the risk of subverting the TOE’s biometric verification. Attacker could present artificial or abnormal biometric characteristics to the TOE to interfere with the TOE’s security objectives. The TOE needs to be able to provide resistance to presentation attacks. \[SD\] explains what resistance should be provided by the TOE in detail.

2.3 TOE Design
----------
The TOE is fully integrated into the mobile device without the need for additional software and hardware. The following figure, inspired from \[ISO30107-1\], is a generic representation of a TOE (other configurations exist). This illustrates the different sub-functionalities on which the mobile biometric enrollment andverification processes rely on.


![cclogo](https://github.com/nils-tekampe/cPP-biometrics/blob/master/output/images/ESR.png)

                         Figure 1: Generic representation of a TOE


As illustrated in the above figure, the TOE is capable of;

-   Capturing samples from user’s biometric characteristics (Data Capture Subsystem)

-   Extracting and processing the features from samples (Signal Processing Subsystem)

-   Generating various templates based on processing of any samples or features during enrolment, and if adaptive, during verifications as well (Signal Processing Subsystem)

-   Storing the extracted information in a database on the mobile device (Data Storage Subsystem)

-   Comparing captured features with data contained in one or more authentication templates (Comparison Subsystem)

-   Detecting the presentation attacks using PAI (Presentation Attack Detection Subsystem)

-   Deciding how well features and any template match and indicating whether or not a verification of identity has been achieved    (Decision Subsystem)

2.4 Relation between TOE and mobile device
--------------------------------------
The TOE is reliant on the mobile device itself to provide overall security of the system. This cPP is intended to be used with \[MDFPP\]and \[MDFPP\] is responsible for evaluating the following securityfunctions:

-   Providing the Password Authentication Factor to support user authentication and management of the TOE security function

-   Providing the secure execution environment that guarantees the TOE and its data loaded inside to be protected with respect to    confidentiality and integrity

-   Invoking the TOE to enroll and verify the user and take appropriate actions based on the decision of the TOE

The evaluation of the above security functions is out of scope of this cPP and expected to be performed separately based on the \[MDFPP\]. Relation between the cPP and \[MDFPP\] is explained in detail in Annex A.


2.5 TOE Use Case
------------
Mobile device itself may be operated in a number of use cases such as enterprise use with limited personal use or Bring Your Own Device(BYOD). The TOE on the device may also be operated in the same use cases however use cases of the TOE should be devised separately considering the purpose of biometric verification and potential attacks. Thefollowing use cases describe how and why biometric verification issupposed to be used. Each use case has its own assurance level depending on its criticality and separate cPP should be developed for each usecase.
   
This cPP only assumes USE CASE 1 described below. USE CASE 2 is out ofscope of this cPP.
 
### 2.5.1 USE CASE 1: Mobile biometric verification for unlocking the mobile device
For enhanced security that is easy to use, mobile device may implement biometric verification on a device once it has been “unlocked”. The initial unlock is generally done by a PIN/password which is required at startup (or possibly after some period of time) and after that the user is able to use an own biometric characteristic to unlock access to the device. In this use case, mobile device is not supposed to be used for security sensitive services through the mobile biometric verification.

Main concern of this use case is the accuracy of biometric verification (i.e. FAR and FRR) and basic level of presentation attacks. Security assurance for mobile device that the TOE relies on should be handled by\[MDFPP\].

This use case assumes that the mobile device is configured correctly to enable the mobile biometric verification by the biometric system administrator.The users can act as the biometric system administrator in this use case.

It is also assumed that the user enrolls his/herself correctly following the guidance provided by the TOE. Attacks during enrolment may be out of scope but optionally addressed. FTE is not security relevant performance matrix for this use case.

### 2.5.2 USE CASE 2: Mobile biometric verification for security sensitive service
This use case is an example of another use case that isn’t considered in this cPP. Another cPP should be developed at higher assurance level for this use case.

Mobile devices may be used for security sensitive services such as payment transactions and online banking. Verification may be done by the biometric for convenience instead of PIN/password to access such security sensitive services.

The requirements for the TOE focus on the biometric performance (FTE, FAR and FRR) and presentation attack.

## 3. CC Conformance
As defined by the references \[CC1\], \[CC2\] and \[CC3\], this cPP:

-   conforms to the requirements of Common Criteria v3.1, Revision 5

-   is Part 2 extended, Part 3 conformant

-   does not claim conformance to any other PP.

The methodology applied for the cPP evaluation is defined in \[CEM\]. This cPP satisfies the following Assurance Families:
APE\_CCL.1, APE\_ECD.1, APE\_INT.1, APE\_OBJ.1, APE\_REQ.1 and APE\_SPD.1.

In order to be conformant to this cPP, a TOE must demonstrate Exact
Conformance. Exact Conformance, as a subset of Strict Conformance as
defined by the CC, is defined as the ST containing all of the SFRs in
chapter 6 (these are the mandatory SFRs) of this cPP, and potentially
SFRs from chapter 8 (these are selection-based SFRs) and chapter 9 
(these are optional SFRs) of this cPP. While iteration is allowed, no
additional requirements (from the CC parts 2 or 3, or definitions of
extended components not already included in this cPP) are allowed to be
included in the ST. Further, no SFRs in chapter 6 of this cPP are
allowed to be omitted.

## 4. Security Problem Definition

4.1 Threats
------------

#### T.Casual\_Attack 

An attacker may attempt to impersonate as a legitimate user without
being enrolled in the TOE. In order to perform the attack, the attacker
only use his/her own biometric characteristic (in form of a zero-effort
impostor attempt).

#### T.Presentation\_Attack

An attacker may attempt a presentation attack to the TOE. In order to
perform the attack, the attacker uses Presentation Attack Instrument
(PAI) except his/her own biometric characteristic.

4.2 Organizational Security Policies
------------

#### OSP.Enrol

The TOE shall enroll a user for mobile biometric verification, only
after successful authentication of a user. The TOE shall ensure that
templates are of sufficient quality in order to meet the relevant error
rates for mobile biometric verification.

#### OSP.Verification\_Error

The TOE shall meet relevant criteria for its security relevant error
rates for mobile biometric verification.

#### OSP.PAD\_Error

The TOE shall meet relevant criteria for its security relevant error
rates for PAD.

#### OSP.Protection

The TOE in cooperation with its environment shall protect itself and
relevant biometric data.

#### OSP.TrialLimit

The TOE in cooperation with its environment shall prevent impostors from
gaining access to the protected services by limiting the ability to make
repeated mobile biometric verification attempts.

4.3 Assumptions
------------

#### A.Authentication

It is assumed that the TOE environment invokes the TOE for mobile
biometric enrolment after authenticating the user or for mobile
biometric verification, and take appropriate actions based on the TOE’s
decision.

#### A.Alternative

It is assumed that an alternative authentication mechanism as a
complement to the TOE is available. This alternative authentication
mechanism can be used in cases where a user is rejected by the TOE
(False Rejection), configure the TOE or enroll the user. It is assumed
that this alternative mechanism reaches at least the same level of
security as the mobile biometric verification mechanism.

#### A.User

It is assumed that the user configures the TOE and its operational
environment correctly in a manner to ensure that the TOE security
policies will be enforced.

#### A.Management

It is assumed that the TOE environment protects the TOE configuration
adequately.

## 5. Security Objectives

5.1 Security Objectives for the TOE
-------------------------------

#### O.BIO\_Verification

The TOE shall provide a mobile biometric verification mechanism to
authenticate a user with an adequate reliability. The TOE shall meet the
relevant criteria for its security relevant error rates for mobile
biometric verification.

Application note:

In this cPP, relevant criteria are FAR and FRR and corresponding error
rates are needed to be specified in the FIA\_BVR\_EXT.1.

#### O.Presentation\_Attack\_Detection

The TOE shall prevent a presentation attack using Presentation Attack
Instrument (PAI). The TOE shall meet relevant criteria for its security
relevant error rates for PAD

Application note:

The TOE may or may not counter a presentation attack during enrollment. 
If the ST author requires the TOE to counter the attack
during enrollment, ST author should include relevant optional
security requirement defined in chapter 9.

According to the \[ISO30107-3\], relevant criteria should be specified
for each type of PAI. \[SD\] specifies PAIs used for attack and
describes how to create and present the PAI to the TOE, and minimum
error rates that the TOE needs to achieve.

#### O.Enrol

The TOE shall implement the functionality to enroll a user for mobile
biometric verification, only after successful authentication of the
user. The TOE shall check the quality of enrolment templates in order to
meet the relevant error rates for mobile biometric verification.

Application note:

A user has to be authenticated using a password to start the enrolment
as required by \[MDFPP\].

In this cPP, relevant criteria are FAR and FRR and corresponding error
rates are needed to be specified in the FIA\_BVR\_EXT.1.

#### O.Protection

The TOE shall protect biometric data except publicly accessible
biometric data using security functions provided by the TOE environment.

Application note:

As described in Annex A, the TOE and TOE environment (i.e. mobile
device) needs to satisfy related requirements defined in this cPP and
\[MDFPP\] respectively.

5.2 Security Objectives for the Operational Environment
---------------------------------------------------

#### OE.Authentication

TOE environment shall invoke the TOE for mobile biometric enrolment
after authenticating the user or for mobile biometric verification, and
take appropriate actions based on the TOE’s decision.

Application note:

As described in Annex A, the TOE environment (i.e. mobile device) needs
to satisfy related requirements defined in the \[MDFPP\].

#### OE.Alternative

Alternative authentication mechanism as a complement to the TOE shall be
available. This alternative authentication mechanism can be used in
cases where a user is rejected by the mobile biometric verification
(False Rejection), configure the TOE or enroll the user. This
alternative mechanism shall reach at least the same level of security as
the mobile biometric verification mechanism.

Application note:

As described in Annex A, the TOE environment (i.e. mobile device) needs
to satisfy related requirements defined in the \[MDFPP\].

#### OE.Protection

The TOE environment shall ensure that the TOE and its biometric data is
adequately protected.

Application note:

As described in Annex A, the TOE and TOE environment (i.e. mobile
device) needs to satisfy related requirements defined in this cPP and
\[MDFPP\] respectively.

#### OE.TrialLimit

The TOE environment shall be able to limit the maximum number of
unsuccessful mobile biometric verification attempts.

Application note:

The TOE environment (i.e. mobile device) needs to limit the maximum
number of unsuccessful verification attempts as required by \[MDFPP\].

#### OE.User

The user will configure the device correctly in a manner to ensure that
the TOE security policies will be enforced.

Application note:

Mobile device needs to be configured by the user as required by
\[MDFPP\].

#### OE.Management

The TOE environment shall protect the TOE configuration securely.

Application note: As mentioned in Annex A, this cPP assumes that the TOE
environment control access to the TOE configuration (e.g. enable/disable
the mobile biometric verification) in a secure manner.

5.3 Security Objectives Rationale
-----------------------------

The following table describes how the assumptions, threats, and
organizational security policies map to the security objectives.

| Threat, Assumption, or OSP	| Security Objectives	| Rationale |
|-------|---------------|-------------|
|T.Casual\_Attack OSP.Verification\_Error | O.BIO\_Verification | The threat T.Casual\_Attack is countered by O.BIO\_Verification as this provides the capability of mobile biometric verification not to allow the user who have not been enrolled to impersonate as a legitimate user. The OSP OSP.Verification\_Error is enforced by O.BIO\_Verificaiton as this requires the TOE to meet relevant criteria for security relevant error rates for mobile biometric verification. |
|T.Presentation\_Attack 	OSP.PAD\_Error | O.Presentation\_Attack\_Detection | The threat T.Presentation\_Attack is countered by O.Presentation\_Attack\_Detection as this provides the capability of biometric verification to prevent attacks with PAI. The OSP OSP.PAD\_Error is enforced by O.Presentation\_Attack\_Detection as this requires the TOE to meet relevant criteria for security relevant error rates for PAD. |
|OSP.Enrol | O.Enrol | The OSP OSP.Enrol is enforced by O.Enrol as this require the TOE to implement the functionality to enroll a user for mobile biometric verification and check quality of templates. |
|OSP.TrialLimit | OE.TrialLimit | The OSP OSP.TrialLimit is enforced by the operational environment objective OE.TrialLimit. |
|OSP.Protection | O.Protection  OE.Protection | The OSP OSP.Protection is enforced by O.Protection and its operational environment objective OE.Protection. |
|A.Authentication | OE.Authentication | The Assumption A.Authentication is satisfied by the operational environment objective OE.Authentication. |
|A.Management | OE.Management | The Assumption A.Management is satisfied by the operational environment objective OE.Management. |
|A.User | OE.User | The Assumption A.User is satisfied by the operational environment objective OE.User. |
|A.Alternative |OE.Alternative | The Assumption A.Alternative is satisfied by the operational environment objective OE.Alternative. |

                   Table 1: Mapping between Security Problem Defintion and Security Objectives

## 6. Security Functional Requirements

6.1 Conventions
-----------

The individual security functional requirements are specified in the
sections below.

The following conventions are used for the completion of operations:

-   \[*Italicized text within square brackets*\] indicates an operation
    to be completed by the ST author

-   [Underlined text] indicates additional text provided as a
    refinement.

-   \[***Bold and italicized text within square brackets***\] indicates
    the completion of an assignment.

-   \[*Italicized text within square brackets*\] indicates the
    completion of a selection.

-   Number in parentheses after SFR name, e.g. (1), indicates the
    completion of an iteration.

Extended SFRs are identified by having a label“EXT” at the end of the
SFR name.

6.2 Identification and Authentication (FIA)
---------------------------------------
### 6.2.1 Timing of the user authentication with biometric verification (FIA\_BVR\_EXT.1)

### FIA\_BVR\_EXT.1 User authentication with biometric verification

**FIA\_BVR\_EXT.1.1** The TSF shall provide a mobile biometric
verification mechanism using \[**selection:** *fingerprint, iris, face,
voice, vein*, \[**assignment:** *other modality* \] \].

**FIA\_BVR\_EXT.1.2** The TSF shall provide a mobile biometric
verification mechanism with the \[**selection:** *FMR, FAR* \] not exceeding
\[**assignment:** *defined value* \] and \[**selection:** *FNMR, FRR* \] not exceeding
\[**assignment:** *defined value* \].

Application note 1:

If the TOE support multiple BAFs, ST author may iterate the SFR to
define different error rates for each BAF.

Application note 2:

ST author needs to select or assign those modalities in FIA_BVR_EXT.1.1 for which \[SD\] defines the Evaluation Activities.

Application note 3:

Value of FMR, FAR, FNMR and FRR needs to be assigned by the ST author
however the ST author should consider the following factors for setting
those values.

a)  Required minimum values defined in the standards

For example, \[NIST800-63B\] requires that FMR shall be 1 in 1000 or
lower. \[ISO21879\] is proposing that FAR would be 1 in 10000 or lower
that is equal to a conventional four-digit PIN-Code for secure
transaction. According to \[Android CD\], finger print verification must
have the FAR lower than 0.002% and recommended to have the FRR lower
than 10%. The cPP doesn’t provide any recommendation for those error
rates however, ST author should set appropriate error rates referring
those value.

For consistency in language throughout this document, referring to a
“lower” number will mean the chance of occurrence is lower (i.e. 1/100
is lower than 1/20). So, saying device 1 has a lower FAR than device 2
means device 1 could have 1/1000 and device 2 would be 1/999 or higher
in terms of likelihood. Saying “greater” will explicitly mean the
opposite.

b)  Technical limitation

Although different modalities are available for the mobile biometric
verification, all modalities may not achieve the same level of accuracy.
For modalities that have different target of error rates, ST author can
iterate the requirement to set appropriate error rates for each
modality.

c)  Number of test subjects required for the performance testing

Target error rates defined in SFR must be evaluated based on \[SD\].
Normally the target error rates will directly influence the size of the
test subject, the time and cost of the testing. \[SD\] describes how
those error rates should be evaluated in an objective manner.

### 6.2.2	Biometric verification not accepting presentation attack instruments (FIA_BVR_EXT.2)

### FIA\_BVR\_EXT.2 Biometric verification not accepting presentation attack instruments

**FIA\_BVR\_EXT.2.1** The TSF shall prevent presentation of biometric
characteristics which result in biometric samples of low quality from
being successful in the biometric verification.

**FIA\_BVR\_EXT.2.2** The TSF shall prevent use of artificial
presentation attack instruments from being successfully verified.

Application note 1:
If the TOE support multiple BAFs, ST author may iterate the SFR to define different error rates for each BAF.

Application note 2: \[SD\] describes that how evaluator should test the TOE to verify that it meets these security requirements.

### 6.2.3	Check of biometric samples for enrolment (FIA_EBR_EXT.1)

### FIA\_EBR.EXT.1 Check of biometric samples for enrolment 

**FIA\_EBR\_EXT.1.1** The TSF shall prevent use of biometric
characteristics of low quality for enrolment that has been presented by
any user of the TSF.

Application note 1: \[SD\] describes that how evaluator should test the TOE to verify that it meets this security requirements.


-------------

***Additional SFRs may be added to the cPP
See Environment protection requirements from MDFPP (https://github.com/nils-tekampe/cPP-biometrics/issues/69)***

--------------

## 7. Security Assurance Requirements

This chapter lists the set of SARs from CC part 3 that are required in
evaluations against this cPP. Individual Evaluation Activities to be
performed are specified in \[SD\].

This cPP is intended to be used with \[MDFPP\] as the mobile device
should provide security functionality that the TOE can rely on, as
explained in Annex A. Any developer’s deliverables required by this cPP
except the ST can be merged into ones required by \[MDFPP\], rather than
preparing separate document for each evaluation to reduce cost and
effort for the evaluations.

The TOE security assurance requirements are identified in Table 2.

| Assurance Class	| Assurance Components |
|--------------|---------------------|
|Security Target (ASE) |Conformance claims (ASE\_CCL.1) Extended components definition (ASE\_ECD.1) ST introduction (ASE\_INT.1) Security objectives for the operational environment (ASE\_OBJ.1) Stated security requirements (ASE\_REQ.1) Security Problem Definition (ASE\_SPD.1) TOE summary specification (ASE\_TSS.1) |  
|Development (ADV) |Basic functional specification (ADV\_FSP.1) |
|Guidance documents (AGD) |Operational user guidance (AGD\_OPE.1) Preparative procedures (AGD\_PRE.1) |
|Life cycle support (ALC) |Labelling of the TOE (ALC\_CMC.1) TOE CM coverage (ALC\_CMS.1) |
|Tests (ATE) |Independent testing – conformance (ATE\_IND.1) |
|Vulnerability assessment (AVA) |Vulnerability survey (AVA\_VAN.1) |

                              Table 2: Security Assurance Requirements

7.1 ASE: Security Target
--------------------

The ST is evaluated as per ASE activities defined in the CEM. In
addition, there may be

Evaluation Activities specified within \[SD\] that call for necessary
descriptions to be included in the TSS that are specific to the TOE
technology type.

The requirements for exact conformance of the Security Target are
described in section 3.

7.2 ADV: Development
----------------

The design information about the TOE is contained in the guidance
documentation available to the end user as well as the TSS portion of
the ST, and any required supplementary information required by this cPP
that is not to be made public. \[SD\] defines required supplementary
information that is necessary for Evaluation Activities.

### 7.2.1 Basic Functional Specification (ADV\_FSP.1)

The functional specification describes the TOE Security Functions
Interfaces (TSFIs). It is not necessary to have a formal or complete
specification of these interfaces. Additionally, because TOEs conforming
to this cPP will necessarily have interfaces to the mobile device that
are not directly invokable by TOE users, there is little point
specifying that such interfaces be described in and of themselves since
only indirect testing of such interfaces may be possible. For this cPP,
the Evaluation Activities for this family focus on understanding the
interfaces presented in the TSS in response to the functional
requirements and the interfaces presented in the AGD documentation. No
additional “functional specification” documentation is necessary to
satisfy the Evaluation Activities specified in \[SD\].

The Evaluation Activities in \[SD\] are associated with the applicable
SFRs; since these are directly associated with the SFRs, the tracing in
element ADV\_FSP.1.2D is implicitly already done and no additional
documentation is necessary.

7.3 AGD: Guidance Documentation
---------------------------

This cPP assumes that the TOE is embedded into the mobile device and it
is configured and managed as described in guidance document that satisfy
requirements defined in the \[MDFPP\].

In addition to guidance document required by the \[MDFPP\], guidance
pertaining to mobile biometric enrolment and verification must also be
provided. Requirements on such guidance are contained in the Evaluation
Activities specified in \[SD\].

### 7.3.1 Operational User Guidance (AGD\_OPE.1)

The operational user guidance does not have to be contained in a single
document. Guidance to users can be included in the mobile device
guidance document or can be spread among other document or web pages.

The developer should review the Evaluation Activities contained in
\[SD\] to ascertain the specifics of the guidance that the evaluator
will be checking for. This will provide the necessary information for
the preparation of acceptable guidance.

### 7.3.2 Preparative Procedures (AGD\_PRE.1)

Preparative procedures are useful for ensuring that the TOE has been
received and installed in a secure manner as intended by the developer.
However, the TOE is embedded into the mobile device and it is assumed
that such information will be provided by the mobile device guidance
document and evaluated by the mobile device evaluation based on
\[MDFPP\]. Therefore, AGD\_PRE.1.1D is implicitly already done by those
evaluation and no additional documentation is necessary.

7.4 ALC: Life-cycle Support
---------------------------

At the assurance level provided for TOEs conformant to this cPP, 
life-cycle support is limited to end-user-visible aspects of the life-cycle,
rather than an examination of the TOE vendor’s development and configuration
management process. This is not meant to diminish the critical role that a 
developer’s practices play in contributing to the overall trustworthiness of 
a product, rather, it is a reflection on the information to be made available 
for evaluation at this assurance level.

### 7.4.1 Labelling of the TOE (ALC_CMC.1)
This component is targeted at identifying the TOE such that it can be 
distinguished from other products or versions from the same vendor and can be 
easily specified when being procured by an end user. The evaluator performs 
the CEM work units associated with ALC_CMC.1.

The TOE is tightly integrated into the mobile device. \[SD\] describes how 
evaluator performs the CEM work units associated with ALC_CMC.1 based on 
the relation between the TOE reference and the mobile device reference.

### 7.4.2 TOE CM Coverage (ALC_CMS.1)
Given the scope of the TOE and its associated evaluation evidence requirements, 
the evaluator performs the CEM work units associated with ALC_CMS.1.

7.5 ATE: Tests
---------------------------

Testing is specified for functional aspects of the system as well as aspects 
that take advantage of design or implementation weaknesses. The former is 
done through the ATE_IND family, while the latter is through the AVA_VAN 
family. For this cPP, testing is based on advertised functionality and 
interfaces with dependency on the availability of design information. 
One of the primary outputs of the evaluation process is the test report 
as specified in the following requirements.

### 7.5.1 Independent Testing – Conformance (ATE_IND.1)
Testing is performed to confirm the functionality described in the TSS 
as well as the guidance documentation. The focus of the testing is to 
confirm that the requirements specified in chapter 6 are being met. 
The Evaluation Activities in \[SD\] identify the specific testing 
activities necessary to verify compliance with the SFRs. The evaluator 
produces a test report documenting the plan for and results of testing, 
as well as coverage arguments focused on the platform/TOE combinations 
that are claiming conformance to this cPP.

7.6 AVA: Vulnerability Assessment
---------------------------

\[SD\] developed by the iTC describes the minimum penetration test items 
based on the attack potential that the cPP assumes, publicly available 
vulnerability information and technical discussion within the iTC. 
Evaluator shall refer \[SD\] to device the penetration test items.

### 7.6.1 Vulnerability Survey (AVA_VAN.1)
\[SD\] provides a guide to the evaluator in performing a vulnerability analysis.

## 8. Selection-Based Requirements
As indicated in the introduction to this cPP, the baseline requirements 
(those that must be performed by the TOE) are contained in the chapter 6. 
Additionally, there are two other types of requirements specified in 
chapter 8 and 9.

The first type (in this chapter) comprises requirements based on 
selections in other SFRs from the cPP: if certain selections are made, 
then additional requirements in this chapter will need to be included 
in the body of the ST.

The second type (in chapter 9) comprises requirements that can be 
included in the ST, but are not mandatory for a TOE to claim conformance 
to this cPP. 


**_TBD_**

## 9. Optional Requirements

If a TOE fulfils any of the optional requirements, the vendor is 
encouraged to add the related functionality to the ST. Therefore, 
in the application notes of this chapter the wording "This option 
should be chosen..." is repeatedly used. But it also is used to 
emphasize that this option should only be chosen if the TOE provides 
the related functionality and that it is not necessary to implement 
the related functionality to be compliant to the cPP. ST authors are 
free to choose none, some or all SFRs defined in this chapter. Just 
the fact that a product supports a certain functionality does not 
mandate to add any SFR defined in this chapter.


**_SFR for PAD during the enrollment (e.g. The TSF shall perform Presentation Attack Detection testing on each biometric enrollment) will be added here_**

## 10. Extended Component Definitions
This appendix contains the definitions for the extended requirements 
that are used in the cPP, including those used in chapter 8 and 9.

(Note: formatting conventions for selections and assignments in this chapter are those in \[CC2\].)

**_TBD_**

## Annex A

## 1.	Overview
This Annex describes relation between this cPP and \[MDFPP\].

The TOE in this cPP is comprised of biometric capture sensors and 
firmware/software that provide functions described in Section 2.3 
(TOE design). The TOE is invoked by the mobile device (i.e. TOE 
environment) when user’s biometric characteristics is presented to 
the sensor, creates and stores the template or compares the features 
with the stored template and returns the verification outcome to 
the mobile device. 

This cPP assumes that the mobile device satisfies SFRs defined in the 
\[MDFPP\] so that the TOE can satisfy SFRs defined in this cPP. The next 
section explains what SFRs in the \[MDFPP\] are directly relevant to 
the TOE security functionality.

## 2.	Relevant SFRs in the \[MDFPP\]
Relation between SFRs defined in this cPP and \[MDFPP\] is described below. **Bold SFRs** are those defined in this cPP and *italicized SFRs* are those defined in the \[MDFPP\]

### 2.1	Password authentication
Mobile device needs to implement the Password Authentication Factor as 
required by the *FIA_UAU.5.1*. This password authentication is used to 
configure (e.g. enable/disable) the TOE, enroll the user, and as an 
alternative authentication mechanism when the user is rejected by the 
mobile biometric verification.

This cPP assumes that above requirements are satisfied by the TOE environment as defined in OE.Alternative.

### 2.2	Invocation of the TOE
Any BAF selected in *FIA_UAU.5.1*, the TOE must be invoked by the mobile 
device to unlock the device when the user presents his/her biometric 
characteristic and the TOE shall provide a mobile biometric verification 
mechanism that satisfy SFRs defined in this cPP. This means that same 
BAF shall be selected in **FIA_BVR_EXT.1.1**, and relevant criteria and 
its error rate shall be specified in **FIA_BVR_EXT.1.2**. If multiple BAFs 
are selected in *FIA_UAU.5.1*, **FIA_BVR_EXT.1** shall be iterated for each BAF. 
Mobile device need to authenticate the user following the rule specified in 
*FIA_UAU.5.2*. Mobile device needs to invoke the TOE as specified in *FIA_UAU.6.1(2)*.

This cPP assumes that above requirements are satisfied by the TOE environment as defined in OE.Authentication.

### 2.3	Handling the verification outcome
Mobile device needs to take appropriate actions after receiving the 
verification outcome from the TOE as defined in *FIA_AFL_EXT.1*. *FIA_AFL_EXT.1* 
defines rules regarding how the authentication factors interact in terms of 
unsuccessful authentication and actions mobile device needs to take when number 
of unsuccessful authentication attempts surpass the pre-defined number. Mobile device 
also needs to apply authentication throttling after failed biometric verification as 
required by *FIA_TRT_EXT.1.1*.

This cPP assumes that above requirements are satisfied by the TOE environment as defined in OE.Authentication and OE.TrialLimit.

### 2.4	Protection of the TOE and its biometric data
Mobile device needs to provide the secure execution environment (e.g. restricted 
operational environment) so that TOE can work securely. This secure execution 
environment guarantees code and data loaded inside to be protected with respect 
to confidentiality and integrity. Security of this secure execution environment 
needs to be evaluated based on \[MDFPP\]. Mobile device also needs to verify 
the integrity of the TOE prior to its execution as required by *FPT_TST_EXT.2*, 
and keep secret of any sensitive information regarding the biometric when mobile 
device receives the verification outcome from the TOE as required by *FIA_UAU.7.1*.

This cPP assumes that above requirements are satisfied by the TOE environment as defined in OE.Protection

However, the TOE shall use this secure execution environment correctly to protect 
biometric data except publicly accessible biometric data (e.g. face image) and 
satisfy the following requirements.

  * The TOE shall save all biometric data (e.g. samples, features and templates) inside the secure execution environment
  * The TOE shall not transmit biometric data to the outside the secure execution environment.
  * The TOE shall process biometric data in the secure execution environment to enroll and verify the user.

The TOE shall also protect biometric data, especially the templates, residing outside the secure execution environment.

  * The TOE shall store only the encrypted form of the templates on the file system.
  * The TOE shall erase templates on the file system when they are no longer needed (e.g. when template is revoked)

The above requirements are defined in **_FPTXXXX, FPTXXXX and FPTXXXX**_. 
**FDP_PBA_EXT.1.1** to protect the main TOE security functions, i.e. mobile 
biometric enrolment, mobile biometric verification and PAD as required by 
**FIA_EBR.EXT.1**, **FIA_BVR_EXT.1** and **FIA_BVR_EXT.2** in this cPP.

### 2.5	Management of the TOE configuration
Mobile device needs to enable/disable the BAF as required by *FMT_SMF_EXT.1 (Management function 23)* 
and revoke the BAF as *FMT_SMF_EXT.1 (Management Function 46)*. Any change 
to the BAF (e.g. adding or revoking templates) requires re-authentication 
via the Password Authentication Factor as required by *FIA_UAU.6.1(1)*. 

This cPP assumes that above requirements are satisfied by the TOE environment as defined in OE.Management.


