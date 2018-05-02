# Change proposal to \[MDFPP\]

## 1. Boundary between the TOE and mobile device

See Annex A in our cPP. This Annex explains relation between SFRs in
\[MDFPP\] and our cPP that sets a clear boundary between the mobile
device and the biometric system (TOE in our cPP). Some SFRs in the
\[MDFPP\] should be moved to the cPP following this boundary. This
document explains what modification should be done to \[MDFPP\] 
so that the mobile device can be evaluated based on both \[MDFPP\] 
and our cPP at the same time without any conflict.

## 2. Procedure to evaluate the mobile device based on \[MDFPP\] and the cPP

\[MDFPP\] and our cPP are separate PPs and developer must make a
conformance claim to both \[MDFPP\] and our cPP. Developer must select 
the same biometric modalities in FIA\_UAU.5.1 in \[MDFPP\] and
FIA\_MBV\_EXT.1 in our cPP.

Developer doesn’t need to prepare separate document such as AGD guidnace
for both evaluations if document satisfy requirements defined in both
\[MDFPP\] and cPP/SD.

## 3. Change proposal

This section lists the change proposals to \[MDFPP\] from the Biometric Security iTC.

### 1) 1.2 Scope of Document

***Proposed change***

Add following text at the end of section.

*Biometric security is out of the scope of this Protection Profile and
should be evaluated separately based on the collaborative Protection
Profile for Mobile biometric enrolment and verification - for unlocking
the device - \[Bio cPP\]*

***Rationale***

Scope of each PP should be defined.

### 2) 1.4 Glossary

***Proposed change***

Delete following terms.

*Adaptive (template), Authentication Template, Biometric Data, ,
Enrollment (Biometrics), Enrollment Template, False Accept Rate (FAR),
False Reject Rate (FRR), (Biometric) Feature(s), Liveness Detection,
NIST Fingerprint Image Quality (NFIQ), Presentation Attack Detection
(PAD), (Biometric) Template, Threshold*

***Rationale***

Above terms should move to the cPP.

### 3) 1.5 TOE Overview

***Proposed change***

Add the following text at the end of section

*Biometric system is out of scope of the TOE. If the mobile device
support biometric authentication, the biometric system shall be
complied with \[Bio cPP\].*

***Rationale***

Biometric system is the TOE for the cPP. \[MDFPP\] shall excludes the
biometric system from the TOE scope and biometric system shall complied 
with the cPP endorsed by the CCRA.

### 4) 2 CC Conformance

***Proposed change***

Add the following text at the end of section

*This PP allows conformance claims to it in combination with \[Bio
cPP\].*

***Rationale***

This statement is required to use \[MDFPP\] and the cPP at the same
time. See para 30 in Exact Conformance, Selection-Based SFRs, Optional
SFRs May 2017.

### 5) 3.1 Threats

***Proposed change***

Delete text indicated by ~~strikethrough~~ and add text in **Bold**.

*The threats considered in this Protection Profile are those of network
eavesdropping, network attacks, physical access, malicious or flawed
applications, persistent presence **and** backup, ~~biometric
impersonation, revocation of biometric credentials, and revocation of
biometric template~~ as detailed in the following sections*

***Rationale***

The cPP covers threats above.

### 6) 4.1 Security Objectives for the TOE

***Proposed change***

Remove *FDP\_PBA\_EXT.1 (optional), FIA\_BMG\_EXT.1 (optional),
FIA\_BMG\_EXT.2 (optional), FIA\_BMG\_EXT.3 (optional), FIA\_BMG\_EXT.4
(optional), FIA\_BMG\_EXT.5 (optional), FIA\_BMG\_EXT.6 (optional)* from
the SFR listed after “*Addressed by*”

***Rationale***

The cPP covers SFRs above.

### 7) 5.1 Security Fundamental Requirements

***Proposed change***

Replace

\[*Italicized text within square brackets*\] indicates the completion of
a selection.

with

\[text within square brackets\] indicates the completion of a selection.

***Rationale***

Editorial mistake.

### 8) 5.1.1 Class: Security Audit (FAU)

***Proposed change***

Change the *number 4* to *number 5* in the application note below.

*Application Note: Administrator actions are defined as functions labeled 
as mandatory for FMT_MOF_EXT.1.2 (i.e. ‘M-MM’ in Table 5). If the TSF does 
not support removable media, **number 4** is implicitly met*

***Rationale***

Editorial mistake.

***Proposed change***

Remove *FDP\_PBA\_EXT.1 (optional), FIA\_BMG\_EXT.1 (optional),
FIA\_BMG\_EXT.2 (optional), FIA\_BMG\_EXT.3 (optional), FIA\_BMG\_EXT.4
(optional), FIA\_BMG\_EXT.5 (optional), FIA\_BMG\_EXT.6 (optional)* from
“*Table 2: Additional Auditable Events*” in “*Evaluation Activity*”

