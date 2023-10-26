---
layout: post
title:  Custom Code Upgrades
permalink: /docs/project/maintenance/upgrades
parent: Maintenance
grand_parent: Project
nav_order: 3
---

# Custom Code Upgrade

- **Custom Code Upgrade covers conversion of the custom module code to newer version of Odoo.**

### What is covered:

- Odoo will upgrade following types of custom code if its covered by maintenance on customer’s subscription.
  - Custom developments done by PSUS Technical Team in form of python module(SH), importable modules(Saas).
    - Based on specification on the tasks under project **PSUS - Tech Quickstart**.
  - Studio customizations.
  - 3PA from odoo app store approved via code review.
- Maintenance on the subscription can be in any of the following forms.
  - **LOC [Current Pricing]:** Maintenance charged based on the total LOC count of Custom Modules installed on the database.
  - **5$/Hour [Old Pricing]:** Maintenance based on the hours spent on the development.

### What is not covered:

- Any custom module for which customer is not paying maintenance.  
- E-Commerce connectors installed on odoo.sh(Excluded from maintenance)  
  - Shopify  
  - WooCommerce  
  - HubSpot  
- 3rd Party Themes:  
  - Ex. [Clarico Vega Theme](https://apps.odoo.com/apps/themes/13.0/theme_clarico_vega/)


### What if the customer is not paying Maintenance for a PSUS development?

- If customer is not paying maintenance fee ($5/Hour) or LOC MRR, then it’s not covered under Maintenance, hence we can not provide the custom code upgrade service.  
- Customer has the following options in that case:
  - Customer can do the upgrade themselves
  - Customer can work with a Partner to upgrade
  - If the Customer wants PSUS team to upgrade
    - Refer to [code review](code-review.md) section.
  - If the request is from Partner, then we can provide this service using partner’s Success Pack.
    - No Maintenance will be required
    - No Estimate of hours needed will be given, hours to upgrade custom code may vary.

### How to request custom code upgrade?
- Check if there is any existing task for customer in **[Upgrade Projects](https://www.odoo.com/web#cids=3&menu_id=4720&action=333&active_id=4429&model=project.task&view_type=kanban)** in **PSUS Custom Upgrades** stage.
  - If found, follow up on the task for the status of custom code upgrade.
  - if none found, Go to [Odoo Support Page](https://odoo.com/help) to report an Upgrade Issue.  
    ![Test upgrade issue](test_upgrade_issue.png)
  - [Step-by-step video](https://youtu.be/yg_iCS34An4)

## IMPORTANT

  - Request custom code upgrade at the same time of requesting test upgrade.
  - If target version has some feature dropped/removed and If technical team used those feature in development then developers will try their best to make it compatible to the target version.
  - It may require success pack hours in order to re-engineer the initially developed solution.
  - Code upgrade will be done with target standard odoo version before it can be tested with upgraded database.