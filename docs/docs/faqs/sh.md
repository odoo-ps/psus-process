---
layout: post
title:  "SH"
permalink: /faqs/sh/
parent: FAQs
nav_order: 1
---


# Odoo.sh

# Creating a new SH Project

[Creating a new SH Project](https://docs.google.com/document/d/1uXA_GnHJwtv6A8l0XAGJle1a3j43Cex_tMATHL2oAQU/edit#)

## Creating an Odoo-managed SH Project

Do not create a new repository from the SH project creation page, always make a repository beforehand and click on "Link your existing repo", to select your previously created repo.
### Creating a repository for SH Projects

1. Go to [Odoo (PS)](github.com/odoo-ps) and click on "New"
2. You can either create the repo from the ground up or by selecting the template `odoo-ps/psus-sh-template`
  * Creating the repository from SH template:
    1. Select the `odoo-ps/psus-sh-template`
      a. By default this template has the requirements.txt file, a simple readme, gitignore and a staging branch called 'sandbox'. If you want to get the staging branch when creating the repo, select the _include all branches_ checkbox.
    2. Go to Settings/Collaborators/Add Team and add PSUS (US PSUS Team), give them “admin” access.
    3. If you need to add staging branches, just go to the branches menu on the repo, type the name of your new staging branch and click on create.
        a. Tip: Before creating the branches, edit the readme file to display the staging branches names, so that you don't have to edit the readme files from each branch.
  * Creating the repository from the ground up:
    1. Create a repo named “psus-companyname”
      a. Repo settings: Private repo, initialize with readme, and add .gitignore for Python.
    2. Go to Settings/Collaborators/Add Team and add PSUS (US PSUS Team), give them “admin” access.
    3. In the production branch add requirements.txt (can be empty to start with), copy over contents into readme.md.
    4. Go to the branches menu on the repository, and click on "See all branches", there you can rename the "main" branch to "production" (Recommended).
    5. Once the branch is renamed, you can go to the branches menu on the repository and type "sandbox" and click on "Create from production", you should do this for all the remaining staging branches for the customer.
3. Once you have the repository created you can go ahead and create the SH project.

# Developments (Customizations)
## Adding yourself to the SH project

* Go to the db’s support page: <business_url>/_odoo/support using incognito (or similar based on browser)
* Log in using your Odoo credentials
* Note: Don’t use your Tri/Quadgram, just use  [tri/quadgram@odoo.com](mailto:tri/quadgram@odoo.com)on the user field.
* If you do not have Technical Support page access to add yourself, ask your Team Lead or CIC to add you.
* Impersonate a user with admin privileges (Users with stars).
* Once on the project page, go to the Project settings, and under contributors add your github username.
* Log out, and log in again in odoo.sh with your credentials, and the project should be under your username>My Projects.

## Requesting access to repositories not owned by Odoo

There are some cases where the customer or partner manages the SH project repository, when this is the case we won’t be able to create new development branches (Or git operations for that matter) on the project, so we need to ask for repo access to the BA of the project.

These are special cases including: 
1. Partner Developments
2. Legacy Customers
   1. We will usually request the Customer to transfer ownership of the repo to PSUS due to the new ALl or Nothing policy on Repo ownership
   2. We only allow Legacy Customers to do one last development if they will not transfer the ownership to PSUS team, however we will remove maintenance
      1. Any issues that come up will require pack hours to resolve after this
3. Special Case MMCs
   1. An agreement to make an exception must be made and the customer/BSA/Account Manager/Technical Lead must be made aware

* How to check if Github Collaborator Access needs to be requested
  * Tip: A quick way to find out if the github repository is owned by us, is to check the project name on the top right corner of the SH project. If it starts with ‘odoo-ps’, the PSUS team owns it and all of us should have access.
  * If this is not the case:
    * Mark the task as blocked (Kanban stage **Orange(Changes Requested)**) if it has been a while
    * Recommendation: Schedule an activity to follow up.
* Tip: Another quick way to find the repo linked to the project, is to go to any of the branches on the SH project, and on its history you can click on any of the commits made on that branch, that’ll lead you to the commit on Github, there you can navigate to the repository itself, if you encounter a 404 error, the repo is private, and you don’t have access, sometimes they are visible but until they add you as a contributor you won’t be able to create the branch for your dev.

## Creating your development branch

To create a new development branch for your development, you need to click the ‘+’ button on the project page, on the left pane, where the branches are, there is a section called “Development”, fork it from production and give it a name using the following structure:
* **`<odoo_version>-<task_id>-<consise_module_name_description>-<gram>`**

## Moving Dev into UAT

Once that your PR is approved, then you can merge your branch into the staging branch for **U**ser **A**cceptance **T**esting, you can do this by dragging your development branch to the staging branch, you should click on “Merge” on the pop up. However the best practice is to squash your commits to make the commit history cleaner.

You can do so from your CLI by issuing the following steps:

* Commit all your changes into your dev branch before the merge.
* Git pull, to ensure that your repo is up to date.
* Move into the staging branch by using `git [switch | checkout] <branch_name>`
  * Example: `git switch staging`
* Issue the `git merge: git merge <your_dev_branch> --squash`
  * In some cases there might be merge conflicts, you must resolve them before finishing the merge, VScode and other IDEs have great tools to solve conflicts.
  * If there are no conflicts, you must add your changes using `git add .` and then `commit` and `push` your changes.
* Once the merge is complete the staging branch will update.
* Go to Apps inside the Odoo instance using debug mode, select “Update Apps list” then find your module and install it. There you can test your development and, if working correctly.
* In case you need to make changes you should Never commit changes directly to the staging branch, in case you need to make modifications, you should make them on your dev branch and do the merge process again.
  * Tip: By going to the “Editor” tab on the staging branch, you will find your code under the /src/user directory, here you could test out some small changes to test small fixes with the staging data without having to go through the whole process by modifying a part of your code, then under the “Odoo” tab of the editor, you can click on “Update current module” and it will update the code on the branch. **However be aware that these changes won't take effect on the Github branch**, and all of these modifications should be made to test solutions that should end up on your dev branch while doing the merge process again. If the branch rebuilds, **all these changes will be lost**.
## Moving Dev into Production
The process of moving to production is almost the same as the move to staging, just, instead of merging into staging, merge your dev branch into the production branch. Once the merge is done Go to **Apps inside the Odoo instance using debug mode**, select “**Update Apps list**” then find your module and install it.
# Bug Fix Flow in SH
To start the bugfix flow, first, we have to add ourselves to the SH project in order to start working on it, to do so, follow these steps: [Adding yourself to the SH project](#Adding-yourself-to-the-SH-project)

If the project is not hosted by Odoo, ask the reviewer for Github access ([Requesting access to repositories not owned by Odoo](#Requesting-access-to-repositories-not-owned-by-Odoo)) in order to provide a fix. This should not block you from reproducing the issue. Ask the reviewer for which staging to use for reproducing the issue.
Use the dev-staging if SH is managed by odoo.
* It is advisable to rebuild dev-staging, so that you will have fresh data from production to test. This will also match the steps to reproduce in the task description.
* **NOTE: Don’t Rebuild staging without confirming with the reviewer/customer in case SH is owned/managed by the customer.**
## Testing the bugfix
Create a new development branch from production for your fix by clicking the ‘+’ button on the project page, under the “Development” section, and give it a name using the following structure:
* **`<odoo_version>-<task_id>-fix-<odoo_gram>`**
  * I.e: `15.0-435244-fix-cvan`
* Once the fix is ready, merge your development branch into the designated staging branch, following the same steps as here: [Moving Dev into UAT](#Moving-Dev-into-UAT).
* Send the url of the instance to the reviewer and ask for testing. Move the task to **UAT**.
## Applying the bugfix
If the customer is satisfied with the fix you applied on the staging branch. Apply the same fix to the production following these steps: [Moving Dev into Production](#Moving-Dev-into-Production)

# Upgrade
For DB upgrades we need to have access to the SH project [Adding yourself to the SH project](#Adding-yourself-to-the-SH-project) as well as the Github repository ([Requesting access to repository](#Requesting-access-to-repository)). Once we have access to the project and the repository;
## Code Upgrade
* Create a new development branch from production for your fix by clicking the ‘+’ button on the project page, under the “Development” section, and give it a name using the following structure:
* **`<odoo_version>-<task_id>-upgrade-<odoo_gram>`**
  * I.e: `15.0-123456-upgrade-cvan`
* In case of migrating code from SaaS to SH (From [Code upgrade: Saas to SH](https://docs.google.com/document/d/1TTLwS_7W8UAszjwaDZptmGCts0cASS5aFRYMiEveNlo/edit)):
1. Convert fields and models from XML to PY.
  * Create a model.py file for every new model or standard model that has fields added.
  * Rename x_ models by removing the x_ prefix, and replacing _ with . (except when a model without x_ already exists).
  * Rename fields by removing the x_ prefix. (Except when a field without x_ already exists).
  * If the models/fields are not in English, you can translate them (it's recommended to leave a comment next to the model/field with its previous name, so you can find it easily in case there are references to it). This is NOT mandatory, it's just improvement for the developers, not for the customer. If it's likely to create more work than advantages, avoid it, or leave it for the end. (You might need to fix views, reports, templates, translations, actions, ...).
2. Everything that uses models/fields should be adapted to use the new name.
  * E.g.: domains, views, filters, ...
3. Convert Server Action from XML to PY with comment (E.g.: #SA756 for server action 756):
  * Move the Server Action to the corresponding model.py file (create a new file if necessary).
  * Replace call to actions for the model method.
  * Pay attention, some Server Actions could have been created to update every model record after development and might not be required anymore.
  * Upgrade Server Actions that are not declared in the modules are referenced in views/code.
4. Apply flag ‘imported’: False to the module __manifest__ in case an importable module is being converted to a python module.
## Setting up staging branch
You may need a new staging branch if there is only one staging branch available with old changes made by the client or partner that are not up to date with production.
* **DO NOT Delete** the current staging branch - move it to Development instead.
* Check how many staging branches the customer is paying for under the Settings tab up top.
  * If they have extra branches that are not being used
    * Create a new staging branch by forking production.
  * If they do not have extra staging branches
    * Ask BSA first if it’s okay to drop and move a new dev branch up as the upgrade branch for upgrade staging testing
    * They may want to make a backup or have the customer purchase another staging branch(we recommend they have at least 2, one for the upgrade testing and one for functional testing)
* Staging branch Naming convention should follow:
  * **`<version>-upgrade-test`**
    * ex: `15.0-upgrade-test`
## Upgrading Staging Branch
To stage the upgrade process on the staging branch, we need to upgrade it. There are two options;
### Using the Upgrade tab on SH
* You can go to the staging branch that you’re planning to upgrade, and there should be an “Upgrade” Tab for the branch, click on it and you should see an upgrade wizard asking for a “Target Version”.
* Once you select the version, SH will retrieve the latest production backup and upload it to https://upgrade.odoo.com/.
  * While upgrading the tab will show the upgrade logs so that you can see the process.
* **If the upgrade request is successful** it should reach a stage where it will require merging the custom upgraded code, follow this guide to do so [Moving Development into UAT](#Moving-Dev-into-UAT)
  * It’s worth noting that this upgrade tool will rebuild the staging branch on every new commit, so If the build fails when merging to the staging branch, you can fix the code and merge it again until the build is successful.
* **If the upgrade request fails**, the process on upgrade.odoo.com will require manual intervention, so create a ticket on https://odoo.com/help
  * Select the “**An Issue related to my Upgrade(Test)**” option.
  * For more information: https://www.odoo.com/documentation/15.0/administration/upgrade/odoo_sh.html#odoo-sh
* Once the staging branch is up and running with the migrated code, you can send the URL of the DB to the reviewer of the task so that they can start the **UAT** process.
### Bug Fixes and UAT Feedback
You should follow up on the task every two weeks for feedback or issues, it is recommended to schedule activities with consultant or account manager.

If you receive feedback from the customer, request steps to reproduce the issue, photos and videos that display the issue as well as expected behavior and check if this is standard Odoo behavior or new behavior from new version features.

If the issue is coming from a customization, fix the bug and push the changes to the staging branch. If the issue is not coming from customizations ping Keyur (KGA) and he’ll take over it from there.


### Tips
* Sometimes especially when upgrading from an old version, some computed/related fields might cause performance issues if they were done incorrectly through Studio. So it is a good idea to review all these fields to check if they are stored, in case they are this value should be set to False. First double check with the BSA the intention behind those fields and make the field modifications on the staging branch, let the BSA know of the changes so that the customer and BA can test out functionally if everything is working as intended.
* In case a performance issue is reported you can monitor the performance of the staging branch by going to the branch on the SH project, and clicking on the “Monitor” tab, there you will see two options;
  * Resource monitoring, where you’ll be able to visualize performance metrics such as CPU utilization, memory usage, etc…. This can be useful to debug the issue, however you can use the profiler as well.
  * Profiler: The profiler is a tool that lets you see a flame graph of all the processes running in a given period of time on the SH instance. As well as a breakdown of subprocesses of a given process. I.e if you start the profiler, and then reproduce the bug, you will be able to see the breakdown of processes all the way through the SQL calls queries to the DB, so it is easier to visualize if a process is taking too much time to execute.
    * To start the profiler, click on the “Start profiler” button, go to the db, reproduce the bug(s) and when you are done, click on the “Stop Profiler” button.
    * A new record should display on the Monitor page displaying when the profiler ran, there you should be able to see an “Open Flamegraph” button, click on it and you’ll see the process breakdown mentioned earlier.
## Upgrading Production
### Schedule the upgrade
* Schedule to do the final Production Upgrade during a specific day/time
  * Only schedule on **Monday, Tuesday, Wednesday, Thursday**
Preferably Tuesday or Wednesday
  * Schedule a downtime for 2+ hours depending on how complex the migration is
    * ex: More custom code/larger database > longer down time
    * Check upgrade request process duration to have an Idea of hours.
* Rehearsal for SH Production Upgrade.
  * One should do another test upgrade a day before doing the production upgrade to make sure that everything goes as expected.
  * Rehearsal is just another test upgrade, follow the same steps as on [Setting Up Test Instance + Installing Upgraded Development](https://docs.google.com/document/d/1sCxZ43NSdbpxVhsK3yRC97H1JJyHOXXiYq6lmmVOJEE/edit#heading=h.jo8sqjjoktg7)
  * Expected result is Successful(Green) build once you merge the upgraded code with the Staging.
### Do the upgrade
When all the necessary tests have been completed by the customer and BAs, and everything seems to be working as expected, **Production branch will be unavailable throughout the process**;
* Exit the upgrade mode on the staging branch
* Navigate to the production branch>Upgrade tab
  * Select the target version and click on “Test Upgrade”, the upgrade process will start as soon as the branch gets a new commit so in this stage merge the upgraded code into production.
  * SH will create the latest production backup and upload it to upgrade.odoo.com
* You will be able to see the process on the “Upgrade” tab on the production branch.
* The process should finish with a Yellow/Green build if everything goes well.
* In case something goes wrong, the process will revert back to the original production version.
* For more information: https://www.odoo.com/documentation/15.0/administration/upgrade/odoo_sh.html#odoo-sh
# Access
## SSH Access
* To gain access to any instance of an SH project, you must use an SSH key, you can use the same ones that are used for Github authentication or generate new ones following this guide: https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key
* If new keys are used, then you can add them to your profile in SH by clicking your username on the project page>Profile at the bottom of the pop up (See image below).
  * Here you can either import your Github keys or paste a new one.
    * Note that the content you should be pasting is the information on the .pub file generated when the ssh keys were created.
* With the SSH key saved, you can click on any of the instances on the SH project and on the upper right corner click on the “SSH” tab, and copy the SSH command. If done correctly once you paste the command on your terminal, you should now be on the instances environment.
## SCP: Moving files from and to SH Instance.
SCP (secure copy) is a command-line utility that allows you to securely copy files and directories between two locations. It uses SSH access to an instance to copy files from your local machine to a remote one and vice versa.

* Copy from local machine to remote (I.e SH instance):
    * `scp path_to_file.txt remote_username@remote_ip_or_domain:/remote/directory`
    * Example: `scp /home/emab/test.xml [4211951@cubecare.odoo.com](mailto:4211951@cubecare.odoo.com):/home/odoo/`
* Copy from remote machine to local:
    * `scp remote_username@remote_ip_or_domain:/path/to/file local/directory`
    * Example: `scp [4211951@cubecare.odoo.com](mailto:4211951@cubecare.odoo.com):/home/odoo/test.xml /home/emab`
