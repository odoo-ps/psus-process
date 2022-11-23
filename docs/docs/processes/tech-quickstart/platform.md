---
layout: post
title:  "SaaS or SH"
permalink: /docs/process/qs/saas-or-sh/
parent: Tech Quickstart
grand_parent: Process
nav_order: 4
---


# BELOW INFO TO BE CLEANED
# What we can develop in SaaS, SH and On Premise

| Saas | SH | On Premise |
| ----------- | ----------- | ----------- |
| no Python files (except \__manifest__.py and \__init__.py) | All file types okay | All file types okay
| All fields created in xml files as records | Fields created in python(prefered) or xml files(technically doable but not recommended) | Fields created in python(prefered) or xml files(technically doable but not recommended)
| Import(button) to install Custom Modules | Github manages code to install Custom Modules | Give Partner Module Zip
| Test in Trial Database | Test in Staging Branch | Customer Installs/Tests by themselves
| Less common development type | Most common development type | Rare development type

## Did the customer purchase SH?

The customer might have purchased SH but still could be on Saas(we might have to migrate them or they can do the migration themselves, or they still need to create the project). We can check if they have SH purchased on their subscription.
1. On the development task check “Extra Info” Tab for Subscription
2. Click on Subscription Field and Look at “Subscription Lines” Tab
3. Look for “Odoo.sh GB”, “Odoo.sh Staging Branches”, and “Odoo.sh Worker”
   - This means customer has purchased SH on their subscription

## Is a Customer on SaaS, SH, or On Premise?
There are multiple ways to check
1. On the development task check “Databases” Tab for “On SaaS” field
   - On SaaS = ✓
      - Customer is on SaaS
   - On SaaS = ✖
      - Customer not on SaaS (But could be On Premise or SH)

2. On the development task check “Extra Info” Tab for “Has Odoo.sh” field
   - This is not 100% reliable, but usually correct

3. Guaranteed Way - Databases > “Hosted On”
   - Customer > Subscription > Databases > Customer’s Database > “Hosted on” Value
   - On the development task check “Extra Info” Tab for Subscription.

   - Click on Subscription Field and find the “Databases” Smart button

   - Click button to show all database(s) that customer has linked to their subscription

   - Find the “Hosted on” Field this will tell what that database is it is hosted on

# How to Sign onto the Support Page
### SaaS Support Page Access
1. Go in Incognito/Private Mode for your Browser
   - or use a different Browser than the one you often use (ex: chrome instead of firefox)
2. Add “/_odoo/support” to the end of the customer database URL
   - ex: customer-database.odoo.com/_odoo/support
3. Fill out Login info
   - Email > Tri/Quadram
      - Not Fully trigram.odoo.com email
   - Password > Tri/Quadram
      - Same as logging into our production, odoo.com
4. Click “Log in” button to get access

### SH Support Page Access
1. Go in Incognito/Private Mode for your Browser
   - or use a different Browser than the one you often use (ex: chrome instead of firefox)
   - This is mainly for impersonation of a User’s SH account, this will log you out of your SH account when impersonating
2. Add “/_odoo/support” to the end of the customer database URL
   - ex: customer-database.odoo.com/_odoo/support
3. Fill out Login info
   - Email > Tri/Quadram
      - Not Fully trigram.odoo.com email
   - Password > Tri/Quadram
      - Same as logging into our production, odoo.com

# Regular Development Process

## Saas Development Process

1. Access Customers database through support page
  - add “/_odoo/support”
    - ex: customer-database.odoo.com/_odoo/support
  - TODO: add screenshot
2. Create a duplicate(trial) database
   - (Optional) Name it with “customer-dev-testing” or something similar
3. Log into the new trial db’s support page
   - ex: customer-dev-testing.odoo.com/_odoo/support
      - This will land on the support page for the Duplicate
   - Extend expiration beyond 4 hours
      - Usually 2 months in the future is good estimate
         - In case the customer needs more time, this can be extended further for UAT
