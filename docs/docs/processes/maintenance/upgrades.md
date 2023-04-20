---
layout: post
title:  Code Upgrades
permalink: /docs/process/maintenance/upgrades
parent: Maintenance
grand_parent: Process
nav_order: 2
---

# Code Upgrade

- Code Upgrade covers upgrade of the code to newer version of Odoo based on specification on the tasks under project PSUS - Tech Quickstart and paying maintenance actively.
  - If target version has some feature dropped/removed and If technical team used those feature in development then developers will try their best to make it compatible to the target version.
  - It may require success pack hours in order to re-engineer the initially developed solution.
- Pay attention to following:
  - Code upgrade will be done with target standard odoo version before it can be tested with upgraded database.
  - Request code upgrade at the same time of requesting test upgrade.

### What if the customer is not paying Maintenance for a PSUS development?
If customer is not paying maintenance fee ($5/Hour) or LOC MRR, then it’s not covered under Maintenance, hence we can not provide the code upgrade service.  
**Customer has the following options in that case:**
- Customer can do the upgrade themselves
- Customer can work with a Partner to upgrade
- If the Customer wants PSUS team to upgrade
  - Refer to [code review](code-review.md) section.
- If the request is from Partner, then we can provide this service using partner’s Success Pack.
  - No Maintenance will be required
  - No Estimate of hours needed will be given, hours to upgrade custom code may vary.

### How to start code upgrade request
- Go to [Odoo Support Page](https://odoo.com/help) to report an Upgrade Issue.
  - Select ticket type: An issue related to my future upgrade(I am testing an upgrade)
    ![Test upgrade issue](test_upgrade_issue.png)