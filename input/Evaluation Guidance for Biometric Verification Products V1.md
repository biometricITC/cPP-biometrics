Evaluation activity for developer’s biometric performance testing

Note to iTC member:

Assurance activity for FIA\_BMG\_EXT.1 requires that “*Adequate
documentation is required to demonstrate that testing was completed to
support the claimed FAR and FRR*” however it’s not clear about what
“*Adequate documentation*” is and similar assurance activity should also
be defined in the mobile bio cPP. So this document aims to clarify the
requirements that “*Adequate documentation*” needs to satisfy and I plan
to include this document into the final mobile bio cPP as Annex.

This document was developed based on a general biometric PP (EAL2) and
accompanying supporting document developed by Japanese national project.
Original document includes guidance for evaluator’s independent testing
which is required for EAL1 and EAL2 but this guidance has not been
translated yet. All part of original document will be included in the
final mobile bio cPP. The same document will be submitted to the ISO/IEC
19989 project as a contribution.

This document is a preliminary draft and will be updated by mid of
September but if you have any comments please let me know.

Some requirements will be removed from assurance activity for use case
1.

This document is intended to be used for ISO/IEC 15408 evaluations for
biometric performance testing and defines requirements for developer’s
biometric performance test document. Developers need to create a test
plan for performance testing, execute the test and report the result of
test based on this document. Evaluators need to verify that the
performance test document satisfies the requirements to make sure that
the result of test is trustworthy.

This document refers following international standards.

ISO/IEC 19795-1:2006 Biometric performance testing and reporting - Part
1: Principles and framework

ISO/IEC 19795-2:2007 Biometric performance testing and reporting - Part
2: Testing methodologies for technology and scenario evaluation

This document doesn’t include all requirements defined in the both
standards. However all requirements are thoroughly vetted to select ones
with modification:

1\) that are actually valuable and attainable for developers

2\) that enable developers to conduct the repeatable and reproducible
performance testing

1. Developer's task

1.1  Overview

Developers shall provide an evidence for biometric performance testing
(hereafter “test document”) for ISO/IEC 15408 evaluations. Test document
normally consists of the following two parts.

(1) Biometric performance test plan: a document created before
    conducting performance testing, which specifies procedures for test
    preparation, execution and analyzing the test result.

(2) Biometric performance test report: a document created after the
    testing, which provides result of performance test conducted based
    on the performance test plan.

This document defines items that shall be described in the test
document.

1.2  Overview of reporting items

Table-1 shows items that should be described in the test document. Name
or structure of test document doesn’t need to follow this document.
Developer’s test plan and report may be documented separately or merged
into one document, and are not required to follow the order shown in
Table-1. However, items defined in this document shall be written
somewhere in the test document. Also, if some items are not included in
the test document, the developer shall provide a rationale for such
exclusion to evaluators.

\(1) Reporting items

The following items shall be reported in the test document.

Table-1: Reporting items

  Paragraph   Item
  ----------- --------------------------------------------
  1.3.1       General information
  
  1.3.2       Target application and influential factors
  
  1.3.3       Test subject selection
  
  1.3.4       Test instructions and training
  
  1.3.5       Test subject management
  
  1.3.6       Test procedure
  
  1.3.7       Result of testing

1.3  Reporting items description

This sub paragraph describes each reporting items in detail. All items
are defined and explained in the ISO/IEC 19795-1 and 19795-2 however
some of them are modified to fit to the ISO/IEC 15408 evaluation.

1.3.1 General information

Developer shall report following general information about the
performance testing.

(1) Performance test configuration

> Test document shall report the following information to uniquely
> identify the test configuration of the performance testing.
> Information stated here shall be consistent with the security target.

1. TOE reference

> Information that uniquely identify the TOE (e.g., product name,
> version, product code)
>
> Note: Modification to the TOE for performance testing, if any, shall
> be reported. The rationale that such modification doesn’t affect the
> TOE performance shall also be provided (e.g. Performance is not
> affected because modified code is executed only after making the
> matching decisions)

2. TOE configuration

> Any configurable parameters or setting of the TOE that may affect the
> performance shall be reported. Value of each parameter set for the
> testing shall also be provided. For example, if threshold (e.g.
> decision threshold and image quality threshold) is configurable by
> users, value of threshold set for the testing shall be reported.

3. TOE operational environment

> Information that uniquely identify any components that are necessary
> to run the TOE (e.g. mobile device and operating system information if
> the TOE is a mobile biometric authentication application running on
> the mobile device).

4. Performance test tools

