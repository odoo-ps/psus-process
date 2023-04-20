---
layout: post
title:  "Development FAQ"
permalink: /docs/process/qs/faq/
parent: Tech Quickstart
grand_parent: Process
nav_order: 6
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# PSUS - Tech Quickstart FAQ

## General Info
Project Leader: Cindey Caine(CIC) + Ali Alkaheli(AAL)

Project Link: [PSUS - Tech Quickstart](https://www.odoo.com/web#action=333&active_id=360&model=project.task&view_type=kanban&cids=3&menu_id=4720)

Task Template(Make a Copy): [Template](https://www.odoo.com/web#id=2684795&cids=3&menu_id=4720&action=333&active_id=360&model=project.task&view_type=form)
### What types of Developments are NOT allowed?
1. Odoo Debranding
   1. Exception: “Powered by Odoo” on email templates/website
2. Whole Website Themes
3. e-Commerce integrations (we already have solutions)
4. Connectors to self-hosted systems or home grown/developed systems
5. Any automation that does not save time or does not help improve process when implementing Odoo
6. API Integration for any feature that is available in Odoo
7. Anything that looks like their existing system

### What Developments are allowed on the Saas Platform (Odoo SH not required)?
1. QWeb Only Reports
2. Mexico Localization Addendas ([doc](https://www.odoo.com/documentation/15.0/applications/finance/accounting/fiscal_localizations/localizations/mexico.html))

### What API Connector Developments are allowed?
For the PSUS team to consider an API Connector we need several things:
1. Clear Documentation from the API
   1. Example: Link to API, PDF of Documentation, etc.
2. Access to an API Testing environment
   1. Example: API Sandbox Account, Testing Account, etc.
3. Flowchart or written flow of the actions that will happen between Odoo and the API software
4. Exact Requirements of the Connector and what information will be transferred
5. Field mapping in the API and Odoo(if required)

If these requirements are not met, we may request additional information from the API Software or we may decline to proceed with the Estimate/Development.

### Can IoT Box Drivers be developed?
No, the PSUS Technical Team does not do IoT Box Driver development. The customer should contact a Partner or use the Odoo Developer on Demand service for these requests. ([Info](https://www.odoo.com/page/developers-on-demand))

### SPS Commerce EDI Developments
1. EDI Experts(who to contact with questions):
   - Ben(BMU) (SF office)
   - John(JOT) (BF office)
2. SPS Commerce Integration Options
https://docs.google.com/document/d/1DwWyriV_Kj53EqmDostZoY8FXZ0whAVdU-zNHIv9T1w

### Can Developments be done for Partners?
Yes, the Partner must have a partner pack/partnership.
Some Rules:
1. The Partner will not be charged a Maintenance fee
2. The Partner will be responsible for Testing and installation into their or their customer’s database
   - We will give the customer a zip file of the module to test and deploy into Production
3. If there are any errors or changes, the Partner will need to use pack hours to resolve these

### What if the Customer no longer wants the Development?
If the Development is still in progress, we cancel the development. The pack hours that the Developer took to do everything so far will stay on the ticket. The customer will not get charged any Maintenance fee if they want to cancel the development. <br />
If the Development is in Production, and they are currently paying Maintenance fees, we can remove(uninstall) the development and remove the code from their database. The Account Manager will be responsible for removing the Maintenance fee from their subscription. Create a ticket in PSUS - Technical Support to have this done.

### What if the Customer doesn’t want to pay the Maintenance Fee anymore(ex: goes to a Partner) or if the Customer wants ownership of the Github/SH Project?
We will transfer the SH Project and Github Repository to the Partner or Customer. Talk to Cindey(CIC) to initiate this. The Account Manager will be responsible for removing the Maintenance fee from their subscription.<br />
Any issues with the original Development will not be covered anymore once they stop paying for Maintenance. If the Customer wants the PSUS Team to fix any issues/bugs, they will need to have Success Pack Hours, and we will use those to resolve any issues. <br />
The PSUS team will only upgrade the code in the future if the customer agrees to pay 12 months of backpay LOC maintenance and agrees to pay maintenance going forwards for all their custom modules. If the customer has added other 3PA or custom modules developed by a partner, they will be subject to a code review. The PSUS team can refuse to maintain the code if it is not up to our coding standards or has excess code that is not viable. The customer must also agree to transfer their Odoo.sh project to the PSUS team.

## Odoo Studio: Not Allowed in Developments
### Why are Studio fields/models/etc. not allowed in Developments?
We want all developments created by the PSUS Technical team to be usable(installable) into any database with no dependencies except on standard Odoo code. We do not allow any Studio created fields/models/views/groups for this reason. <br />

Other reasons that using Studio in developments can pose several issues:
1. Studio fields/models/views/groups can be deleted
   - If the field, for example, gets deleted, this will break the development and create errors
2. Studio fields/models/views/groups maybe be changed during Upgrade
   1. Everything done in Studio is stored in Odoo via Data(no python code gets created by Odoo).
      1. Python code can get added to studio created objects(ex: server actions can contain user added Python code)
   2. During Upgrade, there may be changes to the Studio data. This may cause errors in the development.
   3. Studio Data Upgrade(values in the studio fields) is handled by the Upgrade team in IN and BE in the script that is run to upgrade the database. The PSUS team only handles code upgrades and errors from the studio created python code/views if any.
   4. If the development depends on Studio, this would add more time to the upgrade process as more communication would need to be done between upgrade teams.
      - We want to separate studio from development to prevent these issues

### How to keep the data in Old Studio fields in new Development fields?
We request the BSA to export the data from the old field(s) and import them into the new field(s). This can be done with a UI import and export with a CSV or XLS file. <br />
Example:<br />
Old Studio Field: x_studio_project_manager <br />
New Python Field: project_manager<br />

The Developer will give a list of new fields that are mapped to the old studio fields. If they did not provide the list, please request this from them.
