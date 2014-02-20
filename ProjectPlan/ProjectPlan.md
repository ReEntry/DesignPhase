Re-Entry - “Sidekick” Tools to Reduce Recidivism

# Table of Contents: 

Project Team
Problem Description
Project/Application Summary
Design Phase Catalyst Support
Background
Application Description
Timeline
Next Steps
Parking Lot, Issues, Notes, Etc:
Privacy Issues

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

## Development:

The application will be developed using an API-Based Open Network. This will allow for continued development in a distributed fashion and customization to the specific requirements of federal, state, and local courts. The application will be device agnostic/web applications.

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

## Approximately 3 month Design Phase

Early March 2014 – Early May 2014

## Milestone: End-Phase Deliverables:

### Transmission of Deliverables:

* A markdown file describing a conceptual design architecture for the ReEntryApp and it's intended use, context and future development path;

* A prototype file demonstrating the user experience and other key featured, functions and flows of the App (this may be based on interactive wireframes or may include working code); and

* Transfer and Handoff of Project Resources:

 - Account transfer and ownership assignment of the GitHub organization within which the repositories (both public and private) containing all project data, work flow (ie via issues tickets, authorization roles for accounts of contributors and other participants, open source licenses, etc). 

 - It is also anticipated that the hand-off will include a Google Hangout for a presentation using slides, screen share, video and/or other online methods to walk through the deliverables and repositories, discuss the project and respond to questions.

## Subsequent Phases and Future Roadmap for ReEntryApp

The markdown file describing a conceptual design architecture and proposed future roadmap for ReEntryApp will also include the then current feedback from the Stakeholder Committee qnd best effort recommendations by the Project Team on the subsequent phases for future development and deployment of ReEntryApp.

# Next Steps

Dan Emails Judge Aiken w/Draft end of day, and that we’ll get her a proper draft end of week or over weekend.  Purpose: request is she can join Tue 25th, 4pm EST or other time with her.  
Request day/time we can go through this doc (the plan), timing and get feedback on “Kick-Off” date to start the agile design phase. 

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

