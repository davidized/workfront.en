---
filename: migrate-resource-scheduling-to-workload-balancer
product-area: resource-management
navigation-topic: resource-management-overview
title: Migrate from Resource Scheduling to the [!UICONTROL Workload Balancer]
description: We want you to experience as little work disruption as possible by helping you design a migration plan. The steps below will help you get your team trained and determine the best time for you to switch to the Workload Balancer.
author: Alina
exl-id: 4bc08d5f-99c7-40e2-85d6-1de0b585aef8
---
# Migrate from Resource [!UICONTROL Scheduling] to the [!UICONTROL Workload Balancer]

>[!IMPORTANT]
>
>The information in this article applies to you only if you have managed the scheduling of your resources in the Resource [!UICONTROL Scheduling] areas of Adobe Workfront. Workfront started the deprecation of the [!UICONTROL Scheduling] tools in November 2020 and plans to replace them with the [!UICONTROL Workload Balancer].   
>For information about the deprecation plan for the [!UICONTROL Resource Scheduling] tools and the timeline for their replacement with the [!UICONTROL Workload Balancer], see [Deprecation of Resource Scheduling tools in Adobe Workfront](../../resource-mgmt/resource-mgmt-overview/deprecate-resource-scheduling.md).

We want you to experience as little work disruption as possible by helping you design a migration plan. The steps below will help you get your team trained and determine the best time for you to switch to the [!UICONTROL Workload Balancer].

## Locate the Resource Scheduling tools

You and your teams may be using some of the Resource [!UICONTROL Scheduling] tools in the following areas of Workfront:

* The [!UICONTROL Scheduling] section in the [!UICONTROL Resourcing] area
* The [!UICONTROL Scheduling] section of a project
* The [!UICONTROL Schedule] section of a team

With this deprecation, the [!UICONTROL Workload Balancer] replaces all the  [!UICONTROL Resource Scheduling] tools in all areas.

## Step 1: Get your teams trained

