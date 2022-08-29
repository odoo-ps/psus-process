---
layout: post
title:  "Staging Rules"
permalink: /stagingrules/
date:   2022-08-29 10:19:51 -0700
categories: jekyll update
---

Our goal of this policy is to avoid BSAs losing any configuration or data that was created during testing in the staging branches. We want to maintain the work that has been put into implementation while also giving the developer a place to work and finish their task as smoothly as possible.

Developers may need to rebuild staging branches for different reasons, some being: the code will need to be pulled to a new database, the data on the staging branch is outdated and needs to pull a new copy from production, upgrade requires restoring a dump for testing, etc.

For Odoo Managed github repositories and SH projects, the Odoo PS team adheres to the following conventions:
- Odoo.sh with one staging branch: we will name the staging branch “sandbox”
- Odoo.sh with two or more staging branches: we will name one branch “sandbox” and second branch “dev-staging” and rest will named to BSA or Customer liking

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
- The developer can/will Rebuild the staging branch at any time without prior notice as required
- The developer will be pushing code to the branch as required
- The developer may change staging branch configuration and create random data for  testing in the staging branch

As a Strict Rule now onwards:
- If a customer has only one staging branch then the Odoo Developers are required to make a manual backup of the staging branch before rebuilding as a precaution. This way if it ever needs to be restored, we do have a copy of the data. Important note here, this manual backup may increase their storage usage and also on SH, manual backups are kept for only 7 days. 
- If a customer has more than one staging branch then, the Odoo Developers will always use a staging branch named “dev-staging” unless a specific branch name is specified in the task. The developer will not make any manual backup of this branch and may rebuild the branch as required. No configuration should be done on this branch for testing purposes. This branch should not have stale data, i.e. older than one month.

It is the BSA's responsibility to educate customers on how these branches are managed and the rules around it.








