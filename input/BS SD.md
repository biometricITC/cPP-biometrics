# Supporting Document Mandatory Technical Document

# Evaluation Activities for collaborative Protection Profile for Mobile biometric enrolment and verification - for unlocking the device - cPP
## Version 0.1 28-MAR-2018

**Foreword**

This is a supporting document, intended to complement the Common
Criteria version 3 and the associated Common Evaluation Methodology for
Information Technology Security Evaluation.

Supporting documents may be “Guidance Documents”, that highlight
specific approaches and application of the standard to areas where no
mutual recognition of its application is required, and as such, are not
of normative nature, or “Mandatory Technical Documents”, whose
application is mandatory for evaluations whose scope is covered by that
of the supporting document. The usage of the latter class is not only
mandatory, but certificates issued as a result of their application are
recognized under the CCRA.

This supporting document has been developed by the biometric Security
iTC (BS-iTC) and is designed to be used to support the evaluations of
TOEs against the cPPs identified in section 1.1.

**Technical Editor:** Biometric Security international Technical
Community (BS-iTC)

**Document history:**

*V0.1, March 2018 (Initial Release for Public review)*

**General Purpose:** See section 1.1.

**Field of special use:** This Supporting Document applies to the
evaluation of TOEs claiming conformance with the collaborative
Protection Profile for Mobile biometric enrolment and verification - for
unlocking the device - \[BScPP\].

**Acknowledgements:**

This Supporting Document was developed by the Biometric Security
international Technical Community with representatives from industry,
Government agencies, Common Criteria Test Laboratories, and members of
academia.



Introduction
============

Technology Area and Scope of Supporting Document
------------------------------------------------

This Supporting Document defines the Evaluation Activities associated
with the collaborative Protection Profile for Mobile biometric enrolment
and verification - for unlocking the device - \[BScPP\].

The Biometric Security technical area has a number of specialised
aspects, such as those relating to the mobile biometric enrolment and
verification, and to the particular ways in which the TOE need to be
assessed across a range of different Presentation Attack Instruments
(PAI). This degree of specialisation, and the associations between
individual SFRs in the cPP, make it important for both efficiency and
effectiveness that evaluation activities are given more specific
interpretations than those found in the generic CEM activities

This Supporting Document is mandatory for evaluations of products that
claim conformance to \[BScPP\].

Although Evaluation Activities are defined mainly for the evaluators to
follow, the definitions in this Supporting Document aim to provide a
common understanding for developers, evaluators and users as to what
aspects of the TOE are tested in an evaluation against the associated
cPPs, and to what depth the testing is carried out. This common
understanding in turn contributes to the goal of ensuring that
evaluations against the cPP achieve comparable, transparent and
repeatable results. In general the definition of Evaluation Activities
will also help developers to prepare for evaluation by identifying
specific requirements for their TOE. The specific requirements in
Evaluation Activities may in some cases clarify the meaning of SFRs, and
may identify particular requirements for the content of Security Targets
(especially the TOE Summary Specification), user guidance documentation,
and possibly supplementary information (e.g. for biometric performance
testing – see section 6).

Structure of the Document
-------------------------

Evaluation Activities can be defined for both Security Functional
Requirements and Security Assurance Requirements. These are defined in
separate sections of this Supporting Document.

If any Evaluation Activity cannot be successfully completed in an
evaluation then the overall verdict for the evaluation is a ‘fail’. In
rare cases there may be acceptable reasons why an Evaluation Activity
may be modified or deemed not applicable for a particular TOE, but this
must be agreed with the Certification Body for the evaluation.

In general, if all Evaluation Activities (for both SFRs and SARs) are
successfully completed in an evaluation then it would be expected that
the overall verdict for the evaluation is a ‘pass’. To reach a ‘fail’
verdict when the Evaluation Activities have been successfully completed
would require a specific justification from the evaluator as to why the
Evaluation Activities were not sufficient for that TOE.

Similarly, at the more granular level of Assurance Components, if the
Evaluation Activities for an Assurance Component and all of its related
SFR Evaluation Activities are successfully completed in an evaluation
then it would be expected that the verdict for the Assurance Component
is a ‘pass’. To reach a ‘fail’ verdict for the Assurance Component when
these Evaluation Activities have been successfully completed would
require a specific justification from the evaluator as to why the
Evaluation Activities were not sufficient for that TOE.

