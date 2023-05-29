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

There have been [many instances](https://teslamotorsclub.com/tmc/threads/feature-request-tesla-feature-request-and-bug-tracking-platform.301409/) of people suggesting a public bug tracking system for Tesla vehicle software, either operated by Tesla or [by a third party](https://www.reddit.com/r/teslamotors/comments/ei6rd8/tesla_software_bugs_tracking_bugs_and_bug_fixes/), such as a public forum, or [even GitHub](https://github.com/teslacommunity/tesla-bugs). As far as I know, none of these has succeeded.

Tesla has not produced such a system itself possibly because:
1. It may not be in Tesla's best interests to have a publicly available list of known issues. Witness how news articles refer to Tesla recalls that are addressed by over the air updates.
2. Tesla already has such a system for its own internal use, and is using an enhanced bug reporting system for its Full Self Driving Beta program, complete with comprehensive release notes.

Third party schemes such as forums or GitHub may have failed for various reasons:
1. Tesla owners may be unwilling to contribute to a publicly visible bug tracking system because it may put Tesla in a bad light.
2. Forums are too unstructured, with [issues mixed in with other discussion](https://www.reddit.com/r/TeslaLounge/comments/xjq8nk/reporting_bug_to_tesla/), and it is difficult to [track the resolution of issues](https://www.reddit.com/r/teslamotors/comments/arj0sd/sentry_mode_201953_second_update_bug_fixed/) [via such a discussion forum](https://www.reddit.com/r/teslamotors/comments/g0pw39/sentry_mode_keeps_turning_off_since_the_2020125/).
3. The use of public systems like GitHub is too difficult to administer with respect to access controls.
4. There may not have been enough interest in such schemes.

##### Types of issues to report and track

A Tesla issue reporting and tracking system should concentrate on issues with Tesla's in-vehicle software, especially the non-FSD Beta software. Some specific software features lend themselves to issue reporting and tracking, such as:
1. Speed Assist via either speed sign detection, or maps, or both.
2. Traffic light detection.
3. Traffic regulation sign detection (e.g. stop and give way signs).
4. Auto high beam.
5. Auto wipers.

##### Issue reporting

Reported issues should be specific enough to be addressible, but generic enough to apply to many instances. For example:

* "Auto high beam does not work properly" is too vague to be addressible.
* "Auto high beam turns on high beams on Northbourne Avenue in Canberra" is too specific.
* "Auto high beam turns on high beams on roads where there is street lighting" is about right.

##### Instance reporting

Since a reported issue can apply to many instances, it is also useful to report these instances. 
Instance reporting should at least include:
Software version, date and time of occurence, location of occurence, expected behaviour, observed behaviour,
and can also include enough vehicle identification to distinguish vehicles, and any extra notes.
Such instance reporting can highlight that:
1. Instances of an issue can persist across many software versions.
2. Instances of an issue can be confined to a specific geographical area or jurisdiction, or can be global in nature.

##### Capturing metadata

If you are reporting instances, one way to remind yourself of the time an location of occurrence is to save a TeslaCam clip.
As stated above, Tesla's own bug reporting also automatically captures metadata, but unfortunately only minimal metadata, such as time and location, is captured with TeslaCam clips.
A possible exception to this is the FSD Beta program.
Automatic capture of metadata relevant metadata with TeslaCam clips would greatly help instance reporting, so it should be suggested to Tesla as a feature request.

##### Issue tracking

Since Tesla, outside of the FSD Beta program, is vague about which software releases affect which issues, the onus would be on the people who reported instances of the issue to test to see if the issue persists or is solved by each software release. Confirming that an issue has been addressed by a software release would lead to the issue being closed in the tracking system. The remaining open issues would be those which have not yet been confirmed to have been addressed.

#### A public or a private issue tracking system?

A completely public issue tracker that would allow any person to self-register and create issues would probably be too open to abuse.
It might not be wise to have a completely publicly visible issue tracker, but this is debatable.

#### Who should run this type of system?

Ideally, Tesla Owners Clubs should run this type of system on behalf of members. 
This would be a good compromise between a completely public system and a private system.
All members would have access to report issues and instances, and make comments, and possibly a smaller number of members would have the ability to close issues and perform other admin tasks.

##### Candidate hosts for the issue tracker

[There are a number of candidates for an issue tracker that provides suitable access controls](https://en.wikipedia.org/wiki/Comparison_of_issue-tracking_systems), including [Bugzilla](https://www.bugzilla.org/), [GitHub Enterprise](https://docs.github.com/en/enterprise-server@3.6/admin/overview/about-github-for-enterprises), [Gitlab](https://docs.gitlab.com/ee/subscriptions/), [Jira](https://www.atlassian.com/software/jira) and [Trac](https://trac.edgewall.org/).
The choice of which one to use would consider factor such as:
1. Does the issue tracker support the required features?
2. Does the issue tracker make it easy to control access, including integration with existing user athentication systems?
3. Does the issue tracker have an open source licence? (e.g. Trac is 
4. Who would provide user support and which issue trackers are they most familiar with?
5. [Cost of hosting](https://trac.edgewall.org/wiki/CommercialServices), etc.

##### How would access control work?

Ideally, if a Tesla Owners Club ran an issue tracker, it would use the same user authentication system for Club members as the Club's main web page.
All members would have access to report issues and instances, and make comments, and possibly a smaller number of members would have the ability to close issues and perform other admin tasks.
If Tesla Owners Clubs had some method of identifying members of sister clubs, they might be able to make their issue tracking system visible to members of all such sister clubs.
