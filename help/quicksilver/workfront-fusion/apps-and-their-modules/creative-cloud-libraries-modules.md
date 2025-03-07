---
filename: creative-cloud-libraries-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe Creative Cloud Libraries modules
description: With the Adobe Workfront Fusion Adobe Creative Cloud Libraries modules, you can start a scenario when an element or library is created or updated. You can also upload, retrieve, archive, or list elements, or make a call to the Adobe Creative Cloud Libraries API.
author: Becky
exl-id: 8affa34b-803d-48a5-a986-9fbe0cb8c8f5
---
# Adobe Creative Cloud Libraries Modules

With the Adobe Workfront Fusion Adobe Creative Cloud Libraries modules, you can start a scenario when an element or library is created or updated. You can also upload, retrieve, archive, or list elements, or make a call to the Adobe Creative Cloud Libraries API.

If you need instructions on creating a scenario, see [Create a scenario](../../workfront-fusion/scenarios/create-a-scenario.md).

For information about modules, see [Modules in Adobe Workfront Fusion](../../workfront-fusion/modules/modules.md).

## Access requirements

You must have the following access to use the functionality in this article:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Adobe Workfront plan*</td>
      <td>
        <p>Pro or higher</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront license*</td>
      <td>
        <p>Plan, Work</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront Fusion license**</td>
      <td >
        <p>Workfront Fusion for Work Automation and Integration</p>
      </td>
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

To use Adobe Creative Cloud Libraries modules, you must have an Adobe Creative Cloud account.

## Adobe Creative Cloud Libraries modules and their fields

When you configure Adobe Creative Cloud Libraries modules, Workfront Fusion displays the fields listed below. Along with these, additional Adobe Creative Cloud Libraries fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another in Adobe Workfront Fusion](../../workfront-fusion/mapping/map-information-between-modules.md).

![](assets/map-toggle-350x74.png)