Application of this Supporting Document
---------------------------------------

This Supporting Document (SD) defines three types of Evaluation
Activities (EAs) – TOE Summary Specification (TSS), Guidance
Documentation, and Tests and is designed to be used in conjunction with
cPPs. cPPs that rely on this SD will explicitly identify it as a source
for their EAs. Each security requirement (SFR or SAR) specified in the
cPP could have multiple EAs associated with it. The security requirement
naming convention is consistent between cPP and SD ensuring a clear one
to one correspondence between security requirements and evaluation
activities.

The cPP and SD are designed to be used in conjunction with each other,
where the cPP lists SFRs and SARs and the SD catalogues EAs associated
with each SFR and SAR. Some of the SFRs included in the cPP are optional
or selection-based. Therefore an ST claiming conformance to the cPP does
not necessarily have to include all possible SFRs defined in the cPP.

In an ST conformant to the cPP, several operations need to be performed
(mainly selections and assignments). Some EAs define separate actions
for different selected or assigned values in SFRs. The evaluator shall
neither carry out EAs related to SFRs that are not claimed in the ST nor
EAs related to specific selected or assigned values that are not claimed
in the ST.

EAs do not necessarily have to be executed independently from each
other. A description in a guidance documentation or one test case, for
example, can cover multiple EAs at a time, no matter whether the EAs are
related to the same or different SFRs.

Terminology
-----------

### Glossary

For definitions of standard CC terminology see \[CC\] part 1.

**TBD**
                            
                            
                            
                            

### Acronyms

**TBD**
                                                                                                                               
                                                              
Evaluation Activities for SFRs
==============================

The EAs presented in this section capture the actions the evaluator
performs to address technology specific aspects covering specific SARs
(e.g., ASE\_TSS.1, ADV\_FSP.1, AGD\_OPE.1, and ATE\_IND.1) – these
actions are derived from the CEM work units that are performed in
Section 5 (Evaluation Activities for SARs) and provide more specific and
detailed instructions that evaluator must follow to perform those work
units.

Structure of EAs defined in this SD include the following items that
ISO/IEC 15408-4 requires. This standard describes a framework that shall
be used for deriving EAs from CEM work units and specifies how to define
EAs.

1. Objective

Objective defines the goal of an EA. Assessment Strategy describes how
the evaluator can achieve this goal in more detail and Pass/fail
criteria defines how the evaluator can determine whether the goal is
achieved or not.

2. Relationship of the evaluation activity to SFRs, SARs, and other EAs

SFRs or SARs that an EA is directly related are identified here.

Where an EA depends on completion of another EA then the dependency and
the other EA is identified here.

3. Tool types required to perform the activity

If performing an EA requires any tool types in order to complete the EA
then these tool types are defined here.

4. Required input from the developer or other entities

Additional detail is specified here regarding the required format and
content of the inputs to an EA.

5. Assessment Strategy

Assessment Strategy provides guidance and details how to perform an EA.
It includes, as appropriate to the content of the EA:

a)  how to assess the input from the developer or other entities for
    completeness with respect to the EA

b)  how to make use of any tool types required (potentially including
    guidance for the calibration or setup of the tools)

c)  guidance on the steps for performing the EA


6. Pass/fail criteria

The evaluator uses these criteria to determine whether the EA has
demonstrated that the TOE has met the relevant requirement or that it
has failed to meet the relevant requirement.

7. Requirements for reporting　　

Specific reporting requirements that support transparency and 
reproducibility of the pass/fail judgement are defined here.

FIA: Identification and Authentication
--------------------------------------

### EA for FIA\_MBE\_EXT.1

#### Objective

The evaluator shall verify that the TOE enrols a user only after
successful authentication of the user by his/her password. Security
requirements for the password authentication are defined in \[MDFPP\]
and out of scope of this EA.

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FIA\_MBE\_EXT.1. There is no dependency to other
EAs defined in this SD.

#### Tool types required to perform the activity

No tool is required for this EA.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FIA\_MBE\_EXT.1 at high level
    description

