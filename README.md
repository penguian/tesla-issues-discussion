# tesla-issues-discussion
Third party reporting and tracking of issues with Tesla software.

This repository is based on [teslacommunity / tesla-bugs](https://github.com/teslacommunity/tesla-bugs) by @rickbassham. It is intended to provide a proof of concept and a focus for discussion on ways to improve the reporting and tracking of issues with Tesla software, in particular the software that runs Tesla vehicles.

#### Note
The current repository cannot be used to provide a public reporting service for such issues, for reasons discussed in detail below and elsewhere. The main reason is that [a GitHub personal repository does not provide the access controls that would be needed for public reporting of issues](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-personal-account-settings/permission-levels-for-a-personal-account-repository#collaborator-access-for-a-repository-owned-by-a-personal-account).

#### Why report and track issues in this way?

##### What Tesla currently does

[Tesla provides an in-car "bug report" voice command. This sends a driver's comments to Tesla, along with metadata](https://www.tesla.com/ownersmanual/model3/en_gb/GUID-85DDA8E1-596D-4980-9C17-C4F4E0FAA280.html).
The advantage of Tesla's method of bug reporing is that it automatically includes relevant metadata.
The disadvantage is that it is essentailly write-only. The driver does not receive a copy of the bug report and has no way to track any actions taken to address it, unless Tesla contacts the owner of of the car directly.

Tesla is well known for providing scant details about bug fixes in release notes, with the exception of Full Self Driving Beta software releases.
Often the release notes will say nothing other than, ["This release contains minor bug fixes and improvements."](
https://teslascope.com/teslapedia/software/2021.4.18) or will list feature changes and then say "Bug fixes," or will not mention bug fixes at all.

Even when a software fix is part of a NHTSA recall, it is not always clear which Tesla software release fixed which defect.

##### Previous attempts and why they failed



##### Types of issues to report and track

##### Issue reporting

##### Instance reporting

##### Capturing metadata

##### Issue tracking

#### A public or a private issue tracking system?

#### Who should run this type of system?

##### Trac as a candidate host for the issue tracker

##### How would access control work?





