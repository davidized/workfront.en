---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: MIME modules
description: You can use MIME types in Adobe Workfront Fusion. Multipurpose Internet Mail Extension (MIME) types are labels that allow software to identify different types of data shared on the internet. Web servers and browsers use the MIME type to determine what should be done with a file. For example, a file with the MIME type text/html will be processed in a browser differently than a file with MIME type image/jpeg. MIME types function independent of operating system and hardware.
author: Becky
feature: Workfront Fusion
exl-id: ebbf6ad0-a1d0-47f8-849f-7bba1e0763d3
---
# MIME modules

You can use MIME types in Adobe Workfront Fusion. Multipurpose Internet Mail Extension (MIME) types are labels that allow software to identify different types of data shared on the internet. Web servers and browsers use the MIME&nbsp;type to determine what should be done with a file. For example, a file with the MIME type `text/html` will be processed in a browser differently than a file with MIME type `image/jpeg`. MIME types function independent of operating system and hardware.

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
   <td> <p>Workfront Fusion for Work Automation and Integration </p> <p>Workfront Fusion for Work Automation</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>Your organization must purchase Adobe Workfront Fusion as well as Adobe Workfront to use functionality described in this article.</td> 
  </tr> 
 </tbody> 
</table>

&#42;To find out what plan, license type, or access you have, contact your Workfront administrator.

&#42;&#42;For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md)

## MIME&nbsp;modules and their fields

### Get a MIME type

This transformer module return the MIME&nbsp;type associated with a given name, path, or extension.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">File</td> 
   <td> <p>Enter or map the file that you want to determine the MIME type for. </p> <p>You can enter the file using:</p> 
    <ul> 
     <li> <p><strong>File path</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Example: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>File name</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Example: </b></span></span>image.jpeg</p> </li> 
     <li><strong>File extension</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Example: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Get a file extension

This transformer module returns the original file extension for a given MIME type.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">MIME&nbsp;type</td> 
   <td> <p>Enter or map the MIME type that you want to determine the file extension for. </p> </td> 
  </tr> 
 </tbody> 
</table>