> Information that uniquely identify any testing tools (e.g. SDK) used
> for the performance testing.

(2) General test information

> Test document shall report the following general information about the
> test. Information stated here shall be consistent with the security
> target.

1. Biometric verification method

> Biometric characteristic and body part used for the TOE and overview
> of the matching method
>
> Note: Whether the TOE returns matching scores or accept/reject
> decisions shall be specified. Description of matching scores shall be
> provided if applicable (e.g., minimum/maximum values). Also, whether
> or not the TOE returns template quality scores or success/failure
> decisions for template creation in the enrolment shall be specified.
> Description of template quality scores shall be provided if
> applicable.

2. Performance matrices

> Performance matrix (e.g. FTE, FAR or FRR) measured

3. Type of performance testing

> Type of performance testing (e.g. technology evaluation or scenario
> evaluation, or both). If both type of testing were conducted, type of
> testing applied to measure each matrix shall be reported.

4. Tester information

> The name and entity of the tester as well as relationships between the
> tester and the developer (independent/dependent) shall be reported.
> While most tests are assumed to be conducted by a developer’s
> employees, some part of testing such as gathering test crew may be
> conducted by another entity.

5. Test period and location

> Period and location of testing shall be reported.

1.3.2 Target application and influential factors

Test document shall specify a target application modeled in the test,
such as biometric verification in an indoor office environment with a
non-habituated crew. Test document shall also report influential factors
that may influence performance and measures to control such factors.
Influential factors can be determined by referring appropriate documents
(e.g. ISO/IEC 19795-3). These factors shall be consistent with the
target application and security target.

The following factors are examples of controlling factors for
finger/hand vein verification.

(1) Test crew demographics

<!-- -->

1.  Age: age distribution ratio by arbitrary age groups (e.g., 1, 5, 10
    years) shall be reported.

2.  Gender: male/female distribution shall be reported.

3.  Ethnic origin: Distribution ratio by ethnic origin shall be
    reported. Category of ethnic origin can be arbitrarily defined by
    developer.

<!-- -->

(2) Posture and positioning

> Posture of test crew or positioning of his/her hand/finger (e.g.
> Orientation of hand/finger in relation to the sensor or distance to
> the sensor) shall be reported. Such information shall be consistent
> with the TOE operational guidance or automated feedback provided by
> the TOE.

(3) Indoor or outdoor

> Indoor or outdoor environment in which testing is to be conducted
> shall be reported. In case of outdoor environment, other factors
> affecting the performance (e.g. environmental illumination) shall also
> be reported.

(4) Temperature

> Range of temperature at which the testing is to be conducted shall be
> reported (e.g. “Testing was conducted in an air-conditioned
> environment where temperature was kept between X and Y degrees”).

(5) Time interval

> Time interval (e.g. minimum, maximum and average time) between
> enrolment and verification shall be reported.

(6) Habituation

> The degree to which the crew is familiarized with the TOE shall be
> reported (e.g. historical frequency of use of the TOE)

1.3.3 Test subject selection

Following information about test subject for the testing shall be
reported.

(1) Number of test subjects and selection method

> Number of test subjects, the body parts captured from each subject
> (e.g. right and left hand for palm vein) and number of samples
> captured from each body part shall be reported. Selection method shall
> also be reported (e.g. gather test subjects from developer’s employees
> or recruit them from public).

(2) Number of test subjects used in the past development or testing

> If templates or biometric data collected for the past developments or
> tests were reused for the testing, numbers of subjects, body parts,
> samples used in the past and selection method for such reused data
> shall be reported. Rationale shall also be provided for reuse of data.

(3) Use of artificially generated sample or features data

> For technology evaluation, the use of artificially generated data, if
> any, shall be reported. The numbers of test subjects, body parts and
> samples derived from artificially generated images or feature data
> along with the rationale for using artificial data shall be provided.

1.3.4 Test instructions and training

Following information about instructions and training for the testing
shall be reported.

(1) Acclimatization

> When a test subject enters a test room from outside for enrolment,
> performance may vary because of large temperature changes. Method of
> subject acclimatization to avoid such effect shall be reported for
> genuine/imposter transaction or biometric data collection.

(2) Test information and general test instructions

> Test information and general test instructions given to test subject
> prior to or after an enrolment, genuine/imposter transactions or
> biometric data collection shall be reported.
>
> Note: Performance testing shall be done in accordance with the
> instruction given by the TOE or TOE operational guidance (i.e. Testing
> shall not be adjusted to the TOE specification that is not described
> in the TOE operational guidance)

(3) Confirmation of habituation

