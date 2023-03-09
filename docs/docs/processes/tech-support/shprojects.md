---
layout: post
title:  "Odoo.sh Migration"
permalink: /docs/process/support/sh-migration/
parent: Tech Support
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

# Saas To SH Migrations and New Project Creation
## Customer Options for Saas To SH Migration
The customer has three options if they want us to do a migration from Saas to SH platform.

### Option 1: For the May 2021 Policy of SH Projects Created/Managed by the PSUS Team, the customer must agree to these conditions:

```text
- Customer will NOT have access to the SH project and Github Repository
- PSUS Technical Team will maintain all aspects of the project and repository
- Third Party Apps can NOT be installed aside from the following ecommerce apps:
  - Shopify/Woocommerce/Magento connectors
```

### Option 2: The PSUS Technical Team can migrate the database from Saas to SH but the customer needs to:

```text
- Create the SH Project and Github Repository themselves
- Provide the Saas database URL and new SH project database URL
- Understand the PSUS Technical Team will be hands off for everything else (no custom developments, no assistance with 3PA installs, no assistance with creating/managing github, etc.)
```

### Option 3: New Creation of a SH Project owned and managed by PSUS Team. The customer must agree to these conditions:

```text
- Customer will NOT have access to the SH project and Github Repository
- PSUS Technical Team will maintain all aspects of the project and repository
- Third Party Apps can NOT be installed aside from the following ecommerce apps:
  - Shopify/Woocommerce/Magento connectors
```

## Saas to SH Migration Steps

### Option 1: Saas To SH migration(Odoo Managed)

1. Find the user’s Subscription in the Subscription App and take a screenshot of the price 
   1. If there are any automatic entries, the total might change, we need a snapshot before that happens
2. Use the email linked to the subscription, impersonate them, go to accounts.odoo.com.
   1. Go to accounts.odoo.com in incognito mode or a different browser. Using the email linked to the subscription (Subscription ->  Customer- >  Email) login with the password: <trigram/your_password> to impersonate the user.
3. Navigate to Profile -> My Databases and download the database from the gear dropdown icon and make sure the zip file extracts (i.e, it’s not corrupted).
4. Rename the database to something else 
   1. eg: \<existing-name\>-movetosh
   2. This will free up the domain name in about 15 to 20 mins.
5. In the customer’s Odoo Subscription, disable the database for the subscription 
   1. Cindey has the access to disable a database, so message her with the link to DB. 
   2. If she is not available, ask Jigar to disable it.
   3. Then check that the subscription is not linked to any database (stat button on subscription for database should have zero).
