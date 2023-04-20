---
layout: post
title:  "Development Policies"
permalink: /docs/process/qs/policies/
parent: Tech Quickstart
grand_parent: Process
nav_order: 3
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# PSUS - Tech Quickstart Info/Policies
## PSUS Development Guidelines and Policies
This policy began on May 1st, 2021.

### This Policy Affects:
1. All customers who have purchased Subscriptions after May 1st, 2021.
2. Any customer with no previous development done with PSUS Technical Team
Including any customers with Subscriptions before May 1st, 2021.

### Rules for PSUS Developments:
1. PSUS Technical Team reserves the right to select what development requests Team may not accept the development request based on feasibility and technical limitations, or if a workaround can be proposed to solve the given business use case.
2. Any technical specification or design Idea written in the task description is treated as a suggestion. The feature development design is done independent of any suggestion based on developers own Ideas and thought process with the Odoo framework in mind. This allows developers to make simple and the most efficient solutions to solve given requests.
3. PSUS Technical Team must own the SH Project and Github Repository
4. Customer will not have access to the SH Project and Github Repository(with exception mentioned below)
   1. Their Business Analyst can have access to the SH Project
   2. Their Account Manager can have access after Success Pack is finished and Project Implementation is over
5. No customer created developments are allowed in the SH Project
6. No Third-Party Apps are allowed in the SH Project except
   1. The following connectors:
      1. Shopify/Woocommerce/Magento connectors
      2. For these ecommerce connectors, the customer must install(Click Install button in Apps app) and manage these themselves, PSUS Technical Team will not help with these
   2. Code Reviewed and Approved 3PA
      1. If the customer wants to install any App/Module that is not developed by Odoo
         1. They must first purchase/get the code and have a Code Review done in the PSUS - Maintenance Project
         2. Talk to Keyur(KGA) to get more information or initiate the process
      2. This 3PA will be charged with LOC Maintenance
7. The customer must pay Line of Code(LOC) Maintenance per each 100 Lines
   1. Final LOC is rounded to the nearest 100 ceiling
      1. Example: 1240 LOC > Rounded up to 1300 LOC

### Exceptions(Updated as of January 2023):
1. Partners can own their github repository. PSUS team will do the development but will not charge pack hours. For any bugs or upgrades requested by the Partner, they will need pack hours to resolve the issues. 
2. Customers can have access to the SH project(Only, No Github Access) if they take the official Odoo Technical Training


All development requests require customers to have enough remaining success pack hours to begin the development(the balance should be at the least the given estimated hours + 30% of the estimate). If customers do not have hours after an estimate is given then the request will stay on hold until they buy enough hours and they will be pushed back in the queue.

All developments are served on a First Come, First Served (FCFS) basis. After the customer approves the development, there will be a lead time to start the development request. Please, check with the Technical Team to confirm the current lead time to set the right expectations with the customer.

Please set these expectations if a customer is requesting developments done by the PSUS Technical Team. Any further questions or concerns can be directed to PSUS - Tech Quickstart Project Leader, Cindey(CIC).

## Odoo.sh branch management policies (August 4th 2022)

Our goal of this policy is to avoid BSAs losing any configuration or data that was created during testing in the staging branches. We want to maintain the work that has been put into implementation while also giving the developer a place to work and finish their task as smoothly as possible.

Developers may need to rebuild staging branches for different reasons, some being: the code will need to be pulled to a new database, the data on the staging branch is outdated and needs to pull a new copy from production, upgrade requires restoring a dump for testing, etc.

For Odoo Managed github repositories and SH projects, the Odoo PS team adheres to the following conventions:
* Odoo.sh with one staging branch: we will name the staging branch “sandbox”
* Odoo.sh with two or more staging branches: we will name one branch “sandbox” and second branch “dev-staging” and rest will named to BSA or Customer liking

“sandbox” branch is for functional testing/configuration. It should always be updated to the code/data of production. The data should not be more than 3 months old.

“dev-staging” branch is for developments/upgrades/bug fixes. And this branch should not be used by the BSA or the customer to enter large data or testing configurations.

