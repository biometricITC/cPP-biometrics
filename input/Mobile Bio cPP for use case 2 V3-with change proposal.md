Note for iTC members:

This draft SPD is created for use case 2. Development for draft SPD for
use case 1 is underway (Separate cPP should be developed for use case 1
and use case 2 because assurance level is different between use case 1
(EAL1) and 2 (EAL2)).

The TOE is biometric system running on mobile device. It is assumed that
Mobile device is evaluated at EAL2 or higher based on another PP
(However currently there is no such EAL2 PP for mobile device). Mobile
bio cPP should focus on the biometric issues like PAD and performance.

This note in yellow will be removed from final document.

Assumed use case for this SPD:

**\[USE CASE 2: Mobile device biometric authentication for security
sensitive service\]**

Mobile devices may be used for security sensitive service such as
payment transactions and online banking. Authentication may be done by
biometrics for convenience instead of PIN/password.

The requirements for the biometric system focus on the FTE/FAR/FRR and
presentation attack as the security of the biometric system is assumed
to be handled by the device itself. Independent testing of the
FTE/FAR/FRR shall be required with small number of test subjects.

The level of assurance would be EAL2 because this use case require more
in depth vulnerability analysis than the use case 1.

**\[USE CASE 3: Mobile devices biometric authentication for security
sensitive service at various environments\]**

This use case is the same as use case 2 except this one consider
mobility aspect of mobile device. Biometric authentication may be
conducted at various environment but performance may vary depending on
environmental condition (e.g. Capturing vein pattern is sensitive to the
surrounding light condition. Performance measured in the dark room and
normal light condition may be different). This use case evaluates
performance at several different environments.

The level of assurance would be EAL2. Evaluator needs to conduct
independent evaluator testing for performance at various environments.

**\[Security Problem Definition\]**

**Threats**

**T.Casual\_Attack **

(Original text in the integrated cPP)

An attacker may attempt to impersonated as a legitimate user without
being enrolled in the system themselves. In order to perform the attack,
the attacker only uses their own biometric characteristic (in form of a
zero-effort-attack)

(Proposed text for use case 2 mobile biometrics cPP)

An attacker may attempt to impersonate as a legitimate user without
being enrolled in the TOE. In order to perform the attack, the attacker
only uses his/her own biometric characteristic (in form of a
zero-effort-attack)

*Rational*

Editorial changes marked in green

**T.PA\_Enrolment **

(Original text in the integrated cPP)

An attacker may attempt to get impersonated as another user during
enrolment. In order to perform the attack, the attacker uses artificial
biometric characteristics, carrying the biometric characteristic of the
attacked user (as so called Presentation Attack)

(Proposed text for use case 2 mobile biometrics cPP)

This threat isn’t necessary for mobile bio cPP

*Rational*

