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
which is a justification for the derivation of EAs from one or more work units. 
This rationale isn't provided for each EA but summarized separately in section 5.

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

Biometric systems that comply with \[BScPP\] have certain characteristics that require dedicated attention during evaluation. 
Evaluators shall therefore consider the guidance for the assurance classes as provided by \[19989-1\] in addition to \[CEM\]. 
In addition, the following paragraphs provide some specific application notes that result from the specific characvteristics of \[BScPP\].


## Application note for AGD_OPE.1-6

\[BScPP\] defines the assumptions for the mobile device that is the 
operational environment of the TOE. These assumptions are implicitly 
satisfied if the mobile device is successfully evaluated based on \[MDFPP\] 
and the operational guidance doesn’t need to describe *the security measures to be 
followed in order to fulfil the security objectives for the operational environment* 
derived from those assumptions.



5.6 AVA: Vulnerability Assessment
--------------------------

### 5.6.1 Vulnerability Survey (AVA_VAN.1)

While vulnerability analysis is inherently a subjective activity, a minimum
level of analysis can be defined and some measure of objectivity and
repeatability (or at least comparability) can be imposed on the vulnerability
analysis process. In order to achieve such objectivity and repeatability it is
important that the evaluator follows a set of well-defined activities, and
documents their findings so others can follow their arguments and come to the
same conclusions as the evaluator. While this does not guarantee that different
evaluation facilities will identify exactly the same type of vulnerabilities or
come to exactly the same conclusions, the approach defines the minimum level
of analysis and the scope of that analysis, and provides Certification Bodies a
measure of assurance that the minimum level of analysis is being performed
by the evaluation facilities.

When evaluating AVA_VAN.1, the evaluator performs the work units 
as presented in the CEM, taking the following application notes into account
to meet goals described above.
There is no application note for AVA_VAN.1-1, AVA_VAN.1-2, ***tbd*** .

#### Application note for AVA_VAN.1-3

See Appendix D.5.1. 

#### Application note for AVA_VAN.1-4

See Appendix D.2. 

#### Application note for AVA_VAN.1-5

See Appendix D.5.2.

***tbd***


6 References
--------------------------

\[CC1\] Common Criteria for Information Technology Security Evaluation, Part 1: Introduction and General Model, CCMB-2017-04-001, Version 3.1 Revision 5, April 2017.

\[CC2\] Common Criteria for Information Technology Security Evaluation, Part 2: Security functional components, CCMB-2017-04-002, Version 3.1 Revision 5, April 2017.

\[CC3\] Common Criteria for Information Technology Security Evaluation, Part 3: Security assurance components, CCMB-2017-04-003, Version 3.1 Revision 5, April 2017.

\[CEM\] Common Methodology for Information Technology Security Evaluation, Evaluation Methodology, CCMB-2017-04-004, Version 3.1 Revision 5, April 2017.

\[BScPP\] collaborative Protection Profile for Mobile biometric enrolment and verification - for unlocking the device - \[TBD\]

\[MDFPP\] Protection Profile for Mobile Device Fundamentals, Version:3.1, 2017-06-16

\[ISO19792\] Security evaluation of biometrics

\[ISO30107-1\] Biometric presentation attack detection — Part 1: Framework

\[SD\] Evaluation Activities for Mobile biometric enrolment and verification – for unlocking the device – cPP \[TBD\]

\[19989-1\] ISO/IEC 19989 (CD1) Security techniques — Criteria and methodology for security evaluation of biometric systems — Part 1: Framework \[TBD\]



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
test items for modalities selected in FIA_MBV_EXT.1, however, the evaluator can 
skip some of them if he/she can provide a valid rationale.

## C.1 Face

This section describes test items for face presentation attacks. Each item 
defines tool types required to perform the test, its assessment strategy and 
pass/fail criteria for the test.

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

In any type of attack, presentation attack is succeeded if the TOE captures the 
fake face image from the spoofing medium and unlock the mobile device because 
the TOE can’t tell the difference between real and fake face.

### C.1.2 Tool types required to perform the presentation attack testing

Face images captured by the TOE from the spoofing medium may visually look very 
similar to the images captured from real ones, however, they are not exactly the 
same. For example, printed or displayed faces on the paper or screen reflect light 
in different ways because a human face is a complex non-rigid 3D object, whereas 
the photo or screen can be seen as a planar rigid object. The surface properties, 
e.g. pigments, of real faces and fake ones are also different. In addition, fake 
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

