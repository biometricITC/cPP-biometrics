**\[Security Problem Definition\]**

***Threats***

**T.Casual\_Attack **

An attacker may attempt to impersonate as a legitimate user without
being enrolled in the TOE. In order to perform the attack, the attacker
only uses his/her own biometric characteristic (in form of a
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
