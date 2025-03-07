---
title: Configure the SharePoint integration
user-type: administrator
product-area: system-administration;workfront-integrations;setup
navigation-topic: administrator-integrations
description: You can integrate Workfront with SharePoint Online, providing users with the ability to navigate to, link, and add SharePoint documents within Workfront. The functionality provided is similar to that of other Workfront integrations, such as Google Drive, Box, and Dropbox.
author: Becky, Caroline
feature: System Setup and Administration, Workfront Integrations and Apps, Digital Content and Documents
role: Admin
exl-id: fd45e1bc-9a35-4960-a73a-ff845216afe4
---
# Configure the Legacy SharePoint integration

<!--
<p data-mc-conditions="QuicksilverOrClassic.Draft mode">**DON'T DELETE, DRAFT OR HIDE THIS ARTICLE. IT IS LINKED TO THE PRODUCT, THROUGH THE CONTEXT SENSITIVE HELP LINKS. **</p>
-->

>[!IMPORTANT]
>
>The new SharePoint integration was released to production with the 22.3 release (July 2022.) Although your users can still access documents linked through the legacy SharePoint integration, you must use the new SharePoint integration to link documents from SharePoint.
>
>1.  Disable the legacy SharePoint integration so that your users do not use it to link to new documents.
>    
>     For instructions, see [Disable linking to the legacy SharePoint integration](#disable-linking) in this article.
>
>1. Configure your legacy SharePoint Client Secret so that your users will continue to have access to documents linked through the legacy SharePoint integration. 
>
>    For more information, see [Configure the Client Secret for continued access to the legacy SharePoint integration](#configure-client-secret-for-continued-access-to-the-legacy-sharepoint-integration) in this article.
>    
>1.  Link documents that are currently linked through the legacy SharePoint integration through the new integration.
>    
>     For instructions, see [Link documents from external applications](../../documents/adding-documents-to-workfront/link-documents-from-external-apps.md).
>    
>The procedure described in this document was deprecated with the 22.3 release, and is here for your information only.

You can integrate Workfront with SharePoint Online, providing users with the ability to navigate to, link, and add SharePoint documents within Workfront. The functionality provided is similar to that of other Workfront integrations, such as Google Drive, Box, and Dropbox.

This integration is compatible only with SharePoint Online. On-premise instances of SharePoint are not supported.

## Access requirements

You must have the following to perform the steps in this article:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront plan</td> 
   <td>Any</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td>Plan</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Access level configurations*</td> 
   <td> <p>You must be a Workfront administrator. For information on Workfront administrators, see <a href="../../administration-and-setup/add-users/configure-and-grant-access/grant-a-user-full-administrative-access.md" class="MCXref xref">Grant a user full administrative access</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

&#42;To find out what plan, license type, or access you have, contact your Workfront administrator.

## Prerequisites

You must have any necessary access or permissions in SharePoint to modify or configure your organization's SharePoint.

## Configure OAuth

Workfront connects to SharePoint Online using OAuth 2.0, a standard used by most web-based integrations for the authentication and authorization of users.

To configure OAuth, you need to create a Sharepoint site and a Site App within SharePoint. This process is described in the following sections.

For more information about OAuth, see [http://oauth.net](http://oauth.net/).

>[!TIP]
>
>To make it easy to copy and paste information between Workfront and SharePoint in these steps, we recommend keeping both applications open in separate tabs.

* [Create and configure a Sharepoint site](#create-and-configure-a-sharepoint-site) 
* [Grant write permissions to the site app](#grant-write-permissions-to-the-site-app) 
* [Create a Workfront SharePoint integration instance](#create-a-workfront-sharepoint-integration-instance) 
* [Complete your integration](#complete-your-integration) 
* [Add documents](#add-documents)

### Create and configure a Sharepoint site  {#create-and-configure-a-sharepoint-site}

In order for Workfront to authenticate with SharePoint, Workfront ca use a master site where users have the Full Control permission level or specific Manage permissions. This master site acts as an Authentication Entry Point for Workfront..

To create and configure a Sharepoint Site:

1. (Optional) If you do not want to use your organization's root site, you can create a master site in SharePoint.

   For instructions, visit [Create a site](https://docs.microsoft.com/en-us/sharepoint/create-site-collection) in the Microsoft Documentation.

   * Select the **Team Site** option when creating the site.

1. (Conditional) If you created a site in step 1, go to the site you just created.

   Or

   If you did not create a site in step 1, go to your organization's root site.

1. Add `/_layouts/15/appregnew.aspx` to the end of the URL in the search bar at the top of your browser window.
1. Configure the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Client ID</p> </td> 
      <td> <p>Click <strong>Generate</strong> to generate a Client ID. Copy this ID to a secure location. You will use it later when you set up the SharePoint integration in Workfront.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Client Secret</p> </td> 
      <td> <p>Click <strong>Generate</strong> to generate a Client Secret. Copy this Secret to a secure location. You will use it later when you set up the SharePoint integration in Workfront.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Title</p> </td> 
      <td> <p>Enter a title, such as Workfront Site App. Users see this title when adding documents..</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>App Domain</p> </td> 
      <td> <p><code>my.workfront.com</code> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Redirect URI</p> </td> 
      <td> <p><code>https://oauth.my.workfront.com/oauth2/redirect</code> </p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Create**
1. Continue to [Grant write permissions to the site app](#grant-write-permissions-to-the-site-app).

### Grant write permissions to the site app  {#grant-write-permissions-to-the-site-app}

At this point, you have successfully created a Site App and registered it within Workfront. This site app is also known as an app principal in SharePoint. It resides within your tenant. New site apps do not automatically have access to site collections within the tenant. Permissions must be granted explicitly, for each site collection. The steps below will show you how to grant Write permission to the new Site App a site collection. Repeat these steps for each of the site collections you added under Visible Site Collections in the steps above.

This site app must have Write permission to any site collections that users need to access through Workfront.

1. Add '/_layouts/15/appinv.aspx' to the URL in Sharepoint.

   **Example:**

   ```
   https://mycompany.sharepoint.com/sites/mysite/_layouts/15/appinv.aspx
   ```

1. Configure the following fields

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">App ID</td> 
      <td> <p>Add the Client ID that you created in <a href="#create-and-configure-a-sharepoint-site" class="MCXref xref">Create and configure a Sharepoint site </a>and click <strong>Lookup</strong>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Client / App Domain / Redirect URL</p> </td> 
      <td> <p>These automatically fill when you click Lookup.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Permission Request XML</td> 
      <td> <p>Copy the following XML to the Permission Request XML field. Make sure that it is added exactly as shown without additional spaces etc. in order to avoid errors.</p> 
      <div>Copy</a> 
      <div style="mc-code-lang: XML;" class="codeSnippetBody" data-mc-continue="False" data-mc-line-number-start="1" data-mc-use-line-numbers="False"> 
       <pre><code><span style="color: #63a35c; ">&lt;AppPermissionRequests&gt;</span><br><span style="color: #63a35c; ">&lt;AppPermissionRequest <span style="color: #795da3; ">Scope</span><span style="color: #df5000; ">="http://sharepoint/content/sitecollection/web"</span> <span style="color: #795da3; ">Right</span><span style="color: #df5000; ">="Write"</span>/&gt;</span><br><span style="color: #63a35c; ">&lt;/AppPermissionRequests&gt;</span></code></pre> 
      </div> 
      </div> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Create**. 
1. In the dialog that appears, click **Trust it**.
1. Verify that the site app has access to the site collection by clicking the **Site collection app permissions** link in Site Settings.
1. Repeat the steps above for the remaining site collections, then continue with [Create a Workfront SharePoint integration instance](#create-a-workfront-sharepoint-integration-instance).

### Create a Workfront SharePoint integration instance {#create-a-workfront-sharepoint-integration-instance}

When you have created a site app in SharePoint, you can now copy information from the site app into Workfront. The site app is an app principal and acts as the conduit through which OAuth requests are made to access documents within site collections.

1. Log into Workfront as an administrator.
1. Click the **Main Menu** icon ![](assets/main-menu-icon.png) in the upper-right corner of Adobe Workfront, then click **Setup** ![](assets/gear-icon-settings.png).

1. In the left panel, click **Documents** > **SharePoint Integration**.
1. Click **Add SharePoint**.
1. Configure the following fields:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Name</p> </td> 
      <td> <p>Enter a name for the SharePoint integration. Users see this name when they click Add &gt; From 'name of integration'. </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Sharepoint Host Instance</p> </td> 
      <td> <p><code>&lt;YourDomain&gt;.sharepoint.com</code> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Azure Access Domain</p> </td> 
      <td> <p><code>&lt;YourDomain&gt;.onmicrosoft.com</code> </p> <p>This refers to the Master Site that users will use to authenticate through. It is likely the same domain as the Sharepoint Host Instance.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Site Collections Authentication</p> </td> 
      <td> <b>Important</b> Site collections are used only in the Legacy Sharepoint Integration.
       <ul> 
        <li> <p><b>If you are using your organization's root site</b><b>:</b> </p> <p>Enter <code>/</code></p> </li> 
        <li> <p><b>If you are using a master site and subsites:</b> </p> <p><b>IMPORTANT</b>: Microsoft SharePoint no longer recommends the use of subsites.</p> <p>Enter the URL stem for the site collection that you created in the section above.</p> <p>This is the section of the URL after .com.</p> <p>Example: for the URL <code>https://mycompany.sharepoint.com/sites/mysite</code>, the stem would be <code>/sites/mysite</code>.</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">SharePoint Client ID</td> 
      <td>Enter the Client ID that you generated in <a href="#create-and-configure-a-sharepoint-site" class="MCXref xref">Create and configure a Sharepoint site </a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">SharePoint Client Secret</td> 
      <td>Enter the Client Secret that you generated in <a href="#create-and-configure-a-sharepoint-site" class="MCXref xref">Create and configure a Sharepoint site </a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Visible Site Collections</td> 
      <td> <b>Important</b> Site collections are used only in the Legacy Sharepoint integration.
       <ul> 
        <li> <p><b> If you are using your organization's root site</b><b>:</b> </p> <p>Enter <code>/</code></p> </li> 
        <li> <p><b>If you are using a master site and subsites:</b> </p> <p><b>IMPORTANT</b>: Microsoft SharePoint no longer recommends the use of subsites.</p> <p>For each subsite you want to add to your SharePoint integration, enter the stem of the subsite.</p> <p>Example: for the URL<code>https://mycompany.sharepoint.com/sites/mysite/mysubsite</code>, the stem would be <code>/sites/mysite/mysubsite</code>.</p> <p><b>NOTE</b>:   <p>If you want to test your configuration only (no subsites), enter the stem of the master site. </p> <p>Example: for the URL <code> https://mycompany.sharepoint.com/sites/mysite</code>, the stem would be <code>/sites/mysite</code>.</p> <p>When you have tested your configuration as described in <a href="#complete-your-integration" class="MCXref xref">Complete your integration</a>, you must remove the master site and enter the subsites.</p> 
          <ol> 
           <li value="1">Click the <strong>Main Menu</strong> icon <img src="assets/main-menu-icon.png"> in the upper-right corner of Adobe Workfront, then click <strong>Setup</strong> <img src="assets/gear-icon-settings.png">.<li><p>In the left panel, click <strong>Documents</strong> &gt; <strong>SharePoint Integration</strong>.</p></li><li><p>Click the SharePoint integration you are setting up, then click Edit.</p></li><li><p>Delete the stem for the master site from the Visible Site Collections field.</p></li><li><p>For each subsite you want to add to your SharePoint integration, enter the stem of the subsite.</p></li><p>Example: for the URL<code>https://mycompany.sharepoint.com/sites/mysite/mysubsite</code>, the stem would be <code>/sites/mysite/mysubsite</code>.</p></li> 
          </ol> </p> </li> 
       </ul> <p> </p> <p> </p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Save**
1. Continue to [Complete your integration](#complete-your-integration).

### Complete your integration {#complete-your-integration}

The basic configuration is almost complete.

1. In Workfront, Click the **Main Menu** icon ![](assets/main-menu-icon.png) in the upper-right corner of Adobe Workfront, then click **Documents** ![](assets/document-icon.png).
1. Click **Add new**.
1. Click **From `<title of your SharePoint site>`** in the dropdown.

   A dialog that invites you to Trust this site appears.

   >[!NOTE]
   >
   >If this dialog does not appear, your SharePoint integration is not configured correctly.

1. Click **Trust it**.

### Add documents {#add-documents}

You can now add documents from your SharePoint site.

For instructions, see [Link an external document to Workfront](../../documents/adding-documents-to-workfront/link-documents-from-external-apps.md#linking-existing-documents) in [Link documents from external applications](../../documents/adding-documents-to-workfront/link-documents-from-external-apps.md)

>[!IMPORTANT]
>
>If the user who linked a folder no longer has access to the external application, Workfront can no longer access the contents of the folder. This may happen, for example, if the user who originally linked the folder leaves the company. To ensure continued access, a user with access to the folder must re-link the folder.
> 


## Disable linking to the legacy SharePoint integration{#disable-linking}

To ensure that you can access documents linked through the legacy SharePoint integration, while ensuring that your users cannot link new documents through that integration, complete the following procedure.

>[!NOTE]
>
> * The legacy SharePoint integration is labeled "SharePoint."
> * The new SharePoint integration is labeled "SharePoint (Graph API)." 

1.   Click the Main Menu icon ![Main menu](assets/main-menu-icon.png) in the upper-right corner of Adobe Workfront, then click Setup ![Setup](../get-started-wf-administration/assets/gear-icon-settings.png).
1.   Select **Documents** in the left navigation, then select **Cloud Providers**.
1.   Make sure that the **SharePoint** option and **SharePoint (Graph API)** option are both enabled.
1.   Click **Save**.
1. Select **Documents** in the left navigation, then select **SharePoint Integration**.
1. Select the checkmark on the left of the list for all existing integrations, then select **Disable**.
    
## Configure the Client Secret for continued access to the legacy SharePoint integration

Your SharePoint Client Secret expires once a year. To ensure continued access to the documents in your legacy SharePoint integration, you must keep its SharePoint Client Secret up to date.

>[!IMPORTANT]
>
> Because SharePoint Client Secrets are handled by Microsoft, Client Secret features and procedures may change based on updates to SharePoint made by Microsoft. Always check the Microsoft documentation for the latest information about procedures and features in SharePoint.

<!--1. Go to the site that your SharePoint integration uses. This may be a site that you created when setting up the integrations, or it may be your organization's root site.

1. Add `/_layouts/15/appregnew.aspx` to the end of the URL in the search bar at the top of your browser window.-->

1. Generate a new client secret as described in [Replace an expiring client secret in a SharePoint Add-in](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/replace-an-expiring-client-secret-in-a-sharepoint-add-in#generate-a-new-secret)
1. Copy this Client Secret to a secure location. 
1. Log into Workfront as an administrator.
1. In Workfront, click the **Main Menu** icon ![](assets/main-menu-icon.png) in the upper-right corner of Adobe Workfront, then click **Setup** ![](assets/gear-icon-settings.png).
1. In the left panel, click **Documents** > **SharePoint Integration**.
1. Click on the SharePoint integration you want to update, then click **Edit**.
1. Enter the new Client Secret into the **Client Secret** field.
1. Click **Save**.


## Troubleshooting

* [Problem: Users experience authentication-based errors when using the SharePoint integration.](#problem-users-experience-authentication-based-errors-when-using-the-sharepoint-integration) 
* [Problem: As a Workfront user, I am unable to provision a new SharePoint instance. When I attempt to do I see an error.](#problem-as-a-workfront-user-i-am-unable-to-provision-a-new-sharepoint-instance-when-i-attempt-to-do-i-see-an-error) 
* [Problem: When attempting to browse SharePoint files in Workfront, I do not see any or all of my site collections.](#problem-when-attempting-to-browse-sharepoint-files-in-workfront-i-do-not-see-any-or-all-of-my-site-collections) 
* [Problem: I cannot access previously linked folders and documents in SharePoint.](#problem-i-cannot-access-previously-linked-folders-and-documents-in-sharepoint)

### Problem: Users experience authentication-based errors when using the SharePoint integration. {#problem-users-experience-authentication-based-errors-when-using-the-sharepoint-integration}

Solutions:

Users must be a member of a group that has appropriate permissions to the SharePoint site.

Users with Full Control access have all necessary permissions for your SharePoint integration. If you do not want to grant Full Control access to your users, you must grant the following permissions:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Design</p> </td> 
   <td> <p>Can view, add, update, delete, approve, and customize</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Edit</p> </td> 
   <td> <p>Can add, edit, and delete lists; can view, add, update, and delete list items and documents</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Contribute</p> </td> 
   <td> <p>Can view, add, update, and delete list items and documents</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>View only</p> </td> 
   <td> <p>Can view pages, list items, and documents (Document types with server-side file handlers can be viewed in the browser but not downloaded)</p> </td> 
  </tr> 
 </tbody> 
</table>

For instructions on creating and editing permissions levels, see [How to create and edit permission levels](https://docs.microsoft.com/en-us/sharepoint/how-to-create-and-edit-permission-levels) in the Microsoft documentation.

### Problem: As a Workfront user, I am unable to provision a new SharePoint instance. When I attempt to do I see an error. {#problem-as-a-workfront-user-i-am-unable-to-provision-a-new-sharepoint-instance-when-i-attempt-to-do-i-see-an-error}

Solutions:

This can be caused by a number of things, originating in either Workfront or SharePoint's configuration. Verify that:

* The Client ID, Client Secret, return URL and other configuration fields are correctly mapped between the Workfront SharePoint Integration instance and the SharePoint Site App.
* The user has Full Control permission to the Site Collection used for authentication.
* The Site App is listed under Site App Permissions for the Site Collection used for authentication.

### Problem: When attempting to browse SharePoint files in Workfront, I do not see any or all of my site collections. {#problem-when-attempting-to-browse-sharepoint-files-in-workfront-i-do-not-see-any-or-all-of-my-site-collections}

Solutions:

To see a site collection in Workfront, the following conditions must be met:

* The site collection must be registered in the Workfront SharePoint Integration instance.

  To verify this in Workfront:

   1. Go to Setup > Documents > SharePoint Integration.
   1. Edit the SharePoint Integration instance information.
   1. Verify that the site collection is listed under Visible Site Collections.

* The user must have view access to the site collection in SharePoint.
* To verify this in SharePoint, go to SharePoint, and open the site collection > Settings > Site permissions.
* The SharePoint Site App must have access to the site collection.

  To verify this in SharePoint:

   1. Go to the site collection > Settings > Site app permissions.
   1. Ensure that the Site App used by Workfront is listed here.
   1. (Conditional) If the Site App is not listed, add to the site collection using _layouts/15/appinv.aspx.

      For information about adding the site collection, see Granting Write Permissions To The Site App.

### Problem: I cannot access previously linked folders and documents in SharePoint. {#problem-i-cannot-access-previously-linked-folders-and-documents-in-sharepoint}

Solution:

If the user who linked a SharePoint folder can no longer authenticate, Workfront can no longer access the contents of the folder. This may happen, for example, if the user who originally linked the folder leaves the company.

To ensure continued access, a user with access to the folder must re-link the folder.

For information on linking folders from external providers, see [Link documents from external applications](../../documents/adding-documents-to-workfront/link-documents-from-external-apps.md).

### Problem: I see a "404 not found" error when attempting to add a document from Sharepoint

#### Solution:

This error might occur if one of the sites configured in the Visible Site Collections list has been deleted in Sharepoint. Check the Visible Site Collections list, and remove any sites that have been deleted in Sharepoint.
