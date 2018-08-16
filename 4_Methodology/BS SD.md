# Supporting Document Mandatory Technical Document

# Evaluation Activities for collaborative Protection Profile for Mobile biometric enrolment and verification - for unlocking the device - cPP
## Version 0.2 17-AUG-2018

**Foreword**

This is a supporting document, intended to complement the Common
Criteria (CC) version 3 and the associated Common Evaluation Methodology for
Information Technology Security Evaluation.

Supporting documents may be “Guidance Documents”, that highlight
specific approaches and application of the standard to areas where no
mutual recognition of its application is required, and as such, are not
of normative nature, or “Mandatory Technical Documents”, whose
application is mandatory for evaluations whose scope is covered by that
of the supporting document. The usage of the latter class is not only
mandatory, but certificates issued as a result of their application are
recognized under the CCRA.

This supporting document has been developed by the Biometric Security
iTC (BS-iTC) and is designed to be used to support the evaluations of
TOEs against the cPPs identified in section 1.1.

**Technical Editor:** Biometric Security international Technical
Community (BS-iTC)

**Document history:**

*V0.1, March 2018 (Initial Release for Public review)*  
*V0.2, August 2018 (Second Release for Public review)*

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



1 Introduction
============

1.1 Technology Area and Scope of Supporting Document
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
testing – see Appendix A).

1.2 Structure of the Document
-------------------------

Evaluation Activities can be defined for both Security Functional
Requirements and Security Assurance Requirements. These are defined in
separate sections of this Supporting Document.

1.3 Application of this Supporting Document
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

1.4 Terminology
-----------

### 1.4.1 Glossary

For definitions of standard CC terminology, see CC part 1.

For definitions of biometrics and mobile device, see \[BScPP\] and \[MDFPP\].                            

### 1.4.2 Acronyms

| Acronym	| Meaning |
|-------|----------------------------|
|**BAF** |Biometric Authentication Factor |
|**CC** |Common Criteria for Information Technology Security Evaluation |
|**CEM** |Common Methodology for Information Technology Security Evaluation |
|**cPP** |collaborative Protection Profile |
|**EA** |Evaluation Activity |
|**iTC** |International Technical Community | 
|**PAI** |Presentation Attack Instrument |
|**PP** |Protection Profile |
|**SAR** |Security Assurance Requirement | 
|**SD** |Supporting Document | 
|**SFR** |Security Functional Requirement | 
|**ST** |Security Target | 
|**TOE** |Target Of Evaluation | 
|**TSS** |TOE Summary Specification | 

2 Evaluation Activities for SFRs
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

1\) Objective of the EA

Objective defines the goal of the EA. Assessment Strategy describes how
the evaluator can achieve this goal in more detail and Pass/fail
criteria defines how the evaluator can determine whether the goal is
achieved or not.

2\) Relationship of the EA to SFRs, SARs, and other EAs

SFRs or SARs that the EA is directly related are identified here.

Where the EA depends on completion of another EA then the dependency and
the other EA is identified here.

3\) Tool types required to perform the EA

If performing the EA requires any tool types in order to complete the EA
then these tool types are defined here.

4\) Required input from the developer or other entities

Additional detail is specified here regarding the required format and
content of the inputs to the EA.

5\) Assessment Strategy

Assessment Strategy provides guidance and details how to perform the EA.
It includes, as appropriate to the content of the EA;

a)  how to assess the input from the developer or other entities for
    completeness with respect to the EA

b)  how to make use of any tool types required (potentially including
    guidance for the calibration or setup of the tools)

c)  guidance on the steps for performing the EA

6\) Pass/fail criteria

The evaluator uses these criteria to determine whether the EA has
demonstrated that the TOE has met the relevant requirement or that it
has failed to meet the relevant requirement.

7\) Requirements for reporting　　

Specific reporting requirements that support transparency and
reproducibility of the pass/fail judgement are defined here.

ISO/IEC 15408-4 also requires the SD to provide the rationale for the EA, 
which is a justification for the derivation of EAs from one or more 
work units. This rationale isn't provided for each EA but summarized  
separately in section 5.

2.1 FIA: Identification and Authentication
--------------------------------------

### 2.1.1 EA for FIA\_MBE\_EXT.1

#### 1\) Objective of the EA

The evaluator shall verify that the TOE enrols a user only after
successful authentication of the user by his/her password. Security
requirements for the password authentication are defined in \[MDFPP\]
and out of scope of this EA.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FIA\_MBE\_EXT.1 and defines activities the evaluator
shall perform to examine whether the TOE meets FIA\_MBE\_EXT.1 or not. 

There is no dependency to other EAs defined in this SD.

#### 3\) Tool types required to perform the EA

No tool is required for this EA.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meet FIA\_MBE\_EXT.1 at high level
    description

b)  AGD guidance shall provide clear instructions for a user to enrol
    his/herself.

AGD guidance may include online assistance, prompts or warning provided by
the TOE during the enrolment attempt.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS to understand how the TOE enrols a
user and examine the AGD guidance to confirm that a user is required to
enter his/her valid password before the mobile biometric enrolment.

\[Strategy for ATE\_IND\]

The evaluator shall perform the following test to verify that the TOE
performs the mobile biometric enrolment correctly.

Step 1: The evaluator shall try to enrol he/herself without setting a
password and confirm that he/she can’t enrol his/herself.

Step 2: The evaluator shall set a password and confirm that he/she can’t
enrol his/herself without entering the password correctly beforehand.

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance

b)  only authenticated users by password can enrol his/herself and any
    attempts to enrol without the authentication are rejected through the 
    independent testing

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

### 2.1.2 EA for FIA\_MBE\_EXT.2

#### 1\) Objective of the EA

Mobile biometric verification performance depends on quality of the
template that is compared to the samples presented to the TOE. The
evaluator shall examine that the TOE checks the quality of enrolment and
authentication templates based on the assessment criteria to verify a
user with an adequate reliability.

If the TOE doesn’t create authentication templates, this EA is only
applicable to enrolment templates.

The evaluator shall keep in mind that the assessment criteria for
different biometric modalities may not be the same. The evaluator shall
evaluate each biometric modality separately if the ST author selects
multiple biometric modalities in FIA\_MBV\_EXT.1.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FIA\_MBE\_EXT.2 and defines activities the evaluator
shall perform to examine whether the TOE meets FIA\_MBE\_EXT.2 or not. 

The evaluator shall perform the EA for FIA\_MBE\_EXT.1 first to confirm 
the mobile biometric enrolment can be done correctly.

#### 3\) Tool types required to perform the EA

Developer shall provide a test platform for the evaluator to conduct the
test described in the Assessment Strategy.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FIA\_MBE\_EXT.2 at high level
    description

b)  AGD guidance shall provide clear instructions for a user to enrol
    his/herself

c)  Supplementary information (Assessment criteria for templates) shall
    describe assessment criteria for creating templates

AGD guidance may include online assistance, prompts or warning provided by
the TOE during the enrolment attempt.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

**Enrolment templates**

The evaluator shall examine the TSS to understand how the TOE generate
sufficient quality of templates at enrolment. The evaluator shall also
examine the guidance about how the TOE supports a user to enrol his/herself
correctly and how the TOE behaves when low quality samples are presented
to the TOE.