b)  AGD guidance shall provide clear instruction for a user to enrol
    his/herself.

AGD guidance includes online assistance, prompt or warning provided by
the TOE during the enrolment attempt.

#### Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall refer the TSS to understand how the TOE enrol a user
and examine the AGD guidance to confirm that a user is required to enter
valid his/her password before the mobile biometric enrolment.

As described in the \[BScPP\], formal or complete specification of the
interfaces is not required however, if such information is available,
evaluator may also refer the specification for enrolment interface to
examine that it checks whether a successful password authentication is
done or not before starting the enrolment.

The above EA is derived from ASE\_TSS.1-1, ADV\_FSP.1-7, AGD\_OPE.1-4
and AGD\_OPE.1-5.

\[Strategy for ATE \_IND\]

The evaluator shall perform the following test to verify that the TOE
performs the mobile biometric enrolment correctly.

Step 1: The evaluator shall try to enrol he/herself without setting a
valid password and confirm that he/she can’t enrol his/herself without
setting a password.

Step 2: The evaluator shall set a valid password and confirm that he/she
can’t enrol his/herself without entering the valid password beforehand
in any case.

The above EA is derived from ATE\_IND.1-3, ATE\_IND.1-4, ATE\_IND.1-5,
ATE\_IND.1-6, and ATE\_IND.1-7.

#### Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance

b)  only authenticated users by password can enrol his/herself and any
    attempts to enrol without the authentication are rejected though the
    independent testing

#### Requirements for reporting

This EA does not require reports or report details other than those
given in the work unit from which it is derived.

### EA for FIA\_MBE\_EXT.2

#### Objective

Mobile biometric verification performance depends on quality of
enrolment and authentication templates that is compared to the samples
presented to the TOE. The evaluator shall examine that the TOE checks
the quality of enrolment and authentication templates based on the
assessment criteria to verify a user with an adequate reliability.

If the TOE doesn’t create authentication templates, this EA is only
applicable to enrolment templates.

The evaluator shall keep in mind that the assessment criteria for
different biometric modalities may not be the same. The evaluator shall
iterate this EA for each biometric modality if the ST author selects
multiple biometric modalities in FIA\_MBV\_EXT.1.

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FIA\_MBE\_EXT.2. The evaluator shall perform the
EA for FIA\_MBE\_EXT.1 first to confirm the mobile biometric enrolment
can be done correctly.

#### Tool types required to perform the activity

Developer shall provide a test platform for the evaluator to conduct the
test described in the Assessment Strategy.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FIA\_MBE\_EXT.2 at high level
    description

b)  AGD guidance shall provide clear instruction for a user to enrol
    his/herself

c)  Supplementary information (Assessment criteria for templates) shall
    describe assessment criteria for creating templates

AGD guidance includes online assistance, prompt or warning provided by
the TOE during the enrolment attempt.

#### Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

**Enrolment templates**

The evaluator shall refer the TSS to understand how the TOE generate
sufficient quality of enrolment templates. The evaluator shall also
examine the guidance, including online assistance or prompt provided by
the TOE, about how the TOE supports a user to enrol his/herself
correctly and how the TOE behaves when low quality samples are presented
to the TOE.

The evaluator shall examine that “assessment criteria for templates” to
check that how the TOE creates the enrolment templates based on its
assessment criteria. The “assessment criteria for templates” may
include;

a)  quality requirements for the biometric sample to ensure that a
    sufficient amount of distinctive features is available

b)  method to quantify the quality of samples (e.g. method to generate
    quality score)

c)  assessment criteria to accept the sample of sufficient utility (e.g.
    compare quality score to quality threshold)

d)  quality standard that the TOE uses to perform the assessment if the
    TOE follows such standard (e.g. NFIQ for fingerprint)

e)  additional assessment criteria to applied to creation of enrolment
    templates


**Authentication templates**

If the TOE creates authentication templates, the evaluator shall refer
the TSS to understand how the TOE generate sufficient quality of
authentication templates.

The evaluator shall examine that the “assessment criteria for templates”
to check that how the TOE creates the authenticate templates based on
its assessment criteria. The “assessment criteria for templates” may
include a) – d) and;

a)  additional assessment criteria to applied to creation of
    authentication templates