4. Find Existing Custom Modules for customer in:
   - [psus-custom repo](https://github.com/odoo-ps/psus-custom)
   - or [ps-custom](https://github.com/odoo/ps-custom)
   - Search for customer name in branches
5. Create a Development branch in [psus-custom](https://github.com/odoo-ps/psus-custom) to store the SaaS development code
   - Naming convention:
      - version-general_module_name-task_id-tri/quadgram
      - ex: “13.0-sale-2319423-cic” or “14.0-pos-2345338-kga”
6. Develop code for Development Request Locally
7. NOTE: For New developers, request a code review from a Senior team member before zipping/installing for customer UAT
8. Zip module directory
   - Terminal:
      - sudo apt-get install zip
      - zip -r my_module.zip my_module
   - UI:
      - right click on module > compress
      - save as a zip
9. Check if the Import Module is installed
10. Import the Module zip
    - Module should auto install
11. Do a quick functional check to see module is installed correctly
12. Send Duplicate(Trial) URL for UAT

## SH Development Process
1. Access Customers database through support page
2. Click on “Project” button on support page and access Customer’s Project by Impersonating an admin
   - Admin is a user with a ⭐ next to their name
3. Give yourself SH project access as an admin
   - Settings > Collaborators
      - Enter your github username
   - Change access from User to Admin
      - Now you should have project SH access on your own odoo.sh account
4. Check if PSUS owns the customers repository
   - Easiest way to check is try making the Development branch and forking from Production branch
      - If access is denied then you do not have Github Collaborator Access
   - Another way to tell we own the repository is the name should follow “psus-companyname” if it is created by us
      - Note there are some cases where this is not correct
         - ex: we transferred the repository to them, legacy repositories, etc.
5. Request Github Collaborator Access if needed (repository not owned by us)
   - Ask consultant to request access from the customer
   - [Doc](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository) if customer hasn't done it before
6. Once you have access, create a Development branch that forks from production
   - Naming convention:
      - version-general_module_name-task_id-tri/quadgram
      - ex: “13.0-sale-2319423-cic” or “14.0-pos-2345338-kga”
7. Clone the Repository locally
   - Checkout the Development branch that was created
8. Develop code for Development Request Locally
9. Push code to branch
   - This code will show up now on SH
10. NOTE: For new developers, request a code review from a Senior team member before pushing to staging for customer UAT
11. Check which staging branch customer wants to use with their Consultant
    - Usually it is “dev-staging” if we created the project
    - If there is only one branch double check with consultant still
12. Merge code to staging branch from development branch
    - Example through Terminal:
      - git checkout staging-branch
      - git merge 13.0-sale-2319423-cic
      - git push
13. Install the module in Staging branch
    - Check module shows up in Apps
       - If not there, click “Update Apps List” > “Update”
14. Do a quick functional check to see module is installed correctly
15. Send Duplicate(Trial) URL for UAT
16. Repeat from Step 8 until Customer approves Development
17. Check there are no left over Print statements, unnecessary comments, TODO comments
    - Remove all of these and push to development branch
18. Create a Github Pull Request from Development branch to Production
19. Merge this PR(Pull Request)

## On Premise Development Process
1. Develop code for Development Request Locally
2. NOTE: For New developers, request a code request from a Senior team member before zipping/sending to partner for UAT
3. Zip module directory
   - Terminal:
      - sudo apt-get install zip
      - zip -r my_module.zip my_module
   - UI:
      - right click on module > compress
      - save as a zip
4. Give the Zip to the Partner to test
5. Repeat from 1 until Customer approves Development

## Script Development Process
### SaaS Script Development Process
1. Access Customers database through support page
   - add “/_odoo/support”
      - ex: customer-database.odoo.com/_odoo/support
   - TODO: add screenshot
2. Create a duplicate(trial) database
   - (Optional) Name it with “customer-dev-testing” or something similar
3. Log into the new trial db’s support page
   - ex: customer-dev-testing.odoo.com/_odoo/support
      - This will land on the support page for the Duplicate
   - Extend expiration beyond 4 hours
      - Usually 2 months in the future is good estimate
         - In case the customer needs more time, this can be extended further for UAT
4. Write/Run Code for Script Locally
5. Run Script in Duplicate(Trial) database
6. Do a quick functional check to see script ran successfully
7. Send Duplicate(Trial) URL for UAT

### SH Script Development Process
1. Access Customers database through support page
   - add “/_odoo/support”
      - ex: customer-database.odoo.com/_odoo/support
2. Access customer’s Project by Impersonating an admin
   - Admin is a user with a ⭐ next to their name
3. Give yourself SH project access as an admin
   - Settings > Collaborators
      - Enter your github username
      - Change access from User to Admin
   - Now you should have project SH access on your own odoo.sh account
4. Write/Run Code for Script Locally
5. Check which staging branch customer wants to use with their Consultant
   - Usually it is “dev-staging” if we created the project
   - If there is only one branch double check with consultant still
6. Run Script in Staging Branch
7. Do a quick functional check to see script ran successfully
8. Send Staging Branch URL for UAT

### On Premise Script Development Process
1. Write/Run Code for Script Locally
2. Give Partner the Script file

## Development Process Tips
### Support Page Differences SaaS Vs SH
1. SaaS Support Page
   - Saas support page has No mention of Saas or SH
2. SH Support Page
   - Has a message that says this is an Odoo.sh database
### How to impersonate the Database Admin User on the Support Page
1. SaaS Support Page
   - Select login user and click Impersonate
   - Or input the username of the person to impersonate and click Impersonate
2. SH Support Page
   - Click the “Connect as admin” button to auto impersonate as the admin user
   - Or input a specific login username and click connect arrow

### SaaS Development Tips
1. No Python files allowed
   - Except __manifest__.py and __init__.py within the module directory

#### How to create a field with an XML file
1. Create data.xml file in data directory in the Module
2. Use <record> tags
3. Fill out necessary Field fields
   - ex: name, ttype, model_id, etc.
4. Note: name and external id of the field defined in xml must start with “x_”
   - ex: “x_new_field” or “x_customer_note”

Example Record:
```xml
        <record id="x_project_number" model="ir.model.fields">
            <field name="name">x_project_number</field>
            <field name="field_description">Project Number</field>
            <field name="model_id" ref="sale.model_sale_order"/>
            <field name="ttype">char</field>
        </record>