The evaluator shall examine that “assessment criteria for templates” to
check that how the TOE creates the templates based on this assessment
criteria. The “assessment criteria for templates” may include;

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

If the TOE creates authentication templates, the evaluator shall examine
the TSS to understand how the TOE generate sufficient quality of
authentication templates.

The evaluator shall examine that the “assessment criteria for templates”
to check that how the TOE creates the authenticate templates based on
its assessment criteria. The “assessment criteria for templates” may
include a) – d) and;

f)  additional assessment criteria to applied to creation of
    authentication templates

\[Strategy for ATE\_IND\]

**Enrolment templates**

The evaluator shall perform the following test to verify that the TOE
generates templates of sufficient quality.

The following test requires the developer to provide access to a test
platform that provides the evaluator with tools that are typically not
found on factory products.

Step 1: The evaluator shall perform mobile biometric enrolment that
results in creation of templates that don’t satisfy the assessment
criteria described in “assessment criteria for templates” (e.g.
presenting biometric samples of low quality).

Step 2: The evaluator shall check the TOE internal data (e.g. quality
scores and quality threshold) to confirm that the TOE doesn’t create
enrolment templates that don’t meet the assessment criteria specified in
the “assessment criteria for templates”.

**Authentication templates**

The evaluator shall perform the following test to verify that the TOE
generates authentication templates of sufficient quality only if the
evaluator judges that creating authentication templates is feasible.

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

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS,
    AGD guidance and “assessment criteria for templates”

b)  the TOE creates only templates that pass the assessment criteria
    through the independent testing

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

### 2.1.3 EA for FIA\_MBV\_EXT.1

#### 1\) Objective of the EA

The evaluator shall verify that the TOE implements the mobile biometric
verification mechanism whose error rates is equal or lower than the
claimed error rates (i.e. value of FAR/FMR and FRR/FNMR specified in
FIA\_MBV\_EXT.1.2).

The evaluator shall solely rely on the supplementary information
(developer’s performance test document) to achieve this objective
following instruction defined in Assessment Strategy.

This cPP assumes that the mobile biometric verification is not used for
the security sensitive services and the TOE operational environment also
limits the maximum number of failed verification attempts in succession.
Therefore, risk of zero-effort impostor attempts is low and the
developer may not follow the statistical method (e.g. Rule of 3 or Rule
of 30) to measure the mobile biometric verification performance.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FIA\_MBV\_EXT.1 and defines activities the evaluator
shall perform to examine whether the TOE meets FIA\_MBV\_EXT.1 or not. 

The evaluator shall perform the EAs for FIA\_MBE\_EXT.1 and FIA\_MBE\_EXT.2 
first to confirm the mobile biometric enrolment can be done correctly.

#### 3\) Tool types required to perform the EA

No tool is required for this EA.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FIA\_MBV\_EXT.1 at high level
    description

b)  AGD guidance shall provide clear instruction for a user to verify
    his/herself to unlock the mobile device

c)  Supplementary information (developer’s performance test document)
    shall describe developer’s performance test protocol and result of
    testing

AGD guidance may include online assistance, prompts or warning provided by
the TOE during the verification attempt.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS to understand how the TOE verify a
user with his/her biometric characteristics. The evaluator shall also
examine the guidance about how the TOE supports a user to verify his/herself
correctly and how the TOE behaves when mobile biometric verification is
succeeded or failed.

The evaluator shall examine “developer’s performance test document” to
verify that the developer conducts the objective and repeatable
performance testing. Minimum requirements for conducting performance
testing are defined in Appendix A.

Requirements defined in Appendix A is based on the ISO/IEC 19795. This
standard specifies requirements on performance test protocol, recording
and reporting of results based on the best practices developed by
relevant organizations. The evaluator shall confirm that “developer’s
performance test document” meets all requirements in Appendix A and seek
a rationale if “developer’s performance test document” doesn’t meet any
requirements and determine whether the rationale is valid or not.

Finally, the evaluator shall check that the measured error rates
(FRR/FAR or FNMR/FMR) reported in ”developer’s performance test
document” is equal or lower than the error rates specified in the
FIA\_MBV\_EXT.1.2.

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance

b)  “developer’s performance test document” meets all requirements in
    Appendix A and valid rationale is provided by developer if
    “developer’s performance test document” doesn’t meet any
    requirements

c)  FRR/FAR or FNMR/FMR measured by the developer’s performance testing
    is equal or lower than “*defined value*“ specified in
    FIA\_MBV\_EXT.1.2

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

The evaluator shall also report a justification why evaluator determines
the rationale provided by developer is valid if “developer’s performance
test document” doesn’t meet any requirements in Appendix A.

### 2.1.4 EA for FIA\_MBV\_EXT.2

#### 1\) Objective of the EA

Mobile biometric verification performance depends on quality of samples
that is compared to templates. The evaluator shall examine that the TOE
checks the quality of samples based on the assessment criteria to verify
a user with an adequate reliability.

The evaluator shall keep in mind that the assessment criteria for
different biometric modalities may not be the same. The evaluator shall
evaluate each biometric modality separately if the ST author selects
multiple biometric modalities in FIA\_MBV\_EXT.1.

The evaluator shall also keep in mind that assessment criteria used for
templates and samples may not be the same. Assessment criteria for
templates may be stricter than the one for samples.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FIA\_MBV\_EXT.2 and defines activities the evaluator
shall perform to examine whether the TOE meets FIA\_MBV\_EXT.2 or not. 

The evaluator shall perform the EAs for FIA\_MBE\_EXT.1, FIA\_MBE\_EXT.2 
and FIA\_MBV\_EXT.1 first to confirm the mobile biometric enrolment and 
verification can be done correctly.

#### 3\) Tool types required to perform the EA

Developer shall provide a test platform for the evaluator to conduct the
test described in the Assessment Strategy.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FIA\_MBV\_EXT.2 at high level
    description

b)  AGD guidance shall provide clear instruction for a user to verify
    his/herself

c)  Supplementary information (Assessment criteria for samples) shall
    describe assessment criteria for creating samples

AGD guidance may include online assistance, prompts or warning provided by
the TOE during the verification attempt.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS to understand how the TOE checks
quality of samples captured. The evaluator shall also examine the
guidance, including online assistance or prompts provided by the TOE,
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

\[Strategy for ATE\_IND\]

The evaluator shall perform the following test to verify that the TOE
checks the quality of samples based on the assessment criteria.

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

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS,
    AGD guidance and “assessment criteria for samples”

b)  the TOE accepts only samples that pass the assessment criteria
    through the independent testing

#### 7\) Requirements for reporting　

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

### 2.1.5 EA for FIA\_MBV\_EXT.3

#### 1\) Objective of the EA

The evaluator shall verify that the TOE prevents use of artificial
Presentation Attack Instruments (PAI). This EA defines the minimum PAIs
that the evaluator shall create and test protocol that evaluator shall
follow to test the TOE. Appendix C specifies such PAIs and test protocols.