The above EA is derived from ASE\_TSS.1-1, ADV\_FSP.1-7, AGD\_OPE.1-4
and AGD\_OPE.1-5.

\[Strategy for ATE \_IND\]

**Enrolment templates**

The evaluator shall perform the following test to verify that the TOE
generates enrolment templates of sufficient quality. If the TOE supports
multiple biometric modalities, the same test shall be done for each
modality.

The following test requires the developer to provide access to a test
platform that provides the evaluator with tools that are typically not
found on factory products.

Step 1: The evaluator shall present biometric samples of low quality for
the mobile biometric enrolment that don’t satisfy the assessment
criteria described in “assessment criteria for templates”.

Step 2: The evaluator shall check the TOE internal data (e.g. quality
scores and quality threshold) to confirm that the TOE doesn’t create
enrolment templates that don’t meet the assessment criteria specified in
the “assessment criteria for templates”.

**Authentication templates**

The evaluator shall perform the following test to verify that the TOE
generates authentication templates of sufficient quality only if the
evaluator judge that creating authentication templates is feasible. If
the TOE supports multiple biometric modalities, the same test shall be
done for each modality.

The following test requires the developer to provide access to a test
platform that provides the evaluator with tools that are typically not
found on factory products.

Step 1: The evaluator shall enroll his/herself.

Step 2: The evaluator shall present biometric samples repeatedly to
trigger the TOE to create authentication templates.

Step 3: The evaluator shall check the TOE internal data (e.g. quality
scores and quality threshold) to confirm that the TOE doesn’t create
authentication templates that don’t meet the assessment criteria
specified in the “assessment criteria for templates”.

The above EA is derived from ATE\_IND.1-3, ATE\_IND.1-4, ATE\_IND.1-5,
ATE\_IND.1-6, and ATE\_IND.1-7.

#### Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS,
    AGD guidance and “assessment criteria for templates”

b)  the TOE creates only templates that pass the assessment criteria
    though the independent testing

#### Requirements for reporting

This EA does not require reports or report details other than those
given in the work unit from which it is derived.

### EA for FIA\_MBV\_EXT.1

#### Objective

The evaluator shall verify that the TOE implements the mobile biometric
verification mechanism whose error rates is equal or lower than the
claimed error rates (i.e. value of FAR/FMR and FRR/FNMR in
FIA\_MBV\_EXT.1.2).

The evaluator shall solely rely on the supplementary information
(developer’s performance test document) to achieve this objective
following instruction defined in Assessment strategy.

This cPP assumes that the mobile biometric verification is not used for
the security sensitive services and the TOE operational environment also
limits the maximum number of failed verification attempts in succession.
Therefore, risk of zero-effort impostor attempts is low and the
developer may not follow the statistical method (e.g. Rule of 3 or Rule
of 30) to measure the mobile biometric verification performance.

\[BScPP\] doesn’t support multimodal TOE which is measuring two or more
different biometric modalities (e.g. iris and face) to verify a user.

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FIA\_MBV\_EXT.1. There is no dependency to other
EAs defined in this SD.

#### Tool types required to perform the activity

No tool is required for this EA.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FIA\_MBV\_EXT.1 at high level
    description

b)  AGD guidance shall provide clear instruction for a user to verify
    his/herself to unlock the mobile device

c)  Supplementary information (developer’s performance test document)
    shall describe developer’s performance test protocol and result of
    testing

AGD guidance includes online assistance, prompt or warning provided by
the TOE during the verification attempt.

#### Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall refer the TSS to understand how the TOE verify a
user with his/her biometric characteristics. The evaluator shall also
examine the guidance, including online assistance or prompt provided by
the TOE, about how the TOE supports a user to verify his/herself
correctly and how the TOE behaves when mobile biometric verification is
succeeded or failed.

The evaluator shall examine “developer’s performance test document” to
verify that the developer conducts the objective and repeatable
performance testing. Minimum requirements for conducting performance
testing are defined in XXXX.

Requirements defined in XXXX is based on the ISO/IEC 19795. This
standard specifies requirements on performance test protocol, recording
and reporting of results based on the best practices developed by
relevant organizations. The evaluator shall confirm that “developer’s
performance test document” meets all requirements in XXXX and seek a
rationale if “developer’s performance test document” doesn’t meet any
requirements and determine whether the rationale is valid or not.

