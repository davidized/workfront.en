---
content-type: tips-tricks-troubleshooting
navigation-topic: tips-tricks-and-troubleshooting-workfront-basics
title: Working across time zones
description: It can be helpful to understand how Adobe Workfront uses time zones to calculate the following - EDIT ME.
feature: Get Started with Workfront
exl-id: b6574165-a6dc-4694-a367-d98927abf1e3
---
# Working across time zones

It can be helpful to understand how Adobe Workfront uses time zones to calculate the following:

* Time fields for objects
* Times in other Workfront areas, such as automated Workfront emails

## Time zones in Workfront

Times you see in Workfront are based on time zone configurations for your organization's Workfront instance and for your user profile. If these two time zones are different, you might see time discrepancies in different areas and features you use in Workfront. 

>[!NOTE]
>
><div class="preview">In a custom form attached to an object, date and time statements in calculated custom fields are calculated and saved by Coordinated Universal Time (UTC), not by the time zone configurations set for your organization's instance and your user profile. Calculations in a custom form are generated and displayed based on each users' individual time zones.</div>


* [Your organization's Workfront instance](#your-organization-s-workfront-instance) 
* [Your user profile](#your-user-profile)

### Your organization's Workfront instance {#your-organization-s-workfront-instance}

The time zone for your organization's Workfront instance is usually set for the location of the main office. This determines the following:

* The time shown in emails generated by&nbsp;Workfront
* The time zone for newly added users (before the Workfront administrator configures a different time zone for them based on where they work)

  For more information about these two examples, see [Configure basic information for your system](../../administration-and-setup/get-started-wf-administration/configure-basic-info.md).

* The start or end of an overridden billing rate for a project. For more information, see [Override Job Role Billing Rates at the project level](../../manage-work/projects/project-finances/override-job-role-billing-rates-at-the-project-level.md).

### Your user profile {#your-user-profile}

The time zone in your user profile should be configured for the location where you work. This determines the following:

* The time shown in your outgoing Workfront email messages
* Times for an object you work on, such as start and end times

  If users in multiple time zones are assigned to an object, Workfront converts the object times for everyone involved, using the time zone configured in each user profile.

  **Example:** In the Eastern Standard Time (EST) zone where you work, you set a task to start at 4:00 PM and assign it to users working in the Pacific Standard Time (PST) zone. For those users, the start time displays as 1:00 PM. If it were to display it as 4:00 PM, they would start working on it three hours late.

  If the object creator doesn't note the difference between the assignees' time zones and make the necessary adjustments when setting object times, or the assignees don't note that difference, it can be hard to get the timing right while everyone collaborates on the object.

  **Example:** You configure a one-day task to start at 9:00 AM EST, forgetting that some users on the task work in the PST zone. For them, the start time 6:00 AM. Because they won't start working on it until 9:00 their time (noon your time), the task begins and finishes three hours late.

For information configuring your time zone in your user profile, see [Configure My Settings](../../workfront-basics/manage-your-account-and-profile/configuring-your-user-profile/configure-my-settings.md).

For information about how a Workfront administrator (or someone with Edit access to users) can configure the time zone in a user profile, see [Edit a user's profile](../../administration-and-setup/add-users/create-and-manage-users/edit-a-users-profile.md).

## How you can make it easier for users to work across time zones

You can help users working more easily across several time zones in several ways:

* [Use schedules](#use-schedules) 
* [Use calculated time fields in a custom form](#use-calculated-time-fields-in-a-custom-form) 
* [Use text fields instead of date fields in a custom form](#use-text-fields-instead-of-date-fields-in-a-custom-form)

### Use schedules {#use-schedules}

Workfront administrators create separate schedules for each time zone within your organization to ensure that work is scheduled appropriately for everyone, wherever they are. Once the administrator creates the schedules, they can be associated with certain projects and users:

* **Projects**: A project creator can select a schedule for an individual project. This determines the scheduling of the tasks in the project, based on the working hours set for the assignees' time zones. 
* **Users**:&nbsp;A Workfront administrator (or someone with Edit access to users) can select a schedule for individual user in the user's profile.

  This schedule might be different from a project schedule. For example, when someone creates a task in the project and hasn't assigned anyone to it yet, the task uses the project schedule. When a user is assigned to the task, the task uses that user's schedule.

  If multiple users are assigned to a task, the system uses one of the following, as configured in the system-wide project preferences:

   * The time zone for the schedule of the task's primary owner
   * The time zone for the schedule of the project.

  This can cause tasks dates to change.

  **Example:** An EST user is assigned to a one-day task scheduled to start at 9:00 AM PST, which is noon EST. Because the EST user has only 2 working hours remaining for the day, the task completion date extends by about 6 hours into the next working day.

  For information about the Project&nbsp;Preferences area of Setup, see [Configure system-wide project preferences](../../administration-and-setup/set-up-workfront/configure-system-defaults/set-project-preferences.md).

  For instructions on assigning a schedule to a project or a user, see [Create a schedule](../../administration-and-setup/set-up-workfront/configure-timesheets-schedules/create-schedules.md).

  For information about how the time zone configured in your schedule affects the distribution of Planned Hours in the Scheduling tools and in the Workload Balancer, see the following:

   * [Manage user allocations in the Scheduling areas](../../resource-mgmt/resource-scheduling/manage-allocations-scheduling-areas.md) 
   * [Manage user allocations in the Workload Balancer](../../resource-mgmt/workload-balancer/manage-user-allocations-workload-balancer.md)

### Use calculated time fields in a custom form {#use-calculated-time-fields-in-a-custom-form}

You can use a series of calculated custom fields on a custom form to display the current time for users in your organization, like a row of airport clocks displaying the time in multiple cities. You could create a field for each of the time zones where your users work, each calculating the time for its time zone.

For more information, see [Add calculated data to a custom form](../../administration-and-setup/customize-workfront/create-manage-custom-forms/add-calculated-data-to-custom-form.md), as well as the section [Date & time calculated custom fields](../../reports-and-dashboards/reports/calc-cstm-data-reports/calculated-data-expressions.md#date) in the article [Calculated data expressions](../../reports-and-dashboards/reports/calc-cstm-data-reports/calculated-data-expressions.md).

### Use text fields instead of date fields in a custom form {#use-text-fields-instead-of-date-fields-in-a-custom-form}

If you don't want Workfront to convert times you configure for in an object for users in different time zones, you can use a text field in a custom form that you attach to an object, rather than a date field. This way, the time displays the time you type for everyone on the project.

If you do this, we recommend that you remind the form's users to calculate the difference between their time zone and yours so that they can determine when work should start and end. You could include this in the instructions you type for the custom form, or in a tool tip for that field. For more information, see [Add a custom field to a custom form](../../administration-and-setup/customize-workfront/create-manage-custom-forms/add-a-custom-field-to-a-custom-form.md).