Table-C2: Quality factors

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
Scanner | 300 DPI | 600 DPI | | 
Printer | Home SoHo Inkjet | Laser | Printing Service
Paper | Standard Letter | Cardstock | Photo Paper
Computing resources | Mobile device | PC or laptop | Professional
Output Screen | 1080p 10" | 1080p -> 2160p under 20" | 4K above 24"

Table-C3: Tool category and level

### C.1.2 Assessment strategy for presentation attack testing
This section specifies test items for face presentation attack. 

#### C.1.2.1 Format of test item 
All test items in C.1.2.2 are specified using the following common format.

1\) Number

Identification of test item. 

2\) Attack type

Either of the following type is assigned to each test item.

- 2D face, printed photo attack 
- 2D face, digital photo attack 
- 2D face, replay video attack 

3\) Overview

Brief overview of the presentation attack scenario.

4\) Input

Target user’s face information available to the attacker.

5\) Tools

Tools required to create the PAI and to perform the attack.  

6\) Recipe

Method to create the PAI. Stepwise instructions.

7\) Variations

Identification of potentially useful variations to the recipe. 

8\) Prerequisite

All prerequisite conditions that need to be established before the attack. 

9\) Presentation

How to present the PAI to the TOE.

10\) PAD technique

Possible PAD technique that can detect the attack. 

11\) Reference

Existing research papers based on which each test item is created. 
Evaluator should look at them because detailed test procedure may be 
described in the papers.

#### C.1.2.2 Test items 

-------

Number
=======
1-1 

Attack type
===========
2D face, printed photo attack

Overview
========
In this test, user’s face digital image is not available but photo of the target can be 
used to create PAI.

Target user is privacy aware. The user doesn’t publish any face images on the internet
so user’s digital face images are not available to attacker. However, the user places 
photo of the user on his/her desk. Attacker can scan such picture to make the PAI.

Input
======
Photo of target user that meet the following conditions:
- photo was taken under controlled environment where the background of the scene 
is uniform, the light in the office is switched on and the window blinds are down
- photo was taken right after the target user’s enrolment and under the same 
environment to reduce the possibility that the PAI is rejected because of the 
difference of the background scene or expression
- target user’s face occupies about 20% of the full image
- photo includes user’s full face
- photo was taken by level 3 camera

Tools
=====
The following tool shall be used when the evaluator create PAIs following the recipe.

- Scanner: level 1 or 2
- Printer: level 1 or 2
- Paper: level 1 or 2

Recipe
======
1) Evaluator scans user’s photo image and saves it in PC. 
2) Evaluator crops the face image using basic image editing software (e.g. Microsoft Paint) 
to enlarge it to cover as much of the paper as possible while maintaining the original 
image aspect ratio. If multiple options are available for enlarging the image, an option 
that achieves best image quality should be selected. Evaluator doesn’t use image editing 
software to enhance quality of face image (such attack is considered later).
3) Evalautor prints it out on a paper.

Variations
==========
tbd

Prerequisite
============
Target user turns on the face unlock and registers user’s face following instructions 
provided by the device and manual (i.e. target user should not wear glasses, hat, beard, 
or heavy make-up during the enrollment if the guidance instructs not to do so) under 
the controlled environment.

If the ST covers the multiple configurations for face unlock, the same test should be 
done for all configurations.

Presentation
============
Evaluator presents the photo to the device by hand at controlled environment. 
Evaluator adjusts the distance between the photo and the device to right distance 
so that the device camera can’t see the edge of photo. Evaluator also presents 
the photo to minimize the reflection from ambient lighting.

PAD technique
=============
During scanning, enlarging and copying the image, lots of information like high 
frequency information of original face will be lost. Such changes can be detected 
by, for example, LBP that require relatively low computational power.

Reference
=========
There is no research paper that conduct attacks following this scenario. All PAIs 
were created using live image of target user, not photo image of the user in all researches.

Pass Criteria
=============
The evaluator shall create at least one PAI for one user and make at least 10 presentation attempts.
All attempts shall be rejected. Proposed algorithm in the existing research papers are 
capable to detect this primitive attack.

-------

***tbd***  
***other test items will be included from https://github.com/biometricITC/cPP-biometrics/tree/master/4_Methodology/attacks***
***similar test items for iris will also be included***

-------

Appendix D Application notes for Vulnerability Analysis
==============================================================================

