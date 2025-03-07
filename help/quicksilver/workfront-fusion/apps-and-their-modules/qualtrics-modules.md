---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: connector
navigation-topic: apps-and-their-modules
title: Qualtrics modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Qualtrics, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 146802cd-b863-4c93-b767-50e05892c4de
---
# Qualtrics modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use Qualtrics, as well as connect it to multiple third-party applications and services.

If you need instructions on creating a scenario, see [Create a scenario in Adobe Workfront Fusion](../../workfront-fusion/scenarios/create-a-scenario.md).

For information about modules, see [Modules in Adobe Workfront Fusion](../../workfront-fusion/modules/modules.md).

## Access requirements

You must have the following access to use the functionality in this article:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront plan*</td> 
   <td> <p>Pro or higher</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license*</td> 
   <td> <p>Plan, Work</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td> <p>Workfront Fusion for Work Automation and Integration </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>Your organization must purchase Adobe Workfront Fusion as well as Adobe Workfront to use functionality described in this article.</td> 
  </tr> 
 </tbody> 
</table>

&#42;To find out what plan, license type, or access you have, contact your Workfront administrator.

&#42;&#42;For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md)

## Prerequisites

To use Qualtrics modules, you must have a Qualtrics account.

## Connecting Qualtrics to Workfront Fusion

You can create a connection to your Qualtrics account directly from inside a Qualtrics module.

1. In any Qualtrics module, click **Add** next to the Connection field.
1. Enter the following information:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Connection name</p> </td> 
      <td> <p>Enter a name for the new connection.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Data Center ID&nbsp;</td> 
      <td>Use the format <code>&lt;Data Center ID&gt;.qualtrics.com</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API Key</td> 
      <td>To locate your API key, see <a href="https://api.qualtrics.com/instructions/docs/Instructions/api-key-authentication.md">API Token Authentication</a> in the Qualtrics documentation.</td> 
     </tr> 
    </tbody> 
   </table>

1. Click **Continue** to create the connection and go back to the module.

## Qualtrics modules and their fields

The following modules are available for the Qualtrics connector:

* Watch New Survey Response
* Create a Directory Contact
* Delete a Directory Contact
* Get a Directory Contact
* Update a Directory Contact
* Create a New Survey Distribution via SMS
* Distribute a Survey via Email
* Make an API call
* List Directory Contacts
