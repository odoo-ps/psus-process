---
layout: post
title:  "Services"
permalink: /services/
date:   2022-08-29 10:19:51 -0700
categories: jekyll update
---

# What is what? 

1. Pre-Sales
   - Presales technical support refers to technical advice or estimate related activities that occur bedore sale has been closed
2. Upgrade
   - Upgrade refers to upgrading customer's instance/databse from version A to version B
3. Migration
   - Migration refers to process of moving customer from their old software solution to new software solution, i.e. moving customer from Quickbooks to Odoo. Upgrade is not equal to Migration
4. Maintenance
   -  Maintenance refers to providing ongoing support to customer if a customer agrees to Odoo’s Custom Code Maintenance Policy and pays an ongoing maintenance fee
5. Technical Support
   - Technical Support allows a customer/partner to use Success Packs hours to get technical consulting with Development Services Team

# [Customization VS Development](https://github.com/odoo-ps/psus-process/wiki/Difference-between-development-and-customization)

# Services Offered
## Pre Sales

- All pre sales requests are managed under project “PSUS - PreSales”.
  - Process Leader Technical: Ben ([bmu@odoo.com](mailto:bmu@odoo.com))
  - Process Leader Functional: Massiel ([mac@odoo.com](mailto:mac@odoo.com))
- Customization and Development is not same at Odoo 
- Get a quote of possible developments early and set expectation in sales
- All developments will require Odoo.sh 
- Exception is QWeb Reports or MX Addenda Developments
- Most small business customers do not understand how project management works so setting expectation about lead time, task estimates, timesheet and success pack hours consumption is key and helps in building successful work relation.
- Some effects of developments on QuickStart project implementation :
- Slows down QuickStart project implementation
- Development creates a delay in upgrade

### How to get a quote of developmet during Pre-Sales
- Make a copy of the following template task : [[TRIGRAM] Prospect Name : Requirements Short Title (Make copy of this)](https://www.odoo.com/web#id=2260536&cids=3&menu_id=4720&action=333&active_id=3138&model=project.task&view_type=form)
- Or send a direct email to  “[psus-presales@mail.odoo.com](mailto:psus-presales@mail.odoo.com)”
- Smart button on sales lead
- For more information on the Pre-Sales process, [check out this presentation](https://docs.google.com/presentation/d/1xqhNsesJd1UVw26ggFjfk8eCO00sf7S7THUIgi5nvms/edit?usp=sharing)

### What we don’t develop :
- e-Commerce integration (Odoo does offer OOB eCommerce solution)
- Connectors to self-hosted systems or home grown/developed systems
- Any automation that does not save time or does not help improve process when implementing Odoo
- API Integration for any feature that is available in Odoo
- Anything that looks like customer’s existing system
- Debranding (some exception may be allowed) or Backend Theme customization
- This is not a complete list, integrations may by approved on a case by case basis 

### Pre-Sales Estimates
- Pre-Sales estimates include the time required for development, technical analysis, integration, project management, and functional analysis. - Time is also built in for a reliability ratio on the development hours
- This complete estimate sets realistic expectations for project implementation
- Estimates are calculated [using this spreadsheet](https://docs.google.com/spreadsheets/u/0/d/1waWz4-JIwCi_ogosXXYV8wtamKZiTQwYAYtlb4lFjY8/edit) by the Pre-Sales consultant
- In certain cases, a lower functional weight may be applied to the estimate if agreed upon by the technical & pre-sales consultants 
- A lower functional weight may be used for projects where the development will require a larger proportion of hours compared to the functional implementation
- Possible examples include new payment acquirers and delivery carriers

### Pre-Sales process diagram

![image](https://user-images.githubusercontent.com/104387570/186529954-0ad7c914-eede-4873-bd7d-63379a8a0326.png)

[How to create a development request during sales ?](https://youtu.be/AVIB-dEYIQE)


## Development Requests
- All the development requests are managed under project “PSUS - Tech Quickstart”.
  - Process Leader : Cindey ([cic@Odoo.com](mailto:cic@Odoo.com))
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
If we do not receive any feedback within six weeks of when the task enters User Acceptance Testing(UAT), the task will be canceled. 
Any hours consumed to develop and test the development will still be consumed on the success pack. 
No Maintenance Fee will be charged once the development has been canceled. 
Upon customer request that the development is still required and feedback is provided, the development task can be reopened and resumed. 
However, the task will be moved back to the Planning stage and will be pending the assignment of a developer with the current development lead time. 
The previous developer may or may not be assigned to the same task.
More hours may be consumed than the initial estimate when task is reopened.