## D.1 Attack to the TOE

Various types of attack to the general biometric system are defined in \[ISO19792\] 
and \[ISO30107-1\]. The evaluator doesn't need to evaluate all of them for the TOE because 
of the assumptions defined in the \[BScPP\] and assurance level (i.e. required attack potential) 
claimed by the \[BScPP\]. However, the evaluator shall consider the following three 
types of attack that the TOE must counter.

a)  An attacker may attempt to impersonate as a legitimate user using only his/her own 
    biometric characteristic (i.e. zero-effort impostor attempt) 

b)  An attacker may attempt to impersonate as a legitimate user using artificial 
    Presentation Attack Instrument (PAI).

c)  An attacker may attempt to access plaintext biometric data through mobile device 
    interfaces to create the PAI

The above a) can be evaluated through EA for FIA_MBV_EXT.1 and c) can be evaluated 
through EAs for FPT_BDP_EXT.1, FPT_BDP_EXT.2, FPT_BDP_EXT.1-3 and FPT_PBT_EXT.1. 

b) can also be evaluated through EA for FIA_MBV_EXT.3, however, this EA defines the 
minimum presentation attack testing that all evaluator shall conduct. The evaluator 
shall also conduct additional penetration testing to make sure that the TOE is 
resistant to presentation attacks by an attacker possessing a Basic attack potential. 

This Appendix provides the guidance for the evaluator’s presentation 
attack testing that shall be conducted during the AVA evaluation.

Any other types of attack are out of scope of the \[SD\] because the BS iTC can't find
such attacks from information published by the release date of this \[SD\].

If the evaluator may find such attacks that aren't covered by this \[SD\] but can be 
conducted by the attacker possessing Basic attack potential, the evaluator shall 
seek a guidance from the BS iTC to evaluate those novel attacks.

## D.2 Assumptions for AVA presentation attack testing

The evaluator shall assume the following assumptions described in the \[BScPP\].

1\)	Motivation of attackers

The TOE is used to unlock the devices but not used for financial transactions. Attacker 
doesn’t have strong motivation to unlock the device but tries to unlock his/her friends’ 
or co-workers’ mobile devices just for fun. Therefore, \[SD\] assumes that the attacker 
conducts attacks simply following scripts (i.e. step by step guide (e.g. demo on YouTube) 
to create the PAI and run the attack with those PAI) that are publicly available.
However if the attackers recognizes that it takes too much time and cost to follow the 
scripts, they would simply give up attacking the TOE. 
Attacker would use any tools or materials that are normally available at home and normal 
office environment such as laptop PC or office printer. Attacker would also use available 
services such as online printing services to create the PAI if such services are available 
at low cost.

2\)	Assumption from the cPP

\[BScPP\] defines A.User and the evaluator shall assume that the mobile devices are configured 
securely by users. Especially the evaluator shall make the following assumptions:

a)	A user enroll him/herself following guidance provided by the TOE   
b)	Mobile device is securely configured and maximum number of unsuccessful biometric 
    authentication attempts is limited.

However, the evaluator can increase the maximum number of unsuccessful biometric 
authentication attempts to conduct the penetration testing efficiently. However, 
the mobile device shall be evaluated in the evaluated configuration, which means 
that attack needs to be succeeded within the allowed number of biometric authentication 
attempts.

\[BScPP\] also defines A.Protection and the evaluators shall assume that biometric 
data is adequately protected if the evaluator doesn't find any flaws during peforming 
the EAs for FDP_BDP_EXT.1, FDP_BDP_EXT.2, FDP_BDP_EXT.3 and FPT_PBT_EXT.1.
Especially the evaluator shall make the following assumptions:

a)	Attacker can’t access to the result of PAD subsystem so they can’t tune the PAIs 
    based on the PAD score   
b)	Attacker can’t gain the templates from the mobile device to create the PAIs

## D.3 Test timeframe

The evaluator shall keep in mind that attacker’s motivation is not so high. 
Timeframe for the presentation attack testing should be one week at maximum.

## D.4 Prerequisite for evaluators

Successful presentation attacks may require fine-tuning of parameters such as 
distance between the PAI and mobile device or lightning condition. The evaluator 
may learn good parameters through the EA for FIA_MBV_EXT.3. In addition to 
that, there are lots of videos, presentation slides or research papers on the 
internet that show how presentation attack can be conducted successfully. 
The evaluator shall watch those videos to learn, for example, how to present 
the PAI or how to create the PAI to conduct the testing efficiently as much 
as possible. 

