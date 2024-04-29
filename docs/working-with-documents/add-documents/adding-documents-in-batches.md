---
layout: default
title: Adding Documents in Batches
nav_order: 7
parent: Add Documents
grand_parent: Working with Documents
has_children: false
has_toc: false
---
# Adding Documents in Batches
---
If you are adding or indexing a batch document (i.e., a document that contains several documents within one PDF), you can split the documents when adding them to the system.

{: .important}
If for any reason during batch assembly the web browser closes, crashes, or freezes, the system will save your current progress, and you can return to assembling the batch later.

Actions that prompt an auto-save on the Batch Assembly window include:
* Creating a document  
* Rearranging pages (moving up/down)   
* Deleting pages   
* Selecting Next Document
* Putting back a batch 
* Changing the Classification or Document Type fields on a document within the batch

Within the Batch Assembly window, try using the following keyboard navigation shortcuts:

|**Key Stroke Combination**|**Operation**|
|CTRL + J|Display Next Page|
|CTRL + Shift + J|Display Previous Page|
|CTRL + I|Display Next Document|
|CTRL + Shift + I|Display Previous Document|
|CTRL + Click|Select Multiple Pages|
|CTRL + D|Create Document|
|CTRL + Enter|Add Batch|
|Tab|Move to Next Field or Option|
|Shift + Tab|Move to Previous Field or Option|

Follow the steps below to explore the Batch Assembly screen.

1.  On the Upload Documents window, select a PDF and click Batch and Split Document.  
    * The Batch Assembly window appears.  
    * This window works very similarly to the Batch Assembly window users can open from the _Index Documents_ screen.  
    ![](/assets/images/batch-assembly-screen.PNG)
    
2.  Click Show Shortcuts at the top of the window to view available shortcuts.  
    ![](/assets/images/batch-assembly-tool-tips.PNG)
    
3.  Click **Hide Shortcuts** to close the shortcuts pane.
4.  Right-click on a page to see a menu of available options.  
    ![](/assets/images/batch-assembly-right-click-page.png)  

    * **Create Document** will split the batch into a second document with the selected page as the first page in the second document.  This option is not available on the first page in a document.  
    * **Move Up** and **Move Down** shift the selected page up or down in the page order. The first and last pages in a document will only have options to move the page in one direction.  Note that you can also drag and drop pages to change the order.  
    * **Duplicate** adds a copy of the selected page to the end of the page order in the current document.  
    * **Copy as Cover Sheet** adds a copy of the selected page to the top of the page order in the current document only.  
    * **Copy as Cover Sheet for all documents** adds a copy of the selected page to the top of the page order in every document in the batch.

5.  Right-click on a document to see a menu of available options.  
    ![](/assets/images/batch-assembly-right-click-document.png)  
    * **Merge with Previous** adds the pages in the selected document to the previous document, and removes the selected document.  
    * **Move Up** and **Move Down** shift the selected document up or down in the document order.  The first and last documents in the batch will only have options to move the document in one direction.
    {: .note}
    Note that you can also drag and drop documents to change the order.

    * **Delete Document** removes the selected document and any pages within the selected document from the batch.

6.  After entering the required fields for each document, click Next Document.  
    * The Next Document button is available when a document is selected that is not the last document in a batch.
7.  When finished indexing all documents in the batch, click Add Batch to add all documents in the batch to the system.

{: .important}
The Batch Assembly screen can be accessed either from the Upload Documents screen or the Index Documents screen.  In both cases the functionality is very similar, but there are some differences.   
For instance: from the Index Documents screen, users have additional options on the Batch Assembly screen to put back and re-route batches,  and from the Upload Documents screen, users have different notifications that will happen when batches are completed.  Learn more about each of these functions below.

## Re-Route & Download
Sometimes documents end up in the indexing queue for the wrong organization, for instance if a fax is sent to the wrong place.  To send the batch to the correct group, simply click on **Re-Route** under the **Additional Batch Options** at the bottom of the screen.

![](/assets/images/additional-batch-options-reroute.png)

{: .note}
The Re-Route and Download options are only available when opening the Batch Assembly window from the Index Documents screen.  When opening the Batch Assembly window from the Upload Documents screen, the Re-Route and Download options do not appear.

After clicking **Re-Route**, the _Assignee Selection_ window will open, where the user can select a different organization to route the batch to for indexing.

If the batch was sent to Q-Action altogether in error, the user can click **Download** to save the batch to their computer and send it to the proper contact.

## Notifications
If working from the Upload Documents screen, you will receive a notification once the Batch Assembly has succeeded or failed.  If it succeeded, clicking on the notification will take you to the Document Search screen with the documents from the batch showing in the results.

**Batch Assembly Success Notification**  
![](/assets/images/success-notification.png)

**Batch Assembly Failure Notification**  
![](/assets/images/failed-notification.png)

A failed batch will also appear on the Upload Documents screen with an error message.
**Failed Batch on Upload Documents Screen  **
![](/assets/images/failed-upload-doc-screen.png)