# Change proposal to \[GPOSPP\]

## 1. Boundary between the TOE and Operating System

See Annex A in our cPP. This Annex explains relation between SFRs in \[GPOSPP\] and our cPP that sets a clear boundary between the operating system and the biometric system (TOE in our cPP). This document explains what modification should be done to \[GPOSPP\] so that the operating system can be evaluated based on both \[GPOSPP\] and our cPP at the same time without any conflict.

## 2. Procedure to evaluate the operating system based on \[GPOSPP\] and the cPP

\[GPOSPP\] and our cPP are separate PPs and developer must make a conformance claim to both \[GPOSPP\] and our cPP. Developer must select the same biometric modalities in FIA\_UAU.5.1 in \[GPOSPP\] and FIA\_MBV\_EXT.1 in our cPP.

Developer doesn’t need to prepare separate document such as AGD guidnace for both evaluations if document satisfy requirements defined in both \[GPOSPP\] and cPP/SD.

## 3. Change proposal

This section lists the change proposals to \[GPOSPP\] from the Biometric Security iTC.

### 1) 1.3.1 TOE Boundary

***Proposed change***

Add the following text at the end of section

*Biometric system is out of scope of the TOE. If the operating sytem supports biometric authentication, the biometric system shall comply with \[Bio cPP\].*

***Rationale***

Biometric system is the TOE for the cPP. \[GPOSPP\] shall excludes the biometric system from the TOE scope and biometric system shall complied with the cPP endorsed by the CCRA.

### 2) 1.3.2 TOE Platform

***Proposed change***

Add following text at the end of section.

*Biometric security is out of the scope of this Protection Profile and should be evaluated separately based on the collaborative Protection Profile for Mobile biometric enrolment and verification - for unlocking the device - \[Bio cPP\]*

***Rationale***

Scope of each PP should be defined.

### 3) 2 Conformance Claims

***Proposed change***

Add the following text at the end of section

*This PP allows conformance claims to it in combination with \[Bio cPP\].*

***Rationale***

This statement is required to use \[GPOSPP\] and the cPP at the same time. See para 30 in Exact Conformance, Selection-Based SFRs, Optional SFRs May 2017.

### 4) FIA\_AFL.1.1

***Proposed change***

Add the following text to the second selection.

*authentication based on biometric template*

Update the Evaluation Activity with the italicized text.

The evaluator will set an administrator-configurable threshold for failed attempts, or note the ST-specified assignment. The evaluator will then (per selection) repeatedly attempt to authenticate with an incorrect password, PIN, *biometric sample* or certificate until the number of attempts reaches the threshold. Note that the authentication attempts and lockouts must also be logged as specified in FAU_GEN.1.

***Rationale***

This adds the biometric as an option for authentication for the operating system.

### 5) FIA\_AFL.1.2

***Proposed change***

Add the following text to the Evaluation Activity.

*Test 4: The evaluator will attempt to authenticate repeatedly to the system with a known bad biometric sample. Once the defined number of failed authentication attempts has been reached the evaluator will ensure that the account that was being used for testing has had the actions detailed in the assignment list above applied to it. The evaluator will ensure that an event has been logged to the security event log detailing that the account has had these actions applied.*

### 6) FIA\_UAU.5.1

***Proposed change***

Add the following text to the selection.

*authentication based on biometric template*

Add the following text to the Evaluation Activity.

*If user name and biometric is selected, the evaluator will configure the OS with a known user name and biometric and conduct the following tests:
Test 1: The evaluator will attempt to authenticate to the OS using the known user name and biometric. The evaluator will ensure that the authentication attempt is successful.
Test 2: The evaluator will attempt to authenticate to the OS using the known user name but an incorrect biometric. The evaluator will ensure that the authentication attempt is unsuccessful.*

***Rationale***

This adds the biometric as an option for authentication for the operating system.

## 4. Reference

\[GPOSPP\] Protection Profile for General Purpose Operating Systems, Version: 4.2, 2018-05-22
National Information Assurance Partnership
