---
layout: default
title: Modifying Document Indexes
nav_order: 8
parent: Document Actions
grand_parent: Working with Documents
has_children: false
has_toc: false
---
# Modifying Document Indexes
## Single Document
You must have permission to modify indexes on a given document.  Some documents you may be able to view, but not modify indexes on.

1. In the left navigation pane, click Documents, and perform a search to locate a document.
    
2. Click the Actions menu next to the document title.
    
3. Click Modify Index.  
    The Modify Document Indexes window appears.  
    ![Modify Document Indexes Window](https://qaprod.qflow.com/QAction_help//assets/images/images/QAction-modify-documents-indexes-window.png "Modify Document Indexes Window")
4. Update any fields and click Save.

## Multiple Documents
The system also has the ability to modify indexes on multiple documents at once.  This functionality should be used with caution as mistakes are not easily caught or reverted, but if you are confident that many documents need to be changed at once, this helps such a task go much more quickly.

* Modify Multiple Indexes in Actions Menu
* Modify Multiple Indexes Screen
* Editing a Field with Multiple Values
* Error After Submitting

1. Perform a search for documents you wish to update Since Modify Multiple Indexes can only be performed with documents within the same Classificaiton, consider filtering by Classification in your search.  Alternatively, open a folder containing documents you wish to update.
    
2. Select the documents you wish to update, and open the Actions menu at the top of the screen.  
    * If you selected all documents from the same Classification, the Modify Multiple Indexes option will be available.  
    ![](/assets/images/actions-menu.png)  
    
3. Click Modify Multiple Indexes to open the Modify Multiple Indexes screen.  
![](/assets/images/same-doc-type.png)  

{: .note}
If the selected documents are from different Document Types, then both Document Type and Classification will be uneditable.  To change several documents' Document Type or Classification at once, you must select all documents from the same Classification _and_ Document Type.
    
4. Index fields for which the selected documents all have the same value will be editable.  
    * Index fields for which the selected documents do NOT all have the same value (denoted by [Multiple Values]) will NOT be editable by default to prevent accidental overwrites.  
    * To edit fields with multiple values, you must first click on the Edit (![](/assets/images/edit-icon.png)) icon.  The newly displayed value will be the value that one of the selected documents has for the field in question.  
    ![](/assets/images/overwrite-multiple-values.png)  
    * If you wish to revert an index field to the original values each document had for it, simply click on the reset (![](/assets/images/reset-icon.png)) icon.  This will revert the field to uneditable.
    
5. Modify whichever fields you wish to modify, and then click Save.    
    * A pop-up will ask you to click Submit again to be sure that you want to modify all of the documents you have selected.  
    ![](/assets/images/failed-1.png)  
    * If you left any required fields blank, you will see messages in red for those fields on the screen.  
    * If any other errors occurred, such as if you selected a document that you don't have permission to modify indexes on, then the document will have a red icon (![](/assets/images/info-alert.png)) next to it on the left-hand side of the screen.  Hover over the red icon to view the error.  
    * The total number of Successful and Failed documents will display at the top of the left-hand side of the screen.