The evaluator shall utilize such knowledge to conduct the testing. However,
all effort and required knowledge or experience to identify the successful 
presenation attack methods shall be taken into account when the evaluator 
caluculate the attack potential.

## D.5 vulnerability analysis process

This section specifies the process for the vulnerability analysis that the 
evaluator shall follow.

### D.5.1 Internet search

There are lots of scripts available in the internet that define the procedure 
to create the PAI and run the attack with those PAI. The presentation test 
items for ***face (C.1.2.2), iris (XXXXX), tbd*** .. are created based on such scripts 
and the most of them are covered by those test items.

However, the evaluator may gain useful knowledge from such scripts because
they may provide the following information that the test items don't provide.

a) Specific presentation attack method to the TOE
   If the evaluator can find the script that is actually used to attack the
   TOE being evaluated or previous version of the TOE, the evaluator shall 
   conduct the attack following the script if the attack can be conducted 
   by the attacker possessing a Basic attack potential. Test items defined 
   in this \[SD\] specify only general information applicable to all type 
   of biometric verification products. 

b) More detailed presentation attack method to the TOE 
   Some scripts include a video clip to show how to create the PAI and 
   how to present the PAI to the TOE in detail. Other ones specify 
   identification information of tools that actually used to create the PAI.
   The evaluator shall take such information into account to conduct
   the presentation attacks.

c) Cost of conducting the presentation attack to the TOE
   Some scripts show cost, time and effort to conduct the presentation 
   attack (e.g. cost of developing tools to create the PAI and 
   the number of total presentations of PAI to the TOE). The evaluator
   shall consider such information to determine whether the attack is 
   beyond the Basic attack potential or not and how much effort should
   be spent for the presentation attack.
   
d) New presentation attack method to the TOE
   If the evaluator can find the script that is not covered by this \[SD\],
   the evaluator shall conduct the attack following the script if the 
   attack can be conducted by the attacker possessing a Basic attack potential. 

### D.5.2 Determine the presentation attack test items
  
The evaluator can modify the presentation test items specified in the \[SD\] or
create new test items based on the scripts available in the internet. However,
evaluator shall keep in mind the test timeframe (see D.3) to devise presentation
attack test items.

The evaluator may spend equal time and effort on each test items, however, the 
evaluator shall prioritize the test items considering information gained from 
scripts as much as possible. For example, the evaluator may give higher priority 
to the test item for which detail and clear scripts are avaiable because the 
attacker are easy to follow such ones or one for which scripts that successfuly 
attack the previous version of the TOE are available. The evaluator shall
report how he/she prioritize the test items based on which information in the 
ETR.

### D.5.3 Produce penetration test documentation

The evaluator shall create clear presentation method in sufficient detail to 
enable the tests to be repeatable, especially, if evaluator succeed the 
presentation attacks.

The evaluator may gradually change the presentation attack methods, for example,
the distance between the TOE and PAI, ambient lighting condition and resoluation
of PAI untill the attack succeed. However, the evaluator shall add such 
detail to the test documentation so that other evaluators can also successfully 
attack the TOE.

### D.5.4 Attack potential calculation

If the evaluator can succeed the presentation attack, the evaluator shall confirm
that the attack can be conducted by the attacker possessing the Basic attack potential.
The evaluator shall follow Appendix E in \[SD\] to calculate the attack potential. 
Appendix E adjusts the caluculation methods defined in \[CEM\] to the biometric verification.

### D.5.5 Pass Criteria

***TBD***

Appendix E Attack Potential and TOE resistance
==============================================================================

## E.1 Calculating attack potential

Attack potential is a function of expertise, resources and motivation, as is written in 
\[CEM\]. Regarding motivation, see B.4.1.1 in \[CEM\].

### E.1.1 Identification and exploitation of attacks

#### E.1.1.1 Identification of attacks

Identification corresponds to the effort required to create the attack, and to demonstrate 
that it can be successfully applied to the TOE (including setting up or building any 
necessary test equipment). The demonstration that the attack can be successfully applied 
needs to consider any difficulties in expanding a result shown in the laboratory to create 
a useful attack. One of the outputs from identification could be a script that gives a 
step-by-step description of how to carry out the attack. This script is assumed to be used 
in the exploitation phase.