While this EA allows to develop an overall statement about the performance 
of the TOE with respect to its PAD mechanism, they cannot provide any 
assurance about the PAD functionality with respect to variations of PAIs 
that are not covered by this EA. It falls into the focus of the 
vulnerability assessment to evaluate whether the use of additional PAIs 
can lead to increased error rates. During the vulnerability analysis, 
the evaluators will use all their knowledge that they gained during the 
evaluation for penetration testing. Another EA is defined for this 
penetration testing (AVA\_VAN.1).

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FIA\_MBV\_EXT.3 and defines activities the evaluator
shall perform to examine whether the TOE meets FIA\_MBV\_EXT.3 or not. 

The evaluator shall perform the EAs for FIA\_MBE\_EXT.1, FIA\_MBE\_EXT.2, 
FIA\_MBV\_EXT.1 and FIA\_MBV\_EXT.2 first to confirm the mobile biometric 
enrolment and verification can be done correctly.

#### 3\) Tool types required to perform the EA

See Appendix C.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FIA\_MBV\_EXT.3 at high level
    description. TSS may only states that the TOE implements PAD
    mechanism and may not disclose any information about the PAD
    mechanism itself in detail because such information is highly 
    sensitive and may be exploited by attackers.

b)  AGD guidance may provide information about how the TOE reacts when
    artificial PAI is detected.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS and AGD guidance to check that
the TSS and AGD guidnace states that the TOE prevents the use of 
artificial PAI.

\[Strategy for ATE\_IND\]

See Appendix C.

#### 6\) Pass/fail criteria

See Appendix C.

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

2.2 FPT: Protection of the TSF
--------------------------

### 2.2.1 EA for FPT\_BDP\_EXT.1

#### 1\) Objective of the EA

\[BScPP\] assumes that the mobile device provides the Secure Execution
Environment (SEE), an operating environment separate from the main
mobile device operating system. Access to the SEE is highly restricted
and may be made available through special processor modes, separate
security processors or a combination to provide this separation.

Evaluation of this SEE is out of scope of \[BScPP\] and the evaluator
doesn’t need to evaluate this environment itself. However, the evaluator
shall examine that the TOE processes any plaintext biometric data within 
the security boundary of the SEE. The SEE is responsible for preventing 
any entities outside the environment from accessing plaintext biometric 
data.

FPT\_BDP\_EXT.1 applies to plaintext biometric data being processed 
during mobile biometric enrolment and verification. Protection of 
transmitted and stored biometric data is out of scope of this EA 
and covered by FPT\_BDP\_EXT.2 and FPT\_BDP\_EXT.3 respectively.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FPT\_BDP\_EXT.1 and defines activities the evaluator
shall perform to examine whether the TOE meets FPT\_BDP\_EXT.1 or not. 

There is no dependency to other EAs defined in this SD.

#### 3\) Tool types required to perform the EA

No tool is required for this EA.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FPT\_BDP\_EXT.1 at high level
    description.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS\]

As depicted in Figure 1 of \[BScPP\], biometric characteristics is
captured by biometric capture sensor and then sent to the processors in
mobile device for signal processing, PAD and comparison and return the
decision outcome. This is a typical process flow of mobile biometric
verification, however, biometric capture sensor may do the all tasks
within the sensor. In either case, all TSF modules (i.e. biometric
capture sensor and any software running in biometric capture sensor and
mobile device processors) that process plaintext biometric data must be 
separated from any entities outside the SEE. Any plaintext biometric data
must not be accessible from any entities outside the SEE.

In any cases, the evaluator shall examine the TSS to confirm that;

a)  All TSF modules run within the SEE and any entities outside the SEE
    including mobile device operating system can’t interfere with
    processing of these modules

-   if biometric capture sensor returns plaintext biometric data, any
    entities outside the SEE can’t access the sensor and data captured
    by the sensor.

b)  All plaintext biometric data is retained in volatile memory within
    the SEE and any entities outside the SEE including mobile device
    operating system can’t access these data.

c)  Any TSFIs doesn’t reveal plaintext biometric data to any entities
    outside the SEE

The evaluator shall keep in mind that the objective of this EA is not
evaluating the SEE itself. This EA is derived from ASE\_TSS.1.1 which
requires that the TSS to provide potential consumers of the TOE with a
high-level view of how the developer intends to satisfy each SFR. The
evaluator shall check the TSS to seek for a logical explanation why
above a) – c) is satisfied considering this scope of the requirement.

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

### 2.2.2 EA for FPT\_BDP\_EXT.2

#### 1\) Objective of the EA

The intention of this requirement is to prevent the logging, backing up
or sending of plaintext biometric data to a service that transmits the
information outside the security boundary of the SEE.

For example, the TOE may transmit plaintext biometric data to the
developer’s server for diagnostic purpose with a consent of the user.
However, the TOE must not send plaintext biometric data as it is to the
developer. The TOE must encrypt the data first before sending it.

In any case, the evaluator shall determine that the TOE doesn’t transmit
any plaintext biometric data outside the security boundary of the SEE.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FPT\_BDP\_EXT.2 and defines activities the evaluator
shall perform to examine whether the TOE meets FPT\_BDP\_EXT.2 or not. 

The evaluator shall perform the EAs for FPT\_BDP\_EXT.1 first to confirm 
the TSF processes any plaintext biometric data within the security boundary 
of the secure execution environment.

#### 3\) Tool types required to perform the EA

No tool is required for this EA.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FPT\_BDP\_EXT.2 at high level
    description.

b)  AGD guidance shall describe all functions that transmit biometric
    data.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS and AGD guidance to identify any
functions that transmit biometric data to any entities outside the SEE
and type of biometric data that is transmitted.

If the TOE transmits biometric data, the evaluator shall examine that
the activities that happen on the data transmission to confirm that;

a)  The TOE requires an explicit user consent and user authentication to
    enable the transmission.

b)  The TOE never transmits plaintext biometric data to outside the SEE.
    This means;

   1.  The TOE encrypts plaintext biometric data to be transmitted
       using the cryptographic functions evaluated based on \[MDFPP\]
       within the SEE.

   2.  If the TOE stores the encrypted biometric data outside the SEE
       for transmission, the TOE deletes such data after the
       transmission

   3.  If the TOE displays the plaintext biometric data to the user to
       seek approval for transmission, such process is performed within
       the SEE

c)  The TOE disables the transmission right after the TOE achieves its
    purpose

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance.

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

### 2.2.3 EA for FPT\_BDP\_EXT.3

#### 1\) Objective of the EA

Plaintext biometric data, especially templates, are highly sensitive
personal data because biometric characteristics may be recovered from
them. Plain text biometric data shall be processed within the SEE as
required by FPT\_BDP\_EXT.1. However, part of plaintext biometric data
including templates may need to be stored in mobile device for mobile
biometric verification. However, protection of such stored biometric
data is not covered by FPT\_BDP\_EXT.1.

