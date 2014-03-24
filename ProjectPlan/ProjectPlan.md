Re-Entry - “Sidekick” Tools to Reduce Recidivism

# Table of Contents: 

* Project Team
* Problem Description
- Project/Application Summary
- Design Phase Catalyst Support
- Background
- Application Description
* Timeline
* Next Steps
* Parking Lot, Issues, Notes, Etc:

# Project Team

Dazza Greenwood
Lina Kaisey
Eric Adler
Joshua Lenon
Joyce Searls
Dan Lear  

# Problem Description

[WOULD LIKE TO PULL THIS FROM JUDGE AIKEN’S DECK OR ELSEWHERE; MAY ALSO MAKE SENSE TO MERGE THIS WITH THE “BACKGROUND” SECTION]

# Project/Application Summary

Build prototype system to provide a technological aspect of Judge Aiken’s innovative re-entry/recidivism prevention program.  As currently envisioned, the project has two functional pieces. A court-facing or parole officer-facing dashboard module that will allow the court/parole officer to track the individual’s progress, real-time movements, and to provide timely strategic interventions to help reduce recidivism. The project will also include a participant-facing module, most likely in the form of an application developed for a mobile platform (currently expected to be Andriod), that will enable and empower program participants to succeed in their re-entry journey.     

## Design Phase Catalyst Support

