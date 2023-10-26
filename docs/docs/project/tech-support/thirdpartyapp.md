---
layout: post
title:  "Third party app"
permalink: /docs/project/support/3pa/
title:  "Third Party Apps"
permalink: /docs/process/support/3pa/
parent: Tech Support
grand_parent: Project
nav_order: 2
---

# Preapproved Third Party Apps
## PSUS Team Install Flow:

1. Check if the 3PA is one of the approved ecommerce 3PA
   1. Usually the PSUS - Technical Support Project Leader should have checked
      1. Check with them if you are unsure if it is approved or not
   2. [CRM & Sales Rules](https://docs.google.com/document/d/1SAGTe5ql0bqsuV_9cSPvbIk-xjz66RcfLY4dWf-Pghc/edit#heading=h.bdgsb4dun3wx)
2. PSUS must own the github repo, if we do not, they should install it themselves
   1. You should already have github access in this case
3. Create a development branch, fork from production
4. Put 3PA code on development branch
   1. [Modify the Manifest to cloc_exclude the 3PA module](https://www.odoo.com/documentation/15.0/developer/cli.html?highlight=cloc_exclude#with-the-database-option)
   2. Make sure the exclude is:
      1. `"cloc_exclude": [‘**/*’]`
   3. Sometimes the 3PA may already have exclude but it might not be the all exclude like the snippet we need above ^
5. Merge 3PA development branch into a Staging branch
   1. You can check whether the lines have been excluded properly by running `odoo-bin cloc` in the odoo.sh shell, `-v`flag will show individual files if specific files need to be excluded
6. Customer should Install(click install in Apps) and Test
7. If the customer approves, create PR from the 3PA development branch into Production
   1. Do NOT merge Staging into Production, staging might have other code that is not approved for production yet(custom code, other 3PA code).
8. Customer Installs(click install in Apps) in their Production


## CAN SHARE BELOW STEPS WITH CUSTOMER/BSA

### How to install 3PA in Odoo.sh

1. Create a development branch, fork from production
2. Put 3PA code on development branch
3. (Optional) Install and Test 3PA on development branch
4. Merge 3PA development branch into a Staging branch
5. Install and Test 3PA on Staging branch
6. If everything works, merge 3PA development branch into Production
   1. Do NOT merge Staging into Production, staging might have other code that is not approved for production yet(custom code, other 3PA code).
   2. If Errors occur or app does not work, contact 3PA developer
7. Install 3PA into production

# Unapproved/Code Reviewed Third Party Apps

## Code Review Process

1. Check that the requested review has not been reviewed previously. The full list of reviewed apps is [here](https://docs.google.com/spreadsheets/d/1oEz2B8mlJFFQYGedOfEgSdw6nCnCCdLQjdJTXgsWTxg/edit#gid=0).
2. Review code. Use the same [process](https://docs.google.com/presentation/d/11dycRLfyHxE7WIgKqLR4Zmc69txwUR0zDAZDHqriMug/edit#slide=id.g14a4c23e845_0_20) as code reviews for PRs. For some rough guidelines, you can use Belgium's [doc](https://github.com/odoo-ps/psbe-process/wiki/Technical-analysis-specific-cases#code-review).
3. Update spreadsheet with list of approved and rejected [apps](https://docs.google.com/spreadsheets/d/1oEz2B8mlJFFQYGedOfEgSdw6nCnCCdLQjdJTXgsWTxg/edit#gid=0)
4. Install the app if you approve it. Use the standard UAT process for developments in Tech Quickstart.
5. If this app is approved and installed, message Cindey(cic) to update the customer's LOC.