The evaluator shall confirm that the TOE encrypts plaintext biometric
data within the SEE before storing it in any non-volatile memory that 
entities outside the SEE can get access to. If the evaluator confirms 
that the TOE doesn’t store plaintext biometric data outside the SEE 
(e.g. biometric capture sensor processes biometric data within the 
sensor and return only decision outcome to the TSF modules running 
inside the SEE) during performing the evaluation activity of 
FPT\_BDP\_EXT.1, this requirement deems satisfied.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FPT\_BDP\_EXT.3 and defines activities the evaluator
shall perform to examine whether the TOE meets FPT\_BDP\_EXT.3 or not. 

The evaluator shall perform the EAs for FPT\_BDP\_EXT.1 first to confirm 
the TSF processes any plaintext biometric data within the security boundary 
of the secure execution environment.

#### 3\) Tool types required to perform the EA

Developer shall provide a test platform for the evaluator to conduct the
test described in the Assessment Strategy.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FPT\_BDP\_EXT.3 at high level
    description.

b)  Supplementary information (file list/format and cryptographic
    algorithm) shall list locations and format of files that contain
    biometric data, and cryptographic algorithm used to encrypt those
    files.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS\]

The evaluator shall examine the TSS to understand the activities that
happen on mobile biometric enrolment and verification relating to
encrypting and storing biometric data. The evaluator shall confirm that;

a)  The TSS lists type of biometric data that the TOE stores in
    non-volatile memory outside the SEE

b)  The TOE encrypts all plaintext biometric data listed in the TSS
    within the SEE before storing it in the non-volatile memory

c)  The TOE uses cryptographic functions evaluated based on \[MDFPP\] to
    encrypt the data

\[Strategy for ATE\_IND\]

The evaluator shall perform the following test to verify that the TOE
encrypts plaintext biometric data if the TOE stores the data in
non-volatile memory outside the SEE.

The following test requires the developer to provide access to a test
platform that provides the evaluator with tools that are typically not
found on factory products.

Step 1: The evaluator shall check that all cryptographic algorithms
listed in “file list/format and cryptographic algorithm” are
successfully evaluated based on \[MDFPP\]

Step 2: The evaluator shall load an app onto the mobile device. This app
shall attempt to traverse over all file systems and report any newly
created files.

Step 3: The evaluator shall perform mobile biometric enrolment and
verification and run the app to list new files.

Step 4: The evaluator shall compare files reported by the app and ones
listed in “file list/format and cryptographic algorithm”.

Step 5: If evaluator finds newly created files not listed in “file
list/format and cryptographic algorithm”, the evaluator shall confirm
that those files don’t include plaintext biometric data with the support
from developer.

Step 6: For all files listed in “file list/format and cryptographic
algorithm”, the evaluator shall display the contents of files and check
that the files are encrypted. The evaluator can assume that encryption
is done correctly because the TOE uses cryptographic algorithms
evaluated based on \[MDFPP\]. The evaluator shall compare the content of
files to the format defined in “file list/format and cryptographic
algorithm” to check that the files don’t follow the defined format to
implicitly assume files are encrypted.

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS.

b)  the TOE encrypts any plaintext biometric data before storing it
    outside the SEE through the independent testing

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

### 2.2.4 EA for FPT\_PBT\_EXT.1

#### 1\) Objective of the EA

Only authenticated user can add his/her own templates during mobile
biometric enrolment as defined in the FIA\_MBE\_EXT.1 and those
templates are not stored outside the SEE without encryption as required
by the FPT\_BDP\_EXT.3. However, the TOE may provide functions (e.g.
revocation of templates) to access the templates. The evaluator shall
confirm that only authenticated user either using a PIN, password or by
other secure means, as specified by the ST author can access the
templates through the TSFI provided by the TOE.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FPT\_PBT\_EXT.1 and defines activities the evaluator
shall perform to examine whether the TOE meets FPT\_PBT\_EXT.1 or not. 

The evaluator shall perform the EA for FIA\_MBE\_EXT.1 first to confirm 
the mobile biometric enrolment can be done correctly.

#### 3\) Tool types required to perform the EA

No tool is required for this EA.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FPT\_BDP\_EXT.1 at high level
    description.

b)  AGD guidance shall describe how the user can access the templates.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS and AGD guidance to identify any
TSFI through which the user can access (e.g. revoke) the templates. The
evaluator shall confirm that those TSFI requires either using a PIN,
password or by other secure means, as specified by the ST author.

\[Strategy for ATE\_IND\]

The evaluator shall perform the following test to verify that the TOE
protects the templates as specified in TSS and AGD guidance.

Step 1: The evaluator shall perform functions through the TSFIs that
access the templates.

Step 2: The evaluator shall check that the TSFI requires either using a
PIN, password or by other secure means, as specified by the ST author.

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance.

b)  the TOE protects the templates either using a PIN, password or by
    other secure means, as specified by the ST author.

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

3 Evaluation Activities for Selection-Based Requirements
==============================

3.1 FIA: Identification and Authentication
--------------------------------------

### 3.1.1 EA for FIA_HYB_EXT.1

#### 1\) Objective of the EA

A hybrid authentication mechanism is one where a user has to submit a 
combination of biometric sample and PIN or password with both to pass 
and without the user being made aware of which factor failed, if either 
fails. The evaluator shall verify that the TOE use only selected 
modality for this hybrid authentication.

#### 2\) Relationship of the EA to SFRs, SARs, and other EAs

This EA is created from FIA_HYB_EXT.1 and defines activities the evaluator
shall perform to examine whether the TOE meets FIA_HYB_EXT.1 or not. 

The evaluator shall perform the EA for FIA\_MBE\_EXT.1 first to confirm 
the mobile biometric enrolment can be done correctly.

#### 3\) Tool types required to perform the EA

No tool is required for this EA.

#### 4\) Required input from the developer or other entities

Following input is required from the developer.

a)  TSS shall explain how the TOE meets FIA\_MBE\_EXT.1 at high level
    description.

b)  AGD guidance shall describe how the hybrid authentication can
    be done.

#### 5\) Assessment Strategy

\[Strategy for ASE\_TSS, AGD\_OPE and ADV\_FSP\]

The evaluator shall examine the TSS to understand how the TOE verify a
user with his/her biometric characteristics and PIN or password. 
The evaluator shall also examine the guidance about how the TOE 
supports a user to verify his/herself correctly and how the TOE 
behaves when hybrid authentication is succeeded or failed.

\[Strategy for ATE\_IND\]

The evaluator shall perform the following test to verify that the TOE
protects the templates as specified in TSS and AGD guidance.

Step 1: The evaluator shall configure and perform hybrid authentication.

Step 2: The evaluator shall check that the TOE can conduct hybrid 
        authentication as specified, especially, when either factor is 
        failed, the TOE doesn't reveal any information about which
        factor is failed.

#### 6\) Pass/fail criteria

The evaluators can pass this evaluation activity only if the evaluator
confirms that:

a)  information necessary to perform this EA is described in the TSS and
    AGD guidance.

b)  the TOE can conduct hybrid authentication using modality as specified 
    by the ST author.

#### 7\) Requirements for reporting

The evaluator shall report the summary of result of EA defined above,
especially how the evaluator reaches the pass/fail judgement based on
the Pass/Fail criteria.

4 Evaluation Activities for Optional Requirements
==============================

4.1 FIA: Identification and Authentication
--------------------------------------

