Mobile Device Biometric System Use Case

August 3, 2017 (spelling and URL reference update on May 15, 2020)

Background
==========

A Mobile Device is composed of a hardware platform and its system
software. The device typically provides wireless connectivity and may
include software for functions like secure messaging, email, web, VPN
connection, and VoIP (Voice over IP), for access to the network, data
and applications, and for communicating to other Mobile Devices.

A Biometric System is composed of multiple individual components (such
as sensor and matching algorithm) that combine to make a fully
operational system. A biometric system is automated and capable of:

1.  Capturing biometric samples from an end user

2.  Extracting and processing the biometric data from a sample

3.  Generating various templates based on processing of any samples
    during enrollment, and if adaptive, during verification as well

4.  Storing the extracted information in a database on the device (the
    security of this data may be outside the scope of the biometric
    system)

5.  Comparing a captured biometric sample with data contained in one or
    more authentication templates

6.  Deciding how well sample and any template match and indicating
    whether or not a verification of identity has been achieved

A Biometric system running on a mobile device can authenticate a user
based on her biometric characteristics (e.g. fingerprint, iris, face and
finger vein) to unlock devices, initiate financial services and access
cloud services. However, such biometric authentication may introduce new
threats, such as biometric impersonation. This document describes
typical use cases for a mobile device biometric system that will be
considered for Biometric Security cPP development.

When considering mobile devices, any biometric system is reliant on the
device itself to provide overall security of the system (such for
security communications, storage and audit). The review of the mobile
device security is expected to be performed separately, such as through
a Mobile Device Fundamentals (MDF) evaluation.

In many cases, the biometric system is fully integrated into the mobile
device without the need for additional software. It is possible for
third-party vendors (i.e. not the OEM of the device) to provide software
that may integrate with an existing biometric system. It is also
possible for a third-party vendor to use other components (such as a
camera or motion sensors) to create a biometric system separate from one
an integrated one or even on a mobile device which does not include a
built-in biometric system.

Note: The following paragraph is a response to the Nils comment
(*https://github.com/biometricITC/cPP-biometrics/issues/38*). I am not
sure that the here is the right place to insert below paragraph so it
may be moved anywhere in the future.

Generally a mobile device only has a single user and doesn’t support
different level of user-based privileges. However, most mobile devices
support the concept of an administrative role, not through a user
account, but by a system concept of a device administrator (this is
usually some sort of system privilege where-in an application is
provided with special rights on the device). The Administrator role
provides the ability to perform management activities, including setting
the policy by the enterprise on the Mobile Device. This administrator
role is normally acting remotely and could be the Mobile Device
Management (MDM) Administrator acting through an MDM Agent (which is
assigned the administrator role). In the case where the device is not
enrolled in a management system, the user is considered to be the
administrator.

Use Cases
=========

Mobile device itself may be operated in a number of use cases such as
described in the MDF Protection Profile. Biometric system on the device
may also be operated in the same use cases however use cases of
biometric system on the device should be devised separately considering
the purpose of biometric authentication and potential attacks. The
following use cases describe how and why biometric authentication is
supposed to be used. Each use case may require additional configuration
and applications to achieve the desired security. A selection of these
use cases is elaborated below.

Each use case has its own assurance level. Therefore following separate
cPPs are developed for each use case.

Use case 1: XXX cPP

Use case 2: YYY cPP (this document)

Note: The above modification is a response to Nils comment \#40
(https://github.com/biometricITC/cPP-biometrics/issues/40)

**\[USE CASE 1: Mobile device biometric authentication on “unlocked”
device\]**

For enhanced security that is easy to use, mobile devices may implement
biometric authentication on a device once it has been “unlocked”. The
initial unlock is generally done by a PIN/password which is required at
startup (or possibly after some period of time) and after that the user
is able to use a biometric to unlock access to the device. Mobile device
is not supposed to be used for security sensitive services as described
in the use case 2 through biometric authentication.

Main concern of this use case is the biometric performance (i.e. FAR and
FRR) and ensuring access cannot be bypassed. Security assurance for
mobile device itself should be handled through another CC evaluation
(e.g. evaluation based on MDFPP).

.

Note: The above modification is a response to Nils comment \#40
(https://github.com/biometricITC/cPP-biometrics/issues/40)

**\[USE CASE 2: Mobile device biometric authentication for security
sensitive service\]**

Mobile devices may be used for security sensitive service such as
payment transactions and online banking. Authentication may be done by
biometrics for convenience instead of PIN/password.

The requirements for the biometric system focus on the biometric
performance (i.e. FTE, FAR, and FRR and presentation attack. Security
assurance for mobile device itself should be handled through another CC
evaluation (e.g. evaluation based on MDFPP).

The level of assurance would be EAL2 because this use case require more
in depth vulnerability analysis than the use case 1.

The target of this cPP is use case 2.

Note: The above modification is a response to Nils comment \#40
(https://github.com/biometricITC/cPP-biometrics/issues/40)

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

**\[USE CASE 4: General application protection/authorization by
biometric authentication\]**

Many applications have started to be integrated with the biometric
system API framework on the devices and can use the biometric system to
provide some level of authorization, whether to the application itself
or for actions taken within the application. This is specifically not
for payment or device authentication.

The requirements here are generally very basic as the application is
trusting the system completely.

**\[USE CASE 5: Biometric use for external authentication system\]**

The best example of this is the FIDO Alliance where-in the biometric
system of the device is used to verify the local user to the
authenticator (FIDO term). Because this is specifically targeted to
trusted authentication and authorization using the mobile device the
requirements are higher.

In general, these requirements are similar to USE CASE 1 though they
could diverge in terms of the specific FAR/FRR values (or ranges). The
testing here is expected to at least in part be done by a third party
lab (which could be the FIDO certification lab or another as this
specific example) though it could be largely done by the vendor with a
smaller amount done by the lab with appropriate documentation provided
to the lab.

SPD/Security Objectives Considerations
======================================

Common set of assumptions/threats/OSP and security objectives is defined
in the current SPD/Security objectives. SPD/Security objectives for
mobile device biometric authentication will be created referring the
current SPD, after fixing use cases to be considered for cPP
development.

We would like to follow the same procedure to do later tasks like
security requirement development for mobile device biometric
authentication cPP.
