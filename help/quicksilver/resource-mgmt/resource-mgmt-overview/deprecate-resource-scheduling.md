---
content-type: reference
product-area: resource-management
keywords: workload,balancer
navigation-topic: resource-management-overview
title: Deprecation of Resource Scheduling tools in Adobe Workfront
description: We are currently in the process of deprecating all Scheduling tools from Adobe Workfront and replacing them with the Workload Balancer.
author: Alina
feature: Resource Management
exl-id: 7fa644cd-cf6a-40f8-ae28-bf222bb45d3f
---
# Deprecation of Resource Scheduling tools in Adobe Workfront

<span class="preview">The highlighted information on this page refers to functionality not yet generally available. It is available only in the Preview environment.</span> 

We are currently in the process of deprecating all Scheduling tools from Adobe Workfront and replacing them with the Workload Balancer.

>[!IMPORTANT]
>
>The deprecation of the Scheduling tools means that as of now, we are no longer implementing new feature functionality for the current Scheduling solution and we no longer consider nor prioritize defects for a fix in this area of Adobe Workfront.

This article describes a tentative timeline for this deprecation and it compares the functionality of the Scheduling tools and that of the Workload Balancer. 

A more exact timeline will be announced through the Announcement Center and this article will be updated as this process continues during the following months.

>[!NOTE]
>
>The changes described in this article do not affect any other resource management tools. For example, they do not affect the [!UICONTROL Resource Planner] or the [!UICONTROL Utilization] report.

## How you should prepare

For detailed information about how you should prepare for the transition between Scheduling and the Workload Balancer, see [Migrate from Resource Scheduling to the Workload Balancer](../../resource-mgmt/resource-mgmt-overview/migrate-resource-scheduling-to-workload-balancer.md).

If you currently use Scheduling tools we recommend that you consider discontinuing them and start using the Workload Balancer. 

![The global Resource Scheduling area](assets/resource-scheduler-global-350x127.png)

Most of the functionality previously available in the Scheduling areas is now available in the Workload Balancer. For information, see the section [Feature availability](#feature-availability) in this article.

![The global Workload Balancer area](assets/workload-balancer-pti-350x111.png)

Over time, you can continue using the Workload Balancer for all your scheduling needs, as more capabilities become available in the near future.

## Information that will not transfer to the Workload Balancer

The following information will not transfer from the Scheduling tools to the Workload Balancer:

* **Daily allocations for users**: You should not use both Scheduling and the Workload Balancer at the same time to adjust the same user allocations. If you have managed user allocations in the Scheduling tools, the adjusted daily allocations do not transfer to the Workload Balancer. Similarly, if you have adjusted user allocations in the Workload Balancer, they do not transfer to the Scheduling tools. We strongly encourage you to ensure that the daily allocations are accurate in the Workload Balancer to prepare for this transition.
* **Filters**: If you have saved filters in the Scheduling areas, they do not transfer to the Workload Balancer. You must recreate the filters in the Workload Balancer.

## Deprecation timeline highlights

>[!IMPORTANT]
>
>Please use this article to understand the latest timeline for deprecating the Scheduling tools. Any updates to this timeline will be communicated in this article and in Announcement Center messages.

The following is a tentative timeline for the deprecation process of Resource Scheduling tools:

* [2020.4 release (November 2020)](#2020-4-release-november-2020) 
* [2021.4 release (October 2021)](#2021-4-release-october-2021) 
* [2022.4 release (October 2022) (tentative) ](#20224-release-october-2022-tentative)

### 2020.4 release (November 2020) {#2020-4-release-november-2020}

* New feature functionality is no longer implemented for the Scheduling solution
* Only High and Critical severity defects will be prioritized for a fix
* New Workload Balancer capabilities added to Workfront

### 2021.4 release (October 2021) {#2021-4-release-october-2021}

* Workload Balancer is set as default for any first-time user of Workfront
* Enhanced filters that can be shared and include additional fields

### 2022.4 release (October 2022) (tentative)

* No defects will be prioritized for a fix during the 2022.4 release
* All Scheduling areas are removed from Workfront
* The Workload Balancer is the only resource scheduling tool available in Workfront

## Feature availability {#feature-availability}

Unless otherwise specified, all Resource Scheduling features have been or will be available in the Workload Balancer. For information about the Workload Balancer, see [Overview of the Workload Balancer](../../resource-mgmt/workload-balancer/overview-workload-balancer.md).

In addition to existing features, the Workload Balancer has or will have new functionality that did not exist in the Resource Scheduling tools, as shown in the following table: 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td rowspan="2"><span style="font-weight: normal;">Features</span> </td> 
   <td rowspan="2"> Resource Scheduling tools feature availability</td> 
   <td colspan="3">Workload Balancer feature availability</td> 
  </tr> 
  <tr> 
   <td>Available now</td> 
   <td>Available soon</td> 
   <td>Not planned</td> 
  </tr> 
  <tr> 
   <td> <p>Access tool from the Resourcing area</p> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Separate areas for unassigned and assigned work</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Apply and create filters for unassigned and assigned work</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Access work items directly from the tool</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Manually assign or unassign tasks and issues</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Adjust individual allocations</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Include issue time</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Display projected dates </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Display completed work</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Show user time off, weekends, and schedule exceptions</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td><span>Assign and unassign tasks and issues by dragging and dropping*</span> </td> 
   <td>✓</td> 
   <td><span>✓</span> </td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Automatically assign tasks and issues</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td><span>Quickly assign users based on roles*</span> </td> 
   <td>✓</td> 
   <td><span>✓</span> </td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td><span>Quickly replace users*</span> </td> 
   <td>✓</td> 
   <td><span>✓</span> </td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td><span>Quickly unassign users*</span> </td> 
   <td>✓</td> 
   <td><span>✓</span> </td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td><span>Access tool from a team</span> </td> 
   <td>✓</td> 
   <td><span>✓</span> </td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td><span>Access tool from a project</span> </td> 
   <td>✓</td> 
   <td><span>✓</span> </td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr>
   <td><span class="preview">Work-license users can adjust user allocations</span> </td> 
   <td>✓</td> 
   <td><span class="preview">✓</span></td> 
   <td></td> 
   <td></td> 
  </tr> 
  <tr> 
   <td><span class="preview">Display issues in the Unassigned Work area</span></td> 
   <td>✓</td> 
   <td><span class="preview">✓</span></td> 
   <td></td> 
   <td></td> 
  </tr> 
  <tr> 
   <td>Visible to all Plan users, without being designated a Resource Manager on the project.</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Group information by project</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Share the Workload Balancer with users with no access to the Resourcing area</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Display and adjust allocations by week</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Access users directly from the tool</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>Access more information about work items without navigating away, using the Summary panel*</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Display and adjust allocation as a percentage value </td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Display the difference between the available and allocated time</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Display user availability in a chart</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Color-code work items and projects by Project Status</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Automatically update Planned Hours as you adjust user allocation (for tasks with a Simple Duration Type)</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td><span>Suggest assignments based on the user's assignment pattern, existing Role or Team assignments</span> </td> 
   <td>&nbsp;</td> 
   <td><span>✓</span> </td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td>Enhanced filters that can be shared and include additional fields</td> 
   <td>&nbsp;</td> 
   <td>✓</td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr> 
  <tr> 
   <td><span>Make advanced assignments</span> </td> 
   <td>&nbsp;</td> 
   <td><span>✓</span> </td> 
   <td>&nbsp;</td> 
   <td>&nbsp;</td> 
  </tr>
  
 </tbody> 
</table>

*These features are available only in the new Adobe Workfront experience.