### 4.1.1 EA for FIA_MBE_EXT.3

The evaluator shall refer the EA for FIA_MBV_EXT.3 to perform evaluation
of this SFR.

4.2 FDP: User data protection
--------------------------------------

### 4.2.1 EA for FDP_RIP.2

The evaluator shall refer the EA for FCS_CKM_EXT.4 in \[MDFPP\] to perform
evaluation of this SFR.

5 Evaluation Activities for SARs
==============================

The sections below specify EAs for the Security Assurance Requirements
(SARs) included in the \[BScPP\]. The EAs in Section 2 (Evaluation 
Activities for SFRs), Section 3 (Evaluation Activities for Selection-Based 
Requirements), and Section 4 (Evaluation Activities for Optional Requirements) 
are an interpretation of the more general CEM assurance requirements as they 
apply to the specific technology area of the TOE.

In this section, each SAR that is contained in the cPP is listed, and the EAs
that are not associated with an SFR or application notes to perform the CEM work 
units are defined here.

5.1 ASE: Security Target Evaluation
--------------------------

When evaluating ASE, the evaluator shall perform the work units as
presented in the CEM, except ASE_TSS.1-1. During ASE_TSS.1-1 evaluation, 
the evaluator shall ensure the content of the TSS in the ST satisfies the EAs 
specified in Section 2 (Evaluation Activities for SFRs), if applicable, Section 3 
(Evaluation Activities for Selection-Based Requirements) and Section 4 
(Evaluation Activities for Optional Requirements).

5.2 ADV: Development
--------------------------

The design information about the TOE may be contained in the AGD guidance 
available to the end user as well as the TSS portion of the ST, and any required 
supplementary information required by \[BScPP\] that is not to be made public. 
\[SD\] defines required supplementary information that is necessary for EAs
specified in Section 2.

### 5.2.1 Basic Functional Specification (ADV_FSP.1)

The functional specification describes the TOE Security Functions Interfaces (TSFIs).
It is not necessary to have a formal or complete specification of these interfaces. 
Additionally, because TOEs conforming to \[BScPP\] will necessarily have interfaces 
to the mobile device that are not directly invokable by TOE users, there is little 
point specifying that such interfaces be described in and of themselves since only 
indirect testing of such interfaces may be possible. 

For \[BScPP\], the EAs for this family focus on understanding the interfaces presented 
in the TSS in response to the functional requirements and the interfaces presented in 
the AGD guidance. No additional “functional specification” documentation is necessary 
to satisfy the EAs specified in this \[SD\].

When evaluating ADV_FSP.1, the evaluator performs the work units 
as presented in the CEM, taking the following application notes into account.

#### Application note for ADV_FSP.1-1, ADV_FSP.1-2 and ADV_FSP.1-3

*SFR-supporting and SFR-enforcing TSFI* can be interpreted as "any 
TSFIs through which the user can enrol and verify his/herself, and 
access any biometric data including templates".

The evaluator shall examine the purpose, method of use and parameters 
(if any) of these TSFIs as required by ADV_FSP.1-1, ADV_FSP.1-2 and ADV_FSP.1-3.

#### Application note for ADV_FSP.1-4

If AGD guidance doesn't describe all available interfaces, for example, 
any secret codes or hidden menu used for diagnostic purposes 
or testing, the developer shall provide *rationale for the implicit 
categorisation of interfaces as SFR-non-interfering* that explain;

a)  type of interfaces that are not described in AGD guidance

b)  rationale why those interfaces are not directly or indirectly
    related to the enforcement of SFRs
    
As described in CEM, individual interfaces should not need to be 
addressed in the rationale. The developer can provide a brief
rationale and the evaluator may ask more information about such 
interfaces for penetration testing if necessary.

#### Application note for ADV_FSP.1-5

The EAs in Section 2, if applicable, Section 3 and 4 of this \[SD\] are associated with 
the applicable SFRs; since these are directly associated with the SFRs, *the tracing from 
the functional specification to the SFRs* is implicitly already done and no additional 
documentation is necessary. Therefore, the intent of this work unit is covered by those EAs.

#### Application note for ADV_FSP.1-6

EAs that are associated with the SFRs in Section 2, and, if applicable, 
Sections 3 and 4, are performed to ensure that all the SFRs where the 
security functionality is externally visible (i.e. at the TSFI) are
covered. Therefore, the intent of this work unit is covered by those EAs.

#### Application note for ADV_FSP.1-7

EAs that are associated with the SFRs in Section 2, and, if applicable, 
Sections 3 and 4, are performed to ensure that all the SFRs where the 
security functionality is externally visible (i.e. at the TSFI) are
addressed, and that the description of the interfaces is accurate with 
respect to the specification captured in the SFRs. Therefore, the intent 
of this work unit is covered by those EAs.

5.3 AGD: Guidance Documents
--------------------------

\[BScPP\] assumes that the TOE is embedded into the mobile device and it is 
configured and managed as described in AGD guidance that satisfy 
requirements defined in the \[MDFPP\].

In addition to AGD guidance required by the \[MDFPP\], guidance pertaining 
to mobile biometric enrolment and verification shall also be provided. 
Requirements on such guidance are contained in the EAs specified in Section 2,
if applicalbe, Section 3 and 4.

### 5.3.1 Operational User Guidance (AGD_OPE.1)

The operational user guidance does not have to be contained in a single document. 
Guidance to users can be included in the mobile device guidance document or can 
be spread among other document or web pages.

When evaluating AGD_OPE.1, the evaluator performs the work units 
as presented in the CEM, taking the following application notes into account.
There is no application note for AGD_OPE.1-7 and AGD_OPE.1-8.

#### Application note for AGD_OPE.1-1

The TOE is used by the single user and these is only one *user role*. All necessary 
information for using *user-accessible functions* (e.g. mobile biometric enrolment 
and verification) are identified by EAs in Section 2, and, if applicable, 
Sections 3 and 4. 

This work unit also require the evaluator to examine that AGD guidance describes 
*appropriate warnings*. Examples of such warnings for mobile biometric verification 
are as follows.

a)  estimated error rates (i.e. FAR/FRR and FMR/FNMR)

b)  paticular type of users that may face higher error rates (e.g. twins and 
    siblings that look like same may see higher FAR/FMR in case of the mobile 
    face verification) 

The evaluator shall take the above aspects into account to perform this work
unit.

#### Application note for AGD_OPE.1-2

*\(T\)he available interfaces provided by the TOE* can be interpreted as 
"any TSFIs through which the user can enrol and verify his/herself, and 
access any biometric data including templates". The evaluator shall focus
on the *secure use* of such interfaces. Example of guidance for *secure use*
is recommending twins not to use mobile face verification if twins will see
higher FAR/FMR.

The evaluator shall recognize that \[MDFPP\] also covers the evaluation of
such *secure use* of interfaces. For example, number of unsuccessful attempts 
for mobile biometric verification must be limitted by the \[MDFPP\]. The evaluator
shall avoid duplicate effort between evaluations under \[BScPP\] and \[MDFPP\].

#### Application note for AGD_OPE.1-3, AGD_OPE.1-4 and AGD_OPE.1-5

