---
layout: post
title:  Tech Quickstart FAQ
permalink: /docs/project/qs/quickstart-faq
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

# Frequently Asked Questions

## What do I do if hit the initial Estimation Reliability?
For example, the development is 10:00 hours with 70% estimation reliability. This means that it can be +/- 30% of hours, so max would be 3:00 hours additional to the original estimation(total 13:00 Hours max). In this scenario you currently have timesheeted 13:00 hours and the development is not completed yet.

1. **Stop working on the task immediately and block the task** 
2. Assess why the development is not complete. If the reason is:
   1. Scope Creep (New Requirements)
      1. See the Scope Creep FAQ below
   2. Change Request
      1. See [[Change Request Doc]({{ site.url }}{% link docs/project/tech-quickstart/change_request.md %})] and give an estimation
   3. Initial estimation was underestimated
      1. Check with Original Estimator/Project Leader to see if something was missed in your implementation. 
      2. Estimate how much additional time you need if the original estimation was underestimated.
      3. Give the estimation of the additional hours you need to the BSA with detailed reasoning of why you need the extra hours. 
      4. Get approval for these extra hours. Do **NOT** continue developing past the estimation reliability max unless the customer approves the hours. 
      5. Once the customer has approved adjust the Allocated Hours to include the new estimated time. 
      6. Update the Description under the original estimate with the additional hours needed. 
      7. Continue the Development 
   4. There are bugs in my implementation, the customer reported errors in UAT feedback
      1. Check with Project Leader/original estimator developer to see if something was missed in your implementation. 
      2. Project Leader will decide whether we will do the hour adjustment later or your time taken to fix the issues should go in to self learning, or if some other exception will be made. This will be decided on a case by case basis. Do **NOT** continue developing past the estimation reliability.
      3. After a decision has been made, continue the Development. 

### What do I do if I've already gone past the Estimation Reliability? 
1. If this happened before October 30th 2023: 
   1. Reach out to the Tech Quickstart Project Leader(AAL, or CIC if AAL is not available).
   2. We will decide what to do on a case-by-case basis. 
      1. This can still result in your hours being adjusted from the task.
2. If this happened after October 30th 2023: 
   1. Was there an exception made? 
      1. Reach out to the Tech Quickstart Project Leader.
   2. If no exception, the hours over the Estimation Reliability with no customer approval will be Adjusted down to the Estimation Reliability.
      1. Adjusted Hours do **NOT** count towards your KPI.
      2. This will negatively affect your KPI and Appraisal.

## What is Scope Creep?
Scope creep is anything that the customer asks for that is not in the original specification. These are new requests that were not added to the task requirements.

### How to handle Scope Creep
1. Assess if the new requirements are related to the existing development
   1. If the new features are unrelated, this should be a new development
   2. Ask the BSA to create a new development task, and they should follow the standard quickstart flow
2. Estimate the additional Requirements
   1. If the new requirements are over turn out to be way bigger than the existing development, ideally this should be in a separate development. 
      1. Check with the Project Leader on what to do with these new requirements, we will decide on a case by case basis. 
   2. Make sure to include the time you spend Estimating the Scope Creep in the new Estimation. Just as any other regular estimation, we include the analysis time in those Estimations as well. 
      1. Scope Creep Estimation: 
         1. Total Estimation = Estimation + Testing(20%) + Analysis Time
3. If the Estimate is over 8+ Hours, have the Project Leader review and approve the Estimate
   1. ping AAL on the task and ask for a review, ping CIC if AAL is not available
4. Send the Estimate to the BSA to get the Customer's written approval
5. If the customer Approves the Estimate
   1. Confirm we have written approval from the customer(usually a screenshot)
      1. Do not continue until we have written approval
   2. For tracking the BSA **must** update the development specifications. Have the BSA add the new points, add new UAT cases and highlight everything(either in a color highlight or color font, like red or yellow). This way it is very clear what is different from the original spec. This is extremely helpful for the upgrade team in the future. 
   3. For tracking the developer **must**: 
      1. Update the Allocated Hours to be initial estimate + additional change request estimate
      2. Update the description under the original estimate with the additional estimate
         1. Example: 
         ```text
            [CIC] 20:00 Hours (Odoo Managed SH Required / ~300 LOC)
            [CIC] 8:00 Hours ( ~100 LOC) 
         ```
   4. Then continue the Development
6. If the customer does not approve the Estimate
   1. Ask if the customer wants to continue the Original Development
   2. Or if they want to cancel the Development

### What if the requirement was mentioned in the UAT test cases but not the specification? 
This is still scope creep if the Estimator did not consider this in the estimation. The BSA should be putting all the requirements inside the Requirement section, they cannot just sneak it into the UAT cases. In this scenario estimate the scope creep and ask for approval of these additional hours. 
