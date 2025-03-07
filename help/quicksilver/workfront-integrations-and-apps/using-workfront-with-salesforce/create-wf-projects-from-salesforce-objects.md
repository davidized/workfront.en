---
product-area: workfront-integrations;projects
navigation-topic: workfront-for-salesforce
title: Create Adobe Workfront projects from Salesforce objects
description: After installing Adobe Workfront for Salesforce, you can define triggers that create Workfront projects when certain criteria are met on Salesforce Opportunities and Accounts.
author: Becky
feature: Workfront Integrations and Apps
exl-id: b38c91ae-342b-4002-a947-7a0ab1aaca93
---
# Create Adobe Workfront projects from Salesforce objects

<span class="preview">The highlighted information on this page refers to functionality not yet generally available. It is available only in the Preview environment.</span> 

After installing Adobe Workfront for Salesforce, you can define triggers that create Workfront projects when certain criteria are met on Salesforce Opportunities and Accounts.

## Access requirements

You must have the following access to use the functionality described in this article:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront plan*</td> 
   <td> <p>Pro or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront license*</td> 
   <td> <p>Plan</p> </td> 
  </tr> 
 </tbody> 
</table>

&#42;To find out what plan, license type, or access you have, contact your Workfront administrator.

## Prerequisites

To submit a Workfront request from a Salesforce Opportunity or Account ensure that you have the following in your environment:

* Your Workfront administrator has installed Workfront for Salesforce.  
  For more information about installing Workfront for Salesforce, see [Install Adobe Workfront for Salesforce](../../workfront-integrations-and-apps/using-workfront-with-salesforce/install-workfront-for-salesforce.md)

* Your Workfront administrator has added the Workfront section to your Opportunity and Account page layouts.  
  For more information about adding the Workfront section to a page layout, see [Configure the Adobe Workfront section for Salesforce users](../../workfront-integrations-and-apps/using-workfront-with-salesforce/configure-wf-section-for-salesforce-users.md).

* You have a Workfront account and you can log in to it from the Workfront section inside your Opportunity or Account.

## Configuring the Creation of Workfront Projects from Salesforce

