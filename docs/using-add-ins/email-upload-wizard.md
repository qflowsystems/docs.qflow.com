---
layout: default
title: Email Upload Wizard
nav_order: 5
parent: Add-ins
has_children: false
has_toc: false
---
# Email Upload Wizard

Emails and attachments can be added to QAction from within Outlook using the [Office Add-In](/docs/using-add-ins/using-add-ins#using-the-office-and-acrobat-add-ins), or from within Gmail using the [Chrome Extension](/docs/using-add-ins/adding-email-chrome-ext).

Adding an Email to QAction from Within Outlook  
![](/assets/images/email-upload-wizard-outlook.png)

After clicking Add to QAction, a browser tab will open and opt the user to login.  Then, the Email Upload Wizard will display.

Email Upload Wizard Screen  
![](/assets/images/email-upload-wizard-single-example.png)  

This screen displays each email the user selected from the email program, represented by the subject line (in the example above, "Example Email").  Beneath each email, the screen displays a list of documents from that email that can be added to the system.   Every email will have the Email File document.  This document is a .msg or .eml file which contains the actual email message and any attachments that were in the email, all embedded within that one file.   Then, each attachment will also be listed as a standalone document which can be added to the system separately.   You can hover over the Information icon (![](/assets/images/info-icon.png)) next to an email subject to view more information about that email.  
 

Info Pop-Up  
![](/assets/images/email-upload-wizard-info.png)  

The Select All checkbox will select every single file displayed on the screen, while the Select Attachments Only checkbox will select all of the standalone attachment files, and not any of the Email File documents.

If you click Cancel, all of the documents will be discarded and you will be taken to the default screen in QAction.

Once you have selected which specific document(s) you want to add to QAction, click Upload Selected.  

Documents Selected  
![](/assets/images/email-upload-wizard-selected.png)  

This will discard any of the documents you did not select, and then move the selected documents into the queue on the [Upload Documents screen](/docs/working-with-documents/add-documents/upload-documents) to be indexed.

Upload Documents Screen  
![](/assets/images/email-upload-wizard-upload-documents.png)