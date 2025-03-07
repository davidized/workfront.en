---
product-area: workfront-integrations
navigation-topic: workfront-for-outlook
title: Permissions levels for Workfront for Outlook
description: The Workfront for Outlook add-in requires Read/write mailbox access. The Workfront for Outlook integration requires the highest level permissions because it has the functionality to download email attachments from the Outlook exchange server and upload them to Workfront, when the user submits a Request from an email that has attachments.
author: Becky
feature: Workfront Integrations and Apps
exl-id: 704da044-21ed-4ca1-be6f-0e0aa832e069
---
# Permissions levels for Workfront for Outlook

Workfront for Outlook requires the highest of the four levels of permissions allowed in Outlook add-ins.

For details regarding permissions in Outlook add-ins, see [Privacy, permissions and security for Outlook add-ins](https://docs.microsoft.com/en-us/office/dev/add-ins/outlook/privacy-and-security) in the Microsoft documentation.

The Workfront for Outlook add-in requires Read/write mailbox access (`ReadWriteMailbox`), which is the highest permission scope.
The Workfront for Outlook integration requires the highest level permissions because it has the functionality to download email attachments from the Outlook exchange server and upload them to Workfront, when the user submits a Request from an email that has attachments. For this functionality to work, Workfront for Outlook uses the function `mailbox.getCallbackTokenAsync()` from Office Add-in JavaScript API to get the Token and use that to download email attachments from the exchange server. The only permission that allows use of that function is `ReadWriteMailbox`. For more information, see [Privacy, permissions and security for Outlook add-ins](https://docs.microsoft.com/en-us/office/dev/add-ins/outlook/privacy-and-security) in the Microsoft documentation.

The Workfront for Outlook add-in also requires `ReadWriteItem` permission (included in `ReadWriteMailbox`), which is used to read the email body and read/update email metadata:

* Read email body:

  Workfront for Outlook reads the email body when a user submits the request or sends the email body as an update to Adobe Workfront Object.
* Read/Update email metadata:
  
  Workfront for Outlook updates email headers when a user submits a request from an email. This is done to store information about the submitted Adobe Workfront object, so the next time the user opens the add-in for the same email the information about previous actions with that email are shown.

Workfront for Outlook accesses a user's Mailbox only when the user performs an action within the add-on. It does not have any background functionality. Workfront for Outlook accesses the user's mailbox in the following scenario only:

* The user attempts to submit a request, create a task, or send an email as an update from Workfront for Outlook (Opening the add-in and selecting an action)
  * Workfront for Outlook reads the email body to populate in the form inside the add-in.
  * Workfront for Outlook reads email metadata to display information on the add-in about the previous actions done in the add-in with the same email.
* When a user submits a request, creates a task, or sends an email as an update from Workfront for Outlook (clicking the submit button on the add-in):
  * Workfront for Outlook reads the email body to send it to Workfront as a request description or a comment.
  * Workfront for Outlook updates the email metadata to store information about the submitted requests or updated object.
  * Workfront for Outlook downloads email attachments from the exchange server to upload to submitted requests, created tasks, or updated objects.
