---
layout: post
title:  "Kanban Stages"
permalink: /docs/project/qs/lifecycle/
parent: Tech Quickstart
grand_parent: Project
nav_order: 2
---
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# Kanban Stages

## Requirements
**Description:** This stage is the start of the Tech Quickstart flow. Developers do not need to do any action in this stage. In this stage, the BSA will make a copy of the Development template and write the development spec in the description. Once the spec is done, the BSA will ask their Team Leader to Review and approve the development(Kanban State Green). 

The Project Leader will then review the Greened tasks. They check the following fields are set: Parent Task, Sale Order Item, Subscription, and Reviewer. The Project Leader will also review the feasibility of the development. If the specification is missing information or is not a suitable development, the Project Leader may ask the BSA for more information, to change certain parts of the spec or may even reject the development. If we reject the development we will provide reasons why and ideally provide an alternate solution or recommend them to work with to a partner.

**Time in stage:** 2-4+ weeks

**Time notes:** 
  - BSA Finished Specification
  - Request Approval from Team Lead

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach / Team Leader

**Kanban State Color**:

  - **Grey**: BSA is working on requirements specification and not ready for review.

  - **Orange(Changes Requested)**: The requirements specification has been updated and ready for reviewing by responsible.

  - **Green**: BSA Team Lead has approved the development and Project Lead will review this now.

**Resulting Stages**:
  - If approved > Tech Review

  - Otherwise > Cancelled

**Billing to customer**: BSA should bill customer on the QS task directly for creating the spec


## Tech Review
**Description:** Once the Project Leader reviews and approves the development spec, they will move it to the Tech Review Kanban Stage. The Task will start in the unassigned Gray state. These tasks are ready for estimate. Anyone who is 1+ year can work on Estimation. We will timesheet directly on the task for the analysis spent on the Estimation. See the [Estimation]() section for more information on the Estimation process.

After the Developer has finished the estimation, they will change the kanban state to Green. Then the Project Leader will review the estimation. If it needs some changes or clarification, the Project Leader will ask the Developer some questions or give suggestions. 

If the Estimation is good, the Project Leader will approve the Estimation and move the task to Scoping.

**Time in stage:** 1 week

**Time notes:** 
  - May take longer if we need more details/followup from BSA or if the spec is large

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach / Team Leader
  - **PS Technical**: Developer/ Project Leader

**Kanban State Color**:

  - **Grey**: Task is ready for Estimation

  - **Orange(Changes Requested)**: The requirements specification has been updated and ready for reviewing by responsible.

  - **Green**: BSA Team Lead has approved the development and Technical team will review this now.

**Resulting Stages**:
  - If approved > Scoping

  - Otherwise > Cancelled

**Billing to customer**: BSA should bill customer on the QS task directly for creating the spec

## Scoping
**Description:** Once the Estimation in Tech Review is approved, the Project Leader will move it to here, the Scoping Kanban stage.

The Project Leader will send out the Log Note template LN01. This will contain the estimated time, if SH is required, and the estimated LOC the development will take. Now we wait for the customer's response. 

The Project Leader will send out the log note template LN02 every few weeks up to 8 weeks. If there is not response, we will automatically cancel the development task. 

If the customer approves the development, the Project Leader will move the task to the Planning Kanban Stage. 

If they do not approve of the development, the project leader will move the development to the Canceled Stage. When a request is cancelled, the initial planned hours will be set to zero so parent task will not show change of hours. These cancelled request can be always re-open; if there is no change in specification then old estimate of hours is till valid and can be moved Scoping again and if there is change in spec start at Requirements stage.

**Time in weeks** : 8

**Time notes**: If no update in eight week task will be cancelled

**Usage notes**:

  - Stage is used to give time to customer on making decision that if they want to move ahead with development or not.
  - Once task has been estimated in stage 'Tech Review' the task will be moved to this stage.
  - The task will be staged for 4 to 6 weeks and if task is not update during this them the request of development will be closed.
  - When a request is cancelled, the initial planned hours will be set to zero so parent task will not show change of hours.

**Send email or log note**:
  - Log note: [PSUST-LN02] Scoping Estimate Reminder (Use for internal note only)
    - only the Project leader sends this out to remind the BSA of the estimate

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach /  Team Leader
  - **PS Technical**: Project Leader

**Kanban State Color**:

  - **Grey**: Customer is working on decision-making (weather this development will fit in project scope or not)

  - **Orange(Changes Requested)**:
    - Something is wrong and requires attention from Customer or BSA.
    - The Project Leader will move task to this state and will let BSA know via chatter communication

  - **Green**: Task is ready for development. When BSA hears back from customer and if the task is approved then, the BSA should mark is green indicating task is ready for development

