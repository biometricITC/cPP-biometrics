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

A.1.  Requirements for the test document

The developer shall provide the test document for CC evaluations that
claim a conform to \[BScPP\]. This section defines required content of
the test document that is inputted to the EA for FIA\_MBV\_EXT.1.

A.2.  Summary of contents

Table-A1 shows items that shall be reported in the test document. Name
or structure of test document doesn’t need to follow Table-A1. However,
all items in Table-A1 shall be written somewhere in the test document.
Also, if some items are not included in the test document, the developer
shall provide a rationale for such exclusion to the evaluator.

  |Section|Item|
  |-------|----------------------------|
  |A.3.1|Overview of the performance testing|
  |A.3.2|Target application and influential factors|
  |A.3.3|Test subject selection|
  |A.3.4|Test instructions and training|
  |A.3.5|Test subject management|
  |A.3.6|Test procedure|

Table-A1: Reporting items

A.3.  Reporting items description

This section describes each item in Table-A1 in detail. All items are
created based on ISO/IEC 19795-1 and 19795-2 however some of them are
modified to adjust to the CC evaluation.

A.3.1 Overview of the performance testing

The developer shall report following general information about the
performance testing.

\(1) Performance test configuration

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

\(2) Result of the performance testing

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
clearly define what constitutes the transaction based on expected user
behaviour and the same rule shall be applied consistently throughout
the performance testing.

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

A.3.2 Target application and influential factors

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
finger/hand vein verification. The developer can define these factors
arbitrarily. However, it’s recommended to control all influential
factors appropriately because different error rates may be measured
under different influential factors.

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

A.3.3 Test subject selection

Following information about test subject for the testing shall be
reported.

1.Selection method of test subject

Selection method shall be reported (e.g. gather test subjects from
developer’s employees or recruit them from public).

2.Use of artificially generated sample or features data

The use of artificially generated data, if any, shall be reported. The
numbers of test subjects, body parts and samples derived from
artificially generated images or feature data along with the rationale
for using artificial data shall be provided.

A.3.4 Test instructions and training

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

A.3.5 Test subject management

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

A.3.6 Test procedure

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

B.1. Recommendations

1.Scenario of mobile biometric verification

The user may use the mobile biometric verification in a different way.
Suppose the mobile device provides both Password Authentication Factor
and BAF and user can use either of factor to unlock the device. One user
may try to unlock the device with BAF until maximum number of
unsuccessful authentication attempts is exceeded. Another user may try
to unlock the device with BAF only three times and switch to the
password if all three attempts were failed. However, it’s not possible
to evaluate all of these scenarios and the developer shall assume only
one typical usage scenario of the verification and conduct performance
testing following such scenario consistently.

For example, if the mobile face verification becomes unavailable after
the five successive failed attempts, the developer may assume that the
user tries five face unlock attempts in succession. In this case, the
developer shall define that the verification transaction is consisted up
to five unlock attempts and only one verification transaction can be run
by each user.

Another example is if the mobile iris verification becomes unavailable
after the five successive failed attempts, the developer may assume that
the user tries mobile iris verification with right iris for the first
three attempts and switch to the left iris for the last two attempts if
all first three attempts were failed. The developer shall define the
verification transaction is consisted of three right iris unlock and two
left iris unlock attempts, and only one verification transaction can be
run by each user.

2.Maximum number of templates

Only one template can be generated from each body part (e.g. right iris,
left hand index finger or face) and used for the performance testing.

Quality of template may have significant impact on the mobile biometric
verification performance. This \[SD\] assumes that the user is familiar
with the mobile devices operation and enroll his/herself correctly. The
test subject may make enough number of practice attempts to get familiar
with the device operation before the final enrollment transaction.

3.Maximum number of samples per test subject

The developer shall define the maximum number of samples per test
subject following the scenario however, only up to 5 samples can be
captured at maximum from one test subject because allowing to capture
too much samples per test subject may decrease test independence and
FMR/FNMR will be significantly underestimated.

For example, the developer may capture 3 samples from right iris and 2
ones from left iris from each test subject, or 5 samples from either of
right or left iris to conduct the performance testing.

4.Maximum number of transaction per test subject

Only one transaction can be run by each test user because the mobile
device locks the mobile biometric verification as required by \[MDFPP\]
after the certain number of attempts are failed.

5.Statistical certainty for FAR/FMR

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
sample and user B’s template separately.

This \[SD\] doesn’t allow intra-individual comparison that is a
comparison between one body part and another body part of the same test
subject (e.g. comparison between right and left iris of the same user).

6.Statistical certainty for FRR/FNMR

Rule of 3 requires no error occurred for all attempts/transactions and
rule of 30 may require too many attempts/transactions if the FNMR/FRR is
quite low. Therefore, the developer may calculate FNMR/FRR directly from
the result of performance testing without considering the statistical
confidence.

B.2. Example – iris verification

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
