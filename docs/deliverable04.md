
# Deliverable 4

## Feature Branch

Before starting this work, ensure that you have merged in your `f/deliverable03`
feature branch.

Now it's time to work on deliverable 4.

Make sure `master` has the latest and greatest code.
(Do not blindly follow these instructions, professor and TA not responsible for lost work)

```
git fetch
git checkout master
git reset --hard origin/master # <---- THIS WILL OVERWRITE LOCAL WORK
```

Ok, now the first contribute can create the branch using

```
git checkout -b f/deliverable04
git push -u origin HEAD
```

Other contributors will need to checkout that new branch

```
git fetch
git checkout f/deliverable04
```

Please consider using feature branches for individual work and using
pull requests back into `f/deliverable04` as a workflow to coordinate
between team members.  Make them SMALL, focused and merge them often.

## Requirements

In this deliverable, you need to implement the patient related functionality.

### Service Provider Search

That is, the app should allow patients to search for a walk in clinic by:

* address
* working hours
* type of services provided

### Booking an Appointment

The application must display the list of available walk in clinics based on
the user search and allow the user to check in/book an appointment.

The application must show the expected waiting time based on the
number of people waiting to be seen (15 minutes per person).

### Rating A Clinic

The patient can rate a clinic by providing a score
between 1 (terrible) and 5 (amazing) as well as provide comment.

This used to (incorrectly) state to rate a service proivder, but
the intent was to rate a clinic.  If you provide rating about
a specific service that was provided that is fine, but the intend
was to provide feedback at the clinic level.


## Building Your APK

For more info: https://developer.android.com/studio/run/

* Go to `Build` -> `Build Bundle(s) / APK(s)` > `Build APK(s)`
* Android Studio saves the APKs you build in `project-name/module-name/build/outputs/apk/`
* Use the `_Debug` one for submission.

## Build Button in GitHub

Here is an example of the code to add to your [README](/README.md)
to enable a build button.  Please make sure you edit it
to point to _your_ project!!!

```
[![Build Status](https://circleci.com/gh/SEG2105F18/ProductCatalog.png?branch=master)](https://circle ci.com/gh/SEG2105F18/ProductCatalog)
```

Here's the [example above in real life](https://github.com/SEG2105F18/ProductCatalog).

<img width="268" alt="Screen Shot 2019-09-20 at 7 56 05 AM" src="https://user-images.githubusercontent.com/48086/65325302-73fe8b00-db7c-11e9-9a59-bcfce4b901c9.png">

Your build must be successful! Green Button instead of a red one.


## Final Report

In addition to your code, you will provide a [REPORT](/REPORT.md)

It should include

* A title page (note this document is "one the web" so there is no explicit notion of pages)
* Short Introduction
* UML class diagram
* Table with the roles in the team and contributions of team members for each deliverable.
* All the screenshots of your app.
* Lessons learned


## Submission

You can install [Hub](https://github.com/github/hub)
a command line tool to create pull requests
from your terminal directly into GitHub.

For deliverable 4, create a Pull Request with
the following information

```
hub pull-request -o -b master -m "Deliverable 4"
```

Your PR description (and text file to submit to BrightSpace)
will look similar to the following:

```
Forward Inc.
Team Members
Andrew Forward, 1484511 
James Url | 1929204 
Ayana Nurse | 2128439

PR:
https://github.com/professor-forward/walkinclinic/pull/2

Last Commit:
https://github.com/professor-forward/walkinclinic/commit/564d6484cce8af2ae6c15891178b2b086a4cb9ff

Instructions

+ Additional instructions about this deliverable
```

You will upload this file to BrightSpace before the deadline.

## Marking Scheme

| Feature or Task | Weight (/130) |
| --- | --- |
| UML Class diagram of your domain model (-2 for each missing class)<br>(-2 for each missing class)<br>(-2 for incorrect generalization)<br>(-0.5 for each incorrect multiplicity)<br>(-0.5 for each missing attribute) | 5 |
| APK submitted and working (see notes below)<br>Make sure you test your APK. An invalid APK will receive 0. | 5 |
| Final Report (see above for details)<br>Title Page (2.5)<br>Intro (2.5)<br>UML Class Diagram<br>Team (10)<br>Screenshots (10)<br>Lessons Learned (5) | 30 |
| 10 Unit test cases (simple local tests).<br>No need to include instrumentation or Espresso Tests (UI)<br>Test cases must be relevant to the features of deliverable 4. | 10 |
| Can search for a service provider | 10 |
| View approximate waiting time and check in/book an appointment | 15 |
| Can rate a clinic by providing a comment and a rate from 1 to 5 | 5 |
| CircleCI - Build button needs to appear in the Github (see instructions above). | 10 |
| All fields are validated. For instance, you should not be able to select a<br>date in the past when creating a timeslot or entering an invalid address.<br>This should be implemented along with valid error messages.<br>(-1 for each field in which the user input is not validated) | 10 |
| BONUS For Excellent UI Design | + 10 |

## Notes

* Ensure your [README](/README.md) includes instructions to sign-in as a homeowner, and instructions on creating a homeowner account from scatch.
* Make sure your apk is correctly generated.