**Resulting Stages**:
  - If approved > Planning
  - Otherwise > Cancelled

**Billing to customer**: None, this is on the customer's side

## Planning
**Description:** Once the development has approval from the customer(usually written and attached to the task), the Project Leader moves the task to the Planning stage.
If the task is ready to start with PSUS repo ownership and enough hours on the pack to cover the estimate, the Project Leader will change the kanban state color to Green. Greened unassigned tasks can be taken to work on. 

Do not take Tasks with Kanban Color Gray or Orange. This is because there may be some pending items for those developments or certain issues. Developers should only take Greened tasks. 

Exception: For very large developments, newer developers must talk to the Project Leader before taking them. 

If the task is missing any of the above, the task will b blocked and the kanban state color will be Orange(Changes Requested).

Project Leader will announce new tasks in the psus-updates channel. They will provide more information if there are certain restrictions on the task(Ex: experienced OWL developer needed, only MX developer allowed, etc.).  

**Time in weeks** : 2+(Depends on current lead time and developer availability)

**Time notes**: Depending on Lead time and size of development this may take longer or shorter

**Usage notes**:
  - Stage is used for queuing all the development before a developer from technical team start working on this.
  - Usual lead time here  is 1 to 2 weeks but this may vary if we have too many things going on at once.
  - Note that requirements specification is now frozen to what has been sent to customer in email and no new change request will be accepted, and if there is a change requested before we start development then we will estimate and will start from requirements stage and will go through approval over again.

**Send email or log note**:
  - Send to Customer: [PSUST-C01] Your request for development has been created

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach /  Team Leader
  - **PS Technical**: Developer/ Project Leader

**Kanban State Color**:

  - **Grey**: Task is ready for development and requires planning action.

  - **Orange(Changes Requested)**:
    - Requires attention from Customer or BSA.
    - The PS Technical responsible will move task to this state and will let BSA know via chatter communication.

  - **Green**:
    - Task has been added to the development queue and developer will pick task based on their availability and workload.
    - When task is planned the BSA and customer will be notified by email which will the final specification.

**Resulting Stages**:

  - If approved => Development
  - If spec changes requested => Requirements
  - Otherwise => Cancelled

**Billing to customer**: None

## Development
**Description:** The assigned developer will move the task to this stage once they start working on the requirements. This is where the development stays as long as it is not finished and ready for testing. Once the development is done they move the task to the Code Review kanban stage. 

**Time in weeks** : ~(depends on the size of the development)

**Time notes**: As many hours as the development requires based on estimated time and developer planning

**Send email or log note**:
  - Send to Customer: [PSUST-C02]  Your development has started

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach /  Team Leader
  - **PS Technical**: Developer

**Kanban State Color**:

  **Grey**:
    - Developer is working on developing the feature.
    - When a task is moved to this stage, the developer will notify BSA and customer with email stating that the development has been stated.

  **Orange(Changes Requested)**:
    - Task is blocked and requires more details from the customer or BSA.
    - Developer will notify the Reviewer about this

  **Green**:
    - Development is ready for UAT and task can be moved to Code Review stage now.

**Resulting Stages**:
  - When ready => Code Review

**Billing to customer**: Amount hours spent will be taken from the success pack hours based on time sheet entered.

## Code Review
**Description**: Once the developer is done with the development, they move the task to Code Review. The developer will set the reviewer on the pr to psus-quickstart-reviewer(this will notify the members of that group). Additionally, the developer will ping the @pr-police discord role in the pr-police discord channel with their PR link. A member of the pr-police will assign themselves to the pr. The pr-police will then review the task and comment if anything needs to be changed or if there are any questions. Following the review if there are changes necessary, they will block the task(Kanban color Orange) and request the developer to make those changes. Or if the development is approved, they will mark the kanban color Green. Once it is greened, the developer can move the task to the UAT stage.  

**Time in weeks** : <1

**Time notes**: Code Review should be top priority for pr-police team members

**Usage notes**:

  - Stage is for code reviews of developments ready for UAT.
  - pr-police team members should keep an eye out for any gray kanban color tasks here as well as in discord.

**Responsible**:
  - **PS Technical**: Developer and pr-police team members

**Kanban State Color**:

  - **Grey**: Task is ready for Code Review

  - **Orange(Changes Requested)**: Task is blocked and requires developer to fix any issues raised by the code reviewer

  - **Green**:

    - The task is ready for UAT, developer should move the task to UAT stage

**Resulting Stages**:

  - If code review approved => UAT

**Billing to customer**: Developer bills on task, if they are out of hours but need to make changes because of code review, the Developer can timesheet in the Project/Task [PSUS - Misc.]  Code Review Improvements(CRI)