EAs defined in \[SD\] specify required guidance in AGD guidance. 
Therefore, the intent of these works unit are covered by those EAs.

#### Application note for AGD_OPE.1-6

\[BScPP\] defines the assumptions for the mobile device that is the 
operational environment of the TOE. These assumptions are implicitly 
satisfied if the mobile device is successfully evaluated based on \[MDFPP\] 
and the operational guidance doesn’t need to describe *the security measures to be 
followed in order to fulfil the security objectives for the operational environment* 
derived from those assumptions.

### 5.3.2 Preparative Procedures (AGD_PRE.1)

Preparative procedures are useful for ensuring that the TOE has been received and 
installed in a secure manner as intended by the developer. However, the TOE is 
embedded into the mobile device and it is assumed that such information will be 
provided by the mobile device guidance document and evaluated by the mobile 
device evaluation based on \[MDFPP\]. Therefore, AGD_PRE.1.1D is implicitly 
already done by those evaluations and no additional documentation is necessary.

5.4 ALC: Life-cycle Support
--------------------------

At the assurance level provided for a TOE conformant to this cPP, life-cycle 
support is limited to end-user-visible aspects of the life-cycle, rather than 
an examination of the TOE vendor’s development and configuration management 
process. This is not meant to diminish the critical role that a developer’s 
practices play in contributing to the overall trustworthiness of a product, 
rather, it is a reflection on the information to be made available for 
evaluation at this assurance level.

### 5.4.1 Labelling of the TOE (ALC_CMC.1)

This component is targeted at identifying the TOE such that it can be distinguished 
from other products or versions from the same vendor and can be easily identified 
when being procured by an end user. The evaluator performs the CEM work units 
associated with ALC_CMC.1.

When evaluating ALC_CMC.1, the evaluator performs the work units 
as presented in the CEM, taking the following application notes into account.
There is no application note for ALC_CMC.1-2.

#### Application note for ALC_CMC.1-1

The TOE is tightly integrated into the mobile device and the reference of mobile
device can also be used for the TOE reference only if the reference of mobile 
device can uniquly identify the TOE, which means that any modification to the TOE
should lead to the change to the reference of mobile device.

### 5.4.2 TOE CM Coverage (ALC_CMS.1)

Given the scope of the TOE and its associated evaluation evidence requirements, 
the evaluator performs the CEM work units associated with ALC_CMS.1. There is no
application note for this assurance family.

5.5 ATE: Tests
--------------------------

### 5.5.1 Independent Testing – Conformance (ATE_IND.1)

The focus of the testing is to confirm that the requirements specified in the
SFRs are being met. Additionally, testing is performed to confirm the
functionality described in the TSS, as well as the dependencies on the
Operational guidance documentation is accurate.

When evaluating ATE_IND.1, the evaluator performs the work units 
as presented in the CEM. However, evaluator shall conduct all applicable test
items in Appendix C.

Appendix A Developer’s performance test document and its assessment strategy
============================================================================

This Appendix A describes requirements for the developer’s performance
test document (hereafter “test document”) and its assessment strategy.

The developer shall create the test document to report the result of
performance testing (e.g. FRR/FAR or FNMR/FMR).

The evaluator shall examine the test document following the assessment
strategy defined in this Appendix to verify that the developer’s
performance test was done in an objective and repeatable manner to check
the trustworthiness of the measured error rates.

The requirements defined in this Appendix are created based on following
international standards.

ISO/IEC 19795-1:2006 Biometric performance testing and reporting - Part
1: Principles and framework

ISO/IEC 19795-2:2007 Biometric performance testing and reporting - Part
2: Testing methodologies for technology and scenario evaluation.

# A.1 Requirements for the test document

The developer shall provide the test document for CC evaluations that
claim a conform to \[BScPP\]. This section defines required content of
the test document that is inputted to the Evaluation Activity for 
FIA\_MBV\_EXT.1.

# A.2 Summary of contents

Table-A1 shows items that shall be reported in the test document. Name
or structure of test document doesn’t need to follow Table-A1. However,
all items in Table-A1 shall be written somewhere in the test document.
Also, if some items are not included in the test document, the developer
shall provide a rationale for such exclusion to the evaluator.

| Section | Item                                       |
|:--------|:-------------------------------------------|
| A.3.1   | Overview of the performance testing        |
| A.3.2   | Target application and influential factors |
| A.3.3   | Test subject selection                     |
| A.3.4   | Test instructions and training             |
| A.3.5   | Test subject management                    |
| A.3.6   | Test procedure                             |


Table-A1: Reporting items

# A.3 Reporting items description

This section describes each item in Table-A1 in detail. All items are
created based on ISO/IEC 19795-1 and 19795-2 however some of them are
modified to adjust to the CC evaluation.

## A.3.1 Overview of the performance testing

The developer shall report following general information about the
performance testing.

### 1\) Performance test configuration

The test document shall report the following information to uniquely
identify the test configuration of the performance testing. Information
stated here shall be consistent with the ST.

1.TOE reference

Information that uniquely identify the TOE shall be reported.
\[BScPP\] is intended to be used with \[MDFPP\] and reference for the
mobile device can be used as the TOE reference only if the reference
for the mobile device also uniquely identifies the TOE embedded in the
mobile device

Modification to the TOE for performance testing, if any, shall be
reported (e.g. The TOE is modified to export biometric data for
off-line testing). The rationale that such modification doesn’t affect
the TOE performance shall also be provided. For example, the developer
may claim that the performance is not affected because modified code
isn’t executed during mobile biometric verification or the developer
may run regression test to verify that modification doesn’t change the
result of verification (e.g. similarity score).

2.TOE configuration

Any configurable parameters or setting of the TOE that may affect the
performance shall be reported. Value of each parameter set for the
testing shall also be provided. For example, if threshold (e.g.
decision threshold and image quality threshold) is configurable by
users, value of threshold set for the testing shall be reported.

3.Performance test tools

Information that uniquely identify all testing tools (e.g. SDK) used
for the performance testing shall be reported.

### 2\) Result of the performance testing

The test document shall report the following items to provide the result
of testing.

1.Test period and location

Timeline for the performance testing (samples or templates may be
collected over multiple sessions) and location of testing shall be
reported.

2.Modality used for mobile biometric verification

The performance testing shall be done for all modalities selected in
FIA\_MBV\_EXT.1. Result of testing for each modality shall be reported
separately.

3.Definition of genuine and imposter transaction

If FAR/FRR is selected in FIA\_MBV\_EXT.1, the test document shall
clearly define what constitutes the transaction based on the worst 
case senario (See Appendix B for such example) and the same rule 
shall be applied consistently throughout the performance testing.

4.Number of test subjects, templates and samples

The following numbers used for calculating FMR/FNMR or FAR/FRR shall
be reported. See Appendix B for requirements for number of test
subjects, enrollment templates and samples.

This Appendix assumes that at least the FMR or FAR is measured through
offline testing (i.e. cross-comparison) to achieve the maximum number
of attempts or transactions. FNMR or FRR may be measured through
online or offline testing.

a) Test subject

Number of test subjects who participated in the testing shall be
reported.

b) Enrolment templates

Number of enrolment templates used for testing shall be reported.

