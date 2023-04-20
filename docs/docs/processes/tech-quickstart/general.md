---
layout: post
title:  How does it work?
permalink: /docs/process/qs/general
parent: Tech Quickstart
grand_parent: Process
nav_order: 1
---


# Service


# How does the pipe works


# Rules



# BELOW INFO TO BE CLEANED


## Development Requests
- All the development requests are managed under project “PSUS - Tech Quickstart”.
  - Process Leader : Cindey([cic@Odoo.com](mailto:cic@Odoo.com)) + Ali([aal@Odoo.com](mailto:aal@Odoo.com))
- See if development request can be avoided by:
  - Making customers try/use OOTB (out-of-the-box) Odoo
  - Proposing work around (project app can be used in many different ways)
  - See if they are willing to change their business process and save development cost.
- Pay attention to following:
  - Review your all developments when you are doing pipe review with your Coach/TL.
  - All development requests must be reviewed and approved by a Coach/TL and Process Leader.
  - Initially hours is simply estimate of hours given based on our experience for given feature(s), but a developer may end up using more or less hours.
    - The final hours that are charged to customer is based on hours spent on task (timesheets).
  - Once the task is in development the specification is frozen and no new changes(Scope Creep) are accepted, so please make sure customer review the final specification before they give it go.

### How to start development request
- To start new development request; make a copy of the [Development Template](https://www.odoo.com/web#id=2832993&cids=3&menu_id=4720&action=333&active_id=360&model=project.task&view_type=form)
- Task title should follow the following naming conventions :
  - [TRIGRAM] Customer Name : Quick Development Feature Title
  - Video demo on topic at the end slide demonstrates how to create a request
- To write development requirements specification follow development the request template from the Template task here:
  - [[TEMPLATE] [TRIGRAM] Project Name : Feature Title](https://www.odoo.com/web?debug#id=1971657&action=333&active_id=360&model=project.task&view_type=form&menu_id=4720)
    - (please do not create your own version of specification templates or remove things that does you do not have to fill)
  - Use numbering bullet (which can be used when detailed quote is required and also help in referencing something in chatter communication)

All Developments must have the following fields set:
  - Sales Order Item (sale_line_id)
  - Customer (partner_id)
  - Extra Info > Parent Task (parent_id)
  - Extra Info > Subscription (mnt_subscription_id)
  - If any of above field(s) is not set, the task will not be moved forward and you will be requested to complete this first.

Once task is set done (i.e. deployed in production), do-not reopen or follow-up on original development request task,  instead create a maintenance request under “PSUS - Maintenance” for anything not working as expected a.k.a. Bug Ticket.

“Estimation Reliability” lets you prepare a range of line count for the final solution using given estimated line count and also a range of hours that may be deducted from their pack.

Example: For a development with 10 Hours, ~160 LoC and 70% reliability (i.e. 30% is variable here)

- You can tell the customer the hours taken from the pack can be between 7.0 Hours (10.0 - (10.0*0.3)) to 13.0 Hours (10.0 + (10.0*0.3)) but on average it is 10.0 Hours
- Same with lines of code 112 LoC, 160.0 - (160.0*0.3) to 208 LoC, 160.0 - (160.0*0.3)
- A reliability of at Least 7.0 hours and at Most 13.0 hours

### User Acceptance Testing
- If we do not receive any feedback within six weeks of when the task enters User Acceptance Testing(UAT), the task will be canceled.
- Any hours consumed to develop and test the development will still be consumed on the success pack.
- No Maintenance Fee will be charged once the development has been canceled.
- Upon customer request that the development is still required and feedback is provided, the development task can be reopened and resumed.
  - However, the task will be moved back to the Planning stage and will be pending the assignment of a developer with the current development lead time.
  - The previous developer may or may not be assigned to the same task.
  - More hours may be consumed than the initial estimate when task is reopened.

[How to create a development request when implementing a quickstart project?](https://www.youtube.com/watch?v=ecglLX92G2o)



# Customization
Project Leader: Cindey Caine(CIC)

Project Link: Ps - US Tech Quickstart

Task Template(Make a Copy): https://www.odoo.com/web?#id=2580653&action=333&active_id=360&model=project.task&view_type=form&cids=3&menu_id=4720
How to start a Development request:
Make a copy of the Task Template
The Title should follow the naming convention:
[TRIGRAM] Project Name: Feature Title
e.g. [JAM] Winterfell: Make a new castle
Fill out the Task Template (Requirements)
Please do not create your own version of specification templates or remove things
Fill out the following fields on the Task Template:
Customer
The Customer for the Task
Parent Task
The Customer’s Quick Start Task
Subscription
The Customer’s Subscription
Sale Order Line
The Sale Order Line for the Parent task
This will usually auto-fill if the Parent Task is set Properly

How to get a development Estimate:
Make sure Task Template is Complete
Mark the Ticket Kanban State to Red
Ping your Team Leader to Functionally Review the Specification Request
Fix any issues they bring up
If they Approve(in task chatter), you or your Team leader can mark the Ticket Kanban State to Green
Next, a member of the Technical Team will Review the Specification
They may ask you clarifying questions on the Requirements
If the Specification requires more info or investigation the task will be moved to the Tech Review(PSUS) Stage
Once ready, the Technical Team will Ping you with
Estimated Number of Hours
Estimated Lines Of Code
Estimated Reliability
The Task will be moved to the Scoping(PSUS) Stage

What Happens When the Customer Approves the Estimate:
Ping the Technical Member who Estimated the Task with the Approval
Not mandatory, but you can attach the proof of Approval from the customer to the Task
The Task will be moved to the Planning(PSUS) Stage
A Member of the Technical Team will Assign themselves to the Development
Once Assigned, they will move the Task to the Development(PSUS) Stage

What Happens When the Development is Ready for Testing:
The Developer will send an Email to You/Customer with:
Testing URL
Any Additional Instructions
Any Videos or Diagrams if necessary
The Task will be moved to the UAT(PSUS) Stage
The Customer will test the Development
If the Customer has Feedback
Ping/Message the Developer the Feedback
They will make the Changes if Necessary
Any New Requests(not in the original specification) will potentially require more Hour Estimates

What Happens When the Development is Approved for Production:
Ping the Developer with the Confirmation/Approval for Production
The Developer will Push the Development to Production
The Developer will send an Email to You/Customer when it is Done
The Task will be moved to the Deployed(PSUS) Stage
The Project Leader will Apply Billing
They will Add the Billing Maintenance Fee(MRR) to the Subscription
Only if it is required
If there are any Issues After the Development is installed to Production
See Maintenance Section Below

# Customization
Tasks that can be done by the functional consultant. Functional consultants should know how to perform all these tasks.

# Development
 Should be done by Odoo’s technical team

- SaaS Customers: there is a cap of 15 hours for developments. These should be simple developments (New PDF reports, modifying existing reports, new views, etc. Anything related to QWEB or MX Addenda), the technical team will evaluate if the development is feasible in SaaS.
- Odoo.sh Customers: No hour cap. If an integration is needed please refer to this document [Integrations](integrations doc).

Note: As a company policy if any development is done, internally (with Odoo) or externally (by the customer), the customer will be charged maintenance, make sure you make the customer aware of this to avoid any future conflict.

# Development vs Customzation
Anything that can be done with the drag and drop features of Studio’s interface is considered Customization.
This document specifies what is a Development beyond that:

| Customization | Development |
| --- | --- |
| 1. Main Studio Interface: <br />  - Adding/removing elements from view, editing PDF reports, etc) <br> <br> 2. Server/Automated Actions(except the ones specified on the development section) <br> - [Create/Update record](https://drive.google.com/file/d/1eSeY9r7IDvHIaaQcv1DKqH7vxefNf6v2/view) [(Value)](https://drive.google.com/file/d/1cskMiH4eIrv-5J3KEYNHO2zSX1iQatas/view) <br> - [All other types (send email, followers, etc)](https://drive.google.com/file/d/123AR2ClE99M9-E9oYH5FRY515vXyH_y9/view) <br><br> 3. Data structure <br> - Creating a new Model <br> - Creating fields <br> - Creating related fields (non-stored) <br><br> 4. Access Control List <br><br> 5. Imports <br> - Trough the UI: Anything that does not require a script such as: Master Data like partner, product, BOM, etc, and Business data like SO, PO, MO, etc. <br><br> 6. Email Templates: <br> - Simple email templates with one level or two level dynamic placeholders, no python code used or advanced conditional operations <br><br> 7. Odoo.sh <br> - [Rebuild Builds](https://drive.google.com/file/d/1XlNssqokY7rqs03GWH5tW8UxkIelgYBE/view?usp=sharing): If a customer requires an updated testing instance. | 1. Server/Automated Actions: <br> This applies for Server or automated actions that have the following configuration. <br> - When the Action To Do = Execute Python code <br> - When the Action To Do is either Create a new Record or Update the Record and the Evaluation Type in the Data to Write page  is either Reference or Python Expression <br> - Automated action based on time condition <br><br> 2. Views: <br> - Editing QWeb / HTML / XML (even if it was created through studio) <br> - Creating new view (XML, QWeb reports, Website views), or your own inherited view  <br> - Editing CSS, JS <br> - Change layout/behavior of  Calendar/Grid/Gantt/Graph/Dashboard/Activity views <br> - Editing standard financial reports or creating new financial reports <br><br> 3. Data structure: <br> - Computed fields <br><br> 4. Window Actions: <br> - Adding view mode <br> - Creating new action (any kind) <br> - Domain <br> - Context <br><br> 5. Record Rules (Editing / Creating) <br><br> 6. Imports (no maintenance): <br> -Everything that requires a script: Complex/historical data, Import moving business data like SO, PO, Accounting, MO, timesheet <br><br> 7. Website: <br> - Website styles such as: CSS, SCSS, JS, XML, Custom code through the code block feature <br><br> 8. Email Templates: <br> - If it requires advanced dynamic placeholders (navigating through various objects, like tags or one2many fields, more than 2 levels), loop operations to display tables, python formulas to format text, advanced conditional operations, etc. <br><br> 9. Odoo.sh (no maintenance): - Deploy, merge code into branches <br> - Installing 3rd party apps <br> - Creating an .sh project <br> - Restoring backup <br> - Creating/deleting branches <br> - Changing staging branches


This supplement document is designed to help you understand the development process and timeline which can be useful in setting expectations for customers and projecting delivery dates for development requests. This information is based on the amount of current customer development requests.

Full development requests have three different time factors that affect the timeline of delivery. These are Development Lead Time, Development Time, and User Acceptance Testing (UAT) Time.  Below is the explanation of what are those different lead times and how they affect the delivery timeline.

## Development Lead Time

The development lead time given is not a commitment to deliver the development at a given timeframe. Rather, it is a projected timeframe of when development can be assigned to start the development (remember many things could change this projected time but we try to keep our timeline close to what was originally projected).

The development lead starts when a task estimate is approved by the customer and the task is pushed to the "Planning" stage. Also, when a task is pushed to planning, the "Deadline" field value is set to the same day to give a quick idea of when the task was initially moved to planning.

Developments are planned and processed on a first come first serve basis to give equal opportunity to all customers (priority escalations are accepted on a case by case based on the Teamleader’s approval, remember escalating tasks affects other project timelines. For example, if someone is waiting N weeks and they are 1 week away from assigning and we have a large escalation then it will push waiting time for customers a few weeks behind).

## Development Time

Once development is assigned someone will work on it and the developer will prepare the first iteration of the solution based on the given written specification and use cases. Here it is important to understand that the developer does not spend 100% of their daily time toward just QuickStart new development requests, they also have PS Technical Support, Migration, and  Maintenance that they work on the side every day.

A developer spends about 40%-50% of their daily time on new development requests, 30% of time toward migration and maintenance, and 10% time toward ps technical support. If the development estimate is 24 hours, i.e. working days, then this development will usually be ready for testing in the next 7 to 8 working days (depending on their current workload).

## User Acceptance Testing (UAT) Time

Once a development is ready for UAT, it will be pushed to the UAT stage for Customer testing. Here's where we observed the longest wait time which is between four weeks and twenty weeks depending on customer availability and how responsive they are. In our experience, frequent follow-ups of UAT reminders help keep customers on track and test their development, which helps in saving some time in this stage.


With this formula to project when development will be ready is as following:

Development Ready Time = Development Moved Planning Date + Development Lead Time + Development Time + UAT Time

Example:
If we have 24 Hours of development request, approved by the customer today and we push to planning today

Development Ready Time = 21.2 Week

Today  + Lead Time (8 weeks as of May 21st) + 1.2 Week of Development Time + 12 Week UAT (Avg)  = 21.2 Week