#### E.1.1.2 Exploitation of attacks

Exploitation corresponds to achieving the attack on an instance of the TOE in its exploitation 
environment using the analysis and techniques defined in the identification phase. It could 
be assumed that a different attacker carries out the exploitation, the technique (and relevant 
background information) could be available for the exploitation in the form of a script or 
set of instructions defined during the identification phase. This type of script is assumed 
to identify the necessary equipment and, for example, mathematical techniques used in the 
analysis, or presentation attack methods. Furthermore, this same information may also reduce 
the exploitation requirement to one of time measurement, whereas the identification phase may 
have required reverse engineering of hardware or software information hence the expertise 
requirement may be reduced.

NOTE1 For the evaluator, the work of the identification phase has to be fully performed: 
developing hardware and software, creating PAIs if any, etc. The rating of this phase 
corresponds to the "real spending" in defining the attack. For the exploitation, it is 
not necessary to perform the work again and the rating could correspond to an evaluation 
of the necessary effort for each factor.

NOTE2 Exploitation consisting in applying scripts, it is expected that some factor 
values will be reduced from the identification phase, in particular "Elapsed Time" 
and "Expertise". For the same reason, the "Knowledge of the TOE" factor is not 
applicable in the exploitation phase (all the knowledge is scripted).

### E.1.2 Factors to be considered

As in \[CEM\], the factors to be considered consist of ***Elapsed time***, 
***Expertise***, ***Knowledge of the TOE***, ***Window of opportunity***, and 
***Equipment***. But ***Window of opportunity*** is divided into two subfactors 
***Window of opportunity (Access to the TOE)*** and ***Window of opportunity 
(Access to biometric characteristics)*** \.

***Elapsed time*** is the total amount of time taken by the attacker.

In the identification phase, elapsed time corresponds to the time required 
to create the attack, and to demonstrate that it can be successfully applied 
to the TOE (including setting up or building any necessary hardware or software 
equipment). The demonstration that the attack can be successfully applied 
needs to consider any difficulties in expanding a result shown in the 
laboratory to create a useful attack. One of the outputs from identification 
is, for instance, a script that gives a step-by-step description of how to 
carry out the attack. This script is assumed to be used in the exploitation part.

In the exploitation phase, elapsed time corresponds to the time necessary to 
apply the "script" to specific biometric characteristics. For example, for a 
presentation attack to a fingerprint capture device, it corresponds to the 
time required to create a PAI from an image of a print (and not the acquisition 
of this image which is taken into account in the factor ***Window of opportunity 
(Access to biometric characteristics)*** \).

Potential difficulties to have an access to the TOE in exploitation environment 
are taken into account in the factor ***Window of opportunity (Access to the TOE)*** \.

***Expertise*** refers to the level of proficiency required by the attacker and the 
general knowledge that he possesses, not specific of the system being attacked. 
The levels are as follows:

a) Layman is the level no real expertise needed and such that any person with 
   a regular level of education is capable of performing the attack. For example, 
   creating a PAI in a known (published) way without specific difficulties 
   (specific or difficult to buy materials) is considered at this level of expertise.
   
b) Proficient is the level such that some advanced knowledge in certain specific 
   topics (biometrics) is required as well as good knowledge of the state-of-the-art 
   of attacks. An attacker of this level is capable of adapting known attack methods 
   to his needs. For example, adapting a known attack type (published) by the choice 
   of specific (not published and sometimes difficult to find) materials in order 
   to bypass a presentation attack detection mechanism and/or finding a non-evident 
   way to present this PAI to the system can be considered at this level of expertise.
   
c) Expert is the level such that a specific preparation in multiple areas such as 
   pattern recognition, computer vision or optimization is needed in order to carry 
   out the attack. An attacker of this level is capable of generating his own new 
   attacking algorithms. For example, finding a new (unpublished) way of creating 
   an attack type using new and specific materials (unpublished) to counter an 
   advanced presentation attack detection mechanism, can be considered at this 
   level. In addition, this level can be associated with specific equipment (bespoke)
   
d) Multiple experts is the level such that the attack needs the collaboration of 
   several people with high level expertise in different fields (e.g., electronics, 
   cryptanalysis, physics, etc.). It has to be noticed that a specific competence 
   in biometrics is not considered as "multiple expertise". For example, building 
   a "hill climbing" attack by gaining access to the comparison scores requires 
   additional expertise to electrically attack and penetrate the TOE, which can be 
   considered to constitute a "multi expertise" level.
   
