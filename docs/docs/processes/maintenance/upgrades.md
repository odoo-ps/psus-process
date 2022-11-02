---
layout: post
title:  Upgrades
permalink: /docs/process/maintenance/upgrades
parent: Maintenance
grand_parent: Process
nav_order: 2
---

### Code Upgrade

- Code Upgrade covers upgrade of the code to newer version of Odoo based on specification on the tasks under project PSUS - Tech Quickstart for which customer is paying maintenance actively.
  - If target version has some feature dropped/removed and If technical team used those feature in development then developers will try their best to make it compatible to the target version.
    - It may require success pack hours in order to re-engineer the initially developed solution.

- Pay attention to following :
  - Include URLs reference of all development task(s) from PSUS - Tech Quickstart that will needs to be upgraded.
  - Code upgrade will be done with target standard odoo version before it can be tested with upgraded database.
  - Request code upgrade at the same time of requesting test upgrade.
  - Code upgrade has about 4 to 5 week of lead time before one can start working on it.

- What if the customer is not paying Maintenance for a PSUS development?
  - If customer is not paying maintenance fee ($5/Hour) or LOC MRR, then it’s not covered under Maintenance, hence we can not provide the code upgrade service.
  - Customer has the following options in that case:
  - Customer can do the upgrade themselves
  - Customer can work with a Partner to upgrade
  - If the Customer wants PSUS team to upgrade, they will have to pay LOC maintenance for the past missing months and also agree to pay LOC maintenance in the future
    - Ref: [Odoo Enterprise Standard Charges](https://www.odoo.com/documentation/master/legal/terms/enterprise.html#standard-charges)
  - If the request is from Partner, then we can provide this service using partner’s Success Pack
    - No Maintenance will be required
    - No Estimate of hours needed will be given, hours to upgrade the code can vary

- How to start code upgrade request:
  - Create a task in PSUS - Maintenance by making a copy of the following template task : [[CODE UPGRADE TEMPLATE][TRIGRAM] Customer Name : vXX.X(platform) to vYY.Y(platform)](https://www.odoo.com/web?debug=true#id=2496020&cids=3&menu_id=4720&action=333&active_id=3137&model=project.task&view_type=form)
  - Task title should follow the following naming conventions :
    - [TRIGRAM] Customer Name : vXX.X(platform) to vYY.Y(platform)
      - i.e. [KGA] Tap Electronics : v12.0 (SH) to v15.0 (SH)
    - Video demo on next slide demonstrate how to create a request
  - When creating Upgrade request make sure no parent task is set, if you will set quickstart parent task then you will see false billing hours on task

- [How to create a maintenance request for existing development](https://youtu.be/UGzavmOCquc)