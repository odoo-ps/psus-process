---
layout: post
title:  Estimation
permalink: /docs/process/qs/estimation
parent: Tech Quickstart
grand_parent: Process
nav_order: 5
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# Development Task Estimation

### Something to Keep in Mind
Please note that estimations should be made with the newest members in mind.  How long do you think it would take them to complete the task vs your own personal estimation.

### PS estimation Tool + Charging for Estimation
Starting January 1st 2023, we will use the ps-tool to estimate tasks and provide a deliverable outline for the customer/BSA when we give the estimate. 

As the PSUS team, we will also charge the customer for any time taken to do the estimate. This means the analysis time will be logged directly on the development task even before it is approved. If the customer wants an estimate, they will need to use pack hours. The task must have at least 10 hours to begin the estimation, the project leader will check for this first.
This also means that we must be more precise when we are doing the estimation. There is much less room for error since we will be using pack hours to estimate the task.  

Watch this [video](https://drive.google.com/file/d/19hoLmJC67dl5uTVSuOiT0BdnjAoCBgNs/view) on the demo Jigar did for the ps-tool.

If you do not have access to the tool here: [PS-Tool](https://ps-tools.odoo.com/), please reach out to JAM. 

#### Base Estimation

| Type                            |  Hours  | Notes                         |
|---------------------------------|:-------:|-------------------------------|
| Compute Field                   |   2+    | Includes associated method(s) |
| Non-compute Field               |   1+    |                               |
| New PDF Report                  |   12    |                               |
| Labels (printed)                |  6-12   | Depends on complexity.        |
| Financial Report (SQL/HTML)     |  16-24  | New or Modifying              |
| Views: Form/List                |    2    |                               |
| Views: Gantt/Calendar/Graph/etc |    4    |                               |
| Views: Kanban                   |    6    |                               |
| Cron                            |    8    | Each                          |
| Statistical View                |   20    | Each                          |
| Mexican Addenda                 |  4-16+  |                               |
| Smart Button                    |   2+    | Per Button                    |
| Constraint                      |   2+    |                               |

#### Business Logic

A lot of business logic really depends on your own judgment.  Here are some general estimates for common development:

| Type                |  Hours  | Notes                         |
|---------------------|:-------:|-------------------------------|
| Methods(overloading |   2+    |                               |
| Controllers         |   4+    |                               |
| JS Class            |   6+    |                               |
| JS Widget           |   12+   |                               |

#### Security

| Type          | Hours | Notes           |
|---------------|:-----:|-----------------|
| Group         |   2   | New or Existing |
| Record Rules  |   2   |                 |
| Access Rights |   1   |                 |

#### Data Import

| Type       | Hours | Notes           |
|------------|:-----:|-----------------|
| Object     |   8   |                 |
| Sub-Object |   4   |                 |

#### Data Deletion/Cleanup

| Type   | Hours | Notes      |
|--------|:-----:|------------|
| Object |   4   | Per Object |

#### EDI (WIP this is going to be updated, talk to CIC if you have questions)

| Type                           | Hours | Notes                                                                                                                                                                                    |
|--------------------------------|:-----:|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SFTP/FTP                       |  6+   | Depends on the provider for the SFTP/FTP                                                                                                                                                 |
| Model (Document) Export/Import |  6+   | 6 hours is based on if the model information being exported/imported does not require additional modification. Any calculations or logic added before transfer increases estimation time |
| Testing EDI                    |  10+  | for back and forth testing, depending on how many docs, number of trading partners etc.                                                                                                  |

#### Other

| Type                       | Hours | Notes                                                                                     |
|----------------------------|:-----:|-------------------------------------------------------------------------------------------|
| Delivery Carrier           |  80+  |                                                                                           |
| Payment Acquirer           |  80+  |                                                                                           |
| API connector              |  40+  | Really depends on the API and functionality customer requests, might be way more than 40  |
| SSO/O-Auth 2.0/Other Auth  |  18   |                                                                                           |

## Unit Testing and UAT Testing

Starting November 1st 2022, we began adding a 20% increase on top of all estimates. This increase is added on top of the general estimation of the task. 

This time is used to account for writing python Unit Tests and making sure the development branch is green in SH. Also accounts for any time needed to create documentation for the customer or recording any UAT videos for them as well. 


## Formulas
### General Formula

```
LOC Total = ⌈(Estimate Hours + 20% of Estimate Hours) * (Lines of Code per Hour)⌉
```

Line of Cost Total is equal to the Ceiling(to the nearest 100) of Lines of Code per Hour multiplied by Estimated Hours.

**Note**: All Estimated hours should be rounded up to the nearest Even Ceiling value(3 Hours rounded to 4 hours)

#### Example:

Base Estimate = 7\
Total Estimate = ⌈7 + 7*(.2)⌉ Hours = ⌈7 + 1.4⌉ Hours = ⌈8.4⌉ Hours = 10 Hours\
LOC per Hour = 16\
LOC Total = ⌈10 * 16⌉ = 200 LOC

#### On SH

| Type                                   | Line of Code per Hour | Notes |
|----------------------------------------|:---------------------:|-------|
| Models/Fields/Views                    |          16           |       |
| JS/Website/CSS/SASS/API/ PoS/Dashboard |          28           |       |
| API/EDI                                |          28           |       |

#### SaaS
**Note: Remember that only QWeb related Requests and Mexico Addendas are allowed on Saas databases, otherwise the customer will need an Odoo owned SH.**


| Type | Line of Code per Hour | Notes |
|------|:---------------------:|-------|
| Any  |          36           |       |

## Branding

We do not completely de-brand an Odoo database.
Note: Removing the phrase “Powered By Odoo” is the only exception. 

## Estimation Reliability

Each estimation has an estimation reliability (how strong you feel about the estimate). Default is 70% reliable.

For example 70% reliability means that the hours the developer takes on the actual task may vary +/- 30% of the original estimate. In the case of a 10 hour development estimate, if the task goes over by 3 hours or is under by 3 hours, that is within our initial estimate and we will not refund the 3 hours over if the customer asks. 

If you don’t have enough data for estimation, you should adjust the percentage to what you feel should be.  Top reliability is 90%, in this case you are very sure it will be done within the estimated hours.  Anything below 50% reliability needs to get a second opinion.  

If estimates are requested verbally, there is no reliability as it is void unless it’s written down.  Always ask the BSA to make the task first.

## Presales Estimates

When a development is sold with a Subscription and Success Pack, a Presales Estimate can have been given. The pre-sales consulting team separates out functionality that can be done with Odoo out of the box from items that will need development. An estimate is given for the items that need development, which can be very general based on the details provided. 

These estimates can be used as a guideline, but specs may have changed when the BSA creates a development task. Make sure to double-check that the estimate is correct or if additional/fewer hours are needed based on the final requirements. Reach out to the pre-sales team to sync up on any questions.

## Other Considerations

Hourly estimates are not necessarily additive in terms of time, but you can combine them to give an average time to do them in bulk, ie, if you are adding multiple fields it won’t take each field 1h to implement.  In other words, these values are just a baseline.

This section should be a little less relevant, as we are using the ps tool now which gives a more specific break down, but things like testing or set up/pushing code can be lumped together still. Remember you can always add more sections to the ps tool breakdown and manually change or set anything you need. 

- Estimations include start-to-finish stages of development:
- Reading spec
- Setting local env
- Doing dev on local
- Pushing code on GH
- Preparing dev/staging branches
- Testing on dev/staging
- Sending to customer

As a precautionary measure, if your estimate is 40h+, get a second opinion from another team member.

# Giving the Estimate

## Format

#### Follow the Format

```text
[Trigram] 00:00 Hours (~ X LOC / Odoo Managed SH Required/Not Required)
…
…
…
Technical Notes:
*general direction/functions/workflow for developer to follow/get started*
```

#### Example:
```text
[JOT] 24:00 Hours (~500 LOC/ Odoo Managed SH Required)
…
…
…
Technical Notes:
    1. [1 hr] Inherit _get_columns_name() in account_followup/models/account_followup_report.py to remove Source Document column header and rename the others
    2. [2 hr] Inherit _get_lines() in same file to remove source document column in each line
    3. [1 hr] Setup and testing
```

## Where do I timesheet doing estimates?
Starting January 1st 2023, we now timesheet all the time spent on Analysis(working on the estimate) on the task itself. 


## Estimation Steps:

1. Pick a Gray task from the Tech Review Stage.
    1. If the task is already assigned, that means someone else is already working/worked on it.
2. Assign yourself to the Development Task 
3. Check that Reviewer, Parent Task, Sale Order Item, and Subscription Fields are filled out.
   1. If not, ask the BSA to fill them out before giving the final estimate. 
   2. Or you can fill it out yourself if it's quick, and you are certain they are the right values.
4. Use this Guide to do an Estimation + PS tool. 
   1. Use the New ps-tool to do the estimation
      1. https://ps-tools.odoo.com/web#cids=4&home=
   2. Video recording of how to use the tool - Team Meeting
      1. https://drive.google.com/file/d/19hoLmJC67dl5uTVSuOiT0BdnjAoCBgNs/view
5. Calculate the LOC with the formula(see formula section above in this doc). 
6. Note if the development Requires an Odoo Managed SH project or if Saas is okay.
   1. Remember: Only QWeb and Mexican Addendas are allowed on Saas database. Otherwise, SH is required. 
7. Put the Estimate line in the description of the Development Request Task under the text “Planned Hours:”. 
8. Write Technical Details and break down the Estimation under the general estimate
   1. Give reasons why each section will take that amount of estimated time
9. Write Implementation Details under Technical Notes'
   1. Go into detail about the design idea that was in mind that lead to the final estimate and estimate breakdown  
   2. Doesn't have to be super long, just as long as the point and explanation gets through
10. Set the Allocated Hours and Estimation Reliability Fields in the “Timesheets” tab of the task.
11. If you are new to doing Estimates, keep the task in the Kanban Stage “Tech Review” and mark the Kanban color to Green.
    1. A senior team member will review the estimate and let you know if any changes need to be made or if you can send out the estimate. 
12. Log a note with the template “LN01”. 
    1. Make sure Reviewer is set to the BSA
    2. Important: Add the “(~ X LOC / Odoo Managed SH Required/Not Required)” part somewhere in the Log. Paste it into the template. 
13. Move the task to “Scoping” Kanban Stage, you can keep yourself assigned to the task if you want to do follow ups. 

## Estimation Customer Approved Steps:

1. Make sure the BSA has logged a note with the approval in the Chatter. 
   1. Not necessary for them to provide proof of approval, but it’s okay if they did
2. For SH developments, verify if the customer has an SH project:
   1. If Customer has SH:
      1. If Odoo managed:
         1. No Action need
      2. If NOT Odoo Managed: 
         1. **!!Talk to CIC before continuing!!**
   2. If Customer does NOT Have SH but dev Requires SH:
      1. Remind the BSA that the customer needs SH to continue, and they must migrate
      2. If they need help tell them we can assist, and they can make a duplicate of the tech ticket
   3. Block the ticket Red until they migrate to SH
3. If customer’s Dev is approved to be on Saas:
   1. Do Nothing
4. Do one last verification that the Sale Order Item is set on the task.
   1. Important: If it is not set, the pack hours will not be deducted from the Parent task when logging timesheet
5. Verify that the customer has enough pack hours left on their pack.
   1. If they have less than the estimated hours
      1. Block the task and request the customer to purchase more hours
6. Edit the task
   1. Change stage to Planning
   2. Set Deadline to current date(day we moved the task to planning)
   3. Green the Kanban State Color
7. Copy the Requirements Specification from the Task Description and the UAT Steps from the UAT Section
   1. This is important and must be done, so we have a hard copy of the spec and UAT
8. Important: Send C01 email template and paste in the Requirements Specification/UAT Section between:
   1. ----- SPECIFICATION START ----- 
   2. ----- SPECIFICATION END -----
9. Post a link to the task in psus-updates channel in Discord
