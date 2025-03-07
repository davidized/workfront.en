---
title: Adobe PDF&nbsp;Services
description: Adobe PDF&nbsp;Services
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0a5736b-dbdb-43c6-83ff-e88a5625a5bf
---
# Adobe PDF&nbsp;Services

With the Adobe Workfront Fusion Adobe PDF Services, you can extract data from a PDF file, or generate a new PDF file from data you supply. In addition, you can convert a variety of file types to PDFs, or PDFs to other file types. PDF&nbsp;Services also allow you to combine, compress, or read metadata for a PDF&nbsp;file, as well as control password protection on the file.

If you need instructions on creating a scenario, see [Create a scenario in Adobe Workfront Fusion](../../workfront-fusion/scenarios/create-a-scenario.md).

For information about modules, see [Modules in Adobe Workfront Fusion](../../workfront-fusion/modules/modules.md).

For information on the API used for PDF Services, see [Adobe Document Generation API](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html).

## Considerations when using Adobe PDF Services

* [You do not need an Adobe account](#you-do-not-need-an-adobe-account) 
* [Workfront Fusion does not store your files](#workfront-fusion-does-not-store-your-files)

### You do not need an Adobe account {#you-do-not-need-an-adobe-account}

Because Workfront Fusion is part of the Adobe product suite, you don't need a separate Adobe account to use these tools. Each tool accesses Adobe PDF&nbsp;functionality without using a connection.

Although Workfront Fusion does not require an Adobe account to use the PDF Services, the modules do require a connection. There are no credentials involved in this connection, and you provide only a name for the connection itself.

### Workfront Fusion does not store your files {#workfront-fusion-does-not-store-your-files}

The Adobe PDF Services can read, convert, or modify your files, but neither Adobe nor Workfront Fusion store your files or data. This means that :

* You maintain control over your files, including their security
* You do not need to have an Adobe storage or cloud storage account to use the PDF&nbsp;Services.

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

## Adobe PDF Services modules and their fields

When you configure PDF&nbsp;Services, Workfront Fusion displays the fields listed below. Along with these, additional fields might display, depending on factors such as your access level in the app or service. A bold title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another in Adobe Workfront Fusion](../../workfront-fusion/mapping/map-information-between-modules.md).

![](assets/map-toggle-350x74.png)

* [Generate document](#generate-document) 
* [Extract Text / Table](#extract-text-table) 
* [Combine PDF files](#combine-pdf-files) 
* [Compress PDF files](#compress-pdf-files) 
* [Convert document to PDF file](#convert-document-to-pdf-file) 
* [Convert HTML to PDF file](#convert-html-to-pdf-file) 
* [Convert image to PDF file](#convert-image-to-pdf-file) 
* [Convert PDF to document](#convert-pdf-to-document) 
* [Convert PDF to image](#convert-pdf-to-image) 
* [Linearize a PDF file](#linearize-a-pdf-file) 
* [OCR for PDF file](#ocr-for-pdf-file) 
* [PDF page manipulation](#PDF%C2%A0page) 
* [PDF file properties](#PDF%C2%A0file) 
* [Protect PDF file](#protect-pdf-file) 
* [Remove protection of a PDF file](#remove-protection-of-a-pdf-file)

### Generate document {#generate-document}

The Generate document module is a powerful way to create a PDF that contains data you select. You can format it by using a Microsoft Word template, or by providing data in JSON format.

For more information on the Adobe PDF&nbsp;Services Generate document functionality, see the [Overview of Document Generation](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html) in the Adobe Document Services documentation.

* [Use the Generate document module with a Microsoft Word template](#use-the-generate-document-module-with-a-microsoft-word-template) 
* [Use the Generate document module with JSON](#use-the-generate-document-module-with-json)

#### Use the Generate document module with a Microsoft Word template {#use-the-generate-document-module-with-a-microsoft-word-template}

<!--
>[!NOTE]
>
>For a discussion of Microsoft Word templates, see [Microsoft Word Template modules](../../workfront-fusion/apps-and-their-modules/microsoft-word-templates-modules.md). 
>
>You do not need to use Microsoft Word template modules to use a Microsoft Word template with the PDF&nbsp;Services Generate document module.
-->

To use the Generate document module with a Microsoft Word template, you must first create the template. For instructions, search for "Create a template" in the Microsoft Office documentation.

Fill in the Generate document module fields as follows:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source File</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> <p>This source file is the Microsoft Word template that the module uses to generate the new PDF.</p> <p>We recommend creating a project in Workfront for the Microsoft Word templates that you use in Workfront Fusion. You can then use the Workfront &gt; Download document module to pull the appropriate template into your scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output Format</td> 
   <td> <p>Select the format for the generated document.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Data for merge</td> 
   <td> <p>For each value tag in your template that you want to replace with text, fill in the following:</p> 
    <ul> 
     <li> <p>Key</p> <p>Enter a key. In the template, the key is the text shown in the value tag. For example, if you want to place text in the value tag <code>&#123;&#123;name&#125;&#125;</code>, enter <code>name </code>in the key field.</p> </li> 
     <li> <p>Value Type</p> <p>Select whether the data in the value field is a value, an object, or an array of objects.</p> </li> 
     <li> <p>Value</p> <p>Enter or map the text that you want to appear in the generated document in place of the value tag.</p> </li> 
    </ul> <p> <img src="assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Use the Generate document module with JSON {#use-the-generate-document-module-with-json}

To use the Generate document module with JSON, fill in the fields as follows:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source File</td> 
   <td> <p>This source file is the Microsoft Word template that the module uses to generate the new PDF.</p> <p>We recommend creating a project in Workfront for the Microsoft Word templates that you use in Workfront Fusion. You can then use the Workfront &gt; Download document module to pull the appropriate template into your scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output Format</td> 
   <td> <p>Select the format for the generated document.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Data for merge</td> 
   <td> <p>To use JSON in this module, you must enable mapping on this field.</p> <p>Enter or map the JSON to generate the document from. </p> <p>You can type JSON&nbsp;directly into this field, or map JSON output from a JSON module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Extract Text / Table {#extract-text-table}

This action module allows you to extract data from a PDF file. The module outputs individual text elements, such as a paragraph or the text in a single cell of a table.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Elements that should be extracted as JSON</td> 
   <td> 
    <ul> 
     <li> <p>Text</p> </li> 
     <li> <p>Tables</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Extract Bounding boxes?</td> 
   <td>Enable this option to extract data about the bounding box of the text.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Include styling information for output?</td> 
   <td>Enable this option to add styling information to the output JSON.</td> 
  </tr> 
 </tbody> 
</table>

### Combine PDF&nbsp;files {#combine-pdf-files}

This action module takes multiple PDF&nbsp;files and combines them into a single PDF&nbsp;file. For example, this module could combine all of the documents in a Workfront project into a single PDF upon completion of the project.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Documents</td> 
   <td> <p>You can use an aggregator module to gather documents to combine into a PDF, or you can add the documents manually. </p> <p>We recommend using an Array Aggregator module to aggregate output from a previous module. By using an aggregator, you do not need to know the names, locations, or numbers of files to combine. Using an aggregator is therefore much more flexible and scalable than manually entering the documents to be combined.</p> <p>To use the Combine PDF files module with an aggregator, you must enable mapping on the Documents field. </p> <p>In this example, the Read Related Records module identifies documents associated with a project, and the Download Documents module downloads each one. All of the PDFs are aggregated into an array, which is passed into the Combine PDF files module.</p> <p> <img src="assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>You can also enter documents manually.</p> <p>For each document to include in the combined PDF:</p> 
    <ol> 
     <li value="1"> <p>Click Add a Document</p> </li> 
     <li value="2"> <p>In the Source file field, select the module that outputs the document you want to include, or map the source file's name and data. </p> </li> 
     <li value="3"> <p>(Optional) If you want to include only certain pages from the source file, for each page range that you want to add, click <strong>Add item</strong> in the Pages field, then enter the first and last pages of the page range to include, and click <strong>Add</strong>. You can include more than one page range from a single document.</p> </li> 
     <li value="4"> <p>Click <strong>Add</strong>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Compress PDF&nbsp;files {#compress-pdf-files}

This action module takes a PDF&nbsp;file and compresses it. This can be useful for conserving bandwidth or memory.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> <p>The source file must be in PDF&nbsp;format. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Compression level</td> 
   <td>Select the compression level that you want to use.</td> 
  </tr> 
 </tbody> 
</table>

### Convert document to PDF file {#convert-document-to-pdf-file}

This tool converts a document to a PDF file. The source file must be one of the following document formats:

* DOC
* XLS
* PPT
* TXT
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> <p>The source file must be in one of the following formats:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Language</td> 
   <td> <p>Select the default language for the source document. This allows the module to select an appropriate font, if not font is included in the source file.</p> <p>Select from the following languages:</p> 
    <ul> 
     <li> <p>en-US (Default): English (United States of America)</p> </li> 
     <li> <p>ca-ES: Catalan (Spain)</p> </li> 
     <li> <p>cs-CZ: Czech (Czech Republic)</p> </li> 
     <li> <p>da-DK: Danish (Denmark)</p> </li> 
     <li> <p>de-DE: German (Germany)</p> </li> 
     <li> <p>en-AE: English (United Arab Emirates)</p> </li> 
     <li> <p>en-GB: English (United Kingdom)</p> </li> 
     <li> <p>en-IL: English (Israel)</p> </li> 
     <li> <p>en-US: English (United States of America)</p> </li> 
     <li> <p>es-ES: Spanish (Spain)</p> </li> 
     <li> <p>es-MX: Spanish (Mexico)</p> </li> 
     <li> <p>eu-ES: Basque (Spain)</p> </li> 
     <li> <p>fi-FI: Finnish (Finland)</p> </li> 
     <li> <p>fr-CA: French (Canada)</p> </li> 
     <li> <p>fr-FR: French (France)</p> </li> 
     <li> <p>fr-MA: French (Morocco)</p> </li> 
     <li> <p>hr-HR: Croatian (Croatia)</p> </li> 
     <li> <p>hu-HU: Hungarian (Hungary)</p> </li> 
     <li> <p>it-IT: Italian (Italy)</p> </li> 
     <li> <p>ja-JP: Japanese (Japan)</p> </li> 
     <li> <p>kr-KR: Korean (South Korea)</p> </li> 
     <li> <p>nb-NO: Norwegian Bokmål (Norway)</p> </li> 
     <li> <p>nl-NL: Dutch (Netherlands)</p> </li> 
     <li> <p>pl-PL: Polish (Poland)</p> </li> 
     <li> <p>pt-BR: Portuguese (Brazil)</p> </li> 
     <li> <p>pt-PT: Portuguese (Portugal)</p> </li> 
     <li> <p>ro-RO: Romanian (Romania)</p> </li> 
     <li> <p>ru-RU: Russian (Russia)</p> </li> 
     <li> <p>sk-SK: Slovak (Slovakia)</p> </li> 
     <li> <p>sl-SI: Slovenian (Slovenia)</p> </li> 
     <li> <p>sv-SE: Swedish (Sweden)</p> </li> 
     <li> <p>tr-TR: Turkish (Turkey)</p> </li> 
     <li> <p>uk-UA: Ukrainian (Ukraine)</p> </li> 
     <li> <p>zh-CN: Chinese (Mainland China)</p> </li> 
     <li> <p>zh-TW: Chinese (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Convert HTML to PDF file {#convert-html-to-pdf-file}

This tool converts an HTML&nbsp;file to a PDF file. 

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> <p>Important: Source file must be in HTML or ZIP format. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">JSON</td> 
   <td> <p>If your HTML references JavaScript variables, you can include those variables here. </p> <p>For each variable, click <strong>Add item</strong> and include the variable's key and value.</p> <p>Note:   
     <ul> 
      <li> <p>When creating a PDF from a ZIP file, the source collateral must include a script element such as: &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt; </p> </li> 
      <li> <p>When creating a PDF from a URL, the content of this JSON object is injected into the browser VM before the page is rendered. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Include header and footer</td> 
   <td> <p>Enable this option to create headers and footers for the PDF&nbsp;document.</p> 
    <ul> 
     <li> <p>The header includes a date and the document title.</p> </li> 
     <li> <p>The footer includes the file name and a page number.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Page width</td> 
   <td>Enter the width of the paper, in inches. The module uses this information to format the pages in the created PDF&nbsp;file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Page height</td> 
   <td>Enter the height of the paper, in inches. The module uses this information to format the pages in the created PDF&nbsp;file.</td> 
  </tr> 
 </tbody> 
</table>

### Convert image to PDF file {#convert-image-to-pdf-file}

This tool converts an image to a PDF file. 

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and image file.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Convert PDF to document {#convert-pdf-to-document}

This tool converts a PDF file to a document. You can select one of the following formats for the output file.

* DOC
* DOCX
* PPTX
* XLSX
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> <p>The source file must be in PDF&nbsp;format. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output Files Format</td> 
   <td> <p>Select the format that you want the files to be output as:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Convert PDF to image {#convert-pdf-to-image}

This tool converts a PDF to an image in PNG or JPEG format., which is then output as a ZIP. The PDF&nbsp;is converted into one image per page, and each image ends with the page number. The image files are then combined into a ZIP file.

For example, a file called "TestFile" with 8 pages would produce 8 images, named "TestFile_1" through "TestFile_8." The module's output is a ZIP file containing the 8 images.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> <p>The source file must be in PDF&nbsp;format. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Output Files Format</td> 
   <td> <p>Select the format that you want the files to be output as:</p> 
    <ul> 
     <li>PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Linearize a PDF&nbsp;file {#linearize-a-pdf-file}

This tool linearizes a PDF document to create a web-optimized PDF document. A linearized PDF document can be viewed page-by-page without needing to download the entire document.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

### OCR for PDF file {#ocr-for-pdf-file}

This tool performs Optical Character Recognition (OCR) on a file and produces a PDF. 

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">OCR type</td> 
   <td> 
    <ul> 
     <li> <p>Modified original image type ensures that text is searchable and selectable, but modifies the original image during the cleanup process (for example, deskews it) before placing an invisible text layer over it. This type removes unwanted artifacts and may result in a more readable document in some scenarios. </p> </li> 
     <li> <p>Unchanged original image type also overlays a searchable text layer over the original image, but in this case, the original image is unchanged. This type produces maximum fidelity to the original image.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Language</td> 
   <td>Select the language of this document.</td> 
  </tr> 
 </tbody> 
</table>

### PDF&nbsp;page manipulation

This module allows you to selectively rotate or delete pages in a PDF document. For example, you can change portrait view to landscape view or remove certain pages from the PDF document.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Action</td> 
   <td> <p>Select the action you want to perform on the file.</p> 
    <ul> 
     <li> <p><b>Delete</b> </p> <p>Select this option to delete pages from the document.</p> </li> 
     <li> <p><b>Rotate</b> </p> <p>Select this option to rotate pages, then enter the angle, in degrees clockwise, that you want to rotate the document pages relative to their starting orientation.</p> <p>To rotate from portrait to landscape or vice versa, rotate the page 90 or 270 degrees.</p> <p>If a page is upside down, rotate it 180 degrees.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pages</td> 
   <td> <p>For each page range you want to delete, click <strong>Add</strong> and then enter the page range's first and last page. </p> <p>Note:   
     <ul> 
      <li> <p>You can use negative numbers to count back from the end of the document. The last page of a document is -1, the second to the last page is -2, and so on.</p> </li> 
      <li> <p>To delete a single page, set the same page number as both the start and end of the range.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limit</td> 
   <td> <p>Enter or map the maximum number of records you want the module to work with during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### PDF&nbsp;file properties

This tool extracts basic information about the document, such as:

* Page count
* PDF version
* Whether the file is encrypted
* Whether the file is linerarized
* Whether the file contains embedded files

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Protect PDF file {#protect-pdf-file}

This tool secures a PDF document with a user or owner password. It also sets restrictions on certain features like printing, editing, and copying in the PDF document. You select the type of content to be encrypted and the encryption algorithm.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Connection</td> 
   <td> <p>For information on creating a PDF&nbsp;Services connection, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> <p>The source file must be in PDF&nbsp;format. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Password Protection Type</td> 
   <td> <p>Enable this option to use passwords to encrypt the input PDF document. If you enable this option, you must specify and enter a value for one or both of the following: </p> 
    <ul> 
     <li> <p>userPassword</p> </li> 
     <li> <p>ownerPassword </p> </li> 
    </ul> <p>Each password can be up to 128 characters in length.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Encryption Algorithm</td> 
   <td> <p>Select the encryption algorithm. </p> 
    <ul> 
     <li> <p>AES-128 encryption</p> <p>The password supports LATIN-I characters only. </p> </li> 
     <li> <p>AES-256 encryption</p> <p>The password supports Unicode character set</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content to Encrypt</td> 
   <td> <p>Select the type of content to be encrypted.</p> 
    <ul> 
     <li> <p>All content</p> </li> 
     <li> <p>All content except metadata</p> </li> 
     <li> <p>Only embedded data </p> </li> 
    </ul> <p>Selecting "Only embedded data" renders any provided access permissions as ineffective.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Permissions</td> 
   <td> <p>Select any permissions you want to include to allow printing, editing, or content copying.</p> <p>Permissions settings are only used if the ownerPassword is set in the Password Protection Type field.</p> </td> 
  </tr> 
 </tbody> 
</table>

This tool returns basic information (metadata) about the page.

### Remove protection of a PDF file {#remove-protection-of-a-pdf-file}

This tool removes security (password protection) from a PDF document.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Connection</td> 
   <td> <p>Select the connection to use for this module.</p> <p>You do not need an Adobe account to create a PDF&nbsp;Services connection. For more information, see <a href="#you-do-not-need-an-adobe-account" class="MCXref xref">You do not need an Adobe account</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source file</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> <p>The source file must be in PDF format.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Passwprd</td> 
   <td>Enter the password that currently protects the file.</td> 
  </tr> 
 </tbody> 
</table>
