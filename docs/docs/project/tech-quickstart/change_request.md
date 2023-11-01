---
layout: post
title:  Change Requests
permalink: /docs/project/qs/change_request
parent: Tech Quickstart
grand_parent: Project
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

# Change Request

## What is a Change Request?

If a customer asks for anything that is not in the original spec then that is a change request. This can be things from, "I want the field name to say 'Project Leader' instead of 'Project Manager'" to "I want to add this same Manufacturing Costing flow to "Inventory" as examples. 

## How to handle Change Request in different Dev stages
### If the Change request is in:

### Tech Review
Official Estimate should not be finalized/approved by the Project Leader yet and should not have been sent to the customer yet. Re-estimate the development. 

### Scoping
Move the task back to Tech Review Stage. Developer who did the Estimation needs to re-estimate the development. Here the hours may increase or decrease depending on what was changed. 

### Planning
Move the task back to Tech Review Stage. Development should not have been started yet. Even if the customer has approved the original development, if they are asking for additional spec we need to re-estimate it. Here the hours may increase or decrease depending on what was changed. 

### Development & Code Review & UAT
Stop working on the task and block it, estimate any changes they are asking for.  Get the additional hours approved in writing before continuing the task with the new changes. The BSA needs to provide written confirmation in the task(usually in the form of an email screenshot). If customer does not approve the additional hours, we can either continue with the original estimated spec(no changes) or cancel the development.

### Deployed & Done
New Task needs to be created, we do not make changes to any task that has been deployed in production.

### Canceled 
Ask the Project Leader to move the task back to Requirements. Whole quickstart process is restarted. Can be moved back to Tech Review depending on Project Leader's discretion. 

## Change Request Estimates over 8 hours
If the change request estimate is estimated for over 8 hours, all developers must get approval/reviewed by the Project Leader(ping AAL on the task and ask for a review, ping CIC if AAL is not available). This is to make sure we are accurate on the change request estimate and that it is something we want to be doing. 

## If Change Request Estimate is approved
For tracking the BSA **must** update the development specifications. Have the BSA add the new points, add new UAT cases and highlight everything(either in a color highlight or color font, like red or yellow). This way it is very clear what is different from the original spec. This is extremely helpful for the upgrade team in the future. 

For tracking the developer **must**: 
1. Update the Allocated Hours to be initial estimate + additional change request estimate
2. Update the description under the original estimate with the additional estimate
   1. Example: 
   ```text
      [CIC] 20:00 Hours (Odoo Managed SH Required / ~300 LOC)
      [CIC] 8:00 Hours ( ~100 LOC) 
   ```  

## If there is any push back or issues from the customer:
Escalate to the Project Leader. 