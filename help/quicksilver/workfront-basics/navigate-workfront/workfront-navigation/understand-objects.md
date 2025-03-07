---
content-type: overview;reference
navigation-topic: workfront-navigation
title: Understand objects in Adobe Workfront
description: Understand objects in Adobe Workfront
feature: Get Started with Workfront
exl-id: f324f198-5472-4cf2-a46e-7fc24605ca90
---
# Understand objects in Adobe Workfront

<!--
<***Linked to several articles, do not remove/ change. 
-->

The information you display in Adobe Workfront is represented by objects which are stored in the Workfront database. The objects are what drives the information in Workfront.

Understanding how the objects are defined in Workfront is important so you can use the correct object for the needs necessary in your organization.

For example, when you plan a large amount of work, you need to use the Project object to define that work. To divide this work into smaller planned increments, you can use the Task object. For a smaller amount of work that is not planned, and can occur unexpectedly, you can use the Issue object. If you want to track the progress and the adherence to budget and timeline of a group of projects, you can organize them in Portfolios and Programs. To define other elements that help you resolve your work, you want to use other objects that are stored under Projects, Tasks, Issues, or Portfolios, like Documents, Notes, Hours, Users, or Job Roles.

Reports and Dashboards are another example of objects that can help you organize the amount of data you have in Workfront visually, to make it easily accessible for all users.

For a complete list of objects in Workfront, see the [API Explorer](../../../wf-api/general/api-explorer.md).

## Interdependency and hierarchy of objects

Objects are linked to one another in Workfront. For example, a task or an issue can never exist independently outside of a project. Tasks and issues are examples of objects that are stored in the project object. Tasks and issues are considered child objects to projects.

The following are some of the most commonly used objects in Workfront and their respective parent and children objects:

| **Object** |**Parent objects** |**Child objects** |
|---|---|---|
| Portfolios |  |Programs, Projects, Documents, Notes, Users |
| Programs |Portfolios |Projects, Documents, Notes, Users |
| Projects |Portfolios, Programs |Tasks, Issues, Documents, Notes, Hours, Users |
| Tasks |Projects |Issues, Children Tasks, Documents, Notes, Hours, Users |
| Issues |Tasks, Projects |Documents, Notes, Hours, Users |
| Dashboards |  |Reports, External Pages |
| Reports |Dashboards |  |
| Groups |  |Users |
| Teams |  |Users |
| Users |Groups, Teams, Companies |Job Roles |
| Companies |  |Users |
| Documents |Tasks, Issues, Projects, Portfolios, Programs, Users |  |
| Plans*  | |Initiatives |
| Goals* | |Results, Activities |
| Campaigns** |Portfolios, Programs |Projects |

For a complete list of objects in Workfront, see the [API Explorer](../../../wf-api/general/api-explorer.md).

*Plans are the objects of the Workfront Scenario Planner. For information about the Scenario Planner, see [The Scenario Planner overview](../../../scenario-planner/scenario-planner-overview.md).

*Goals are the objects of Workfront Goals. For information about Workfront Goals, see [Adobe Workfront Goals overview](../../../workfront-goals/goal-management/wf-goals-overview.md).

**Campaigns are available only in the Preview environment when you participate in the Campaigns beta program. The functionality described here might not be fully available yet. For more information about current available features and how to enroll, see [Campaigns beta](../../../product-announcements/betas/campaign-object-beta.md).

## Customize object names

As a Workfront administrator, you can customize object names in Workfront by using a Layout Template.

For more information about how to customize object names using a Layout Template, see [Create and manage layout templates](../../../administration-and-setup/customize-workfront/use-layout-templates/create-and-manage-layout-templates.md).

After you customize a layout template and you assign it to users, those users see the customized names for the objects. The users that have been assigned to the layout template no longer see the default names for the objects anywhere in the web application.

>[!NOTE]
>
>For the new names of the objects to be visible for your users, they must log out and log back in to Workfront after you have saved the Layout Template.

>[!IMPORTANT]
>
>The Workfront documentation always refers to the default names of the objects. As a Workfront administrator, ensure that you notify users of the changes in object names, so they can understand how to use the Workfront documentation, as well as the areas of the applications which do not reflect the changes in the names of the objects.