* [Understanding the Automatic Creation of Projects](#understanding-the-automatic-creation-of-projects) 
* [Configuring Triggers](#configuring-triggers) 
* [Understanding Project Names](#understanding-project-names)

### Understanding the Automatic Creation of Projects {#understanding-the-automatic-creation-of-projects}

As the Salesforce system administrator, you can define triggers that can automatically create projects in Workfront when the following things happen in Salesforce:

* The Stage of an Opportunity is updated.
* The Type of an Account is updated.&nbsp;&nbsp;

Triggers can be configured only after you have installed Workfront for Salesforce.&nbsp;&nbsp;  
For information about installing Workfront for Salesforce, see [Install Adobe Workfront for Salesforce](../../workfront-integrations-and-apps/using-workfront-with-salesforce/install-workfront-for-salesforce.md).

Consider the following when configuring triggers to automatically create Workfront projects when Salesforce items are created or updated:

* You must be a Salesforce and a Workfront system administrator to configure triggers.&nbsp;
* After you configure the triggers, anyone who updates the Stage of an Opportunity or the Type of an Account can trigger the creation of a Workfront project. This includes Salesforce users who do not have a Workfront account.&nbsp;
* There is no limit to how many triggers you can have.
* You cannot create multiple triggers based on the same conditions. Triggers are unique by default.
* Once the project is created it is automatically linked to the opportunity or the account where it was generated. Once established, this link cannot be broken.
* One opportunity or account can be linked to multiple projects in Workfront when a triggered condition has been met multiple times in the life of the opportunity or the account.

  For example, if you define more then one Stage for an Opportunity to trigger a Project, a project is created for every defined stage that the opportunity reaches, for the life of that opportunity. Also, if you update the Stage of an Opportunity from one defined stage to another, and then update it back to the defined stage, a second project is created for the second time you update the Stage field to the same defined stage.&nbsp;

* One project in Workfront can be linked only to one opportunity or one account in Salesforce at any given time, but not to both at the same time.&nbsp;

### Configuring Triggers {#configuring-triggers}

Once you configure the triggers, the process of creating Workfront projects is enabled for both Salesforce Classic or Lightning Experience frameworks.

To configure triggers in Salesforce:

1. Log in to Salesforce as the system administrator.&nbsp;
1. (Conditional) In Salesforce Classic, click **Setup**, and under the **Build** section, expand **Lightning Bolt**.

   Or

   In Salesforce Lightning Experience, click the **Setup icon**, then **Setup**, and under **PLATFORM TOOLS** expand **Apps**.

1. Click **Installed Packages**.

   Notice that the **Workfront** package has been installed.

1. Click **Configure** next to **Workfront**.

1. Log in to Workfront as a system administrator.

   The **Triggers** page displays.

   ![salesforce_triggers_page_empty.png](assets/salesforce-triggers-page-empty-350x134.png)

1. Click **New Trigger**.&nbsp;
1. From the **Salesforce Object** drop-down menu, select **Opportunity**.

   This is a required field.

1. (Conditional) Specify the following:

   1. From the **Stage** drop-down menu, select a&nbsp;**Stage**.  
      When an opportunity reaches the Stage specified here, a project is created in Workfront. This is a required field.
   
   1. In the **Portfolio or Program** field, start typing the name of a Portfolio or Program where you want the project to be placed in Workfront, then select it when it appears in the list.  
      If you do not specify a Portfolio or a Program, the new project is created and added to the Projects I Own list of the user logged in to Workfront when configuring the triggers. That user is also the Project Owner for the new project.
   
   1. Start typing the name of a Template that you want to associate with the new Workfront project, then select it when it appears in the list.  
      This is a required field.&nbsp;


      >[!NOTE]
      >
      >If you have specified a Template Owner on the template that you are planning to use for this integration, that becomes the Project Owner of the new project. The new projects appear under the Projects I Own list of the user who is the owner of the new project, according to the template.

   1. (Optional) Select the **Create a new project for each sold product type field**, if you want to create a new project for every type of product that is sold under any one opportunity.&nbsp;
   1. (Conditional) Select a **Product** in the **Product** drop-down menu.

      This is a required field.
   
   1. (Conditional)&nbsp;Start typing the name of a **Template** that you want to associate with the new Workfront project if the specified Product is on the Opportunity. Select it when it appears in the list.

      This is a required field.

      The project created when a new product is added to the Salesforce opportunity is placed in the same Portfolio or Program selected for the opportunity.

      >[!IMPORTANT]
      >
      >The project is created only when the Stage is updated on the Opportunity. A unique project is created for each product specified when the Stage field is updated, and not as the products are added to Opportunities.

1. (Optional) Click **New Trigger**.&nbsp;
1. (Optional)&nbsp;From the **Salesforce Object** drop-down menu, select **Account**. 

   This is a required field.&nbsp;
1. (Conditional) Specify the following:&nbsp;

   1. Select a **Type** from the **Type** drop-down menu.

      When any **Account** is designated as the **Type** specified here in Salesforce, a **Project** is created in Workfront.

      This is a required field.&nbsp;
   
   1. (Optional) Start typing the name of a **Portfolio** or **Program** where you want the project to be placed in Workfront in the **Portfolio or Program** field, then select it when it appears in the list.

      If you do not specify a Portfolio or a Program, the new project is created and added to the **Projects I Own** list of the user logged in to Workfront from Salesforce. The user is also the Project Owner for the new project.&nbsp;
   
   1. Start typing the name of a **Template** that you want to associate with the new Workfront project, then select it when it appears in the list.

      This is a required field.&nbsp;

      >[!NOTE]
      >
      >If you have specified a Template Owner on the template that you are planning to use for this integration, that becomes the Project Owner of the new project. The new projects appear under the **Projects I Own** list of the user who is the owner of the new project, according to the template.

   ![salesforce_triggers_page_with_cleaned_up_template_names.png](assets/salesforce-triggers-page-with-cleaned-up-template-names-350x157.png)

1. Click **Save**.  

   Workfront projects are now generated every time any of the triggers are met.

### Understanding Project Names {#understanding-project-names}

Depending on which trigger generated the projects, the names of the projects in Workfront could follow either one of these patterns:

* If the project is created based on an opportunity or account trigger, the name of the project is: *`<Salesforce object name>`: `<Project template name>` (via Salesforce)*.
* If the project is created based on an opportunity trigger that also includes the addition of a new Product, the name of the project is: *`<Salesforce object name>`: `<Salesforce product name>` (via Salesforce)*.

## View Workfront projects

If your Workfront administrator added the Workfront section to your Opportunity or Account page layout, you can see the projects automatically created in the Projects tab of this section.  
For more information about adding the Workfront section to the page layout of an Opportunity or Account, see [Configure the Adobe Workfront section for Salesforce users](../../workfront-integrations-and-apps/using-workfront-with-salesforce/configure-wf-section-for-salesforce-users.md).

You must have a Workfront account and be logged in to Workfront to view the Projects tab.

To view projects created from an Opportunity or Account:&nbsp;

1. Go to an Opportunity or Account.
1. Go to the **Workfront** section.

   >[!NOTE]
   >
   >Depending on how your Workfront administrator configured this section, it might have a different name.

1. Select the **Projects** tab.

   All projects created by defined triggers are listed in this tab. Any user in Salesforce who also has a Workfront account and who might have permissions to see these projects in Workfront can also see them in Salesforce for the Opportunity or the Account that generated them.

   ![salesforce_projects_tab_with_projects_listed.png](assets/salesforce-projects-tab-with-projects-listed-350x150.png)

   You can view the following information about the projects created by the integration:

   * Project Name&nbsp;
   * Reference Number
   * Entry Date
   * Name of the Owner
   * Status
   * Condition
   * Planned Completion Date
   * Percent Complete
   
      When this information is updated in Workfront, you can see the fields updated in this list.&nbsp;

1. (Optional) Click the name of a project to open it in Workfront.
1. (Optional) Click [!UICONTROL **Go to Salesforce**] in the [!UICONTROL Project Details] area <span class="preview">or the project header</span> to access the Opportunity or the Account where the project originated. <span class="preview">Your system or group administrator must add the Integrations field to your layout template to find it in the project header.</span>

   >[!NOTE]
   >
   >The Go to Salesforce link is visible to all Workfront users who can view the project. You must have a Salesforce account to be able to go to the Salesforce Opportunity or Account from where the project was generated.
