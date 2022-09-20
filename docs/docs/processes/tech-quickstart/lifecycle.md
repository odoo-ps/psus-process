---
layout: post
title:  "Stages of a development"
permalink: /docs/process/qs/lifecycle/
parent: Tech Quickstart
grand_parent: Process
nav_order: 2
---


# BELOW INFO TO BE CLEANED

# Requirements
- **Time in weeks**: 2

- **Time notes**:
  - Consultant Finished Specification
  - Request Approval from Team Lead

- **Usage notes**:
  - All new development request are created in this stage.
  - Each task requires review from your Coach/Team Leader/Task reviewer, so while your task is ready log note and tag the one responsible to review the task

- **Responsible**:
  - **PS functional**: Consultant and Consultant's Coach /  Team Leader
  - **PS Technical**: Technical Specification Reviewer

- **Task color**:

  - **Grey**: Functional consultant is working on requirements specification and not ready for review.

  - **Red**: The requirements specification has been updated and ready for reviewing by responsible.

  - **Green**: Responsible has approved the development and Technical team will review this now.

- **Resulting Stages**:
  - If approved => Scoping

  - Otherwise => Cancelled

- **Billing to customer**: None

# Tech review
- **Time in weeks** : 1

- **Time notes**: May take longer if we need more details or followup form Consultant

- **Usage notes**:
  - This stage can be used by technical reviewer for putting task in this stage while they are reviewing it and gathering additional information
  - Consultant will need to followup on required subjects asked

- **Send email or log note**:

  - Log note: [PSUST-LN01] Task Estimate Template (Use for internal note only)

  - Send to Customer:

- **Responsible**:
  - **PS functional**: Consultant (Reviewer on task)
  - **PS Technical**: Technical Specification Reviewer

- **Task color**:

  - **Grey**: Technical Spec Reviewer

  - **Red**: Blocked Need more details

  - **Green**: Hours estimate is given and task is good for moving on scoping with LN01

- **Resulting Stages**:
  - If Reviewed => Scoping
  - Otherwise => Cancelled

- **Billing to customer**: None

# Scoping
- **Time in weeks** : 8

- **Time notes**: If no update in eight week task will be cancelled

- **Usage notes**:

  - Stage is used to give time to customer on making decision that if they want move ahead with development or not.
  - Once task has been estimated in stage 'Requirements' the task will be moved to this stage.
  - The task will be staged for 4 to 6 weeks and and if task is no update during this them the request of development will be closed.
  - When a request is cancelled , the initial planned hours will be set to zero so parent task will not show change of hours.
  - Such cancelled request can be always re-open; if their is no change in specification then old estimate of hours is till valid and can be moved Scoping again and if their change in spec start at requirements stage."

- **Send email or log note**:

  - Log note: [PSUST-LN02] Scoping Estimate Reminder (Use for internal note only)

  - Send to Customer:

- **Responsible**:
  - **PS functional**: Consultant and Consultant's Coach /  Team Leader
  - **PS Technical**: Technical Specification Reviewer

- **Task color**:

  - **Grey**: Customer is working on decision making (weather this development will fit in project scope or not)

  - **Red**:
    - Something is wrong and requires attention from Customer or Functional Consultant.
    - The PS Technical responsible will move task to this state and will let consultant know via chatter communication

  - **Green**: Task is ready for development. When consultant here back from customer and if task is approved then, the consultant should mark is green indicating task is ready  for development

- **Resulting Stages**:
  - If approved => Planning
  - Otherwise => Cancelled

- **Billing to customer**: 11

# Planning
- **Time in weeks** : 2

- **Time notes**: Depending on Lead time and size of development this may takes longer or shorter

- **Usage notes**:
  - Stage is used for queuing all the development before a developer from technical team start working on this.
  - Usual lead time here  is 1 to 2 weeks but this may vary if we have too many thing going on at once.


  - Note that requirements specification is now frozen to what has been sent to customer in email and no new change request will be accepted, and if their is change request before we start development then we will estimate and will start from requirements stage and will go through approval.

- **Send email or log note**:

  - Log note: [PSUST-LN06] Task Moved to Planning Template (Use for internal note only)

  - Send to Customer: [PSUST-C01] Your request for development has been created

- **Responsible**:
  - **PS functional**: Consultant (Reviewer on task) or Coach (Parent Task Reviewer) or Team Leader
  - **PS Technical**: Developer (Assigned on task) or Team Leader

- **Task color**:

  - **Grey**: Task is ready for development and requires planning action.

  - **Red**:
    - Requires attention from Customer or Functional Consultant.
    - The PS Technical responsible will move task to this state and will let consultant know via chatter communication.

  - **Green**:
    - Task has been added to the development queue and developer will pick task based on their availablity and workload.
    - When task is planned the functional consultant and customer will be notified by email which will include hours and the final specification.