This threat should be merged to T.PA\_Verification (see also
[*https://github.com/nils-tekampe/cPP-biometrics/issues/27*](https://github.com/nils-tekampe/cPP-biometrics/issues/27)
,
[*https://github.com/nils-tekampe/cPP-biometrics/issues/24*](https://github.com/nils-tekampe/cPP-biometrics/issues/24),
and https://github.com/nils-tekampe/cPP-biometrics/issues/20

**T.PA\_Verification**

(This threat is missing in the integrated cPP but should be there)

An attacker may attempt to get impersonated (during verification
process) as a legitimate user without being enrolled in the system
themselves. In order to perform the attack, the attacker uses artificial
biometric characteristics, carrying the biometric characteristic of the
attacked user (as so called Presentation Attack)

(Proposed text for use case 2 mobile biometrics cPP)

**T.Presentation\_attack**

An attacker may attempt a presentation attack to the TOE. In order to
perform the attack, the attacker uses any Presentation Attack Instrument
(PAI) except their own biometric characteristic.

Note: Acquisition of biometric characteristic may be cooperative or
non-cooperative.

*Rational*

1)  Presentation attack to enrollment should be optional

> See
> [*https://github.com/nils-tekampe/cPP-biometrics/issues/27*](https://github.com/nils-tekampe/cPP-biometrics/issues/27)

1)  Replace “artificial biometric characteristics” with “presentation
    attack instruments”

> Presentation attack is defined as “presentation to the biometric data
> capture subsystem with the goal of interfering with the operation of
> the biometric system” in ISO/IEC 30107-3 and “The object or
> characteristic used in a presentation attack is a presentation attack
> instrument (PAI)” as defined in ISO/IEC 30107-1. PAI can include
> artificial, human and other natural object as described in the
> following figure and table.
>
> ![](media/image1.emf){width="5.905555555555556in"
> height="1.4701388888888889in"}
>
> ![](media/image2.emf){width="5.905555555555556in"
> height="2.3354166666666667in"}
>
> Presentation attack should not be limited to artificial one because
> the cPP should be modality independent and for example, animal or
> plant based object which is not categorized to artificial one can be
> used for presentation attack to finger vein authentication.
>
> However PAI can be variety of objects including severed finger that
> can’t be used for CC evaluation. cPP needs to define an assurance
> activity that instructs evaluator what type of PAI should be
> considered. We can discuss this later during creating SFRs and related
> assurance activities.
>
> This is related to issue \#3
> ([*https://github.com/nils-tekampe/cPP-biometrics/issues/3*](https://github.com/nils-tekampe/cPP-biometrics/issues/3))

1)  Remove “carrying the biometric characteristic of the attacked user
    (as so called Presentation Attack)”

> Attacker may create masterprints without “carrying the biometric
> characteristic of the attacked user” (\*1). It’s not certain that such
> attack should be considered in the assurance activity for this cPP but
> we can discuss this later.
>
> \*1)[*https://www.nytimes.com/2017/04/10/technology/fingerprint-security-smartphones-apple-google-samsung.html*](https://www.nytimes.com/2017/04/10/technology/fingerprint-security-smartphones-apple-google-samsung.html)

1)  Add note for acquisition of biometric characteristic

> According to the ISO/IEC 30107-3, “Attackers may acquire a capture
> subject’s biometric characteristic directly from the capture subject.
> Such acquisition may be cooperative (e.g. the capture subject provides
> a fingerprint to a sensor) or non-cooperative (the capture subject
> leaves a fingerprint on a glass or a biometric capture device allowing
> the attacker to lift the fingerprint)”. T.PA\_Verification should
> cover both cooperative and non-cooperative acquisition. See more info
> in “4.5.8 Access to Biometrics characteristics” in BEAT project report
> ([*https://www.beat-eu.org/project/deliverables-public/d6-5-toward-common-criteria-evaluations-of-biometric-systems*](https://www.beat-eu.org/project/deliverables-public/d6-5-toward-common-criteria-evaluations-of-biometric-systems)).

**T.General**

(Original text in the integrated cPP)

An attacker can carry out any kind of logical or physical attacks that
do not exceed the attack potential and that are compliant with
A.Environment as defined in the cPP in order to disguise his/her own
identity during the enrolment or verification process or for the sake of
impersonation. More specifically, an attacker may try to modify TSF data
(e.g. settings for the biometric verification process) in order to
impact the normal operation of the TOE.

(Proposed text for use case 2 mobile biometrics cPP)

An attacker may attempt to access the biometric data through external
hardware ports, through mobile device user interface, and also through
direct and possibly destructive access to the device, in order to
facilitate the attack to the TOE.

Note:

This threat covers several scenarios including:

- An attacker may root the mobile device and attempt to access biometric
data in memory and file system of mobile device

*Rational*

1)  A.Environment contradicts the mobile use case (See
    [*https://github.com/nils-tekampe/cPP-biometrics/issues/17*](https://github.com/nils-tekampe/cPP-biometrics/issues/17))

> Mobile device can be stolen or lost and attacker can conduct any kind
> of attack to the devices.

1)  Attack to the enrolment should be optional (see
    [*https://github.com/nils-tekampe/cPP-biometrics/issues/27*](https://github.com/nils-tekampe/cPP-biometrics/issues/27))

2)  This threat may lead to the following requirements that will be
    described later in the cPP as form of SFR.

-   Biometric authentication should be done within a secure location
    (e.g. TEE if the TOE is fully integrated into the mobile device) or
    anti-tamper mechanism should be implemented in the TOE (e.g. in case
    of 3^rd^ party biometric authentication software)

-   Biometric data (like template) in the file system should be
    encrypted.

-   Biometric data such as the threshold values must be destroyed when
    no longer needed

See also
[*https://github.com/nils-tekampe/cPP-biometrics/issues/21*](https://github.com/nils-tekampe/cPP-biometrics/issues/21)

**T.Residual**

(Original text in the integrated cPP)

An attacker may try to take advantage of unprotected residual security
relevant data (e.g. biometric data and settings) during a user's session
or from a previous, already authenticated user. In this way the attacker
tries to get access to the security relevant settings of the TOE. This
threat covers several scenarios including: - An attacker takes advantage
of the verification memory content (e.g. by reading the memory content,
cache or relevant temporary data) using a flaw in a user visible
interface of the TOE. - An attacker may take advantage of residual
images at the capture device. These are likely to be limited to cases
where physical contact with the biometric capture device is necessary
for the biometric modality (e.g. fingerprints)

(Proposed text for this cPP)

This threat is merged to T.General

*Rational*

It seems that T.Residual and T.General is overlapped.

**T.Roles**

(Original text in the integrated cPP)

An enrolled and authenticated user may try to exceed their privileges.
This specifically addresses the cases where an authorized user tries to
get administrator privileges in order to modify TSF data.

(Proposed text for this cPP)

This threat isn’t necessary for Mobile bio cPP

*Rational*

See
[*https://github.com/nils-tekampe/cPP-biometrics/issues/22*](https://github.com/nils-tekampe/cPP-biometrics/issues/22)

[*https://github.com/nils-tekampe/cPP-biometrics/issues/26*](https://github.com/nils-tekampe/cPP-biometrics/issues/26)

**Assumptions**

**A.Admin**

(Original text in the integrated cPP)

It is assumed that the administrator of the TOE is well trained and
non-hostile. Non-hostile specifically means that the administrator does
not become an attacker nor does the administrator give relevant
information to attackers. The administrator is responsible to accompany
the TOE installation and oversees the system requirements regarding the
TOE as well as the TOE settings and requirements.

(Proposed text for this cPP)

**A.User**

It is assumed that the user configures the device correctly in a manner
to ensure that the TOE security policies will be enforced.

*Rational*

See
[*https://github.com/nils-tekampe/cPP-biometrics/issues/16*](https://github.com/nils-tekampe/cPP-biometrics/issues/16)

[*https://github.com/nils-tekampe/cPP-biometrics/issues/19*](https://github.com/nils-tekampe/cPP-biometrics/issues/19)

There should be no assumption for an admin for mobile however user
should at least configure and use the TOE correctly.

**A.Environment **

(Original text in the integrated cPP)

The TOE is assumed to be used in a semi-controlled and observable
environment (i.e. attacks that require extensive time or extensive
access to the TOE or the use of complex tools (in the sense of
conspicuous tools) are considered impractical during exploitation
phase). This assumption also includes the protection of any parameters
used by the TOE.

(Proposed text for this cPP)

This assumption isn’t necessary for mobile bio cPP

*Rational*

See
[*https://github.com/nils-tekampe/cPP-biometrics/issues/17*](https://github.com/nils-tekampe/cPP-biometrics/issues/17)

Mobile device can be stolen and physically attacked. Such threat is
covered by T.General.

**A.Comm**

(Original text in the integrated cPP)

It is assumed that the communication between the components of the
biometric product is adequately protected against manipulation and
eavesdropping of information.

(Proposed text for this cPP)

This assumption isn’t necessary for mobile bio cPP

*Rational*

Attacker can try any attack within his/her attack potential. Attack to
the communication (e.g. communication between matching algorism and
capture device) should also be considered under T.General. However such
physical attacks may be considered during the mobile device evaluations
such as ones with MDFPP if possible.

**A.Fallback**

(Original text in the integrated cPP)

It is assumed that a fall-back mechanism as a complement to the TOE is
available that reaches at least the same level of security as the
biometric verification system does. This fall-back system is used in
cases where an authorized user is rejected by the biometric verification
system (False Rejection).

(Proposed text for this cPP)

It is assumed that a fall-back authentication mechanism as a complement
to the TOE is available. This fall-back authentication mechanism can be
used in cases where a user is rejected by the biometric verification
system (False Rejection).

*Rational*

Meaning of “the same level of security as the biometric verification
system does” is not clear and should be removed.

**Organizational Security Policies**

**OSP.ENROL**

(Original text in the integrated cPP)

The TOE shall implement the functionality to enrol users. The TOE shall
ensure that enrolment records are of sufficient quality in order to meet
the requirements on recognition performance. Start of Enrolment shall
only be possible after authorization of an authorized administrator.

(Proposed text for this cPP)

The TOE shall enrol users for biometric verification, only after
successful authentication of a user. The TOE shall ensure that enrolment
templates are of sufficient quality in order to meet the requirements on
recognition performance.

*Rational*

In case of mobile, there is no admin. So no authorization by admin isn’t
necessary however user should be authenticated with password before
stating enrollment.

**OSP.Verifcation\_Error**

(Original text in the integrated cPP)

The TOE shall meet relevant criteria for its security relevant error
rates for biometric verification (e.g. False Accept Rate (FAR) and False
Rejection Rate (FRR)).

(Proposed text for this cPP)

The TOE shall meet relevant criteria for its security relevant error
rates for biometric verification

*Rational*

(e.g. False Accept Rate (FAR) and False Rejection Rate (FRR)) is deleted
because, for use case 1, FAR and FRR should be evaluated but for use
case 2 FAR, FRR and FTE should be evaluated but I want to share the same
OSP between the two cPP.

**OSP.PAD\_Error**

(Original text in the integrated cPP)

The TOE shall meet relevant criteria for its security relevant error
rates for PAD.

(Proposed text for this cPP)

Same as above

*Rational*

See
[*https://github.com/nils-tekampe/cPP-biometrics/issues/25*](https://github.com/nils-tekampe/cPP-biometrics/issues/25)

Mobile device can be stolen or lost and attacker can conduct any kind of
attack to the device including presentation attack.

However assurance activity in cPP or supporting doc should defines type
of PAI to be tested and test scenario etc and clear criteria on which
evaluators can make a PASS/FAIL decision so that make it possible for
evaluator to conduct repeatable and objective evaluations.

**OSP.TrialLimit**

(Original text in the integrated cPP)

Impostors must be prevented from gaining access to the protected
services by making repeated verification attempts using one or more
claimed user IDs. Therefore the TOE in cooperation with its environment
shall be able to limit the maximum number of unsuccessful verification
attempts.

(Proposed text for this cPP)

Impostors must be prevented from gaining access to the protected
services by making repeated verification attempts using one or more
claimed user IDs.

*Rational*

See https://github.com/nils-tekampe/cPP-biometrics/issues/23

This OSP can be satisfied by the TOE environment (e.g. Mobile device)
and TOE (biometric system) may not need to implement this function.

**OSP.Audit**

(Original text in the integrated cPP)

In order to generate statistics that can be used to adjust the
parameters for better quality (maintenance)

trace modification and

trace possible attacks

the TOE shall generate security-relevant audit events.

(Proposed text for this cPP)

OSP.Audit

The TOE shall record security-relevant audit events so that user can
view user or TOE activity.

*Rational*

It’s uncertain that which event should be logged for the mobile use
case. We will re-visit to this issue when we will develop FAU\_GEN.

**OSP.Residual**

(Original text in the integrated cPP)

The TOE shall erase all residual security-relevant data once they are
redundant.. This specifically includes (but is not limited to) all
information left after enrolment, verification or PAD processing.

(Proposed text for this cPP)

This OSP isn’t necessary for Mobile Bio cPP

*Rational*

This OSP is covered by T.General.

**\[Security Objectives\]**

***Security Objectives for the TOE***

**O.BIO\_VERIFICATION**

(Original text in the integrated cPP)

The TOE shall provide a biometric verification mechanism to ensure
access to a portal with an adequate reliability. The TOE shall meet
relevant criteria for its security relevant error rates for biometric
verification (e.g. False Accept Rate (FAR) and False Rejection Rate
(FRR)). An “Exact match” should not be counted as a positive
verification as it may be a replay attempt.

(Proposed text for this cPP)

The TOE shall provide a biometric verification mechanism to control
access to the protected services with an adequate reliability. The TOE
shall meet relevant criteria for its security relevant error rates for
biometric verification.

*Rational*

“Exact match” should be removed. Attacker can get a fingerprint image
stored in the file in some mobile device (see such example in
[*https://www.blackhat.com/docs/us-15/materials/us-15-Zhang-Fingerprints-On-Mobile-Devices-Abusing-And-Leaking-wp.pdf*](https://www.blackhat.com/docs/us-15/materials/us-15-Zhang-Fingerprints-On-Mobile-Devices-Abusing-And-Leaking-wp.pdf))
and attacker can send this image to the matching algorithm to bypass the
verification. Such attack can be rejected by the TOE if the TOE
implements this “Exact match” mechanism. However attacker can easily
change the image slightly and bypass the verification because format of
fingerprint image is so simple. In this attack scenario,“Exact match”
mechanism may be useless.

Objective should be implementation independent and should not include
any specific mechanism. Developer should be able to select any security
mechanism to successfully meet the TOE objective.

**O.PAD\_ENROL**

(Original text in the integrated cPP)

The TOE shall prevent an attacker facilitating a presentation attack
from being successfully enrolled,

(Proposed text for this cPP)

This Objective is not necessary for this mobile cPP

*Rational*

Attack to the enrolment should be optional.

**O.PAD\_VERIFICATION**

(Original text in the integrated cPP)

The TOE shall prevent an attacker facilitating a presentation attack
from being successfully verified.

(Proposed text for this cPP)

**O.Presentation\_attack\_detection**

The TOE shall prevent a presentation attack using Presentation Attack
Instrument (PAI). The TOE shall meet relevant criteria for its security
relevant error rates for PAD

*Rational*

O.PAD\_ERROR is merged with this objective to be consistent with
O.BIO\_VERIFICATION

**O.AUDIT**

(Original text in the integrated cPP)

The TOE shall report or record

A use of the biometric and the PAD functionality of the TOE and its
result

Every use of a management function All parameters modified by the
management functions

(Proposed text for this cPP)

The TOE shall record security-relevant audit events so that user can
view user or TOE activity.

*Rational*

See OSP.Audit

**O.ENROL**

(Original text in the integrated cPP)

The TOE shall implement the functionality to enrol users. The TOE shall
ensure that enrolment records are of sufficient quality in order to meet
the requirements on recognition performance. The TOE shall ensure that
start of Enrolment shall only be possible after authorization by an
administrator.

(Proposed text for this cPP)

The TOE shall implement the functionality to enrol users for biometric
verification. The TOE shall check the quality of enrolment templates in
order to meet the requirements on recognition performance. The TOE shall
authenticate users before starting the enrolment.

*Rational*

Make some editorial changes to make evaluator’s job easy.

**O.RESIDUAL**

(Original text in the integrated cPP)

The TOE shall ensure that no residual or unprotected security relevant
data remain in memory or on any sensor after operations are completed.

(Proposed text for this cPP)

This objective is not necessary for the mobile bio cPP

*Rational*

This objective is merged with O.PROTECTION

**O.MANAGEMENT**

The TOE shall provide the necessary management functionality for the
modification of security relevant parameters to TOE administrators only.
As part of this management functionality the TOE shall only accept
secure values for security relevant parameters to ensure the correct
operation of the TOE.

(Proposed text for this cPP)

This objective is not necessary for this mobile bio cPP.

*Rational*

There is no admin for the mobile bio use case. However user can enable
or disable the biometric verification after successfully authenticated.
Such SFR will be included in the final cPP however specific objective
for management functions aren’t necessary (Please see ISO/IEC 15446
12.3.1 How should security functional requirements be selected?)

**O.PAD\_ERROR**

(Original text in the integrated cPP)

The TOE shall meet relevant criteria for its security relevant error
rates for PAD

(Proposed text for this cPP)

This objective is merged with O.Presentation\_attack\_detection

*Rational*

See O.Presentation\_attack\_detection

**O.PROTECTION**

(Original text in the integrated cPP)

The TOE in cooperation with its immediate environment shall provide an
adequate level of logical and physical protection in order to ensure the
correct operation of the TOE. This specifically concerns the enrolment
and verification process. Impostors must be prevented from gaining
access to the portal by making repeated verification attempts using one
or more claimed user IDs. Therefore the TOE in cooperation with its
environment shall be able to limit the maximum number of unsuccessful
verification attempts. Also, the TOE ‑ in cooperation with its
environment ‑ shall ensure that any TSF data is adequately protected.

(Proposed text for this cPP)

**O.PROTECTION**

The TOE in cooperation with its environment shall ensure that biometric
data is adequately protected.

Note: Biometric data can be stored in the filesystem and resided in the
memory. All such data shall be protected from unauthorized access or
deleted after its use.

**OE.TrialLimit**

The TOE environment shall be able to limit the maximum number of
unsuccessful verification attempts.

*Rational*

O.PROTECTION should be divided into the above two objective to make it
easy to maintain.
