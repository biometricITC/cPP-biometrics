**Draft Security Functional Requirements (SFR)**

To iTC members: The following are initial draft SFRs for mobile use case
1 and 2. SFRs come from WD ISO/IEC 19989-1 with modifications (modified
requirements are written in red) and MDFPP if there is no relevant SFRs
defined in the 19989-1.

\[Mandatory req\] means that mandatory for both use case 1 and 2

\[Optional req\] means that optional for use case 1 but (probably)
mandatory for use case 2

\[Assurance activity\] I add URL for MDFPP assurance activities (except
FIA\_BVR.2. I add new activity to this SFR). These initial assurance
activities will be updated based on comments from iTC members.

Please look at SFR and Assurance activity first because this is all
evaluator has to do during the CC evaluation. TOE security objectives
should be updated to adjust to the SFRs. I will submit such change
proposals through issues on Github.

**SFRs for O.BIO\_VERIFICATION**

**O.BIO\_VERIFICATION**

The TOE shall provide a biometric verification mechanism to control
access to the protected services with an adequate reliability. The TOE
shall meet relevant criteria for its security relevant error rates for
biometric verification.

**\[Mandatory req\]**

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

Note:

Whether or not the TOE meet the “defined value” shall be evaluated based
on established and internationally recognized method. For example,
ISO/IEC 19795 defines statistical method to estimate the performance
matrices and the “defined value” shall be equal or higher than 95% upper
confidence interval limit calculated from result of developer’s
performance testing.

Note for use case 1:

This use case is assumed to be evaluated with MDFPP.

If a BAF (Biometric Authentication Factor) is selected in FIA\_UAU.5.1
in the MDFPP, then FIA\_BVR.2 can be selected instead of
FIA\_BMG\_EXT.1.

**\[Assurance activity for FIA\_BMG\_EXT.1\]**

http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html\#FIA\_BMG\_EXT.1.1

I propose to replace above activities with new one that is described in
Evaluation Guidance for Biometric Verification Products V1.doc. This
document defines assurance activities for use case 2. Some of them will
be removed from use case 1 activities.

**SFRs for O.Presentation\_Attack\_Detection**

**O.Presentation\_Attack\_Detection**

The TOE shall prevent a presentation attack using Presentation Attack
Instrument (PAI). The TOE shall meet relevant criteria for its security
relevant error rates for PAD

**\[Mandatory req\]**

**FIA\_BVR.4 Biometric verification not accepting presentation attack
instruments**

**FIA\_BVR.4.1** The TSF shall prevent presentation of biometric
characteristics, which result in biometric samples of low quality, from
being successful in the biometric verification.

**FIA\_BVR.4.2\_EXT** The TSF shall perform testing to detect artificial
presentation attack instruments during the biometric verification.

**\[Optional req\]**

**FIA\_EBR.1.2\_EXT** The TSF shall perform testing to detect artificial
presentation attack instruments during the enrolment.

Note for use case 1:

This use case is assumed to be evaluated with MDFPP.

If a BAF (Biometric Authentication Factor) is selected in FIA\_UAU.5.1
in the MDFPP, then FIA\_BVR.4 can be selected instead of
FIA\_BMG\_EXT.6.

**\[Assurance activity for FIA\_BMG\_EXT.6\]**

http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html\#FIA\_BMG\_EXT.6.1

**SFRs for O.AUDIT**

**O.AUDIT**

The TOE shall record security-relevant audit events so that user can
view user or TOE activity.

**\[Optional req\]**

**FAU\_GEN.1 Audit data generation**

**FAU\_GEN.1.1** The TSF shall be able to generate an audit record of
the following auditable events:

a\) Start-up and shutdown of the audit functions;

b\) All auditable events for the \[not specified\] level of audit; and

c\) Unsuccessful use of the authentication mechanism and \[assignment:
other specifically defined auditable events\].

**FAU\_GEN.1.2** The TSF shall record within each audit record at least
the following information:

a\) Date and time of the event, type of event, subject identity (if
applicable), and the outcome (success or failure) of the event; and

b\) For each audit event type, based on the auditable event definitions
of the functional components included in the PP/ST, \[assignment: other
audit relevant information\].

**\[Assurance activity for FAU\_GEN.1\]**

http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html\#FAU\_GEN.1.1

**SFRs for O.ENROL**

**O.ENROL**

The TOE shall implement the functionality to enrol users for biometric
authentication, only after successful authentication of a user. The TOE
shall check the quality of enrolment templates in order to meet the
requirements on recognition performance.

**\[Mandatory req\]**

**FIA\_EBR.1 Check of biometric samples for enrolment **

**FIA\_EBR.1.1** The TSF shall prevent use of biometric characteristics
of low quality for enrolment that has been presented by any user of the
TSF.

**\[Optional req\]**

**FIA\_EBR.2 Biometric enrolment with low failure to enrol rate**

**FIA\_EBR.2.1** The TSF shall provide a mechanism to enrol biometric
data with the FTE not exceeding \[assignment: defined value\].

Note for use case 1:

This use case is assumed to be evaluated with MDFPP.

If a BAF (Biometric Authentication Factor) is selected in FIA\_UAU.5.1
in the MDFPP, then FIA\_EBR.1 can be selected instead of
FIA\_BMG\_EXT.2.

**\[Assurance activity for FIA\_BMG\_EXT.2\]**

http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html\#FIA\_BMG\_EXT.2.1

**SFRs for O.PROTECTION**

**O.PROTECTION**

The TOE in cooperation with its environment shall ensure that biometric
data is adequately protected.

Note: Biometric data can be stored in the filesystem and resided in the
memory. All such data shall be protected from unauthorized access or
deleted after its use.

**\[Optional req\]**

**FPT\_XXX\_XXX.1.1** The TSF shall protect \[assignment: biometric
data\] by

\[selection:

-   not storing any plaintext data in readable non-volatile memory

-   not transmitting any plaintext data outside the security boundary of
    the TOE

-   destroying all plaintext data when no longer needed

-   protecting the template \[selection: using a PIN as an additional
    factor, using a password as an additional factor, \[assignment:
    other circumstances\]\]

-   \[assignment: other methods\]

\].

Note for use case 1:

This use case is assumed to be evaluated with MDFPP.

MDFPP has already defined above requirements in FPT\_KST\_EXT.1,
FPT\_KST\_EXT.2, FCS\_CKM\_EXT.4 and FDP\_PBA\_EXT.1 to protect
biometric data. So there is no need to define SFRs for use case 1 cPP.

**\[Assurance activity for FPT\_KST\_EXT.1, FPT\_KST\_EXT.2,
FCS\_CKM\_EXT.4 and FDP\_PBA\_EXT.1\]**

http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html\#FPT\_KST\_EXT.1.1

http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html\#FPT\_KST\_EXT.2.1

http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html\#FCS\_CKM\_EXT.4.2

http://common-criteria.rhcloud.com/mobile-device/output/mobile-device-release.html\#FDP\_PBA\_EXT.1\_sel-based\_