The above EA is derived from ASE\_TSS.1-1, ADV\_FSP.1-7, AGD\_OPE.1-4
and AGD\_OPE.1-5.

#### Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance

b)  “developer’s performance test document” meets all requirements in
    XXXX and valid rationale is provided by developer if “developer’s
    performance test document” doesn’t meet any requirements

c)  the error rates measured by developer is equal or lower than the
    claimed error rates in FIA\_MBV\_EXT.1.2

#### Requirements for reporting

The evaluator shall report a justification why evaluator determines the
rationale provided by developer is valid if “developer’s performance
test document” doesn’t meet any requirements in XXXX.

### EA for FIA\_MBV\_EXT.2

#### Objective

Mobile biometric verification performance depends on quality of samples
that is compared to templates. The evaluator shall examine that the TOE
checks the quality of samples based on the assessment criteria to verify
a user with an adequate reliability.

The evaluator shall keep in mind that the assessment criteria for
different biometric modalities may not be the same. The evaluator shall
iterate this EA for each biometric modality if the ST author selects
multiple biometric modalities in FIA\_MBV\_EXT.1.

The evaluator shall also keep in mind that assessment criteria used for
mobile biometric enrolment and verification may not be the same.
Assessment criteria for mobile biometric enrolment may be stricter than
one for mobile biometric verification.

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FIA\_MBV\_EXT.2. The evaluator shall perform the
EA for FIA\_MBV\_EXT.1 first to confirm the mobile biometric
verification can be done correctly.

#### Tool types required to perform the activity

Developer shall provide a test platform for the evaluator to conduct the
test described in the Assessment Strategy.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FIA\_MBV\_EXT.2 at high level
    description

b)  AGD guidance shall provide clear instruction for a user to verify
    his/herself

c)  Supplementary information (Assessment criteria for samples) shall
    describe assessment criteria for creating templates

AGD guidance includes online assistance, prompt or warning provided by
the TOE during the verification attempt.

#### Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall refer the TSS to understand how the TOE checks
quality of samples captured. The evaluator shall also examine the
guidance, including online assistance or prompt provided by the TOE,
about how the TOE supports a user to verify his/herself correctly and
how the TOE behaves when low quality samples are presented to the TOE.

The evaluator shall examine that “assessment criteria for samples” to
check that how the TOE checks the quality of samples based on its
assessment criteria. The “assessment criteria for samples” may include;

a)  quality requirements for the biometric sample to ensure that a
    sufficient amount of distinctive features is available

b)  method to quantify the quality of samples (e.g. method to generate
    quality score)

c)  assessment criteria to accept the sample of sufficient utility (e.g.
    compare quality score to quality threshold)

d)  quality standard that the TOE uses to perform the assessment if the
    TOE follows such standard (e.g. NFIQ for fingerprint)

The above EA is derived from ASE\_TSS.1-1, ADV\_FSP.1-7, AGD\_OPE.1-4
and AGD\_OPE.1-5.

\[Strategy for ATE \_IND\]

The evaluator shall perform the following test to verify that the TOE
checks the quality of samples based on the assessment criteria. If the
TOE supports multiple biometric modalities, the same test shall be done
for each modality.

The following test requires the developer to provide access to a test
platform that provides the evaluator with tools that are typically not
found on factory products.

Step 1: The evaluator shall present biometric samples of low quality for
mobile biometric verification that don’t satisfy the assessment criteria
described in “assessment criteria for samples”.

Step 2: The evaluator shall check the TOE internal data (e.g. quality
scores and quality threshold) to confirm that the TOE rejects any
samples that don’t meet the assessment criteria specified in the
“assessment criteria for samples”.

The above EA is derived from ATE\_IND.1-3, ATE\_IND.1-4, ATE\_IND.1-5,
ATE\_IND.1-6, and ATE\_IND.1-7.

#### Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS,
    AGD guidance and “assessment criteria for samples”

b)  the TOE accepts only samples that pass the assessment criteria
    though the independent testing

#### Requirements for reporting

This EA does not require reports or report details other than those
given in the work unit from which it is derived.