## UAT
**Description**: Once the task has been code reviewed and approved by the pr-police, the developer can move the task to UAT stage. Make sure to send out the email template C03 because that marks the start date of the 6 weeks the customer has to do testing. After the 6 weeks we may cancel the task. If there are any feedback, bugs, or changes requested the developer must move the task back to the Development stage and follow the process again. This way C03 gets sent out each time there is a change and the 6 week counter will start over at that point. 

If there are new requests made(change requests/new spec/new requirements), this must be estimated and given to the BSA for the customer to approve. Do not work on new changes unless they have been estimated AND approved by the customer. If the estimate is over 8 hours, it must be approved by the Project Lead(AAL) before given to the BSA/customer. Once the customer approves it, update the estimate in the description and update the Allocated Hours field on the task to include the new estimate. 

**Time in weeks** : 6

**Time notes**: If development not tested in 6 weeks then development will be canceled.

**Usage notes**:

  - Stage is used to the stage task which are under user acceptance testing.
  - This stage is time sensitive, after six week for life in functional review the such task will be moved to the canceled stage.

**Send email or log note**:

  - Log note:

  - Send to Customer: [PSUST-C03]  Your development is ready for user acceptance testing (UAT)

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach /  Team Leader
  - **PS Technical**: Developer

**Kanban State Color**:

  - **Grey**: Customer is doing user acceptance testing .

  - **Orange(Changes Requested)**: Task is blocked and requires attention from BSA or TL (Functional/Technical)

  - **Green**:

    - Task has been passed the UAT from customers end and ready for deploying.

**Resulting Stages**:
  - If approved => Deployed
  - If feedback/bugs/changes requested => Development 
  - After Six week  => Cancelled
  - If rejected => Cancelled

**Billing to customer**: Amount hours spent will be takes from success pack hours based on time sheet entered ( if more adjustment are required)

## Deployed
**Description**: Once the development has been approved and pushed to production, the developer will move the task to this stage, Deployed. There is no further action needed from the Developer. At this point the Project Leader will ping the database and apply the LOC maintenance or request the Account Manager to apply the Maintenance. Once maintenance is applied to the subscription, Project Leader will move the task to the Done kanban stage. 

- **Time in weeks** : 1+

- **Time notes**:  Depends on how long the customer takes to pay for the maintenance or get it updated on the subscription by the AM. Yearly subscriptions take longer for customer approval, monthly subs can be activated by the Project Lead. 

**Usage notes**:

  - Stage is used to park task when development are deployed in production.
  - Maintenance will be added and then the task will be moved to Done.

**Send email or log note**:

  - Log note:

  - Send to Customer: [PSUST-C04] Your development has been deployed in production

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach /  Team Leader
  - **PS Technical**: Project Leader


**Resulting Stages**:
  - Deployed => Done

## Done
**Description**: Customer has LOC maintenance added to their subscription. Task should not have any new changes done in it, any request must be created in a new ticket, be it Bug/Change Request/New Requirements. Do not move this back to any previous stage. 

**Usage notes**:

  - Task ha reached End of life cycled.
  - Odoo has successfully delivered what was asked.

  - Changes, Maintenance and Upgrade
    - For any future feature enhancements or changes, BSA is required to create new task in "PSUS - Tech Quickstart" with this is in reference.
    - For any future bug, BSA is required to create new task in "PSUS - Maintenance" with this is in reference.
    - For any future version upgrade BSA is required to create new task in "Upgrades" with this is in reference.

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach /  Team Leader
  - **PS Technical**: Team Leader and Developer

**Resulting Stages**:
  - End of Life Cycle

## Cancelled
**Description**: Tasks can end up here from various other Kanban stages. At any point where the Customer requested the development to be canceled it will end up in this stage. If there is no response from the Customer/BSA we can cancel the task and move it to this stage. 

If the Customer Requests for the Canceled task be brought back, we will move it all they way back to the Requirements stage and will go through the whole flow again, regardless of what stage it was canceled from. The Project Lead has the right to move it to a different stage, depending on the circumstance(Ex: moving it back to planning). If you are not a project leader do not move any tasks from Canceled, please contact the Project Lead first. 

**Usage notes**:

  - All task cancelled will be collected here.
  - Task from cancel stage can be re-opened by putting task in requirements stage again.

**Send email or log note**:
  - Log note: [PSUST-LN03] Cancel development request  (Use for internal note only)

**Responsible**:
  - **PS Functional**: BSA and BSA's Coach /  Team Leader
  - **PS Technical**: Project Leader

**Resulting Stages**:
  - End of Life Cycle
  - If customer wants it now then => Requirements