MIT Media Lab’s Computational Legal Science research team, who collaborate on this project team (Lina/Dazza) have offered to provide additional assistance on design and stakeholder engagement.  (See: https://github.com/LegalScience/ReEntry/blob/master/DESIGN-PHASE-OVERVIEW.md) 

## Background

In recent years Judge Aiken, Chief Judge of the U.S. District Court for the District Court of Oregon, has implemented an innovative re-entry program in which the “re-entrant” (the “individual”) the court, and the parole officer work closely to support the individual’s efforts to avoid recidivism. Participants in this program have demonstrated a 16% reduction in recidivism as compared with participants in standard re-entry programs.
This innovative program is based upon limiting the following five criminogenic factors that have been shown to correlate to increased recidivism. Specifically:

1. Substance Abuse
2. Mental Health
3. Education
4. Family Environment
5. Employment

The program emphasizes personal responsibility for the individual and is based upon the core values of “Trust, Transparency, and Truth.”

## Application Description

This project will use technology to implement the same principles that Judge Aiken successfully applied in her recidivism prevention program. Specifically, the application will feature five key functionalities:

Crisis
Me
Job
Communication
Schedule

Please see the simple wireframe in Attachment A to this document showing a sample UI for the application homescreen.

Each of these key functionalities is tied to a criminogenic recidivism factor. The app is designed to help reduce the incidence of each criminogenic factor in an individual’s life and, thereby, hopefully limit a given individual’s tendency 
to recidivate. 

Each tab is discussed below:

### Crisis: 

This tab will provide the individual with immediate contact with a parole officer or other support.

### Me:

 This tab will consist of two main pieces.
- First: A status tracker which will enable the individual to monitor their progress against key criminogenic factors manifest in the application.
- Second: Access for the participant to contact information for their family, friends, and other loved ones

### Job: 

This tab will connect the individual with employment resources such as job posts, networking opportunities, and education modules. These modules and resources may be able to be customized depending upon the individual’s needs and skills.

### Communication: 

This tab will provide the individual with access to text functionality to parole officer and volunteer support individuals as well as, potentially, counsellors and other contacts.

### Schedule: 

In this module the individual will have access to a calendaring function. The parole officer or other official will be able to push calendaring events to the individual’s application. Pushed events will include random and scheduled urinalysis appointments, counseling visits (both group and individual), family visitation opportunities (if applicable), court dates, probation “check-in” appointments and others. The individual will also be able to schedule their own events. The receipt of push notifications will be made prominently visible throughout the application UI and reminders for important events will also surface on the homescreen and, possibly, in other places in the app.

### Parole Office Module: 

The court or parole officer-facing module will provide the parole officer with real-time insight into the activities and progress of the individual. Most if not all information visible to the individual in the application will be visible to the parole officer, including the individual’s use of the application and activity. The parole officer module will be combined with “big data” analytics across all program participants and other criminogenic research to try and discern when certain activities by a specific individual in the program may indicate a likelihood for that individual to violate the conditions of their parole. This will give the courts and parole officer an opportunity to intervene in strategic instances to try to support the individual and help to reduce recidivism.  

# Development:

## Open Research Project

Please note, the MIT Media Lab Computational Legal Science research team is providing facilitation and convening support for the Design and Rapid Prototype phase as one of our discretionary/volunteer "Open Research Projects".  This means that we are not charging money or requiring an exisitng research sponsor of the lab to support the activity, but all of our work and contributions are provided under open source free software licenses and creative commons free copyright licenses and all project materials that are contributed under the auspicies of the MIT convening are considered public, non-confidential and are openly accessible on our web site and/or in our GitHub repositories.  

The the extent confidential, secret, private or otherwise access restricted resources are needed or expected as part of work on the ReEntryApp, please be careful not to include those materials in the GitHub repository or to provide them to MIT research or other staff or otherwise to contribute those materials to the GitHub or websites set up by MIT to support this project durign the Design and Rapid Prototype Phase.  However, at the conclusion of this phase, when MIT and the Project Team hand over the materials, repositories and other resources to the Stakeholder Committee, then you may wish to choose other ways to handle intellectual property, confidentiality agreements or other aspects of access control with respect to the project content transmitted as a deliverable.  During this Design and Rapid Prototype Phase, please simply be careful to use other channels for transmission or storage of non-open resources.

## Open Architecture

It is expected that the code comprising the rapid prototuype during the initial phase of this project will leverage existing open source code or will be developed as new code under an open source license.  Similarly, the design phase will focus upon how open source licensing (both with software open source licenses and also for other content using Creative Commons or consistent licenses).  

Likewise, the focus will be on using (and where needed extending or profiling) open standards and open formats for data, interactions, services and other aspects of the project.  

It is expected that the application and related host platforms and services will be developed around an Open Network approach using REST/API accessible service ports, busses and/or other interfaces.  The app can, using this approach, eventually become device agnostic as a mobile web application.  

This approach to the conherent and consistent use of open source, open licensing, open standards, open formats and open interface together comprise what can be thought of as an "Open Architecture".  This will allow for continued development in a distributed fashion and customization to the specific requirements of federal, state, and local courts. 

## Types of Data and Key Interactions

**Schedule Data** - what are the upcoming meetings and compliance events for program participants. Examples include group meetings, urinary analysis appointments, deadlines for completed activities.  This data is date-based.  It will be paired with compliance data as due dates for compliance data points.

**Compliance Data** - conditions of parole and the program with which the participants are required to comply.  Examples would be clean urinary analysis results, check-ins with the parole officer, residency and employment requirements.  These tend to be a binary condition; they are either met or not-met.  They will be paired with schedule data.  Compliance data will have due dates.

**Discrepancy Data** - arises when compliance data triggers occur.  This relies upon two data points.  First, a compliance data point is entered.  Second, a trigger schedule date is assigned to the compliance data point.  Discrepancy data occurs when either a schedule data point passes and compliance data is not set to met.  Outgoing reporting will track the amount of time that has passed from the assigned scheduled data point.

Examples of discrepancy data: Participant has been assigned the compliance task of going 12 months without evidence of substance abuse.  Urinary analysis tests have been scheduled on a monthly basis for the participant.  Each test has a date and a compliance result to track. Discrepancy data occurs if the participant fails to either attend the test or fails to test as substance free.  Program participants and parole officers would be alerted to missed / failed test and how long had passed since the test.

# Ad Hoc Stakeholder Committee 

## Leadership: 

Judge Aiken convenes and chairs and membership consists of appropriate members of key stakeholder group.  

A preliminary directory and placeholder page with more information has been provisioned for this group, at: [https://github.com/LegalScience/ReEntry/blob/master/StakeholderCommittee/Overview.md](https://github.com/LegalScience/ReEntry/blob/master/StakeholderCommittee/Overview.md).  

## Members 

Members of the Stakeholder Committee are expected to includes people of the following groups:

- Judges
- Parole Officers
- Clinics
- Participants

## Expert Advisory Group

A placeholder page for more information has been provisioned for this group, at: 
[https://github.com/LegalScience/ReEntry/blob/master/StakeholderCommittee/ExpertAdvisoryPanel.md](A preliminary directory and placeholder page with more information has been provisioned for this group, at:)

A SubCommittee, Task Force or other invited group supporting the project team and Stakeholder Committee is expected.  This group is anticipated to include top legal, technical, administrative and subject matter experts who are willing to provide hand-on feedback and/or direct assistance to the project team and/or the Stakeholder Committee focused on successful achievement of the goals and outcomes intended for the design phase.  

# Timeline and Milestones

## Tentatively Expected to be Approximately 3 Month Design Phase

March 2014 – May 2014

## Milestone: End-Phase Deliverables:

### Transmission of Deliverables:

* A markdown file describing a conceptual design architecture for the ReEntryApp and it's intended use, context and future development path;

* A prototype file demonstrating the user experience and other key featured, functions and flows of the App (this may be based on interactive wireframes or may include working code); and

* Transfer and Handoff of Project Resources:

 - Account transfer and ownership assignment of the GitHub organization within which the repositories (both public and private) containing all project data, work flow (ie via issues tickets, authorization roles for accounts of contributors and other participants, open source licenses, etc). 

 - It is also anticipated that the hand-off will include a Google Hangout for a presentation using slides, screen share, video and/or other online methods to walk through the deliverables and repositories, discuss the project and respond to questions.

## Subsequent Phases and Future Roadmap for ReEntryApp

The markdown file describing a conceptual design architecture and proposed future roadmap for ReEntryApp will also include the then current feedback from the Stakeholder Committee qnd best effort recommendations by the Project Team on the subsequent phases for future development and deployment of ReEntryApp.

## PHASES

As currently envisioned the design and rapid prototype project has three key phases: 

Prepatory Organizational and Initialization Phase (February 8th - Kick-Off)

* Phase 1: Kick-off

Commences with: Initial Meeting of Steering, Expert and Project Team Groups and Agreement on More Detailed Project Plan

Creates: Initial Design and Rapid Prototype Development Iterations Through Informal Feedback Sessions, GitHub Issues, Weekly Hangouts, etc

Concludes With: Mid-Project Presentation to Stakeholder and Expert Panels

* Phase 2:  Review of Design Concept and First Stable Prototype

Commences With: Steering and Expert Committee Review and Feedback to Project Team on Mid-Project Presentation

Creates: Refined or Revised design concept and corresponding updates to prototype, likely more targeted testing focused on key feedback, criper definition of post design-phase implementation issues and options

Concludes with: Final Presentation to Stakeholder and Expert Panels

* Phase 3: Hand-off of Prototype and Launch of Pilot or Production Projects

Commences with: Project Team Hand-Off of Project to Steering Cmt

Creates: Collaboratively Developed Transition to Pilot or Production Teams, Stakeholder Engagement and Resource Gathering Plan

Concludes with: Launch Event(s) 

* Post-Launch Steering Cmt Pitches/Proposes for Funding and other Resources; Press/Media, Assist Projects Uptake


# Next Steps

Phone call with Judge Aiken and Mark Sherman on March 25th to discuss how best to launch and manage the design phase.

* Specifically ask: Who should be on panel? 

Convene panel


## Attachment A

Note: This wireframe is a sample and the buttons here do not reflect the actual buttons expected to be implemented in the project.  


## Parking Lot, Issues, Notes, Etc:

* Prototype MVP:

Thoughts on Transition from Prototype to Production Grade App:  
- Who would be responsible for support, be the party with whom the Ts&Cs are agreed, etc
- Who would hold the private data that feeds the dashboards?

* Security and Privacy Issues

What are the security and privacy requirements, constraints and other issues?  How do we currently or propose in the future to address the issues? 

See: “Judicial Conference Policy on Privacy and Public Access to Electronic Case Files” 

