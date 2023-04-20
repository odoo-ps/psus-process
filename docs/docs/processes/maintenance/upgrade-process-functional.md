---
layout: post
title:  Upgrade Process[Functional]
permalink: /docs/process/maintenance/upgrade-process-functional
parent: Maintenance
grand_parent: Process
nav_order: 2
---

![Upgrade Process ](upgrade_process.png)    

# Upgrade Process 

1. Test upgrade request.
2. Custom code upgrades(if any).
3. Testing upgraded database with upgraded custom code.  
  a. Test Guidance
4. Report any issues occurred during testing via odoo support.  
  a. Ticket Type: An Issue related to my future upgrade(I am testing an upgrade).
5. Request another test upgrade if required.
6. Upon successful testing and validation, plan production upgrade.
7. Upgrade production database.  
  a. Production database will be unavailable while its being upgraded.  
  b. Contact upgrade services team member for downtime estimate.
8. Report any issues post production upgrade via odoo support.  
  a. Ticket Type: An Issue related to my upgrade (production).