> Method for how to confirm the level of subject habituation prior to an
> enrolment, genuine/imposter transaction or biometric data collection
> shall be reported. If the habituation was confirmed through training,
> method to ensure the consistency of training among test subjects and
> the tools used for training shall be reported.

1.3.5 Test subject management

Following information about test subject management shall be reported.

(1) Management processes

> Biometric data can be corrupted by human error during the collection
> process (e.g. using a middle finger when the index finger is
> required). The test subject management processes to avoid such errors
> shall be reported. Management processes shall cover the following
> processes.

1.  method of initial test subject registration

2.  method of ensuring test subject uniqueness

3.  amount and type of personal data collected

4.  method of avoiding data collection errors (e.g. Use of data
    collection software minimizing the amount of data requiring keyboard
    entry)

1.3.6 Test procedure

A test procedures to measure FTE, FAR and FRR shall be reported. The
following items shall be covered

(1) Type of transaction

> Whether the transaction is executed online or offline shall be
> reported. Online means that enrolment and verification is executed at
> the time of image submission. Offline means that enrolment and
> verification is executed separately from image submission.

(2) Enrolment and transaction flow

> The following shall be reported to explain the flow of enrolment,
> genuine and imposter transaction to measure biometric performance
> (i.e. FTE, FAR and FRR).

1.  quality score threshold to measure performance

2.  details of transaction flow (e.g., flow chart)

3.  maximum duration of transaction

4.  minimum and maximum number of attempts allowed for a transaction

5.  minimum and maximum number of presentations allowed for a
    transaction

6.  minimum number of required samples and maximum number of allowed
    samples for a transaction

> Note: Definition of each enrolment and transaction and success or
> failure of enrolment (i.e. enrolment policy) and transaction shall
> also be specified.

(3) Sample exclusion criteria

> Criteria for sample exclusion shall be reported (i.e. Test operator
> shall not manually discard nor use an automated mechanism to discard
> collected samples unless the samples conform to documented exclusion
> criteria). Number of excluded samples shall be reported. If
> enrollments and transactions are failed because of such excluded
> samples, number of such failed enrollment and transactions shall also
> be reported. These failed enrollment and transactions shall be counted
> as failed enrolment and transaction to calculate the performance
> matrix (See (8) 1 and 2).

(4) Criteria for supervisor intervention

> Criteria for supervisor intervention at the time of each enrolment and
> transaction shall be reported.

(5) Advice or remedial action for a user who fails an enrolment and
    transaction

> Advices or remedial actions to users who fail to complete enrolment
> and transactions or data collections for offline testing shall be
> reported including the following items.

1.  Advices or remedial actions provided

> Note: Advice or actions shall be consistent with that of the target
> application.

2.  Guidance policy shall be reported including

<!-- -->

a)  point(s) in a transaction at which guidance is permitted or required

b)  specific guidance a supervisor is to provide to test subject

c)  aspects of guidance at the discretion of the supervisor, if any.

<!-- -->

(6) Weighting

> If performance are estimated using a weighted proportion, the method
> of weighting shall be specified: e.g., test subjects distribution,
> distribution of the number of executed transactions.

(7) Intra-individual comparisons for imposter transaction

> Whether intra-individual comparisons was made to measure the FAR shall
> be reported. Intra-individual comparisons, if any, shall be fully
> explained in the test document. Intra-individual comparison is a
> comparison between one body part and another body part of the same
> test subject if the test subject has multiple body parts for a
> biometric characteristics (e.g. fingers, hands and eyes).

1.3.7 Result of testing

Each performance matrix shall be measured as follows.

(1) Measured FTE

> FTE shall be measured as follows.

FTE = total number of subjects failed to meet the enrolment policy /
                                                 total number of subjects attempted the enrolments                   

Note: Enrolment policy shall also be specified in the test documents

(2) Measured FAR and FRR

> FAR and FRR shall be measured as follows.

FAR or FRR = total number of failed imposter or genuine transactions /
                                                 total number of imposter or genuine transactions

(3) Upper confidence limit for FTE, FAR and FRR

> Upper confidence limit for each matrix shall be calculated based on
> interval estimation. This limit shall be equal or lower than target
> values specified in the security target. If the limit is calculated
> assuming the binomial distribution, 95% confidence interval shall be
> calculated and upper confidence limit shall be equal or lower than the
> target value. If the limit is calculated assuming other distribution,
> calculation method of confidence interval and rationale for such
> method shall also be reported.

2.  Evaluator’s task

The evaluator shall confirm that the test document provided meets all
requirements defined in the chapter 1.
