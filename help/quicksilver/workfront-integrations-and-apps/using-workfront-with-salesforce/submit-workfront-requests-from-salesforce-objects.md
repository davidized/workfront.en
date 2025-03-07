---
product-area: workfront-integrations
navigation-topic: workfront-for-salesforce
title: Submit Adobe Workfront requests from Salesforce objects
description: After installing Adobe Workfront for Salesforce, you can submit Workfront requests from Salesforce Opportunities and Accounts. This functionality exists in both the Classic and Lightning Experience frameworks.
author: Becky
feature: Workfront Integrations and Apps
exl-id: 84f8cb15-4840-4fe1-bf60-93bc4283b564
---
# Submit Adobe Workfront requests from Salesforce objects

<span class="preview">The highlighted information on this page refers to functionality not yet generally available. It is available only in the Preview environment.</span>

After installing Adobe Workfront for Salesforce, you can submit Workfront requests from Salesforce Opportunities and Accounts. This functionality exists in both the Classic and Lightning Experience frameworks.

## Access requirements

You must have the following access to use the functionality described in this article:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><p>Adobe Workfront plan*</p></td> 
   <td> <p>Pro or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Adobe Workfront license*</p></td> 
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
  Once you log in, you can see the New Requests tab where you can start entering requests.

## Submit Workfront requests from Salesforce

1. Go to an Opportunity or Account in Salesforce. 
1. Go to the Workfront section.
1. In the **New Requests** tab, select a request type in the **Select a Request Type** drop-down menu.

   You can see the same request queues that you have access to see in Workfront.&nbsp;

1. Start filling out the available fields for your request.

   Submitting a request from Salesforce is identical to submitting a request in the Workfront web application.

   >[!NOTE]
   >
   >Uploading a document using the Workfront plugin in Salesforce is temporarily unavailable.

   Continue to follow the steps described in [Create and submit Adobe Workfront requests](../../manage-work/requests/create-requests/create-submit-requests.md).

1. Click **Submit**.

## View Workfront requests

1. Go to an Opportunity or Account in Salesforce.
1. Go to the **Workfront** section.

   >[!NOTE]
   >
   >Depending on how your Workfront administrator configured this section, it might have a different name.

1. Select the **Submitted Requests** tab.

   You can view all the requests that you or others have submitted from this Opportunity or Account in this tab.Requests that are submitted to this request queue in the web application do not display in this list in Salesforce.

   >[!NOTE]
   >
   >Requests that are submitted to this request queue in the web application do not display in this list in Salesforce.

   ![salesforce_submitted_requests.png](assets/salesforce-submitted-requests-350x58.png)

   You can view the following information about the submitted requests:

   * Requests Name (in the Subject column)
   * Reference Number
   * Request Type
   * Status
   * Submitted on Date
   * Requested by Name
   * Assigned to Name  
     When this information is updated in Workfront, it is also updated in this list.

1. (Optional) Click the name of the request to open it in Workfront.

1. (Optional) Click **Go to Salesforce** to access the Opportunity or Account where the issue originated from the following areas of Workfront: 

   * In the Details section of the issue
   * In the Summary panel  when selecting the issue in a list, after clicking Open Summary ![](assets/summary-panel-icon.png) in the list's toolbar. 
   * <span class="preview">In the issue header, when the Integrations field is available. Your system or group administrator must add the [!UICONTROL Integrations] field to your Layout Template to view the Go to Salesforce link in the issue header. For more information, see [Customize object headers using a layout template](../../administration-and-setup/customize-workfront/use-layout-templates/customize-object-headers.md).</span>

   >[!NOTE]
   >
   >The Go to Salesforce link is visible to all Workfront users who can view the issue. You must have a Salesforce account to be able to go to the Salesforce Opportunity or Account where the issue was logged.