All test subjects cannot generate the templates successfully and total
number of templates may be less than (number of test subjects) ×
(number of body parts of a test subject).

c) Samples

Number of samples collected for each body part and total number of
samples collected from all test subjects shall be reported.

All test subjects cannot generate the samples successfully and total
number of samples may be less than (number of test subjects) × (number
of body parts of a test subject) × (number of samples collected for
each body part).

5.Result of testing

Error rates measured by the performance testing shall be reported.

If FAR and FRR is selected in FIA\_MBV\_EXT.1, number of genuine and
imposter transaction shall also be reported.

If FMR and FNMR is selected in FIA\_MBV\_EXT.1, number of genuine and
imposter attempts shall also be reported.

## A.3.2 Target application and influential factors

Test document shall specify a target application modeled in the test,
such as mobile biometric verification in an indoor office environment
with a habituated crew.

Test document shall also report influential factors that may influence
performance, measures to control such factors and under what factors the
performance testing was conducted.

Influential factors can be determined by referring appropriate documents
(e.g. ISO/IEC 19795-3) or referring the product datasheet (e.g.
operating temperature). These factors should be consistent with the
target application.

The following factors are examples of controlling factors for
finger/hand vein verification. The developer shall define these factors properly, 
for example, based on ISO/IEC 19795-3. Any information that are useful in the context
of the used biometric modality shall be considered by the developer to determine the factors.

It’s recommended to control all influential factors appropriately 
because different error rates may be measured under different influential 
factors.

1.Test subject demographics

 - Age: age distribution ratio by arbitrary age groups (e.g., 1, 5, 10
 years)

 - Gender: male/female distribution

 - Ethnic origin: Distribution ratio by ethnic origin. Category of
 ethnic origin can be arbitrarily defined by developer.

2.Posture and positioning

Posture of test subject or positioning of his/her hand/finger (e.g.
Orientation of hand/finger in relation to the sensor or distance to
the sensor). Such information should be consistent with the TOE
operational guidance or automated feedback provided by the TOE.

3.Indoor or outdoor

Indoor or outdoor environment in which testing is to be conducted. In
case of outdoor environment, other factors affecting the performance
(e.g. environmental illumination) should also be reported.

4.Temperature

Range of temperature at which the testing is to be conducted (e.g.
“Testing was conducted in an air-conditioned environment where
temperature was kept between X and Y degrees”).

5.Time interval

Time interval (e.g. minimum, maximum and average time) between
enrolment and verification.

6.Habituation

The degree to which the test subject is familiarized with the TOE
(e.g. frequency of use of the TOE)

7.Template adaptation

How much template adaptation occur prior to measure the FNMR or FRR if
the TOE is able to adapt the templates over time with the aim to
reduce the false rejection rates.

## A.3.3 Test subject selection

Selection method of test subjects shall be reported (e.g. gather test subjects from
developer’s employees or recruit them from public). It is recommended that demographics
of test subjects follow the target application.

## A.3.4 Test instructions and training

Instructions and training given to the test subjects shall be reported.
The same instructions and training shall be given to the all test
subjects.

1.Test information and general test instructions

Test information and general test instructions given to test subject
prior or after biometric data collection shall be reported. Such
instructions shall be consistent to automated guidance or feedback
given by the TOE or instructions described in the TOE operational
guidance. Testing shall not be adjusted to the TOE specification that
is not described in the TOE operational guidance.

2.Confirmation of habituation

Method for how to confirm the level of subject habituation prior to
biometric data collection shall be reported. If the habituation was
confirmed through training, method to ensure the consistency of
training among test subjects and the tools used for training shall be
reported (e.g. developer can prepare the script for training in
advance and apply it to all test subjects to ensure the consistency).

## A.3.5 Test subject management

Following information about test subject management shall be reported.
Proper management is necessary to avoid human errors that may occur
during the testing.

1.Management processes

Biometric data can be corrupted by human error during the collection
process (e.g. using a middle finger when the index finger is
required). The test subject management processes to avoid such errors
shall be reported. Management processes shall cover the following
processes.

a) method of initial test subject registration

b) method of ensuring test subject uniqueness

c) amount and type of personal data collected

d) method of avoiding data collection errors (e.g. Use of data
   collection software minimizing the amount of data requiring keyboard
   entry)

## A.3.6 Test procedure

A test protocol for the testing shall be reported. The following items
shall be covered.

1.Type of attempt or transaction

Whether the attempt or transaction is executed online or offline shall
be reported. Online means that enrolment and verification is executed
at the time of image submission. Offline means that enrolment and
verification is executed separately from image submission.

2.Test flow

Details of flow of genuine and imposter attempt or transaction to
measure the error rates shall be reported. The same flow shall be
applied to all test subjects.

The developer shall maintain a log file in which each interaction with
the TOE is recorded. The log shall include all test attempts, preprative
or practice attempts, set-up procedure (e.g. setting a threshold) and 
maintenance activities (e.g. cleaning a sensor). Such a log file can be 
very useful to make sure the testing was conducted following the test 
flow.

3.Sample exclusion criteria

Criteria for sample exclusion shall be reported. Test operator shall
not manually discard nor use an automated mechanism to discard
collected samples unless the samples conform to documented exclusion
criteria. Number of excluded samples shall be reported. If
transactions are failed because of such excluded samples, number of
such failed transactions shall also be reported. These failed
transactions shall be counted as failed transactions to calculate the
error rates.

4.Advice or remedial action

Advices or remedial actions to test subjects who fail to complete
transactions or sample collections shall be reported. Such advices or
remedial actions shall be limited to the minimum amount necessary
because this \[SD\] assumes that the mobile device is used by the
single user without any support. The same advices or remedial actions
shall be given to test subject at the same condition.

Appendix B Requirement for the number of test subject, transaction and samples
==============================================================================

The developer shall follow recommendations or minimum requirements below
to conduct the performance testing to estimate FAR/FMR and FRR/FNMR. The
developer may exclude, modify or add some recommendations however, the
developer shall show a clear rationale why such modifications could
produce more accurate estimate of the performance.

## B.1 Recommendations

### 1\) Scenario of mobile biometric verification

The user may use the mobile biometric verification in a different way.
Suppose the mobile device provides both Password Authentication Factor
and BAF and user can use either of factor to unlock the device. One user
may try to unlock the device with BAF until maximum number of
unsuccessful authentication attempts is exceeded. Another user may try
to unlock the device with BAF only three times and switch to the
password if all three attempts were failed. However, it’s not possible
to evaluate all of these scenarios and the developer shall assume the 
worst case senario of imposter attempts and conduct performance
testing following such scenario consistently.

For example, if the mobile face verification becomes unavailable after
the five successive failed attempts, the developer shall assume that the
attacker makes all five face unlock attempts in succession to try to unlock
the mobile device. In this case, the developer shall define that the 
verification transaction is consisted up to five unlock attempts and 
only one verification transaction can be run by each user.