***Rationale***

The cPP covers SFRs above.

### 9) FCS\_CKM\_EXT.4.2

***Proposed change***

Delete following text from Application note.

*If a BAF is selected in FIA\_UAU.5.1 the enrollment or authentication
templates are not subject to this requirement, since templates are not
suitable for deriving keying material. However, source biometric data
(i.e. fingerprint image or friction ridge pattern), the features an
algorithm uses to perform biometric authentication for enrollment or
verification (e.g. location of minutia), threshold values used in making
the match adjudication, intermediate values calculated while building an
enrollment or authentication template (i.e. direction maps, minutia
counts, binarized and skeletonized representations of friction ridge
patterns, etc.), and final match scores are examples of critical
security parameters that must be destroyed when no longer needed.*

***Rationale***

Evaluation activity for FCS\_CKM\_EXT.4 (dumping the memory to make sure
the data is destroyed) may not be applicable to all biometric data,
especially data residing in the biometric sensor because such tool to
dump the sensor memory may not be available.

Instead of requiring evaluator to conduct such testing, the cPP requires
evaluator to confirm that the TOE processes biometric data within the
boundary of the Secure Execution Environment (SEE) to prevent any entity
outside the environment (non-secure world) from accessing biometric data
(The cPP assumes that the SEE protects biometric data adequately within
the boundary of SEE. Evaluation of SEE is out of scope of the cPP)

The SD will define corresponding evaluation activity to require
evaluators to examine, for example;

-   how the processor in the secure world and sensor establishes the
    secure connection so that non-secure world can’t gain access the
    sensor and biometric data captured

-   any memory biometric data is retained during the processing and how
    the memory is isolated from non-secure world

-   what kind of information non-secure world can gain from the TOE
    running inside the SEE.

### 10) FCS\_STG\_EXT.2

***Proposed change***

Replace

-   *Protected by the REK with \[selection:*

*encryption by a REK,*

*encryption by a KEK chaining from a REK,*

*encryption by a KEK that is derived from a REK*

-   *Protected by the REK and the password with \[selection:*

*encryption by a REK and the password-derived KEK,*

*encryption by a KEK chaining to a REK and the password-derived or biometric-unlocked KEK,*

*encryption by a KEK that is derived from a REK and the password-derived or biometric-unlocked KEK*

With

1)  *Protected by the REK with \[selection:*

a)  *encryption by a REK,*

b)  *encryption by a KEK chaining from a REK,*

c)  *encryption by a KEK that is derived from a REK*

2)  *Protected by the REK and the password with \[selection:*

a) *encryption by a REK and the password-derived KEK,*

b) *encryption by a KEK chaining to a REK and the password-derived or biometric-unlocked KEK,*

c) *encryption by a KEK that is derived from a REK and the password-derived or biometric-unlocked KEK*

***Rationale***

Selection numbering is missing.

### 11) FIA\_UAU.5.1

***Proposed change***

Replace Application Note with following text.

*Application Note: The TSF must support a Password Authentication Factor
and may optionally implement a BAF. Biometric authentication mechanisms
must be complied with \[Bio cPP\] and biometric modality selected in
this requirement must be consistent with one selected in \[Bio cPP\].*

*A hybrid authentication factor is where a user has to submit a
combination of PIN/password and biometric sample where both have to pass
and if either fails the user is not made aware of which factor failed.*

*If “hybrid” is selected, a biometric modality does not need to be
selected, but should be selected if the biometric authentication can be
used independent of the hybrid authentication, i.e. without having to
enter a PIN/password.*

*The Password Authentication Factor is configured according to
FIA\_PMG\_EXT.1.*

***Rationale***

Remove text that is covered by the cPP.

### 12)  FIA\_UAU.7.1 

***Proposed change***

Change *removed to quickly* to *removed too quickly* in Evaluation Activity Test 2

***Rationale***

Typo

### 13) FPT\_KST\_EXT.1.1

***Proposed change***

Delete following text from Application Note and Evaluation Activity.

*Application Note*

*If a BAF is selected in FIA\_UAU.5.1, keying material also refers to
source biometric data (i.e. fingerprint), enrollment and authentication
templates, the features an algorithm uses to perform biometric
authentication for enrollment or verification (i.e. location of
minutia), threshold values used in making the match adjudication,
intermediate calculations generated while building an enrollment or
authentication template (i.e. direction maps, minutia counts, binarized
and skeletonized representations of friction ridge patterns, etc.), and
final match scores. Any images or metadata identifying the user for
authentication shall be stored encrypted.*

