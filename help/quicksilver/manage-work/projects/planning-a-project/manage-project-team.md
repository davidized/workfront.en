---
product-area: projects;agile-and-teams
navigation-topic: plan-a-project
title: Manage the Project Team
description: The Project Team consists of users who are associated with the project. They display  in the People section of the project.
author: Alina
feature: Work Management
exl-id: 6e8036fc-feda-4277-9502-0b973028fccb
---
# Manage the Project Team

<!--
<drafted for Scheduling deprecation: 
remove the NWE way of doing this when the Scheduling tools will be removed from the app; leave just "adding automatically" and how to remove users - the People tab should still be there </p>
-->

The Project Team consists of users who are associated with the project. They display  in the People section of the project.

## Access requirements

You must have the following access to perform the steps in this article:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront plan*</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront license*</td> 
   <td> <p>Plan </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Access level configurations*</td> 
   <td> <p>Edit access to Projects</p> <p>View or higher access to Users</p> <p><b>NOTE</b> 
   
   If you still don't have access, ask your Workfront administrator if they set additional restrictions in your access level. For information on how a Workfront administrator can modify your access level, see <a href="../../../administration-and-setup/add-users/configure-and-grant-access/create-modify-access-levels.md" class="MCXref xref">Create or modify custom access levels</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Object permissions</td> 
   <td> <p>View or higher permissions to the project</p> <p>For information on requesting additional access, see <a href="../../../workfront-basics/grant-and-request-access-to-objects/request-access.md" class="MCXref xref">Request access to objects </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

*To find out what plan, license type, or access you have, contact your Workfront administrator.

## Add users to a Project Team

When you add users to the project team, they gain permissions on the project and the tasks, issues, and documents of the project. For more information, see the article [Project Team overview](../../../manage-work/projects/planning-a-project/project-team-overview.md).

You can add users to the project team in the following ways:

* [Automatically add users to a Project Team](#automatically-add-users-to-a-project-team) 
* [Manually add users to a Project Team](#manually-add-users-to-a-project-team)

### Automatically add users to a Project Team {#automatically-add-users-to-a-project-team}

The users that fulfill the following roles on the project are automatically added to the project team and appear  in the People section when the project is created:

* The creator of the project
* The project owner
* The project sponsor

Users are also automatically added to the project team when they are assigned to the following:

* Tasks
* Issues

### Manually add users to a Project Team {#manually-add-users-to-a-project-team}

You can manually add users to a project team by using the Scheduling section of the project. 

>[!IMPORTANT]
>
>The Scheduling tools are currently deprecated in Workfront and will be removed. 
> 
>After the removal of the Scheduling tools in Workfront, users will be added to the project team automatically, as described in the section [Automatically add users to a Project Team](#automatically-add-users-to-a-project-team-automatically-add-users-to-a-project-team) in this article
>
>For more information, see [Deprecation of Resource Scheduling tools in Adobe Workfront](../../../resource-mgmt/resource-mgmt-overview/deprecate-resource-scheduling.md). 

You can add users to a Project Team if they don't need to be assigned to any work items in the project but they need to be notified about certain actions that take place on the project. For more information about what notifications can be enabled for users on the project team, see [Event notifications available in Adobe Workfront](../../../administration-and-setup/manage-workfront/emails/event-notifications-available-in-wf.md)

>[!IMPORTANT]
>
>You can add to the Project Team only users that belong to the Group associated with the project.

1. Go to the project where you want to add users to the project team, then click **Scheduling** in the left panel.

   >[!TIP]
   >
   >You might need to click **Show More** to find the Scheduling section, or click Workload Balancer first, and then select **Scheduling** in the upper-left corner of the Workload Balancer.

1. Click **Add Users**.

   The Add Users to Project Team dialog box displays.

   ![add_users_dialog.png](assets/add-users-dialog-350x217.png)

1. In the **Add Users** box, begin typing the name of the user you want to add to the project team, then click the name when it appears in the drop-down list.

   Repeat this step to add multiple users to the project team.

1. Click **Add**.

   The users are now available in the project scheduling area.

## Remove users from a Project Team

When you remove users from their roles on the project, they remain part of the project team.

If you remove a user from the project team and the user is assigned to tasks or issues in the project, the user is unassigned from the tasks, and issues and the tasks and issues are returned to the Unassigned Work area in the Workload Balancer.

For more information about removing users from the project team, see the article [Remove users from projects](../../../manage-work/projects/manage-projects/remove-users-from-projects.md).
