---
layout: default
title: Handling Add Document Errors
nav_order: 6
parent: Add Documents
grand_parent: Working with Documents
has_children: false
has_toc: false
---
# Handling Add Document Errors
---
Although errors when Adding a Document are extremely rare, it is possible to encounter one.  This page runs through the types of errors that can happen and how to handle them.

## Upload Documents Window
### Error Click Here to Retry
When the user is adding a document from the Upload Documents window and the document fails to upload, then the queue item turns red and displays an error message.
* Upload Documents Queue Item Error Message  
![](/assets/images/upload-documents-upload-error-DITCO.png)
* Click the Here link in the error message to prompt the system to retry uploading the document.    
* If this causes the error message to go away, then continue using the application normally.  
* Otherwise, the error message will either remain exactly the same, or change to the message in the following figure.
* Upload Documents Queue Item Retry Error Message  
![](/assets/images/upload-documents-upload-error-retry-error-DITCO.png)
* If the error message changed, click the Browse link to re-select the document to upload.     
* If this does not fix the error, or if the error message did not change, then contact an administrator to determine next steps.

### Failed to Save Document
* If a document uploads successfully but some other error prevents it from being added to the system, then an error message displays at the top of the Upload Documents window.
* Indexing Failure Error Message on Upload Document Window  
![](/assets/images/upload-documents-indexing-error-DITCO.png)
* Fix any incorrect index fields and click Add Document.  If this does not fix the error, contact an administrator to determine next steps.

## Folder or Document Search Screen
The Checklist View on the Document Search Screen works a little differently from a normal document search and has its own troubleshooting section below.

### Error, Click to Retry
The "Error, Click to Retry" message happens in two different situations:
* The document fails to upload, or
* The document uploads successfully but the system encounters an error when trying to index the document

#### Strategy: Retry
1. Click the Error, Click to Retry link.  
    * If the error is due to an upload failure, the Retry Upload dialog appears.  
    ![](/assets/images/retry-upload-dialog.png)  
    * If the error is due to an indexing error, the Retry Indexing dialog appears.  
    ![](/assets/images/retry-indexing-dialog.png)  
    * It is possible that nothing will happen when you click Error, Click to Retry. In that case, skip to the Delete and Re-Upload section below.
    
2. Click Retry.  
    * The Document Indexing window appears.

3. Change any incorrect index fields and click Save.  If this doesn't solve the error, try the Delete and Re-Upload steps below.
    

#### Strategy: Delete and Re-Upload
1. Click the x next to the error message. This will open the Confirm Delete dialog.
2. Click Delete.  The document disappears.  
3. Add the document again.  If this error persists, contact an administrator to determine next steps.

## Checklist View
### Indexing...
When the user is adding a document to a checklist and the document fails to upload, the Indexing... message will remain indefinitely rather than changing to an error message as it does on a normal document search.

Indexing... Message  
![](/assets/images/Indexing-message.png)  

1. If the Indexing... message remains for a significant amount of time, navigate to a different page and then return to the checklist.  
    * The checklist is refreshed, showing the option to add the document again.
2. Add the document again.  If it still does not upload successfully, contact an administrator to determine next steps.

### Failed to Save Document
* Sometimes when the user is adding a document to a checklist and an indexing failure occurs, the checklist item resets and an error message appears at the top of the screen.  
* If this happens, try again, double-checking that all the index fields are correct.  If the error happens again, contact an administrator to determine next steps.