*Evaluation Activity*

*For each For each BAF selected in FIA_UAU.5.1: 
The evaluator shall determine that the TSS
also contains a description of the activities that happen on biometric
authentication, relating to the decryption of DEKs,
stored keys, and data. In addition how the system ensures that the
biometric keying material is not stored unencrypted in persistent
storage.*

***Rationale***

The above requirement is covered by the cPP. The cPP requires the TOE
not to store any plaintext biometric data, especially templates, outside
the SEE. “outside the SEE” is any storage where any software (e.g. rich
OS) in non-secure world can get access to. If the TOE stores plaintext
biometric data outside the SEE, the TOE must encrypt it first before
storing it in the storage outside the SEE, even if the storage is
encrypted as required by FDP\_DAR\_EXT in \[MDFPP\]

The SD will define corresponding evaluation activity to require
evaluators to examine, for example;

-   where biometric template is stored

-   biometric template is encrypted within the SEE and then stored
    outside the SEE

The cPP assumes that template is encrypted with FEK which is unique to
each file as required by \[MDFPP\], which means that copying template
from another device does not work.

### 14) FPT\_KST\_EXT.2.1

***Proposed change***

Delete the following text in Application Note.

*If a BAF is selected in FIA\_UAU.5.1, keying material also refers to
source biometric data (i.e. fingerprint), enrollment and authentication
templates, the features an algorithm uses to perform biometric
authentication for enrollment or verification (i.e. location of
minutia), threshold values used in making the match adjudication,
intermediate calculations generated while building an enrollment or
authentication template (i.e. direction maps, minutia counts, binarized
and skeletonized representations of friction ridge patterns), and final
match scores.*

Delete the following text indicated strikethrough in Application Note.

*If “hybrid” is selected in FIA\_UAU.5.1, ~~in addition to the keying
material included for the BAF, mentioned in the previous paragraph,~~
keying material also refers to the PIN/password used as part of the
hybrid authentication.*

Delete the following text in Evaluation Activity

*For each BAF selected in FIA\_UAU.5.1:*

*In performing their review, the evaluator shall determine that the TSS
contains a description of the activities that happen on biometric
authentication, including how any plaintext material, including critical
security parameters and results of biometric algorithms, are protected
and accessed.*

*The evaluator shall ensure that the TSS describes how functions
available in the biometric algorithms ensure that no unencrypted
plaintext material, including critical security parameters and
intermediate results, is transmitted outside the security boundary of
the TOE or to other functions or systems that transmit information
outside the security boundary of the TOE.*

***Rationale***

The above requirement is covered by the cPP. The cPP requires the TOE to
process plaintext biometric data within the SEE and not to transmit any
plaintext biometric data, especially templates, to any other entities.
Some mobile device provides diagnostic function which transmit biometric
data to developer with permission from mobile owner. Such function must
be disabled in the evaluated configuration.

The SD will define corresponding evaluation activity to require
evaluators to examine, for example;

-   any TOE function, especially diagnostic, backup or maintenance
    function, does not transmit biometric data to any other entities
    outside the SEE.

### 15) Appendix B. FDP\_PBA\_EXT.1 and FIA\_BMG\_EXT.1

***Proposed change***

Delete FDP\_PBA\_EXT.1 and FIA\_BMG\_EXT.1 from \[MDFPP\].

***Rationale***

The cPP defines the same requirement.

### 16) Appendix C. FIA\_BMG\_EXT.2-6

***Proposed change***

Delete FIA\_BMG\_EXT.2-6 from \[MDFPP\].

***Rationale***

The cPP defines the alternative requirement. SD will define more
detailed evaluation activity.

### 17) Appendix H. Biometric Derivation and Examples

***Proposed change***

Delete this Appendix from \[MDFPP\].

***Rationale***

The cPP and SD will describe similar guidance.

### 18) Appendix I References

***Proposed change***

Delete the following references from \[MDFPP\]

\[NFIQ1.0\], \[NFIQ2.0\], \[IBPC\], \[ISO19989\], \[ANSI409.1\],
\[NIST\], \[BROWN\]

Add the following two references

\[Bio cPP\] collaborative Protection Profile for Mobile biometric
enrolment and verification - for unlocking the device -, XX-XX-XX

\[Bio SD\] Evaluation Activities for Mobile biometric enrolment and
verification – for unlocking the device – cPP, XX-XX-XX

***Rationale***

The cPP replaces the reference.

## 4. Reference

\[MDFPP\] Protection Profile for Mobile Device Fundamentals, Version:
3.1, 2017-06-16

National Information Assurance Partnership
