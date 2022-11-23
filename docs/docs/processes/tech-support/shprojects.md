---
layout: post
title:  "Odoo.sh"
permalink: /docs/process/support/sh/
parent: Tech Support
grand_parent: Process
nav_order: 3
---

# Saas To SH Migrations and New Project Creation

#### Saas to SH Migrations Policy as of May 2021: (Only Available For Long Term Support Versions)
  - Option 1: The PSUS Technical Team can create the SH project and move the database from Saas to SH but the customer needs to agree to these conditions:
    - Customer will NOT have access to the SH project and Github Repository
    - PSUS Technical Team will maintain all aspects of the project and repository
    - Third Party App [policy](https://docs.google.com/document/d/1SAGTe5ql0bqsuV_9cSPvbIk-xjz66RcfLY4dWf-Pghc/edit#heading=h.bdgsb4dun3wx)
  - Option 2: The PSUS Technical Team can move the database from Saas to SH but the customer needs to:
    - Create the SH Project and Github Repository themselves
    - Provide the Saas database URL and new SH project database URL
    - Understand the PSUS Technical Team will be hands off for everything else (no assistance with 3PA installs, no assistance with creating/managing github, etc.)
    - Custom developments will not be done by PSUS Team
  - Option 3: The PSUS Technical Team can create the SH Project and Github without a Saas to SH change but the customer needs to agree to these conditions:
    - Customer will NOT have access to the SH project and Github Repository
    - PSUS Technical Team will maintain all aspects of the project and repository
    - Third Party App [policy](https://docs.google.com/document/d/1SAGTe5ql0bqsuV_9cSPvbIk-xjz66RcfLY4dWf-Pghc/edit#heading=h.bdgsb4dun3wx)

#### Necessary information to be placed in the description
- Option:
- Saas Database URL(Only if customer chooses option 1 or 2):
- Odoo Account Email(Only  if customer chooses option 1 or 2; database is tied to this email):
- SH Project or Database URL(Only if customer chooses option 2):
- Target Odoo Version (LTS Only [Editions](https://www.odoo.com/documentation/15.0/administration/maintain/supported_versions.html)):


#### Creating an Odoo-managed SH Project
- Never create the git repo from the SH project creation screen, always prepare it beforehand and then use "link to existing repo"

1. Create a new repo named `psus-companyname` owned by [odoo-ps](https://github.com/odoo-ps) (if you don’t have access, talk to Jigar).
    1. Repo settings: Private repo, initialize with readme, and add .gitignore for Python.
2. Go to Settings/Collaborators/Add Team and add PSUS (US PSUS Team), give them “admin” access.
3. In the master branch add requirements.txt (can be empty to start with), copy over contents into readme.md.
4. Add the consultant only to the sh-project

#### Migrating Saas Modules

1. Check if customer has custom developments done for them on Saas
2. If so, they should have a branch [here](https://github.com/odoo/ps-custom) or a repo [here](https://github.com/odoo-ps)
3. These devs should be moved to the customer’s new repo
4. In ir_module_module, these modules will need to be marked as non-imported modules so they will be properly updated in the future
