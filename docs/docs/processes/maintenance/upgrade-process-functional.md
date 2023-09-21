---
layout: post
title:  Upgrade Process[Functional]
permalink: /docs/process/maintenance/upgrade-process-functional
parent: Maintenance
grand_parent: Process
nav_order: 4
---  
# Upgrade Process 

1. Test upgrade request.
2. Custom code upgrades(if any).
3. Testing upgraded database with upgraded custom code.  
  a. [Test Guidance](https://docs.google.com/document/d/1ypNs7JKPOsjNbKpdiKFH7Al6g6whZ9jr7f7duAQ5E1w/edit)
4. Report any issues occurred during testing via odoo support.  
  ![Test Upgrade Issue](test_upgrade_issue.png)
5. Request another test upgrade if required.
6. Upon successful testing and validation, plan production upgrade.
7. Upgrade production database.  
  a. Production database will be unavailable while its being upgraded.  
  b. Contact upgrade services team member for downtime estimate.
8. Report any issues post production upgrade via odoo support.  
  ![Post Upgrade Issue](post_upgrade_issue.png)

## Upgrade Process by Deployment  

- **Saas(Odoo Online)**
  - [My Database Page](https://www.odoo.com/documentation/16.0/administration/upgrade/odoo_online.html)
  - [\_odoo/support](https://drive.google.com/file/d/18cO7WjVaCy6Wag6Jo1TmpJEJL5qvoO0_/view?usp=sharing)
- **SH**
  - [Upgrade Feature](https://www.odoo.com/documentation/16.0/administration/upgrade/odoo_sh.html)
  - [upgrade.odoo.com](https://upgrade.odoo.com/)
- **[On-Premise](https://www.odoo.com/documentation/16.0/administration/upgrade/on_premise.html)**

  
  ![Upgrade Process ](upgrade_process.png)  





