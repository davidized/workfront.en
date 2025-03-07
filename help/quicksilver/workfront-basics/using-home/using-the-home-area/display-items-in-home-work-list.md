---
product-area: projects
navigation-topic: use-the-home-area
title: Display items in the Work List in the Home area
description: The Work List in the Home area displays all work items that are assigned to you. You can control which items display in the Work List as described below.
author: Lisa
feature: Get Started with Workfront, Work Management
exl-id: eac2e065-9e32-43c1-90ff-0f841b508c35
---
# Display items in the Work List in the Home area

The Work List in the Home area displays all work items that are assigned to you. You can control which items display in the Work List as described below.

## Access requirements

You must have the following access to perform the steps in this article:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><strong>Adobe Workfront plan*</strong></td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><strong>Adobe Workfront license*</strong></td> 
   <td> <p>Review for approvals only</p> <p>Work or higher for all other objects</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><strong>Access level configurations*</strong></td> 
   <td> <p>View or higher access to Projects, Tasks, Issues, and Documents</p> <p>Note: If you still don't have access, ask your Workfront administrator if they set additional restrictions in your access level. For information on how a Workfront administrator can modify your access level, see <a href="../../../administration-and-setup/add-users/configure-and-grant-access/create-modify-access-levels.md" class="MCXref xref">Create or modify custom access levels</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><strong>Object permissions</strong></td> 
   <td> <p>Contribute permissions or higher to the tasks and issues you need to work on</p> <p>For information on requesting additional access, see <a href="../../../workfront-basics/grant-and-request-access-to-objects/request-access.md" class="MCXref xref">Request access to objects</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

&#42;To find out what plan, license type, or access you have, contact your Workfront administrator.

## Filter the Work List {#filter-the-work-list}

You can filter items in the Work List to see only specific types of items. For example, you can filter the work list to display only issues or requests.

>[!NOTE]
>
>The filter options are stored in the browser. If you consistently use the same browser on the same computer (and do not clear the site data) the selected filters do not change. If you switch browsers or computers then the filters revert to the default option which is with all filters deselected.

1. Click the **Main Menu** ![](assets/main-menu-icon.png) in the upper-right corner, then click&nbsp;**Home**. 
1. Click the **Filter** ![](assets/filter-nwepng.png) drop-down menu. 
1. Select from the following filter options to specify the type of items you want to display:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"><strong>All</strong></td> 
      <td>Displays and selects all items. This includes tasks, issues, approvals, personal tasks, and completed tasks and issues. </td>
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Tasks Working On</strong></td> 
      <td> <p>Displays only tasks that you are actively working on. These are tasks assigned to you for which you have clicked the Work On It button.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Tasks Ready to Start</strong></td> 
      <td> 
       <div> 
        <p>Displays only tasks that are ready for you to start. Both of the following statements must be true:</p> 
        <ul> 
         <li> <p>The tasks and their parents have no predecessors or task constraints preventing them from being worked on.</p> </li> 
         <li> <p>The Planned Start Date of the tasks is in the past or up to two weeks in the future.</p> </li> 
        </ul> 
       </div> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Tasks Not Ready</strong></td> 
      <td> 
       <div> 
        <p>Displays only tasks that are not yet ready to start. Either one of the following statements must be true:</p> 
        <ul> 
         <li> <p>The tasks and their parents might have predecessors or task constraints that prevent them from being worked on.</p> </li> 
         <li> <p>The tasks have a Planned Start Date that is more than two weeks in the future.</p> </li> 
        </ul> 
       </div> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Issues Working On</strong></td> 
      <td> <p>Displays only issues that you are actively working on. These are issues assigned to you for which you have clicked the Work On It button.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Issues Requested</strong></td> 
      <td>Displays only issues that you are assigned to but for which you have not clicked the Work On It button.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Personal</strong></td> 
      <td>Displays only personal tasks. These are tasks that you create as a To Do task, as described in the section <a href="../../../workfront-basics/using-home/using-the-home-area/create-work-items-in-home.md#creating-a-personal-task">Create a personal task</a> in the article <a href="../../../workfront-basics/using-home/using-the-home-area/create-work-items-in-home.md">Create work items from the Home area</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Approvals</strong></td> 
      <td> 
       <div> 
        <p>Displays only approvals assigned or delegated to you and approvals you have submitted. Approvals include approvals on work items (projects, tasks, and issues), and approvals for documents, proofs, requests for access, and timesheets. For more information about approvals, see the following articles:</p> 
        <ul> 
         <li><a href="../../../review-and-approve-work/manage-approvals/view-approvals.md" class="MCXref xref">View approvals</a> </li> 
        </ul> 
        <ul> 
         <li> <p><a href="../../../review-and-approve-work/manage-approvals/manage-approvals.md" class="MCXref xref">Manage approvals</a> </p> </li> 
        </ul> 
        <p>Note: Approvals that you submitted and where you are also one of the approvers are counted twice.</p> 
       </div> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Completed</strong></td> 
      <td> <p>Displays only completed tasks, issues, and personal tasks. Completed work displays for the previous two weeks and it is grouped in the Work List according to the week in which they were completed. Approvals are not included.</p> <p>Completed work is hidden in the Work List unless you select this filter.</p> </td> 
     </tr> 
    </tbody> 
   </table>

   ![](assets/displaying-work-items-filters-nwe-350x401.png)

   >[!TIP]
   >
   >* Filter options are based on objects (Tasks, Issues, Approvals, Personal tasks). 
   >* Tasks and issues are further filtered by their state in relationship with our readiness to work on them (Working On, Ready to Start, Not Ready for tasks, and Working On and Requested for issues). You can select to display tasks or issues in a specific state or click Tasks or Issues to select and display all states. 
   >* There is a separate filter for completed items and it includes both tasks and issues. This does not include approvals. The Completed filter includes Personal tasks. 
   >* You can select only one state at a time. For example, you can display only Working On tasks and only Requested issues.   
   >* You cannot apply filters for items assigned to one of your teams and they are not included in the items that are assigned directly to you. 

