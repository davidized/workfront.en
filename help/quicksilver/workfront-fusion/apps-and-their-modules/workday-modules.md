---
filename: workday-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: connector
navigation-topic: apps-and-their-modules
title: Workday modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Workday, as well as connect it to multiple third-party applications and services.
author: Becky
exl-id: 535573e0-b6ad-43a2-b7cb-ed32d1dc8d16
---
# Workday modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use Workday, as well as connect it to multiple third-party applications and services.

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

To use the Workday modules, you must:

*   Have a Workday account.
    
*   Create an OAuth application in Workday. For instructions, see the Workday documentation.

## Connect Workday to Workfront Fusion

1.  In any Workfront Fusion module, click Add next to the Connection field
    
2.  Fill in the following fields:
    
    <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">Connection name</p>
                </td>
                <td>Enter a name for the connection</td>
            </tr>
            <tr>
                <td  role="rowheader">Workday host</td>
                <td>Enter the address of your Workday host without <code>https://</code>. For example: <code>mycompany.workday.com</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">Services URL</td>
                <td>Enter the address of your Workday web services without <code>https://</code>. For example: <code>mycompany-services.workday.com</code>.</td>
            </tr>
            <tr>
                <td  role="rowheader">Tenant name</td>
                <td>Enter the tenant for this Workday account. Your tenant is your organization's identifier, and can be seen in the URL you use to log into Workday. Example: in the address <code>https://www.myworkday.com/mycompany</code>, the tenant is <code>mycompany</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">Client ID</td>
                <td>Enter the Client ID for the Workday application that this connection uses. You obtain this when you create the application in Workday.</td>
            </tr>
            <tr>
                <td  role="rowheader">Client Secret</td>
                <td>Enter the Client Secret for the Workday application that this connection uses. You obtain this when you create the application in Workday.</td>
            </tr>
            <tr>
                <td role="rowheader">Session timeout (min)</td>
                <td >Enter the number of minutes after which your authorization token expires.</td>
            </tr>
        </tbody>
    </table>

    
3.  Click Continue to save the connection and return to the module
    
## Workday modules and their fields

When you configure Workday modules, Workfront Fusion displays the fields listed below. Along with these, additional Workday fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another in Adobe Workfront Fusion](../../workfront-fusion/mapping/map-information-between-modules.md).

![](assets/map-toggle-350x74.png)

*   [Action](#Action)
    
*   [Search](#Search)
    

### Action

*   [Create a record](#Create)
    
*   [Delete a record](#Delete)
    
*   [Make a custom API call](#Make)
    
*   [Update a record](#Update)
    

#### Create a record

This action module updates a single record in Workday.

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">Connection</td>
            <td>For instructions about connecting your Workday account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >Connect Workday to Workfront Fusion</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">Record Type</td>
            <td>Select the type of record that you want to create.</td>
        </tr>
        <tr>
            <td role="rowheader">ID </td>
            <td>Enter or map the ID&#160;of the record you want to create.</td>
        </tr>
        <tr>
            <td role="rowheader">Subresource ID</td>
            <td >Enter or map the ID&#160;of the subresource you want to create.</td>
        </tr>
    </tbody>
</table>

#### Delete a record

This action module deletes a single record in Workday.

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">Connection</td>
            <td>For instructions about connecting your Workday account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >Connect Workday to Workfront Fusion</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">Record type</td>
            <td>Select the type of record that you want to delete.</td>
        </tr>
        <tr>
            <td role="rowheader">Specific record type</td>
            <td>Select the specific type of record that you want to delete. These are based on the record type that you chose.</td>
        </tr>
        <tr>
            <td  role="rowheader">Subresource ID</td>
            <td>Enter or map the ID&#160;of the subresource you want to delete.</td>
        </tr>
        <tr>
            <td role="rowheader">ID </td>
            <td >Enter or map the ID&#160;of the record you want to delete.</td>
        </tr>
    </tbody>
</table>


### Make a custom API call

This action module lets you make a custom authenticated call to the Workday API. This way, you can create a data flow automation that can't be accomplished by the other Workday modules.

When you are configuring this module, the following fields display.

The module returns the a status code, along with the headers and body of the API&nbsp;call.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Connection</p> </td> 
            <td>For instructions about connecting your Workday account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >Connect Workday to Workfront Fusion</a>.</td>
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Enter a path relative to <code style="color: #ff1493;">https://&#60;tenantHostname&#62;/api/&#60;serviceName&#62;/&#60;version&#62;/&#60;tenant&#62;</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Method</td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="../../workfront-fusion/modules/http-request-methods.md" class="MCXref xref">HTTP request methods in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Headers</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion adds the authorization headers for you.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Query String</td> 
   <td> <p>Add the query for the API call in the form of a standard JSON object.</p> <p>For example: <code>{“name”:“something-urgent”}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Body</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Update a record

This action module updates a single record in Workday.

  <table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">Connection</td>
            <td>For instructions about connecting your Workday account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >Connect Workday to Workfront Fusion</a></td>
        </tr>
        <tr>
            <td  role="rowheader">Record Type</td>
            <td>Select the type of record that you want to update.</td>
        </tr>
        <tr>
            <td role="rowheader">ID </td>
            <td>Enter or map the ID&#160;of the record you want to update.</td>
        </tr>
        <tr>
            <td role="rowheader">Subresource ID</td>
            <td >Enter or map the ID&#160;of the subresource you want to update.</td>
        </tr>
    </tbody>
</table>

### Search

*   [Read a record](#Read)
    
*   [List records](#Get)
    

#### Read a record

This action module reads a single record.

  <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">Connection</td>
            <td>For instructions about connecting your Workday account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >Connect Workday to Workfront Fusion</a></td>
        </tr>
        <tr>
            <td  role="rowheader">Record type</td>
            <td>Select the type of record that you want to delete.</td>
        </tr>
        <tr>
            <td role="rowheader">Specific record type</td>
            <td>Select the specific type of record that you want to read. These are based on the record type that you chose.</td>
        </tr>
        <tr>
            <td role="rowheader">ID </td>
            <td >Enter or map the ID&#160;of the record you want to delete.</td>
        </tr>
    </tbody>
</table>

#### List records

This search module retrieves a list of records of the specified type.

  <table style="table-layout:auto"> 
      <col/>
      <col/>
      <tbody>
          <tr>
              <td role="rowheader">Connection</td>
              <td>For instructions about connecting your Workday account to Workfront Fusion, see <a href="#Connect" class="MCXref xref" >Connect Workday to Workfront Fusion</a></td>
          </tr>
          <tr>
              <td  role="rowheader">Record Type</td>
              <td>Select the type of record that you want to retrieve.</td>
          </tr>
          <tr>
              <td role="rowheader">Limit</td>
              <td >
                  <p>Enter or map the maximum number of records you want the module to retrieve during each scenario execution cycle.</p>
              </td>
          </tr>
      </tbody>
  </table>