### EA for FIA\_MBV\_EXT.3

#### Objective

The evaluator shall verify that the TOE prevents use of artificial
Presentation Attack Instruments (PAI). This EA defines the minimum PAIs
that the evaluator shall create and test protocol that evaluator shall
follow to test the TOE. While this EA allows to develop an overall
statement about the performance of the TOE with respect to its PAD
mechanism, they cannot provide any assurance about the PAD functionality
with respect to variations of PAIs that are not covered by this EA. It
falls into the focus of the vulnerability assessment to evaluate whether
the use of additional PAIs can lead to increased error rates. During the
vulnerability analysis, the evaluators will use all their knowledge that
they gained during the evaluation for penetration testing. Another EA is
defined for this penetration testing (AVA\_VAN.1).

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FIA\_MBV\_EXT.3. The evaluator shall perform the
EA for FIA\_MBV\_EXT.1 and FIA\_MBV\_EXT.2 first to confirm the mobile
biometric verification can be done correctly.

#### Tool types required to perform the activity

All tools required to conduct the test are described in the Assessment
Strategy.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FIA\_MBV\_EXT.3 at very high
    level description. TSS may only states that the TOE implements PAD
    mechanism and may not disclose any information about the PAD
    mechanism itself.

b)  AGD guidance may provide information about how the TOE reacts when
    artificial PAI is detected.

#### Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall refer the TSS and AGD guidance to understand how the
TOE prevents the use of artificial PAI.

The above EA is derived from ASE\_TSS.1-1, ADV\_FSP.1-7, AGD\_OPE.1-4
and AGD\_OPE.1-5.

\[Strategy for ATE \_IND\]

See YYYY.

This EA is derived from ATE\_IND.1-3, ATE\_IND.1-4, ATE\_IND.1-5,
ATE\_IND.1-6, and ATE\_IND.1-7.

#### Pass/fail criteria

See YYYY

#### Requirements for reporting

See YYYY

FPT: Protection of the TSF
--------------------------

### EA for FPT\_BDP\_EXT.1

#### Objective

\[BScPP\] assumes that the mobile device provides the Secure Execution
Environment (SSE), an operating environment separate from the main
mobile device operating system. Access to the SEE is highly restricted
and may be made available through special processor modes, separate
security processors or a combination to provide this separation.

Evaluation of this SEE is out of scope of \[BScPP\] and the evaluator
doesn’t need to evaluate this environment itself. However, the evaluator
shall examine that the TOE processes any plaintext biometric data except
publicly accessible biometric data (e.g. face image) within the security
boundary of this SEE. The SEE is responsible for preventing any entity
outside the environment from accessing plaintext biometric data.

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FPT\_BDP\_EXT.1. There is no dependency to other
EAs defined in this SD.

#### Tool types required to perform the activity

No tool is required for this EA.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FPT\_BDP\_EXT.1 at high level
    description.

#### Assessment Strategy

\[Strategy for ASE\_TSS\]

As depicted in Figure 1 of \[BScPP\], biometric characteristics is
captured by biometric capture sensor and then sent to the processors in
mobile device for signal processing, PAD and comparison and return the
decision outcome. During these processing, any plaintext biometric data
must not be accessible from any entities outside the SEE.

The evaluator shall examine the TSS to confirm that;

a)  Only TSF modules can access plaintext biometric data captured by the
    biometric capture sensor

b)  Any TSF modules that access plaintext biometric data run within the
    SEE

c)  Plaintext biometric data is retained in volatile memory within the
    SEE

d)  Any TSFIs doesn’t reveal the plaintext biometric data to any
    entities outside the SEE

The evaluator shall keep in mind that the objective of this EA is not
evaluating the SEE itself. This EA is derived from ASE\_TSS.1.1 which
requires that the TSS to provide potential consumers of the TOE with a
high-level view of how the developer intends to satisfy each SFR. The
evaluator shall check the TSS to seek for a logical explanation why
above a) – d) is satisfied considering this scope of requirement.

\[BScPP\] assumes that integrity of TSF itself is protected by the
mobile device as required by \[MDFPP\].

TOE can store templates which is part of plaintext biometric data in
non-volatile memory. Protection of these stored template is out of scope
of this EA but covered by EAs for FPT\_BDP\_EXT.3 and FPT\_PBT\_EXT.1.