NOTE1 As previously noted, exploitation expertise is usually lower than identification 
expertise. Layman or Proficient can be considered as typical value for expertise in 
the exploitation phase. For the same reason, the multiple expert level is excluded 
from the exploitation phase.

NOTE2 As all the factors, higher rating would require specific justifications from the evaluator.

***Knowledge of the TOE*** refers to the amount of knowledge of system required 
to perform the attack. For instance, format of the acquired samples, size and 
resolution of acquisition systems, specific format of templates, but also specifications 
and implementation of countermeasures are knowledge that could be required to set up an attack.

This information could be publicly available at the website of the capture device 
manufacturer or protected (distributed to stakeholders under non-disclosure agreement 
or even classified inside the company). The levels are as follows:

a) Public information which is fairly easy to obtain (e.g., on the web).

b) Restricted information which is only shared by the developer and organizations 
   which are using the system, usually under a non-disclosure agreement.

c) Confidential information which is only available within the organization that 
   develops the system and is in no case shared outside it.
   
d) Critical information which is only available to certain people or groups 
   within the organization which develops the system.
   
Special attention should be paid in this point to possible countermeasures that may be 
implemented in the system and whether it is necessary or not to have knowledge of their 
existence in order to be successful in a given attack.

It is assumed that all the knowledge required to perform the attack is gained during 
the identification phase and "scripted" for the exploitation. Therefore, this factor is 
not used for the exploitation phase.

***Window of opportunity (Access to the TOE)*** refers to measuring the difficulty 
to access the TOE either to prepare the attack or to perform it on the target system.

For the identification phase, elements that should be taken into account include the 
easiness to buy the same biometric equipment (with and without countermeasures).

For exploitation phase, both technical (such known/unknown tuning) and organizational 
measures (presence of a guard, ability to physically modify the target, limited number 
of tries, etc.) should be taken into account.

The number and the level of equipment requested to build the attack is also taken into 
account in this factor.

This factor is not expressed in terms of time. The levels are as follows:

a) Easy: For identification phase, there is no strong constraint for the attacker to 
   buy the TOE (reasonable price) to prepare its attack. For exploitation phase, there 
   is no limit in the number of tries and the presentation attack is difficult to detecte.
   
b) Moderate: For identification phase, specialised distribution schemes exist 
   (not available to individuals). For exploitation phase, either a tuning of the 
   attack for the final system is required (unknown parameterization of countermeasures 
   for example) or there is a supervision of the biometric system emitting, for example, 
   an alert in case of numerous fail presentations.

c) Difficult: For identification phase, the system is not available except for 
   identified users and access requires compromising of one of the actors. For exploitation 
   phase, for example PAIs must be adapted to the (unknown) specific tuning, or there is 
   a strong supervision (for example a guard), or the system needs physical modification 
   (for example physically accessing a hidden signal significant of the comparison score). 
   Compromising one actor involved in the use of the system (guard, administrator, and 
   maintenance) is often required.
   
***Window of opportunity (Access to biometric characteristics)***

Security evaluations of \[CC\] are dedicated to evaluate the intrinsic resistance of a 
system. Due to the potential number of attack paths (with or without the cooperation 
of an enrolled subject for example) the evaluation does not take into account the way a 
real biometric characteristic is acquired. For presentation attack detection, the 
vulnerability analysis is based on the hypothesis that a real "image" is available, 
and the rating only concerns the creation and the presentation of a PAI.

However, it is important to be able to compare the resistance of various systems, 
even based on different biometrics. In addition, getting a real "image" to build a 
PAI is clearly part of an attack and it is of interest, for the final user of the 
TOE and the pertinence of a certificate to add a factor related to this aspect. 

The levels are as follows:

a) Immediate is for 2D face, signature image, and voice. Samples of these modalities 
   can be collected without difficulty, even without direct contact with an enrolled 
   data subject (an exploration of the web and the social networks and so forth).

b) Easy is for fingerprint. Latent fingerprints are often left on objects the enrolled 
   data subject had in hand, but need to be revealed, acquired and the corresponding 
   images need a preprocessing.
   
c) Moderate is for 3D face, dynamic signature, and 3D fingerprint. 3D images require 
   multiple acquisitions, probably in a controlled way, without the collaboration of 
   an enrolled data subject but probably with a direct contact with them.
   