* [Object names that can be customized using a Layout Template](#object-names-that-can-be-customized-using-a-layout-template) 
* [Areas of Workfront that reflect the customized object names](#areas-of-workfront-that-reflect-the-customized-object-names) 
* [Areas of Workfront that do not reflect the customized object names](#areas-of-workfront-that-do-not-reflect-the-customized-object-names)

### Object names that can be customized using a Layout Template {#object-names-that-can-be-customized-using-a-layout-template}

As a Workfront administrator, you can customize the names of the following objects to match the terminology in your organization:

* Portfolio
* Program
* Project
* Task
* Issue
* Goal*
* Result*
* Activity*

  *Goals, results, and activities are only available if your company purchased Workfront Goals. For information about Workfront Goals, see [Adobe Workfront Goals overview](../../../workfront-goals/goal-management/wf-goals-overview.md).

* Initiative**
* Scenario**
* Plan**

  **Initiatives, scenarios, and plans are available only if your company purchased the Workfront Scenario Planner. For information about the Scenario Planner, see [Get started with the Scenario Planner](../../../scenario-planner/get-started-with-scenario-planning.md).

* Campaigns
  
  Campaigns are available only in the Preview environment when you participate in the Campaigns beta program. The functionality described here might not be fully available yet. For more information about current available features and how to enroll, see [Campaigns beta](../../../product-announcements/betas/campaign-object-beta.md).

For example, if the larger amount of work in your organization is known as a 'Engagement', you can replace the name 'Project' with 'Engagement'. Your Workfront interface shows 'Engagement' instead of 'Project' everywhere where the name 'Project' would appear.

For more information about how you can customize object names using Layout Templates, see [Create and manage layout templates](../../../administration-and-setup/customize-workfront/use-layout-templates/create-and-manage-layout-templates.md).

You cannot customize the names of any other object in Workfront. For a complete list of objects in Workfront, see the [API Explorer](../../../wf-api/general/api-explorer.md).

When you customize the name of an object, the new name for that object appears in most areas of the Workfront application where that object name would appear.

### Areas of Workfront that reflect the customized object names {#areas-of-workfront-that-reflect-the-customized-object-names}

The following areas show the updated name of the objects:

* Top Navigation  
* All  sections in the left panel navigation 
* All menus
* In-app notifications
* Report builder and reporting elements (views, filters, and groupings)
* Save buttons
* Exported files
* Emails
* Mobile Apps

### Areas of Workfront that do not reflect the customized object names {#areas-of-workfront-that-do-not-reflect-the-customized-object-names}

The following areas do not show the updated name of the objects:

  <!--
  <li data-mc-conditions="QuicksilverOrClassic.Draft mode"> <p>Referenced Object Type selection for a Typeahead field in a Custom Form </p> <p>(NOTE: drafting this because I don't think this is true)</p> </li>
  -->

* Outlook Add-in

## Implications of customizing object names

You should be aware of the following when customizing object names in Workfront:

* You may encounter stylistic or grammatical errors in system displays. For example, if you rename 'Issue' to 'Request' and you see anywhere in the system the phrase 'An request', this is functioning as intended and should not be considered a bug.
* Your custom names for the objects are not translatable. Only the Workfront default names can be translated in the supported languages. For more information about languages that are supported in Workfront, see [Supported languages in Adobe Workfront](../../../workfront-basics/supported-languages-in-workfront.md). The custom object name fields support foreign characters so you can input terminology in any language.
* When you customize object names using a Layout Template, we recommend that you assign your Layout Templates around your business units (Teams or Groups).  
  We recommend that you use names that are clearly understood by the users of these business units, to avoid confusion.
* Email notifications and delivered reports always contain object names as defined by the Layout Template of the user who generates the email. Your users should be prepared to see object names in their emails that are not related to their group or team, if they receive email notifications from users in other teams and groups.  
  As a Workfront administrator, advise users to notice the icons associated with each object. The icons remain consistent between various object names and consistent with the default object, as it appears in the database. For a list of all Workfront icons associated with objects, see [Object icons](#object-icons).

  >[!TIP]
  >
  >For common tasks in your organization, consider creating custom documentation to reflect your terminology.

## Object icons {#object-icons}

The Workfront documentation always refers to the default names of objects. If your objects have had their names customized, you can rely on the icon associated with them to understand which customized object corresponds to which Workfront default object.

For more information about which objects can have customized names in Workfront, see [Object names that can be customized using a Layout Template](#object-names-that-can-be-customized-using-a-layout-template).

The following is a list of objects and their corresponding icons in Workfront.

| **Object** |**Icon** |**Customizable object name** |
|---|---|---|
|Campaign* |![](assets/campaing-icon-without-beta-in-color.png),![](assets/campaing-icon-without-beta-black-and-white.png) |✔ |
| Company | ![](assets/company-icon-nwe.png)  , ![](assets/nwe-company-icon-54x54.png)|  |
| Dashboard | ![](assets/dashboard-icon-nwe.png)  , ![](assets/nwe-dashboards-icon.png)|  |
| Goal | ![](assets/nwe-goal-icon.png)|✔ |
| Group | ![](assets/groups-icon-nwe.png)  , ![](assets/nwe-group-icon.png)|  |
| Issue | ![](assets/issue-icon-nwe.png)  , ![](assets/nwe-issues-icon.png)|✔ |
| Job Role | ![job_role_icon.png](assets/job-role-icon-52x50.png), ![job_role_icon__1_.png](assets/job-role-icon--1--53x44.png), ![](assets/job-role-nwe-no-color.png), ![](assets/job-role-icon-nwe-color.png)|  |
| Plan | ![](assets/plan-icon.png), ![](assets/nwe-plan-icon-60x57.png)| |
| Portfolio | ![](assets/portfolio-icon-nwe.png)  , ![](assets/nwe-portfolios-icon.png)|✔ |
| Program | ![](assets/program-icon-nwe.png)  , ![](assets/nwe-programs-icon.png)|✔ |
| Project | ![](assets/project-icon-nwe.png)  , ![](assets/nwe-projects-icon.png)|✔ |
| Report | ![](assets/report-icon-nwe.png) , ![](assets/nwe-reports-icon.png)  |  |
| Task | ![](assets/task-icon-new.png)  , ![](assets/nwe-tasks-icon.png)|✔ |
| Team | ![](assets/team-icon-nwe.png), ![](assets/team-icon-nwe-color.png) , ![](assets/nwe-teams-icon.png)|  |
| Template | ![](assets/template-icon-nwe.png)  , ![](assets/nwe-templates-icon.png)|  |

*Campaigns are available only in the Preview environment when you participate in the Campaigns beta program. The functionality described here might not be fully available yet. For more information about current available features and how to enroll, see [Campaigns beta](../../../product-announcements/betas/campaign-object-beta.md).

## Reference Numbers of objects

Each object created in Workfront is assigned a unique reference number. Reference numbers are useful in distinguishing between two otherwise similar objects (such as tasks with the same name). You can search for objects using their reference numbers and you can include reference numbers in reports.

For information about how to search for objects by reference number, see [Use the reference number of objects](../../../workfront-basics/navigate-workfront/search/reference-number-of-objects.md).

## Object-specific searches

You can search across all the objects that are searchable in Workfront, or you can select a specific object to search for in your basic and advanced searches.

Not all objects are searchable in Workfront. You can run basic and advanced searches for the following objects in Workfront:

| **Object** |**Basic Search** |**Advanced Search** |
|---|---|---|
| Projects |✓ | ✓ |
| Tasks |✓ | ✓ |
| Issues |✓ | ✓ |
| Reports |✓ | ✓ |
|   Users   |✓ | ✓ |
| Templates |✓ | ✓ |
| Documents |✓ | ✓ |
| Portfolios |✓ | ✓ |
| Programs | ✓ | ✓ |
| Dashboards | ✓ | ✓ |
| Companies | ✓ | ✓ |
| Notes | ✓ |  |

For more information about running basic and advanced searches in Workfront, see [Search Adobe Workfront](../../../workfront-basics/navigate-workfront/search/search-workfront.md).

## Report on objects

Understanding the hierarchy and interdependency of objects is extremely important before you start building reports in Workfront. Reports are object-specific. You must select the correct object for your report before you can display the data that you want.

Depending on what object you selected for your report, you can access only those objects that are directly linked to the object of the report.

>[!IMPORTANT]
>
>You can report only on the object you select and the parent objects in the same report. You cannot have information about the children objects in a parent object report. For example, you can display project information in a task report, but not task information in a project report.

You can report on all objects in the database using our open API. For a complete list of all objects in the database, see [API Explorer](../../../wf-api/general/api-explorer.md).

>[!NOTE]
>
>If you have customized the names of your objects using a layout template, the names for the object in the report builder have also been customized. Ensure you know what objects have been customized and look for the customized name in the report builder. For more information about which objects can have customized names in Workfront, see * [Object names that can be customized using a Layout Template](#object-names-that-can-be-customized-using-a-layout-template).* 
>When using text mode in your reports, the names of the objects in text mode expressions are the standard names in Workfront, and not the customized object names. For more information about using text mode in reports, see [Text Mode overview](../../../reports-and-dashboards/reports/text-mode/understand-text-mode.md).

For more information about building a report, see [Create a custom report](../../../reports-and-dashboards/reports/creating-and-managing-reports/create-custom-report.md).  
For more information about our API, see [API Explorer](../../../wf-api/general/api-explorer.md).

You can report on the following objects when using the report builder in the Workfront web application:

* Project
* Task
* Hour
* Issue
* User
* Access Level
* Approval
* Approval Process
* Assignment
* Backlog Work Item  
  Displays tasks or issues on the agile backlog. For more information about the agile backlog, see [Manage the agile backlog](../../../agile/work-in-an-agile-environment/manage-the-agile-backlog.md).

* Baseline
* Baseline Task
* Billing Record
* Budgeted Hour

  This is the Budgeted Hours, as they appear in the in older, deprecated resource management tools.
  
  The "Bud. Hours" field in the Budgeted Hour report refers to the hours budgeted for job roles in the Resource Planner . For more information, see [Understand Budgeted Labor Cost and Budgeted Hours for projects](../../../manage-work/projects/project-finances/budgeted-labor-cost.md).

* Calendar Event
* Category (or Custom Form)
* Company
* Dashboard
* Document
* Document Approval
* Document Version  
  Enables you to view various information about the version of the document, the document the version is associated with, who created the version, and the user who created the proof on the document version if one exists (Proof Creator).
* Email Template
* Expense
* Expense Type
* External Page
* Favorite
* Filter
* Goal

  You can build a report for strategic goals or you can display goal-related information in a project report when projects are associated with goals as goal activities. You can create strategic goals and connect projects them only if your organization has purchased a Workfront Goals license. For information about Workfront Goals, see [Workfront Goals overview](https://one.workfront.com/s/document-item?bundleId=the-new-workfront-experience&topicId=Content%2FWorkfront_Goals%2FGoal_management%2Fwf-goals-overview.htm&_LANG=en). For information about connecting projects to strategic goals, see [Overview of connecting projects to goals](https://one.workfront.com/s/document-item?bundleId=the-new-workfront-experience&topicId=Content%2FWorkfront_Goals%2FResults_and_activities%2Fconnect-projects-to-goals-overview.htm&_LANG=en). 

  <!--
  <MadCap:conditionalText data-mc-conditions="QuicksilverOrClassic.Draft mode">
  (NOTE:&nbsp;hardcoded links in this paragraph)
  </MadCap:conditionalText>
  -->

  >[!TIP]
  >
  >You cannot report on project goals that are associated with a Business Case. For information about project goals vs strategic goals, see [Glossary of Adobe Workfront terminology](../../../workfront-basics/navigate-workfront/workfront-navigation/workfront-terminology-glossary.md).

* Group
* Grouping
* Hour Type
* Initiative

  You can build a report for initiatives which are the children objects of a plan only if your company has purchased a Workfront Scenario Planner license. For information about initiatives, see [Initiatives overview in the Workfront Scenario Planner](https://one.workfront.com/s/csh?context=2066&pubname=the-new-workfront-experience). 

  <!--
  <MadCap:conditionalText data-mc-conditions="QuicksilverOrClassic.Draft mode">
  (NOTE: this link is hardcoded)
  </MadCap:conditionalText>
  -->

* Initiative Job Role

  You can build a report for the job roles associated with the initiatives in a plan only if your company has purchased a Workfront Scenario Planner license. For information about creating initiatives and associating them with job roles, see [Create and edit initiatives in the Workfront Scenario Planner](https://one.workfront.com/s/csh?context=2061&pubname=the-new-workfront-experience). 

  <!--
  <MadCap:conditionalText data-mc-conditions="QuicksilverOrClassic.Draft mode">
  (NOTE: this link is hardcoded)
  </MadCap:conditionalText>
  -->

* Iteration
* Job Role
* Journal Entry

  You can report on tracked system updates in the Updates area of objects like tasks, projects, issues, etc. To learn more, see [Report on the Updates area](../../../reports-and-dashboards/reports/creating-and-managing-reports/create-journal-entry-report.md).

* Layout Template

  <!--
  <li data-mc-conditions="QuicksilverOrClassic.Draft mode"> <p>Legacy Resource Pool (NOTE: drafted; removed at 20.4)</p> <note type="note">
  This report captures information about an area in&nbsp;Workfront that has been removed. The report might display legacy information but it does not update with current data. Although not recommended, you may update the information in this report using the API. For information about the current resource pools, see
  <a href="../../../resource-mgmt/resource-planning/resource-pools/work-with-resource-pools.md" class="MCXref xref"> Resource pools overview </a>.
  </note> </li>
  -->

* Milestone
* Milestone Path
* Note

  >[!NOTE]
  >
  >You can report on comments added by individual users.

* Parameter (or Custom Field)
* Parameter Group (or Section Break)
* Portal Profile (this displays information that has been deprecated)
* Portfolio
* Program
* Project (Financial Data)

  >[!NOTE]
  >
  >Financial information populates in Project (Financial&nbsp;Data) reports only when the data associated with it is less than 5 years old. For example, if a job role was allocated to a task in January 2015 and today is September 2021, a financial filed like the Allocation Date for the job role does not populate in the Project (Financial&nbsp;Data) report.

* Proof Approval  
  Enables you to view various information about the proof approval, including: the proof that was submitted for approval, information about the Approver, information about the Requester (if the Requester is a licensed Workfront user), version information, the proof ID, and the proof creation date.  
  Proof Approval reports include only proofs that are available in users' My Work areas where decisions have not yet been made.  
  Proof approvals are assigned in Workfront as described [Add users to a proof](../../../review-and-approve-work/proofing/managing-proofs-within-workfront/share-a-proof-in-workfront.md#add) in [Share a proof within Adobe Workfront](../../../review-and-approve-work/proofing/managing-proofs-within-workfront/share-a-proof-in-workfront.md).

* Queue
* Queue Topic
* Rate (this displays job role Billing Rate information)
* Reminder Notification
* Report

  <!--
  <li data-mc-conditions="QuicksilverOrClassic.Draft mode"> <p>Resource Estimate (NOTE: drafted; removed with 20.4 - flash)</p> <note type="note">
  This report captures information about an area in&nbsp;Workfront that has been removed. The report might display legacy information but it does not update with current data. Although not recommended, you may update the information in this report using the API. For information about how you estimate resources for projects, see
  <a href="../../../resource-mgmt/resource-planning/get-started-resource-planner.md" class="MCXref xref">Resource Planner overview</a>.
  </note> </li>
  -->

* Resource Pool
* Risk
* Risk Type
* Schedule
* Scorecard
* Team
* Template
* Template Task
* Time Off

  You can report on a user's time off as indicated by the user in their profile.

* Timesheet
* Timesheet Profile
* Topic Group
* User Delegation  

  You can report on users who have been delegated to perform others' tasks and issues while they are out of the office. This report displays the user who is out of the office as well as the user who fulfills their duties while they are out. 
  
* View
* Work Item (this refers to tasks and issues)