The above EA is derived from ASE\_TSS.1-1.

#### Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS

#### Requirements for reporting

This EA does not require reports or report details other than those
given in the work unit from which it is derived.

### EA for FPT\_BDP\_EXT.2

#### Objective

Mobile device may provide diagnostic function which transmit diagnostic
data to developer with permission from mobile owner. Mobile device may
also backup data to protect data. However, \[BScPP\] prohibits the TOE
from revealing any plaintext biometric data for such purpose.

The evaluator shall examine that the TOE in the evaluated configuration
doesn’t transmit any plaintext biometric data outside the security
boundary of the SEE.

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FPT\_BDP\_EXT.2. There is no dependency to other
EAs defined in this SD.

#### Tool types required to perform the activity

No tool is required for this EA.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FPT\_BDP\_EXT.2 at high level
    description.

b)  AGD guidance shall describe all functions that transmit data for any
    purpose.

#### Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS and AGD guidance to make sure that
no functions transmit plaintext biometric data for any purpose to any
entities outside the SEE.

The above EA is derived from ASE\_TSS.1-1, ADV\_FSP.1-7, AGD\_OPE.1-4
and AGD\_OPE.1-5.

#### Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance.

#### Requirements for reporting

This EA does not require reports or report details other than those
given in the work unit from which it is derived.

### EA for FPT\_BDP\_EXT.3

#### Objective

The TOE shall process plaintext biometric data within the boundary of
SEE as required by FPT\_BDP\_EXT.1. However, TOE needs to store the
templates in the mobile device for mobile biometric verification and
protection of those stored templates is not covered by the
FPT\_BDP\_EXT.1

The evaluator shall examine that any plaintext biometric data, including
templates, are not stored outside the SEE. This means that any plaintext
biometric data must not be stored in any non-volatile memory that an
entity outside the SEE can get access to.

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FPT\_BDP\_EXT.3. There is no dependency to other
EAs defined in this SD.

#### Tool types required to perform the activity

No tool is required for this EA.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FPT\_BDP\_EXT.3 at high level
    description.

b)  AGD guidance may describe how the templates are stored securely.

#### Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS and AGD guidance to make sure that
no plaintext biometric data outside the SEE.

The above EA is derived from ASE\_TSS.1-1, ADV\_FSP.1-7, AGD\_OPE.1-4
and AGD\_OPE.1-5.

#### Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance.

#### Requirements for reporting

This EA does not require reports or report details other than those
given in the work unit from which it is derived.

### EA for FPT\_PBT\_EXT.1

#### Objective

The TOE shall not store plaintext biometric data including templates
outside the SEE as required by FPT\_BDP\_EXT.3. However, the templates
may need to be stored in non-volatile memory that entities outside the
SEE can get access to. Those stored templates need to be protected
securely from those entities.

The evaluator shall examine that the TOE encrypts templates within the
SEE before storing it any non-volatile memory outside the SEE, and
controls access to those templates using PIN, password or any other
method specified by the ST author.

\[MDFPP\] requires mobile device to implement data-at-rest protection
that encrypt any sensitive or protected data. FPT\_PBT\_EXT.1 requires
the TOE to encrypt all templates even if the data-at-rest protection
already encrypt templates.

#### Relationship of the evaluation activity to SFRs, SARs, and other EAs

This EA is related to FPT\_PBT\_EXT.1. There is no dependency to other
EAs defined in this SD.

#### Tool types required to perform the activity

No tool is required for this EA.

#### Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FPT\_BDP\_EXT.1 at high level
    description.

b)  AGD guidance may describe how the templates are stored securely.

#### Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS and AGD guidance to check that the
TOE encrypts all templates using encryption algorithm evaluated by
\[MDFPP\] evaluation. The evaluator shall also ensure that either a PIN,
password or other secure means, as specified by the ST author , required
when templates are revoked or added.

The above EA is derived from ASE\_TSS.1-1, ADV\_FSP.1-7, AGD\_OPE.1-4
and AGD\_OPE.1-5.

#### Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance.

#### Requirements for reporting

This EA does not require reports or report details other than those
given in the work unit from which it is derived.