1. (Optional) Further organize the Work List, as described in the section [Group and sort by Date, Project, and Priority](#group-and-sort-by-date-project-and-priority) in this article.

## Group and sort by Date, Project, and Priority {#group-and-sort-by-date-project-and-priority}

You can group and sort the Work List by Planned Completion Date, Commit Date, Project, or My Priority. The option you choose determines how items are grouped in the Work List.

1. Click the **Main Menu** ![](assets/main-menu-icon.png) in the upper-right corner, then click&nbsp;**Home**. 
1. Click the **Group by** drop-down menu.

   ![](assets/group-by-drop-down-expanded-in-home-with-planned-start-date-nwe-350x273.png)

1. Select from the following options:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"><strong>Planned Completion</strong></td> 
      <td> <p> Items display in the following groupings in the Work List, depending on their Planned Completion Date (the number of items contained within each grouping displays in parenthesis next to the heading title):</p> 
       <ul> 
        <li> <p>Late</p> </li> 
        <li> <p>No Planned Completion Date</p> </li> 
        <li> <p>This Week</p> </li> 
        <li> <p>This grouping is expanded by default.</p> </li> 
        <li> <p>Next Week</p> </li> 
        <li> <p>Planned, followed by various Planned Completion Dates (multiple groupings)</p> </li> 
        <li> <p>Complete</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Planned Start</strong></td> 
      <td> <p>Items display in the following groupings in the Work List, depending on their Planned Start Date (the number of items contained within each grouping displays in parenthesis next to the heading title):</p> 
       <ul> 
        <li> <p>Late</p> </li> 
        <li> <p>This Week </p> </li> 
        <li> <p>This grouping is expanded by default.</p> </li> 
        <li> <p>Next Week</p> </li> 
        <li> <p>Planned, followed by various Planned Start Dates (multiple groupings)</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Commit Date</strong></td> 
      <td> <p>Items display in the following groupings in the Work List (the number of items contained within each grouping displays in parenthesis next to the heading title):</p> 
       <ul> 
        <li> <p>No Commit Date</p> </li> 
        <li> <p>Committed Next Week</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>Project</strong></td> 
      <td>Items are grouped according to project, and projects appear alphabetically in the Work List.&nbsp;(The number of items contained within each grouping displays in parenthesis next to the heading title.)</td> 
     </tr> 
     <tr> 
      <td role="rowheader"><strong>My Priority</strong></td> 
      <td>Items display&nbsp;in an order you choose. For more information, see <a href="../../../workfront-basics/using-home/using-the-home-area/prioritize-work-in-home.md" class="MCXref xref">Prioritize work in the Home area</a>.</td> 
     </tr> 
    </tbody> 
   </table>

>[!NOTE]
>
>The default sorting is ascending.. If you change the sorting to descending , the selected sorting options are stored in the browser. If you consistently use the same browser on the same computer (and do not clear the site data) the sorting does not change, but if you switch browsers or computers then the sorting changes to the default sorting.

## View late items

Adobe Workfront uses the following dates to determine if work requests are late:

* **Tasks**: Planned Completion Date
* **Issues**: Planned Completion Date
* **Documents**: Submitted date
* **Timesheets**: Submitted date
* **Approvals**: Submitted date
* **Proof approvals**: Proof deadline

## Search the Work List

When you search the Work List, any items assigned to you are returned in the search (even items that are not currently loaded on the screen). If the Show complete option is selected, any items you marked complete within the past two weeks are also returned.

In addition, only the names of the work items are searched (information within the work item are not searched, neither are the names of the projects where the work item resides).

To search the Work List:

1. Click the **Main Menu** ![](assets/main-menu-icon.png) in the upper-right corner, then click&nbsp;**Home**. 
1. (Optional) Filter the Work List, as described in [Filter the Work List](#filter-the-work-list) and [Group and sort by Date, Project, and Priority](#group-and-sort-by-date-project-and-priority).

1. (Optional) If you are searching for a work item that is already complete, you must configure the Work List to display completed items before searching.
1. ![](assets/search-icon-highlighted-home-new-filters-and-sorting-nwe-350x238.png)

1. Begin typing the name of the item name you are searching for.   
   The Work List is automatically filtered as to include items with a matching name.

## Change the size of the Work List

You can change the size of the Work List so that it consumes anywhere between about a quarter of the Home area to about half of the Home area.

1. Click the **Main Menu** ![](assets/main-menu-icon.png) in the upper-right corner, then click&nbsp;**Home**. 
1. Mouse over the right edge of the Work List, then drag left or right until the Work List is the desired size.

## Collapse and expand groupings

Items in the Work List are displayed within groupings. You can collapse and expand groupings to control how much information is displayed on the page at a given time.

You can collapse and expand groupings within the Work List to better control what information is visible.  
By default, the This Week grouping is expanded and all other groupings are collapsed. Any changes you make are remembered the next time you access the Home area.

1. Click the **Main Menu** ![](assets/main-menu-icon.png) in the upper-right corner, then click **Home**. 
1. Click the **Expand** or **Collapse** arrow next to any grouping you want to expand or collapse.

   ![](assets/expand-section-icon-highlighted-home-new-filters-and-sorting-nwe-350x268.png)

   Or  
   To expand or collapse all groupings simultaneously, click the **Expand** or **Collapse** arrow next to any grouping while holding down the Shift key.
