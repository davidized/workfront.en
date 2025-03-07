---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Data store modules
description: An Adobe Workfront Fusion data store, similar to a database or a simple table, can store data from scenarios, making it possible to transfer data between individual scenarios or scenario runs. You can use a data store to store new data from various systems during synchronization.
author: Becky
feature: Workfront Fusion
exl-id: 1dc9cb88-d1b9-4a67-91fb-be980cc1ccd1
---
# Data store modules

An Adobe Workfront Fusion data store, similar to a database or a simple table, can store data from scenarios, making it possible to transfer data between individual scenarios or scenario runs. You can use a data store to store new data from various systems during synchronization.

The data store modules enable you to add, replace, update, retrieve, delete, search, or count records in your Adobe Workfront Fusion data store.

For information on creating, editing, and troubleshooting data stores, see [Data Stores in Adobe Workfront Fusion](../../workfront-fusion/modules/data-stores.md)

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
   <td> <p>Workfront Fusion for Work Automation and Integration </p>  <p>Workfront Fusion for Work Automation</p></td> 
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

To use Data Store modules, you must first create a data store.

For information on creating data stores, see [Data Stores in Adobe Workfront Fusion](../../workfront-fusion/modules/data-stores.md)

## Data Store modules and their fields

When you configure Data Store modules, Workfront Fusion displays the fields listed below. Along with these, additional Data Store fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another in Adobe Workfront Fusion](../../workfront-fusion/mapping/map-information-between-modules.md).

![](assets/map-toggle-350x74.png)

All Data Store modules are Action type modules.

* [Add/Replace a Record](#add-replace-a-record) 
* [Update a Record](#update-a-record) 
* [Get a Record](#get-a-record) 
* [Check the Existence of a Record](#check-the-existence-of-a-record) 
* [Delete a Record](#delete-a-record) 
* [Delete All Records](#delete-all-records) 
* [Search Records](#search-records) 
* [Count Records](#count-records)

### Add/Replace a Record {#add-replace-a-record}

This action module adds or replaces a record.

You specify the data store and the record's key.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

>[!NOTE]
>
>The module throws an error when you try to add the record which is already in the data store under the same name and the Overwrite an existing record option is disabled.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Data store</td> 
   <td> <p> Select or add the data store where you want to create a record. </p> </td> 
  </tr> 
  <tr> 
   <td>Key </td> 
   <td> <p>Enter the unique key of the record you want the module to add or replace. The key can be used later to retrieve the record. If you leave this field blank, a key is generated automatically.</p> </td> 
  </tr> 
  <tr> 
   <td>Overwrite an existing record </td> 
   <td> <p>Enable this option to overwrite the record. The record you want to overwrite must be specified in the Key field above.</p> </td> 
  </tr> 
  <tr> 
   <td>Record </td> 
   <td> <p>Enter the desired values to the record's fields.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Update a Record {#update-a-record}

This action module updates a record.

You specify the data store and the record's key.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Data store</td> 
   <td> <p> Select or add the data store where you want to create a record. </p> </td> 
  </tr> 
  <tr> 
   <td>Key </td> 
   <td> <p>Enter the unique key of the record you want the module to update.</p> </td> 
  </tr> 
  <tr> 
   <td>Insert missing record </td> 
   <td> <p>Enable this option to create a new record if the record with the specified key doesn't already exist.</p> </td> 
  </tr> 
  <tr> 
   <td>Record</td> 
   <td> <p> Enter the desired values to the record's fields that you want to update.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Get a Record {#get-a-record}

This action module retrieves a record.

You specify the data store and the record's key.

The module returns the ID of the record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Data store</td> 
   <td> <p> Select the data store you want to retrieve a record from</p> </td> 
  </tr> 
  <tr> 
   <td>Key </td> 
   <td> <p>Enter the unique key of the record you want the module to retrieve.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Check the Existence of a Record {#check-the-existence-of-a-record}

This action module specifies whether a particular record exists.

You specify the data store and the record's key.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Data store </td> 
   <td> <p>Select the data store you want to check for the record existence.</p> </td> 
  </tr> 
  <tr> 
   <td>Key </td> 
   <td> <p>Enter the unique key of the record you want the module to check for existence.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Delete a Record {#delete-a-record}

This action module deletes a record.

You specify the data store and the record's key.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Data store </td> 
   <td> <p>Select the data store you want to check for the record existence.</p> </td> 
  </tr> 
  <tr> 
   <td>Key </td> 
   <td> <p>Enter the unique key of the record you want the module to delete.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Delete All Records {#delete-all-records}

This action module deletes all records from a particular data store.

You specify the data store.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Data store </td> 
   <td> <p>Select the data store you want to delete all records from.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Search Records {#search-records}

This search module looks for records in an object in Data Store that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Data store</td> 
   <td> <p> Select the data store you want to search.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Filter</p> </td> 
   <td> <p>Set the filter for the search.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Sort</p> </td> 
   <td> <p style="font-weight: normal;">For each field that you want to sort by, fill in the following fields:</p> <p style="font-weight: bold;">Key</p> <p>Select the column name you want to sort the results by.</p> <p style="font-weight: bold;">Order</p> <p>Select whether you want to sort results in the ascending or descending order.</p> </td> 
  </tr> 
  <tr> 
   <td>Limit</td> 
   <td> <p> Set the maximum number of search results Workfront Fusion returns during one execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>Continue the execution of the route even if the module returns no results</td> 
   <td> <p> If enabled, the route that this module is part of continues processing even if this module returns no results..</p> </td> 
  </tr> 
 </tbody> 
</table>

### Count Records {#count-records}

This action module numbers the records in a data store.

You specify the data store.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Data store </td> 
   <td> <p>Select the data store that contains the records you want to count.</p> </td> 
  </tr> 
 </tbody> 
</table>
