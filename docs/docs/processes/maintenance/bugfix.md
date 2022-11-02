---
layout: post
title:  Maintenance(Bug-Fix)
permalink: /docs/process/maintenance/bugfix
parent: Maintenance
grand_parent: Process
nav_order: 3
---

## Maintenance(Bug-Fix)

  - Maintenance covers Bug fixes for development done based on specifications on the tasks under project PSUS - Tech Quickstart for which customer is paying ongoing maintenance.
  - Be careful of scope creep (Anything outside of original spec on ‘PSUS - Tech Quickstart’ task is scope creep)
  - If customer not paying maintenance fee in any manner then the Bug is not covered under maintenance and task should be created under **PSUS - Technical Support**

- Pay attention to following:
  - Include original task URL reference in the Maintenance request.
  - This is same as /help, so include screenshot/video and give use cases on how to reproduce this with test database you/customer tested on. (we can not figure everything from one line explanation or just a screenshot)
  - Follow-up with the developer who originally developed the task if possible.

- How to Start new maintenance request:
  - Make a copy of the following template task : [[BUG TEMPLATE] [TRIGRAM] Customer Name : Title of the bug](https://www.odoo.com/web#id=2614876&cids=3&menu_id=4720&action=333&active_id=3137&model=project.task&view_type=form)
  - Task title should follow the following naming conventions :
    - [TRIGRAM] Customer Name : Bug Title
      - i.e. [KGA] Electronics123 : Search is missing
    - Video on next slide demonstrate how to create a request
  - When creating Upgrade request make sure no parent task is set, if you will set quickstart parent task then you will see false billing hours on task

[How to create a maintenance request for existing development?](https://youtu.be/UGzavmOCquc)