*   [Elements](#Elements)
    
*   [Libraries](#Librarie)
    
*   [Other](#Other)
    

### Elements

*   [Archive an Element](#Archive)
    
*   [Get an Element](#Get)
    
*   [List Elements](#List)
    
*   [Upload an Element](#Upload)
    
*   [Watch New Element in Library](#Watch)
    
*   [Watch Updated Elements](#Watch2)
    

#### Archive an Element

This action module archives an element from a library.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="../../workfront-fusion/connections/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</td>
    </tr>
    <tr>
      <td role="rowheader">Library ID</td>
      <td >Select the library that contains the element you want to archive.</td>
    </tr>
    <tr>
      <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">Element ID</td>
      <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">Select the element that you want to archive.</td>
    </tr>
  </tbody>
</table>

#### Get an Element

This action module returns a single element from a library.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="../../workfront-fusion/connections/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</td>
    </tr>
    <tr>
      <td role="rowheader">Library ID</td>
      <td >Select the library that contains the element you want to retrieve.</td>
    </tr>
    <tr>
      <td role="rowheader">Element ID</td>
      <td>Enter or map the ID of the element that you want to retrieve.</td>
    </tr>
    <tr>
      <td role="rowheader">Selector</td>
      <td>
        <p>Select the type of information that the module returns. </p>
        <ul>
          <li>
            <p><b>Default</b>
            </p>
            <p>Base data</p>
          </li>
          <li>
            <p><b>Details</b>
            </p>
            <p>All available data</p>
          </li>
          <li>
            <p><b>Representations</b>
            </p>
            <p>A flattened list of assets associated with the library element</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### List Elements

This action module retrieves a list of elements in a library.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="../../workfront-fusion/connections/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</td>
    </tr>
    <tr>
      <td role="rowheader">Library ID</td>
      <td >Select the library that you want to list elements from.</td>
    </tr>
    <tr>
      <td role="rowheader">Order by</td>
      <td>Select whether you want to order results by name or by the last date the element was modified.</td>
    </tr>
    <tr>
      <td role="rowheader">Type</td>
      <td >Enter a MIME type to limit results to elements identified with the specified MIME type. Example: <code>string</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">Selector</td>
      <td>
        <p>Select the type of information that the module returns. </p>
        <ul>
          <li>
            <p><b>Default</b>
            </p>
            <p>Base data</p>
          </li>
          <li>
            <p><b>Details</b>
            </p>
            <p>All available data</p>
          </li>
          <li>
            <p><b>Representations</b>
            </p>
            <p>A flattened list of assets associated with the library element</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Limit</td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>

#### Upload an Element

This action module uploads a small file asset to an existing library. Maximum file size is 5 MB.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="../../workfront-fusion/connections/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</td>
    </tr>
    <tr>
      <td role="rowheader">Library ID</td>
      <td >Select the library that you want to list elements from.</td>
    </tr>
    <tr>
      <td role="rowheader">Invocation Mode</td>
      <td>
        <p>Select the processing mode to invoke this request process with.</p>
        <ul>
          <li>
            <p><b>sync</b>
            </p>
            <p>The API call is processed synchronously. The response is delivered when processing is complete (unless the call times out.)</p>
          </li>
          <li>
            <p><b>async</b>
            </p>
            <p>The async monitor response is immediately returned, and request processing occurs asynchronously. The calling is responsible for polling the endpoint until completion.</p>
          </li>
          <li>
            <p><b>sync,async</b> (Default)</p>
            <p>Synchronous processing of the request is attempted. When the processing extends past 5000 ms, the async monitor response is returned. The monitor URL should be polled until the request is complete.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Type File</td>
      <td >Enter or map the MIME&#160;type of the uploaded file.</td>
    </tr>
    <tr>
      <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">Source File</td>
      <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">
        <p>Select a source file from a previous module, or map the source file's name and data.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Watch New Element in Library

This trigger module starts a scenario when an element is added to a library.


#### Watch Updated Elements

This trigger module starts a scenario when an element in a library is updated.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="../../workfront-fusion/connections/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</td>
    </tr>
    <tr>
      <td role="rowheader">Library ID</td>
      <td >Select the library that you want to watch for new elements.</td>
    </tr>
    <tr>
      <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">Limit</td>
      <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>

### Libraries

*   [Watch New Libraries](#Watch3)
    
*   [Watch Updated Libraries](#Watch4)
    

#### Watch New Libraries

This trigger module starts a scenario when a new library is created.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="../../workfront-fusion/connections/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</td>
    </tr>
    <tr>
      <td role="rowheader">Limit</td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>

#### Watch Updated Libraries

This trigger module starts a scenario when an existing library is updated.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="../../workfront-fusion/connections/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</td>
    </tr>
    <tr>
      <td role="rowheader">Limit</td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
  </tbody>
</table>

### Other

#### Make an API Call

This module makes a custom API call to the Adobe Creative Cloud Libraries API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td> <p>For instructions about connecting your Adobe Creative Cloud account to Workfront Fusion, see <a href="../../workfront-fusion/connections/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions.</a></p>
    </tr>
    <tr>
      <td role="rowheader">URL</td>
      <td>
        <p>Enter a path relative to <code>https://cc-libraries.adobe.io/api</code>.</p>
    <p>For example <code>/v1/libraries</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">API version</td>
      <td>
        <p>Select the version of the Adobe Analytics API that you want to connect to.</p>
      </td>
    </tr>    <tr>
      <td role="rowheader">Method</td>
      <td>
        <p>Select the HTTP request method you need to configure the API call. For more information, see HTTP request methods.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Headers</td>
      <td>
        <p>Add the headers of the request in the form of a standard JSON object.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion adds the authorization headers for you.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Query String</td>
      <td>
        <p>Add the query for the API call in the form of a standard JSON object.</p>
        <p>For example: <code>{“name”:“something-urgent”}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Body</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
       <tr>
      <td role="rowheader">Upload a transient document</td>
      <td>
      <p>If you want to upload a transient document, enter the source file for the document you want to upload.</p>
      <p>Select a source file from a previous module, or map the source file's name and data.</p>
    </td>
    </tr>

  </tbody>
</table>