Customer owned SH projects will have naming conventions based on their own processes, but we do recommend them to follow the ones we have listed above.

The PSUS - Tech Quickstart development task template has been updated to include a section for the BSA to fill out which staging branch the customer grants access/control over for the duration of the development. For PSUS owned SH projects we will use the “dev-staging” branch by default for development.

For version upgrade tasks, the developer will request which staging branch they can use for the upgrade. There should not be any development going on at the same time as an upgrade. For PSUS owned SH projects, the developer may replace the “dev-staging” branch with an “version-upgrade” branch for completing the customer upgrade request .

For maintenance tasks, the developer will request which staging branch they can use for the bug fix. For PSUS owned SH projects, the developer will use the “dev-staging” branch for investigation and testing.

If in the case the customer only has one staging branch, this will be the branch Odoo Developers will also use during the duration of all the development requested. However, we have always highly recommended that the customer must purchase a second staging branch in this case. (NOTE: We are unable to guarantee that a branch will not rebuild with a single branch. Odoo.sh Platform may auto rebuild a branch, if it experiences technical difficulties during merge or upload of a database. The developers have no control on this. However we will try our best to follow the policy and save the build if we can by making manual backups beforehand).

Or if they are deciding to use SH, to purchase two staging branches to begin with. We always recommend having one dedicated development staging branch and one dedicated sandbox staging branch for function testing and configuration.

The customer can choose to go back to one staging branch after the development/upgrade is completed. They can only pay for it during the length of the task.

The specified staging branch will come with the following rules:
* The developer can/will Rebuild the staging branch at any time without prior notice as required
* The developer will be pushing code to the branch as required
* The developer may change staging branch configuration and create random data for  testing in the staging branch
## Summary
* If a customer has only one staging branch then the Odoo Developers are required to make a manual backup of the staging branch before rebuilding as a precaution. This way if it ever needs to be restored, we do have a copy of the data. Important note here, this manual backup may increase their storage usage and also on SH, manual backups are kept for only 7 days.
* If a customer has more than one staging branch then, the Odoo Developers will always use a staging branch named “dev-staging” unless a specific branch name is specified in the task. The developer will not make any manual backup of this branch and may rebuild the branch as required. No configuration should be done on this branch for testing purposes. This branch should not have stale data, i.e. older than one month.
It is the BSA's responsibility to educate customers on how these branches are managed and the rules around it.

## Estimation Policy Change January 1st 2023:

Development Services (PSUS) team’s Estimation Policy for quickstart development requests that will be applied starting January 1st 2023. 

### New Changes:

1. All (PSUS - Tech Quickstart) Estimation Time will be taken from success pack hours
   1. The estimation time taken will be added to the final total estimation time 
   2. Development Estimation + Estimation Time = Final Estimation 
   3. Ex: 10 hours + 2 hours = 12 hours total 
   4. All estimations will still have estimation reliability in case the customer changes their mind about small things or has multiple rounds of UAT feedback
2. The Estimation will now provide a Deliverable Estimation Outline
   1. The outline will provide a detailed breakdown of functionality and how the Final Estimated hours are distributed throughout the development
   2. This outline can be sent to the customer

All new development requests starting 1st of January will be applied with this new policy change. All existing and new customers will be affected regardless of what maintenance or pricing policy they are on. This will drive us to give estimation at higher accuracy, which in turn will help us reduce estimation hours over all for all kinds of requests, this also means we will take some time upfront doing better estimation even for smaller developments.

This means that all the time that a developer uses to research and give an estimation of a task will now be billed to the customer with success pack hours. If the customer does not approve and cancels the development, the success pack hours used will stay on the canceled task and will still be deducted from the customer’s pack. 

Presales estimates(PSUS - Presales) will not be affected. Presales do not require a success pack to get an estimate. Presales estimates are still rough estimates that may change when the actual development is requested. 

If an Estimate(PSUS - Tech Quickstart) previously had a Presales estimate(PSUS - Presales), it will still require success pack hours to get the Final Estimate. We do not provide a deliverable estimation outline in Presales but will need to provide one in Tech Quickstart with this new policy. 