d) Difficult is for iris and vein. Iris images can be acquired with a high resolution 
   camera, but with some difficulties to get a complete high quality image without 
   the cooperation of an enrolled data subject. Veins are a hidden characteristic, 
   but infra-red cameras, close to them, can acquire images to be used.
   
NOTE 1 The above distribution of modalities per level is subject to modification 
depending on the evolution of technologies and usage. The current distribution is 
to be seen as guidance for the evaluator, who will have to adapt the rating to 
state-of-the-art.

NOTE 2 Rating the resistance of a system is based on rating the successful 
attacks and verifying that no successful attack is found at the targeted level. 
Some attacks do not need real biometric data to be available, for example, attacks 
based on synthetic images or templates generation. In such a case, this factor has 
to be considered to be Immediate.

***Equipment*** refers to the type of equipment required to perform the attack. 
This includes the biometric databases used (if any). The levels are follows:

Standard equipment is an ordable, easy to obtain and simple to operate equipment 
(e.g., computer, video cameras, mobile phones, "do it yourself" material, 
and artistic leisure materials).

Specialised equipment refers to fairly expensive equipment, not available in 
standard markets and which require of some specific formation to be used (e.g., 
laboratory equipment, advanced printer specific materials and inks, and advanced 
oscilloscopes).

Bespoke equipment refers to very expensive equipment with difficult and controlled 
access; for example, research printing systems with specific ink definition and 
flexible support adaptation. In addition, if more than one specialised equipment 
are required to perform different parts of the attack, this value should be used. 
Before using this level, it has to be carefully checked that no service is available 
(renting, limited time access, etc.). If such service exists, the level has to be 
moved down to Specialised level.

### E.1.3 Calculation of attack potential

Table E1 identifies the factors discussed in the previous subclause and associates 
numeric values with the total value of each factor.

Factor | Identification | Exploitation
--- | --- | --- 
**Elapsed Time** |  |  
<= one day | 0 | 0 
<= one week | 1 | 2 
<= two weeks | 2 | 4 
<= one month | 4 | 8 
\> one month | 4 | 16  
**Expertise** |  |  
Layman | 0 | 0 
Proficient | 2 | 4 
Expert | 4 | 8 
Multiple experts | 8 | Not applicable 
**Knowledge of TOE** |  |  
Public | 0 | Not applicable 
Restricted | 2 | Not applicable 
Sensitive | 4 | Not applicable 
Critical | 8 | Not applicable 
**Window of Opportunity (Access to TOE)** |  |  
Easy | 0 | 0 
Moderate | 2 | 4 
Difficult | 4 | 8 
**Window of Opportunity (Access to Biometric Characteristics)** |  |  
Immediate | Not applicable | 0 
Easy | Not applicable | 2 
Moderate | Not applicable | 4 
Difficult | Not applicable | 8 
**Equipment** |  |  
Standard | 0 | 0 
Specialised | 2 | 4 
Bespoke | 4 | 8 

Table-E1: Calculation of attack potential

In order to calculate the attack potential value of the entire attack, the 
evaluator shall add all the values of all the factors in identification phase 
and exploitation phase.

### E.1.4 Rating of vulnerabilities and TOE resistance

The "Values" column of Table E2 indicates the range of attack potential values 
(calculated using Table E1) of an attack scenario that results in the SFRs 
being undermined.

Values | Attack potential required to expoit scenario | TOE resistant to attackers with attack potential of | Meets assurance components | Failure of components
--- | --- | --- | --- | --- 
\< 10 | Basic | No rating | - |  AVA_VAN.1, AVA_VAN.2, AVA_VAN.3, AVA_VAN.4, AVA_VAN.5 
10-19 | Enhanced-Basic | Basic | AVA_VAN.1, AVA_VAN.2 | AVA_VAN.3, AVA_VAN.4, AVA_VAN.5 
20-29 | Moderate | Enhanced-Basic | AVA_VAN.1, AVA_VAN.2, AVA_VAN.3 | AVA_VAN.4, AVA_VAN.5 
30-39 | High | Moderate | AVA_VAN.1, AVA_VAN.2, AVA_VAN.3, AVA_VAN.4 | AVA_VAN.5 
=>40 | Beyond-High | High | AVA_VAN.1, AVA_VAN.2, AVA_VAN.3, AVA_VAN.4, AVA_VAN.5 | -  

Table E2 — Rating of vulnerabilities and TOE resistance
