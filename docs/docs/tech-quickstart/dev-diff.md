---
layout: post
title:  "Development Differences"
permalink: /differences/
parent: Tech Quickstart
date:   2022-08-29 10:19:51 -0700
categories: jekyll update
---

# Customization 
Tasks that can be done by the functional consultant. Functional consultants should know how to perform all these tasks.

# Development
 Should be done by Odoo’s technical team

- SaaS Customers: there is a cap of 15 hours for developments. These should be simple developments (New PDF reports, modifying existing reports, new views, etc. Anything related to QWEB or MX Addenda), the technical team will evaluate if the development is feasible in SaaS.
- Odoo.sh Customers: No hour cap. If an integration is needed please refer to this document [Integrations](integrations doc).

Note: As a company policy if any development is done, internally (with Odoo) or externally (by the customer), the customer will be charged maintenance, make sure you make the customer aware of this to avoid any future conflict.

# Development vs Customzation
Anything that can be done with the drag and drop features of Studio’s interface is considered Customization. 
This document specifies what is a Development beyond that:

| Customization | Development |
| --- | --- |
| 1. Main Studio Interface: <br />  - Adding/removing elements from view, editing PDF reports, etc) <br> <br> 2. Server/Automated Actions(except the ones specified on the development section) <br> - [Create/Update record](https://drive.google.com/file/d/1eSeY9r7IDvHIaaQcv1DKqH7vxefNf6v2/view) [(Value)](https://drive.google.com/file/d/1cskMiH4eIrv-5J3KEYNHO2zSX1iQatas/view) <br> - [All other types (send email, followers, etc)](https://drive.google.com/file/d/123AR2ClE99M9-E9oYH5FRY515vXyH_y9/view) <br><br> 3. Data structure <br> - Creating a new Model <br> - Creating fields <br> - Creating related fields (non-stored) <br><br> 4. Access Control List <br><br> 5. Imports <br> - Trough the UI: Anything that does not require a script such as: Master Data like partner, product, BOM, etc, and Business data like SO, PO, MO, etc. <br><br> 6. Email Templates: <br> - Simple email templates with one level or two level dynamic placeholders, no python code used or advanced conditional operations <br><br> 7. Odoo.sh <br> - [Rebuild Builds](https://drive.google.com/file/d/1XlNssqokY7rqs03GWH5tW8UxkIelgYBE/view?usp=sharing): If a customer requires an updated testing instance. | 1. Server/Automated Actions: <br> This applies for Server or automated actions that have the following configuration. <br> - When the Action To Do = Execute Python code <br> - When the Action To Do is either Create a new Record or Update the Record and the Evaluation Type in the Data to Write page  is either Reference or Python Expression <br> - Automated action based on time condition <br><br> 2. Views: <br> - Editing QWeb / HTML / XML (even if it was created through studio) <br> - Creating new view (XML, QWeb reports, Website views), or your own inherited view  <br> - Editing CSS, JS <br> - Change layout/behavior of  Calendar/Grid/Gantt/Graph/Dashboard/Activity views <br> - Editing standard financial reports or creating new financial reports <br><br> 3. Data structure: <br> - Computed fields <br><br> 4. Window Actions: <br> - Adding view mode <br> - Creating new action (any kind) <br> - Domain <br> - Context <br><br> 5. Record Rules (Editing / Creating) <br><br> 6. Imports (no maintenance): <br> -Everything that requires a script: Complex/historical data, Import moving business data like SO, PO, Accounting, MO, timesheet <br><br> 7. Website: <br> - Website styles such as: CSS, SCSS, JS, XML, Custom code through the code block feature <br><br> 8. Email Templates: <br> - If it requires advanced dynamic placeholders (navigating through various objects, like tags or one2many fields, more than 2 levels), loop operations to display tables, python formulas to format text, advanced conditional operations, etc. <br><br> 9. Odoo.sh (no maintenance): - Deploy, merge code into branches <br> - Installing 3rd party apps <br> - Creating an .sh project <br> - Restoring backup <br> - Creating/deleting branches <br> - Changing staging branches



