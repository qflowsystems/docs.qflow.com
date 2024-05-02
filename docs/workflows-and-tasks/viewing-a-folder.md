---
layout: default
title: Viewing a Folder
nav_order: 5
parent: Workflows and Tasks
has_toc: false
---
# Viewing a Folder
{: .no_toc }

## Outline
{: .no_toc .text-delta }

1. TOC
{:toc}

# Overview

Results on the Inbox, Folders, and Workflows Tabs all open a Folder Window when clicked.  This topic will walk you through what you will find there.

![Task Folder Window](/assets/images/add-timesheet-task.PNG "Task Folder Window")

At the top of the window is the Folder Type, and then options to View Folder Security(![](/assets/images/folder-security.png)), Print the Folder(![](/assets/images/print-icon.png)), or, if applicable, to Edit the Folder's index fields.  

The next section contains system data about the Folder.  You can use the **Related Folders** field to associate other folders in the system with the folder you are viewing to conveniently tie workflows together.  You can also use this field to launch a new folder and automatically associate it to the folder you are viewing.

Beneath the horizonal divider are special folder fields related to the type of folder you are viewing.  These may be simple data fields such as a date, or other business objects in the system, such as the Employee pictured above.  You can click the pop-out icon (![](/assets/images/CustomObjectViewIcon.png)) to view a buniess object related to the folder.

Finally, there are Tabs you can navigate between:

- Active Task - The Task that is currently active on the Folder, and the available options to resolve the task.  Learn more about this Tab [here](https://docs.qflow.com/docs/workflows-and-tasks/viewing-a-folder#active-task-tab).
- Documents - Documents that have been added to the folder, and any [documents with associated index fields](/docs/workflows-and-tasks/viewing-a-folder#viewing-the-field-related-documents-in-your-folder).
- Notes - Any Notes that have been added to the Folder.
- Workflow - All of the Tasks that have been and will be worked for this Folder.
- Timeline - Historical record of actions that have been taken with the Folder.

# Active Task Tab
If a task is set up to be worked immediately, then the user sees the following options when a task is first opened:

- Complete Task - Move the task to the next step in the workflow.
- Put Task Back into Inbox - Remove your claim on the task and to put the task back into the group inbox to be worked later. Once selected, another user can claim the task to work or complete it.
- Return to Inbox - Keep your claim on the task to work it later, and for now return to your Inbox.
- Optional: Add Subflow - Create a sub-workflow task.
- Optional: Place Task On Hold - Place the task On Hold until a specific date or for a number of days.  The Task will appear in the On Hold Tab in your Inbox instead of the Active Tasks Tab, until the Hold you specify expires.
- Optional: Terminate Workflow - End a Workflow that should not continue any farther in processing.
- Optional: Cancel Workflow - End a Workflow that should not have been started in the first place.

If a task is set up to be viewed before it is worked, then the user sees the following options when a task is first opened:

- Claim Task and Return to Inbox - Claim the Task to work it later, and for now return to your Inbox.
- Start Working Task - Claim the Task and immediately begin working on it.  This will show you the options for completing the Task listed above.
- Return to Inbox - Return to your Inbox without claiming the Task.

If a task was customized by an administrator in a BPMN workflow, then there may be alternative options available.

{: .important}
Depending on how the administrator has configured the task, the order of the options may be different. Also, a default option may not be selected for every task.

Complete the work for this task, and then select the appropriate option.   To immediately work the next folder task once you complete the current one, select the Show Next Folder checkbox.   Click Done to complete this task.  
If the Show Next Folder checkbox was selected, then the next Folder appears.

# Viewing the Field-Related Documents in Your Folder
To configure folders to view the field-related documents, refer to the Configuring Folders to View Field-Related Documents topic.  
This task can be performed by end-users, as long as a process administrator has configured a folder to comply.

1. From the left navigation pane, click **Inbox > Active Tasks**.
2. Locate and select an active task Title.
3. Click the **Documents** tab.  
    The folder’s Documents tab includes documents added directly to the folder, as well as documents where the value in the field on the folder matches the value in the field on the document.
4. Click the **Actions** menu for a document.  
    If the document only appears because it is connected to the folder by a configured field, then a **Remove From Folder** option does not appear. Users can only select the **Remove From Folder** option (from the Actions menu) for documents added directly to a folder.
5. Click the **Actions** menu for a different document.  
    If the document only appears because it’s connected to the folder by the selected folder field, then a **Remove From Folder** option does not appear. You can only select the **Remove From Folder** option (from the Actions menu) for documents added directly to a folder.
6. To filter documents shown in this folder, click **Filter** on the toolbar.  
    Two options appear with selected checkboxes.  
    ![](/assets/images/folder-documents-filter.jpg)
7. Clear the **Documents added directly to this folder** checkbox.  
    Only documents connected by the configured field values appear.
8. Click Filter and select the **Documents added directly to this folder** checkbox again.  
    Both categories of documents appear again.
9. Click Filter and clear the **Documents connected by field values** checkbox.  
    Only documents added directly to this particular folder by a user appear.


# Printing a Folder
Q-Action allows users to print Folders using the Print Icon(![](https://qaprod.qflow.com/QAction_help//assets/images/images/Icons/print-icon.png)) at the top of the Folder screen, or by selecting the Print menu option in a Folder's Action menu on a Search Screen.  In either case, the Print Folder Window appears.

Print Folder Window  
![Print Folder Window](https://qaprod.qflow.com/QAction_help//assets/images/images/q-action-print-folder-window.png "Print Folder Window")

-   In the Print Folder window, select one of the following options:

- To print all the folder's information, but not the documents themselves, click Print All Folder Data Fields, Workflows, Notes, and a List of Documents, and then click Print.
    
- To print select details, click Print Selected Items, select the necessary checkboxes, and click Print.
    
{: .note}
If the Each Document in Folder checkbox is selected, choose to download the documents as separate PDF files within a zip folder or as one combined PDF. If the checkbox is not selected, then this option is not available.

Once you’ve selected your preferences, the print job is sent to the queue where you can check on its status.  Access the queue by clicking on your username in the top Right-hand corner of the application, and then in the drop-down menu that opens, select Exports.  Finally, click on the Folder Exports Tab to view any Folder print jobs.