Take the training [Resource Management Program for the new Adobe Workfront experience](https://one.workfront.com/s/resource-management-program-nwe) (75 minutes) on Workfront One.

<!--If you use Adobe Workfront Classic, take the training [Resource Manager Training Program](https://customer-sso.workfront.com/training?SAMLRequest=fVJdb9swDPwrftOT448ZqyPEAYIEAwJ0Q5B2fdjLwMh0K1SWNJFes38%2FKW22DOjyJIA8nu6OXBCMxsvVxE92jz8mJM5WRBhYO7t2lqYRwx2Gn1rh1%2F1tJ56YPcmiUBOxi738xYXnITjLs0PQ%2FSOC9zPlxgIiZZHYCwXGHEA9i2wT6bWFxP0OE5Gb%2FWVLHBxAW20fRbbddOK76ufz9jBv83YYPuYN1nU%2B76HJq1q10H6o2rq%2FiVCiCbeWGCx3oi7rMq%2BqvGzu60qWN7JpvonsAQOdRNSzUmTH0ViSSWsnpmClA9IkLYxIkpW8W32%2BlREo4RzM5Yi%2FPuODY6ecEctFQsuTurBM5qP3fyJbFJeIxetmvkTG7WbnjFa%2FspUx7mUdEBg7wWFCkX1yYQS%2BriFVdJ8PJ6j0yTsxWhbF%2BZe31WN%2FOoS4d8YjZ2s3egiaUlB4BMVnE5eotYmx7HFYXk1OSZVwsbyLT9xyv4vBoIpf3gew5F3gN%2F%2Fvkr%2F2%2FiP0T%2FfyjJe%2FAQ%3D%3D) (120 minutes) in Workfront Ascent. You must sign in to Workfront Ascent to access the course.
-->

If you experience difficulty logging in or accessing the course, contact Customer Support. For information, see [Contact Customer Support](../../workfront-basics/tips-tricks-and-troubleshooting/contact-customer-support.md).

## Step 2: Determine the best time to migrate {#step-2-determine-the-best-time-to-migrate}

Follow the steps below to determine when the best time to migrate is for you:

1. Determine which features in the Resource [!UICONTROL Scheduling] tools your team uses most and make sure those features are available in the [!UICONTROL Workload Balancer]. For information about which features are currently available in the [!UICONTROL Workload Balancer], see the "Feature availability" section in the article [Deprecation of Resource Scheduling tools in Adobe Workfront](../../resource-mgmt/resource-mgmt-overview/deprecate-resource-scheduling.md).

   If the features you need are not available yet, you might want to wait to migrate (see Step 3a in the following section in this article).

1. Determine whether your team manages user allocations on assignments. Adjusting or modifying user allocations means modifying the planned hours per day for each user across the duration of a work item. By default, the system equally distributes the total Planned Hours of a work item across the entire duration of the item. For information about managing allocations in the Resource Scheduler, see the “Modify user allocations” section of the article [Manage user allocations in the Scheduling areas](../../resource-mgmt/resource-scheduling/manage-allocations-scheduling-areas.md).

1. Any saved filters in the Scheduling area will not automatically transfer to the Workload Balancer. Make time to create any filters you might need in the Workload Balancer. For information about creating filters in the Workload Balancer, see [Manage filters in the Workload Balancer](../workload-balancer/filter-information-workload-balancer.md).

<!--
1. Using the information gathered from Steps 1 and Step 2, decide which version of Step 3 you should continue with based on the needs of your organization.
-->

## Step 3: Migrate to the [!UICONTROL Workload Balancer]{#step-3-migrate-to-the-workload-balancer}

We have identified the following versions for this step, depending on your findings in Step 2:

* [Step 3a: You or your teams use the [!UICONTROL Scheduling] tools, but do not modify user allocation](#step-3a-you-or-your-teams-use-the-scheudling-tools-but-do-not-modify-user-allocation) 
* [Step 3b: You or your teams manage user allocations in the [!UICONTROL Scheduling] tools](#step-3b-you-or-your-teams-manage-user-allocations-in-the-scheduling-tools)

### Step 3a: You or your teams use the [!UICONTROL Scheduling] tools, but do not modify user allocation

If you or your teams do not modify the daily hour allocations on work assignments, then you are ready to switch scheduling resources to the [!UICONTROL Workload Balancer].

![](assets/nwe-workload-balancer-global-350x125.png)

Do the following:

* Pick a transition date.

  >[!TIP]
  >
  >Give your team 2-4 weeks to get through the training prior to the transition date. For information about training see the section [Migrate from Resource Scheduling to the Workload Balancer](#migrate-from-resource-uicontrol-scheduling-to-the-uicontrol-workload-balancer) in this article. 

* Follow these guidelines to assist your teams:

   * Encourage your teams to visit the [Overview of the [!UICONTROL Workload Balancer]](../../resource-mgmt/workload-balancer/overview-workload-balancer.md) page and all the pages linked from there to dig deeper into how the [!UICONTROL Workload Balancer] works. 
   * Host FAQ meetings for your teams to answer questions the week before the transition, make the switch, and then hold another FAQ meeting to answer follow-up questions.
   * Submit feedback to Workfront using the Feedback button in the top toolbar. Our product developers are always interested in hearing your use cases for how we can make the [!UICONTROL Workload Balancer] provide more value.

### Step 3b: You or your teams manage user allocations in the [!UICONTROL Scheduling] tools

If your workflow matches this scenario, you should be more strategic in your transition plan. The daily allocations that display in the [!UICONTROL Scheduling] tools are stored in a different database than the daily allocations that display in the [!UICONTROL Workload Balancer]. This means that the adjustments of daily allocations that you do in the Resource [!UICONTROL Scheduling] tools do not transfer to the daily allocations in the [!UICONTROL Workload Balancer].

Consider the following when making the transition to the [!UICONTROL Workload Balancer] when you use this [!UICONTROL Scheduling] functionality:

* Decide whether it is possible to put a hold on managing allocations for 1-2 weeks as your resource managers make the switch. To do this:

   * Find out the average duration of tasks in your current projects and take that into consideration when determining how long you need to put a hold on managing the user allocations.

     >[!TIP]
     >
     >You need to only look at your current or planning projects, which are those for which your teams are actively making assignments and managing daily allocations.

   * Create a task report and add the task Duration field in the view and group it by Project Name. Summarize the Duration column in the View by the Average, then save your report.

     For information about creating a report, see [Create a custom report](../../reports-and-dashboards/reports/creating-and-managing-reports/create-custom-report.md) . 
   
   * Analyze your task report. For example, if your average task duration is 3 days, then a one week transition might be best. Have the team stop managing user allocations for a week. The following week, transition the team to the [!UICONTROL Workload Balancer] and begin managing user allocations that following week.

     ![](assets/timeline-stop-using-resource-scheduler-callouts-350x178.png)

     >[!TIP]
     >
     >You can continue to make task and issue assignments during the transition period. Assignments made will be reflected in both the Resource Scheduler and [!UICONTROL Workload Balancer].

* If you are a larger organization with teams managing resources for hundreds of projects, you may consider transitioning from the [!UICONTROL Resource Scheduler] to the [!UICONTROL Workload Balancer] one portfolio at a time. Consider a phased roll-out by creating customized filters in the [!UICONTROL Workload Balancer] to look at one specific portfolio at a time.

* Allow your resource managers to team up: have one person review assignments made in the  [!UICONTROL Resource Scheduling] tools and one making appropriate adjustments in the [!UICONTROL Workload Balancer]. Once that team of two reconciles both tools, have them shift their workflows to the [!UICONTROL Workload Balancer].

## Need more assistance

If you need additional information with this migration, contact Custom Support. For information about contacting Support, see [Contact Customer Support](../../workfront-basics/tips-tricks-and-troubleshooting/contact-customer-support.md).