6. Set up branches in SH (production, sandbox and dev-staging). 
   1. If the SH project is being created for the first time, follow [this](#creating-an-odoo-managed-sh-project)
7. In the SH project make sure to drag drop the production branch to the Production stage.
8. Navigate to the BACKUPS tab of the production branch and upload the downloaded database using the import database button.
9. Rename SH database to target name (that was freed up by the Saas DB earlier) in project settings. Try to open SH production, this may show PSOD, but wait for some time for DNS cache to update.
10. Run Scheduled Action Id=3 (or whatever looks like the subscription server ping. Click on any scheduled action and change the id in the url to 3.)
11. Go to Subscriptions and verify that the user’s subscription is linked to one database.

### Option 2: Saas To SH migration(Customer Managed)
1. Find the user’s Subscription in the Subscription App and take a screenshot of the price 
   1. If there are any automatic entries, the total might change, we need a snapshot before that happens
2. Use the email linked to the subscription, impersonate them, go to accounts.odoo.com.
   1. Go to accounts.odoo.com in incognito mode or a different browser. Using the email linked to the subscription (Subscription ->  Customer- >  Email) login with the password: <trigram/your_password> to impersonate the user.
3. Navigate to Profile -> My Databases and download the database from the gear dropdown icon and make sure the zip file extracts (i.e, it’s not corrupted).
4. Rename the database to something else 
   1. eg: \<existing-name\>-movetosh
   2. This will free up the domain name in about 15 to 20 mins.
5. In the customer’s Odoo Subscription, disable the database for the subscription 
   1. Cindey has the access to disable a database, so message her with the link to DB. 
   2. If she is not available, ask Jigar to disable it.
   3. Then check that the subscription is not linked to any database (stat button on subscription for database should have zero).
6. Navigate to the BACKUPS tab of the production branch and upload the downloaded database using the import database button.
7. Rename SH database to target name (that was freed up by the Saas DB earlier) in project settings. Try to open SH production, this may show PSOD, but wait for some time for DNS cache to update.
8. Run Scheduled Action Id=3 (or whatever looks like the subscription server ping. Click on any scheduled action and change the id in the url to 3.)
9. Go to Subscriptions and verify that the user’s subscription is linked to one database.

### Option 3: New SH Project Creation(Odoo Managed)
1. Set up branches in SH (production, sandbox and dev-staging). 
   1. If the SH project is being created for the first time, follow [this](#creating-an-odoo-managed-sh-project)
2. In the SH project make sure to drag drop the production branch to the Production stage.
3. Run Scheduled Action Id=3 (or whatever looks like the subscription server ping. Click on any scheduled action and change the id in the url to 3.)
4. Go to Subscriptions and verify that the user’s subscription is linked to one 
database. 

## Existing SH to a new SH project steps
This can happen if the customer needs to move from one SH(github) to another SH(new github) with the same subscription.

### Option 1: Customer Owned SH to PSUS Owned SH
1. Ask the customer to agree to the following:
```text
- Customer will NOT have access to the SH project and Github Repository
- PSUS Technical Team will maintain all aspects of the project and repository
- Third Party Apps can NOT be installed aside from the following ecommerce apps:
  - Shopify/Woocommerce/Magento connectors
```
2. Ask the customer to transfer their github repository to ```cic-odoo```
   1. Have them follow these [instructions](https://docs.github.com/en/repositories/creating-and-managing-repositories/transferring-a-repository#transferring-a-repository-owned-by-your-personal-account)
3. Tell CIC to be on the lookout for a repo transfer
4. Afterwards, [CIC] will do the following steps
   1. Check if there is Custom code
      1. If yes does the customer want to:
         1. Have PSUS maintain it?
            1. Get the code reviewed first
         2. Remove the code
            1. Have the customer test the removal/uninstall first in their staging. 
            2. Then remove the code if they approve
      2. If no, no action needed
   2. Accept transfer
   3. Remove any customer collaborators on the github repo
   4. Transfer the repo to odoo-ps
   5. Rename the repo to psus-\<customer-name\>

### Option 2: Customer Owned SH to New Customer Owned SH with Custom Modules
1. Ask for the new github repo link (customer must create this)
2. Ask for collaborator access to the new github repo
   1. Give them this [link](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository) if they are unsure how to do so
3. Schedule downtime to do the transfer
   1. This is important since we will be taking a backup and restoring it to a new SH project
      1. We will need to delete the old project to reuse the Subscription Code(M code)
   2. Ideally on Monday/Tuesday/Wednesday outside their business hours
      1. Do **NOT** schedule it on Friday, avoid thursday if possible 
   3. Remind the customer they will need to stop working in their database during the downtime
4. At the scheduled time, Zip the modules in src/user
5. Download the zip
6. Create a Production branch if there is none in the New github repo(You should have collaborator access at this point)
7. Unzip the code locally and push to the Production Branch
8. Take a backup of the database, download the dump locally
9. In the customer’s Odoo Subscription, disable the database for the subscription 
   1. Cindey has the access to disable a database, so message her with the link to DB. 
   2. If she is not available, ask Jigar to disable it.
   3. Then check that the subscription is not linked to any database (stat button on subscription for database should have zero).
10. Delete the old SH project
11. This will free up the Subscription Code
12. Create a new SH project with the new github repo
    1. Make sure the version is the same as the old SH project
    2. Use the Subscription code(should be free now)
13. Move Production branch up to Production section
14. Navigate to the BACKUPS tab of the production branch and upload the downloaded database using the import database button.
15. Rename SH database to target name (that was freed up by the Saas DB earlier) in project settings. Try to open SH production, this may show PSOD, but wait for some time for DNS cache to update.
16. Run Scheduled Action Id=3 (or whatever looks like the subscription server ping. Click on any scheduled action and change the id in the url to 3.)
17. Go to Subscriptions and verify that the user’s subscription is linked to one database.

### Option 3: Customer Owned SH to New Customer Owned SH without Custom Modules
TODO

## Creating an Odoo-managed SH Project
- Never create the git repo from the SH project creation screen, always prepare it beforehand and then use "link to existing repo"

1. Create a new repo named `psus-companyname` owned by [odoo-ps](https://github.com/odoo-ps) (if you don’t have access, talk to Jigar).
    1. Repo settings: Private repo, initialize with readme, and add .gitignore for Python.
        1. copy paste into readme and update company name
        ```
        # Company Name (repo name)  
        ## Branches:  
        - SH Production Branch: **_production_**
        - Sh Staging (You can only have three staging branches):
          - 1st staging Branch: **_sandbox_**
          - 2nd staging Branch: **_dev-staging_**
        - Development (You can have as many development branches as you like):
          - 1st Development Branch: \*\*\*\*  
        ## Code of Conduct  
        - **IMPORTANT : DO NOT COMMIT anything in the _production_ branch, because _production_ is _Production Instance_**
        - If you want to start development branch fork new branch form _production_ or _staging_ branches and and SH will automatically start new development build.
        ```
2. Go to Settings/Collaborators/Add Team and add PSUS (US PSUS Team), give them “admin” access.
3. In the master branch add requirements.txt (can be empty to start with), copy over contents into readme.md.
4. Add the BSA only to the sh-project(customer should not have access to either SH or Github)

## Migrating Imported Modules

1. Check if customer has custom developments done for them on Saas
2. If so, they should have a branch [here](https://github.com/odoo/ps-custom) or a repo [here](https://github.com/odoo-ps)
3. These devs should be moved to the customer’s new repo
4. In ir_module_module, these modules will need to be marked as non-imported modules, so they will be properly updated in the future
