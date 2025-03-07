---
content-type: overview
product-area: projects
navigation-topic: task-information
title: Task Handoff Date overview
description: The Handoff Date is the date a task becomes available for work. This typically means that its predecessors have resolved and the assignee of the task can start working on it.
author: Alina
feature: Work Management
exl-id: caf2dbba-5311-418d-8c82-ddcc256f9926
---
# Task Handoff Date overview

The Handoff Date is the date a task becomes available for work. This typically means that its predecessors have resolved and the assignee of the task can start working on it.

>[!TIP]
>
>Handoff Dates do not exist for issues and projects.

## How Adobe Workfront calculates the Handoff Date

>[!NOTE]
>
>The Handoff Date is calculated only if the project status equates to the following statuses:
>
>* On Hold
>* Current
>* Complete
>* Dead
>

Workfront uses the following rules for calculating the Handoff Date of a task:

* **When the task has an incomplete predecessor**: The Handoff Date for the task is null. 
* **When the task has a complete predecessor**: The Handoff Date is the same as the Actual Completion Date of the predecessor task. 
* **When the task has no predecessor and**:

   * **The Planned Start Date is in the past**: The Handoff Date is the same as the Planned Start Date of the project. 
   * **The Planned Start Date is in the future (any date after the current date)**: The Handoff Date is the same as the Planned Start Date of the project.

>[!NOTE]
>
>When the task has a cross-project predecessor, the handoff date of the successor recalculates only when either of the following occur:
>
>* You manually recalculate the timeline of the successor's project. You must have Manage permissions to the project to recalculate timeline. 
>* The timeline of the successor's project is automatically recalculated at night. 
>
>For information about recalculating the project's timeline, see [Recalculate project timelines](../../../manage-work/projects/manage-projects/recalculate-project-timeline.md).

* **When the task has a forced constraint for the Planned Dates**: The Handoff Date is always the same as the date set by the constraint, regardless of any other condition.   
  The following are forced constraints on tasks:

   * Must Start On
   * Must Finish On
   * Start No Earlier Than
   * Start No Later Than
   * Fixed Date

## Locate the Handoff Date

You can display the Handoff Date of a task in a task report or the view of a task list.  
For more information about building a report, see [Create a custom report](../../../reports-and-dashboards/reports/creating-and-managing-reports/create-custom-report.md).