- **Resulting Stages**:

  - If approved => Development
  - Otherwise => Cancelled

- **Billing to customer**: None

# Development
- **Time in weeks** : ~

- **Time notes**: As long as development requires based on estimated time and developer planning

- **Usage notes**:

  - All Active feature development that all developer working can be seen here.
  - Development will not be ready at given hours estimate in time frame as developer has many other work they work in parallel so they plan their work according.

  - Note that requirements specification is now frozen now, no new change request or scope screep will be accepted any more, for new requirements please start new task."

- **Send email or log note**:

  - Log note:

  - Send to Customer: [PSUST-C02]  Your development has started

- **Responsible**:
  - **PS functional**: Consultant (Reviewer on task) or Coach (Parent Task Reviewer) or Team Leader
  - **PS Technical**: Developer (Assigned on task)

- **Task color**:

  - **Grey**:
    - Developer is working on developing the feature.
    - When a task is moved to this stage, the developer will notify functional consultant and customer with email suggesting that the development has been stated.

  - **Red**:
    - Task is blocked and requires more details from the customer or consultant.
    - Developer will notify functional responsible about this."

  - **Green**:
    - Development is ready for UAT  and task can be moved to Functional Review stage now.
    - when task ready developer will notify functional consultant and customer with email that ask is ready for testing with URL of instance where it can be tested."

- **Resulting Stages**:
  - When ready => UAT

- **Billing to customer**: Amount hours spent will be takes from success pack hours based on time sheet entered.

# UAT
- **Time in weeks** : 6

- **Time notes**: If development not tested in 6 weeks then MRR will be added manually

- **Usage notes**:

  - Stage is used to the stage task which are under user acceptance testing.
  - This stage is time sensitive, after six week for life in functional review the such task will be moved to the UAT(Billed)  stage adding maintenance fee ($5 per hours per month ) for total hours spend on task.

- **Send email or log note**:

  - Log note:

  - Send to Customer: [PSUST-C03]  Your development is ready for user acceptance testing (UAT)

- **Responsible**:
  - **PS functional**: Consultant (Reviewer on task) or Coach (Parent Task Reviewer) or Team Leader
  - **PS Technical**: Developer (Assigned on task)

- **Task color**:

  - **Grey**: Customer is doing user acceptance testing .

  - **Red**: Task is blocked and requires attention from TL (Functional/Technical)

  - **Green**:

    - Task has been passed the UAT from customers end and ready for deploying.
    - Upon receipt of approval consultant will mark such task to green, indicating task is ready for deploying.

- **Resulting Stages**:

  - After Six week  => UAT (Billed)
  - If rejected => Cancelled

- **Billing to customer**: Amount hours spent will be takes from success pack hours based on time sheet entered ( if more adjustment are required)

# Deployed
- **Time in weeks** :

- **Time notes**:  Development is deployed in production and we can add maintenance to subscription

- **Usage notes**:

  - Stage is used to park task when development are deployed in production.
  - Within week task will be moved to Done and maintenance will be added."

- **Send email or log note**:

  - Log note:

  - Send to Customer: [PSUST-C04] Your development has been deployed in production

- **Responsible**:
  - **PS functional**: Consultant (Reviewer on task) or Coach (Parent Task Reviewer) or Team Leader
  - **PS Technical**: Project Leader


- **Resulting Stages**:
  - Deployed => Done

# Done

- **Usage notes**:

  - Task ha reached End of life cycled.
  - Odoo has successfully delivered what was asked.

  - Maintenance and Migration
    - For Any future bug, functional consultant is required to create new task in ""PS - US Technical Support"" with this is in reference.
    - For Any future feature enhancements, functional consultant is required to create new task in ""Ps - US SaaS Customization"" with this is in reference and change request.
    - For any future version migration functional consultant is required to create new task in ""PS - US Technical Support"" with this is in reference.

- **Responsible**:
  - **PS functional**: Consultant (Reviewer on task) or Coach (Parent Task Reviewer) or Team Leader
  - **PS Technical**: Team Leader and Developer (Assigned on task)

- **Resulting Stages**:
  - End of Life Cycle
  - Can result in maintenance and migration from here

- **Billing to customer**: Maintenance will be added by Line Of code deployed in production upon approval

# Cancelled

- **Usage notes**:

  - All task cancelled will be collected here.
  - Task from cancel stage can be re-opened by putting task in requirements stage  again."

- **Send email or log note**:

  - Log note: [PSUST-LN03] Cancel development request  (Use for internal note only)

  - Send to Customer:

- **Responsible**:
  - **PS functional**: Consultant (Reviewer on task) or Coach (Parent Task Reviewer) or Team Leader
  - **PS Technical**: Developer (Assigned on task) or Team Leader


- **Resulting Stages**:

  - End of Life Cycle
  - If customer wants it now then => Requirements"

- **Billing to customer**: None
