---
layout: post
title:  "Pull request"
permalink: /faqs/pr/
parent: FAQs
nav_order: 4
---


# Peer review process - Development Services
## Pull Requests (PR) Process and Guidelines 

* Everyone in the Team is required to get PR Reviewed (no immunity) at all stages of deployment i.e. dev > staging and dev > production
  * This includes Development, Upgrades, and Bug fixes/Maintenance
  * This policy begins on September 2022
* The PR can only be reviewed by someone on this team  (aka @pr-police) https://github.com/orgs/odoo-ps/teams/psus-quickstart-reviewer
  * If an individual is not part of this team then the individual is not expected to review a PR and if a PR is approved by an individual who is not part of this team is considered void
* When a Branch/Code is ready for review,
* Create a PR
* Tag the Github team  @teams/psus-quickstart-reviewer on the PR and someone from the team will work on reviewing the PR in a timely fashion. Tagging the team will notify everyone on the team that a PR is ready for review. 
* Optionally, discord group, psus-quickstart-reviewer can also is employed to  let the team know that a PR is ready for a review
* For Legacy customers that own their own Github repo
* Create a branch in psus-custom github repo
* Create a PR to production
* Follow same steps as above
* Once the review is approved, cancel the psus-custom PR(do NOT merge it)
* Create a PR in the customer’s repo and merge it yourself
* For a PR to be ready for review, the following needs to be true:
* Development Branch needs to be green before creating a PR
* Either the unit tests must be monkey patched or new unit tests must be fixed/written to make the branch green
* Monkey Patch Example
* This point only applies to code reviews for customers with the new development after September 1st 2022
* Legacy customers/customers with prior development do not need to have green branches (this may change in the future) but we advise putting effort into getting them to green 
* Have a Video recorded showing how the Development works and put it unlisted on youtube  (This is optional for now)
* Have no references to Studio anywhere in the Module
* Any Views/Fields/Models made in Studio must be re-created in the custom module
* BSA is responsible for data transfer from the old Studio Fields to New Custom Fields
* All Odoo Guidelines must be followed
* Once PR is created, the link to the Branch and PR must be present in the task’s “Git (URLs to Code)” section 
* If any of the above is not true then the reviewer will not work on reviewing and will ask the PR Owner to complete the above first. The task will be blocked until everything is true.
* A PR needs to be "approved" before it can be merged, i.e. all the requested  changes/comments must be marked as resolved
* A reviewer will give Mandatory changes and/or Suggestions 
* All mandatory changes must be resolved 
* Whereas suggestions are just opinions or advice from the reviewer and an individual may or may not accept it based on their own understanding regarding the development or an individual may challenge the suggestion to learn more and see if it might help explore something new
* Once a PR is Reviewed and it is ready for merge in production then we must Squash and merge your commits in production  
* If the Repo is not configured for commit squashing for pull requests then you should be able to do it yourself, here is the documentation: https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/configuring-commit-squashing-for-pull-requests
* After Production deployment
* All staging branches must be Rebased on production (here’s   documentation with details on this)


It was presented [here](https://docs.google.com/presentation/d/11dycRLfyHxE7WIgKqLR4Zmc69txwUR0zDAZDHqriMug/edit?usp=sharing)