If the worst case senario can't be determined, the developer may select
an arbitary senario. For example, if the mobile iris verification becomes 
unavailable after the five successive failed attempts, the developer shall 
assume that the attacker tries to all five iris unlock attempts in succession.
However the developer may assume that the user tries right iris for the 
first three attempts and switch to the left iris for the last two attempts 
if all first three attempts were failed, or may assume that the user tries
right iris for all five attempts. The developer can choose either of the 
senario if the developer can't determine which one is the worst case.

### 2\) Maximum number of templates

Only one template can be generated from each body part (e.g. right iris,
left hand index finger or face) and used for the performance testing.

Quality of template may have significant impact on the mobile biometric
verification performance. This \[SD\] assumes that the user is familiar
with the mobile devices operation and enroll his/herself correctly. The
test subject may make enough number of practice attempts to get familiar
with the device operation before the final enrollment transaction.

### 3\) Maximum number of samples per test subject

The developer shall define the maximum number of samples per test
subject following the worst case scenario.

### 4\) Maximum number of transaction per test subject

Only one transaction can be run by each test user because the mobile
device locks the mobile biometric verification as required by \[MDFPP\]
after the certain number of attempts are failed.

### 5\) Statistical certainty for FAR/FMR

FMR/FAR shall be estimated following rule of 3 or 30 because these
errors are most relevant to the security of the TOE and trustworthiness
of those values shall be evaluated statistically. While the rule of 3
would require that one test subject is only involved in one impostor
transaction, it is commonly agreed that the statistical loss of
computing all possible cross-comparisons between test subjects is
acceptable. This \[SD\] allows full cross-comparison to estimate
FAR/FMR.

This \[SD\] also allows cross-comparison of attempts/templates for
ordered pair if there is no explicit reason that this cross-comparison
hinders the accuracy of the result of performance testing.
Cross-comparison of attempts/templates for ordered pair allows to
compare between user A’s template and user B’s sample and user A’s
sample and user B’s template separately. However, if the TOE's 
verification algorithm is symmetric and make no distinction between
the ordered pair, this assumption can't be used.

This \[SD\] doesn’t allow intra-individual comparison that is a
comparison between one body part and another body part of the same test
subject (e.g. comparison between right and left iris of the same user).

### 6\) Statistical certainty for FRR/FNMR

Rule of 3 requires no error occurred for all attempts/transactions and
rule of 30 may require too many attempts/transactions if the FNMR/FRR is
quite low. Therefore, the developer may calculate FNMR/FRR directly from
the result of performance testing without considering the statistical
confidence.

## B.2 Example – iris verification

The developer defines that the iris verification is consisted of 5
attempts using both right and left iris to unlock the mobile device and
specify 0.01 % FAR and 1% FRR in FIA\_MBV\_EXT.1. At least 30,000
imposter transactions shall be conducted with no error to achieve this
performance goal if the rule of 3 is applied. To run more than 30,000
imposter transactions, at least 174 test subjects shall be gathered (173
\* 174 = 30,102). If number of test subjects is 174, only 1 genuine
transaction can be failed to achieve 1% FRR (2/174 = 0.011 &gt; 1%).

If the developer specifies 0.01 % FMR and 1% FNMR in FIA\_MBV\_EXT.1, at
least 30,000 imposter attempts shall be made with no errors. To run more
than 30,000 imposter attempts, at least 78 test subjects shall be
gathered (77 \* 78 \* 5 = 30030). If number of test subjects is 78, the
total number of genuine attempts is 78 \* 5 = 390 and 3 genuine attempts
can be failed to achieve 1% FNMR (4/390 = 0.0102 &gt; 1%)


Appendix C Presentation attack test items for ATE_IND.1
==============================================================================

This Appendix list the minimum presentation attack test items for each biometric 
modality. Test items are mainly derived from relevant reseach papers and discussion 
among BS iTC members. 

Test items are categorized by biometric modality. The evaluator shall conduct all 
test items for selected modality in FIA_MBV_EXT.1.

## C.1 Face

This section describes test items for face presentation attacks. Each item 
defines test protocol including tool types required to perform the test, 
its assessment strategy and pass/fail criteria for the test.

### C.1.1 Overview

Face presentation attack can be carried out through the following process:
1. Get face images of a target user from, for example, uploaded photo on the SNS
2. Display or reconstruct the face image on the spoofing medium such as a photo or
screen (2D attack) or 3D face mask (3D attack). Such a fake face image displayed on
the spoofing medium used for the presentation attack is called a PAI (Presentation
Attack Instrument)
3. Present the PAI to the TOE

The current research categorizes face presentation attacks into the following 
types based on the spoofing medium used and how the face image is recorded.
- 2D face, printed photo attack
- 2D face, digital photo attack
- 2D face, replay video attack
- 3D face, mask attack

All of above types except 3D face, mask attack shall be tested in this EA. 
3D face, mask attack is out of scope because the cost of creating 3D face mask 
doesn’t match to the assurance required by \[BScPP\].

In any type of attack, the TOE captures the fake face image from the spoofing 
medium and unlock the mobile device if the TOE can’t tell the difference between 
real and fake face.

### C.1.2 Type of PAIs for the testing and required tools
Face images captured by the TOE from the spoofing medium may visually look very 
similar to the images captured from real ones, however, they are not exactly the 
same. For example, printed or displayed faces on the paper or screen reflect light 
in different ways because a human face is a complex non-rigid 3D object, whereas 
the photo or screen can be seen as a planar rigid object. The surface properties 
of real faces and fake ones, e.g. pigments, are also different. In addition, fake 
faces may contain artefacts such as moiré patterns that are an undesired aliasing 
of images produced during various image display and image acquisition processes.

The TOE should detect such differences between images taken from real and fake face 
to prevent the presentation attacks. These differences are mainly influenced by 
the following factors listed in the table below and the performance of the PAD 
algorithm may also be affected by them.

| No	| Factor	| Description |
|-------|---------------|-------------|
|1	|Quality of source face image from which the PAI is created | The quality of the source is the foundation of the copy (i.e. PAI). If the source image is poor quality, the quality of PAI will also be limited. Source face images can be taken with a digital camera and quality of digital image varies depending of quality of the camera (e.g. size of sensor and resolution) |
|2	| Quality of tools (e.g.printer and spoofing medium) to create the PAI | A poor quality PAI can be made from a good quality source if the resolution of the printer or screen is low. However, if the screen is 4K resolution that refers to a horizontal screen resolution in the order of 4,000 pixels, it can provide the finest clarity and detail of the face from the good quality source. |

Various quality of PAIs can be created with, for example, smartphone cameras, 
compact or high-professional digital cameras however, it’s time consuming to 
create all possible PAIs using different devices. Therefore, this EA sets the 
two level of quality, normal and high, to cover those variety of PAIs. High 
quality PAIs looks more similar to the real face however, it may show more 
micro facial textures that can be used to differentiate between the real and 
fake. However, such micro textures may not be evident in the normal quality PAIs. 
The TOE may overlook normal quality PAIs if the PAD algorithm completely relies 
on such micro textures to detect the PAIs. So, this EA requires to test both 
levels of quality of PAIs.


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




The TOE should detect such differences between images taken from real and fake face to prevent the presentation attacks. These differences are mainly influenced by the following factors listed in the table below and the performance of the PAD algorithm may also be affected by them.





