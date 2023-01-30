---
layout: post
title:  Estimation
permalink: /docs/process/qs/estimation
parent: Tech Quickstart
grand_parent: Process
nav_order: 5
---


# Development Task Estimation

### Something to Keep in Mind
Please note that estimations should be made with the newest members in mind.  How long do you think it would take them to complete the task vs your own personal estimation.


### Base Estimation

| Type                            |  Hours  | Notes                         |
|---------------------------------|:-------:|-------------------------------|
| Compute Field                   |   2+    | Includes associated method(s) |
| Non-compute Field               |   1+    |                               |
| New PDF Report                  |   12    |                               |
| Labels (printed)                |  6-12   | Depends on complexity.        |
| Financial Report (SQL/HTML)     |  16-24  | New or Modifying              |
| Views: Form/List                |    2    |                               |
| Views: Gantt/Calendar/Graph/etc |    4    |                               |
| Views: Kanban                   |    6    |                               |
| Cron                            |    8    | Each                          |
| Statistical View                |   20    | Each                          |
| Mexican Addenda                 |  4-16+  |                               |
| Smart Button                    |   2+    | Per Button                    |
| Constraint                      |   2+    |                               |

### Business Logic

A lot of business logic really depends on your own judgment.  Here are some general estimates for common development:

| Type                |  Hours  | Notes                         |
|---------------------|:-------:|-------------------------------|
| Methods(overloading |   2+    |                               |
| Controllers         |   4+    |                               |
| JS Class            |   6+    |                               |
| JS Widget           |   12+   |                               |

### Security

| Type          | Hours | Notes           |
|---------------|:-----:|-----------------|
| Group         |   2   | New or Existing |
| Record Rules  |   2   |                 |
| Access Rights |   1   |                 |

### Data Import

| Type       | Hours | Notes           |
|------------|:-----:|-----------------|
| Object     |   8   |                 |
| Sub-Object |   4   |                 |

### Data Deletion/Cleanup

| Type   | Hours | Notes      |
|--------|:-----:|------------|
| Object |   4   | Per Object |

### EDI

| Type                           | Hours | Notes                                                                                                                                                                                    |
|--------------------------------|:-----:|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SFTP/FTP                       |  6+   | Depends on the provider for the SFTP/FTP                                                                                                                                                 |
| Model (Document) Export/Import |  6+   | 6 hours is based on if the model information being exported/imported does not require additional modification. Any calculations or logic added before transfer increases estimation time |
| Testing EDI                    |  10+  | for back and forth testing, depending on how many docs, number of trading partners etc.                                                                                                  |

### Other

| Type                       | Hours | Notes                                                                                     |
|----------------------------|:-----:|-------------------------------------------------------------------------------------------|
| Delivery Carrier           |  80+  |                                                                                           |
| Payment Acquirer           |  80+  |                                                                                           |
| API connector              |  40+  | Really depends on the API and functionality customer requests, might be way more than 40  |
| SSO/O-Auth 2.0/Other Auth  |  18   |                                                                                           |

## Unit Testing and UAT Testing

Unit testin

## Formulas
### General Formula

```
LOC Total = ⌈(Estimate Hours) * (Lines of Code per Hour)⌉
```

Line of Cost Total is equal to the Ceiling(to the nearest 100) of Lines of Code per Hour multiplied by Estimated Hours.

### Example:

Estimate = 8:00 Hours\
LOC per Hour = 20\
LOC Total = ⌈20 * 8⌉ = 200 LOC







