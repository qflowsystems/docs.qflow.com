---
layout: default
title: Process Administrators
nav_order: 3
parent: Administrator Roles
has_toc: false
---
# Process Administrators
{: .no_toc }
The following sections describe the various activities that a process administrator role can perform.

## Outline
{: .no_toc .text-delta }
1. TOC
{:toc}

## Creating Folder Definitions

Folder Definitions link to a workflow and define the index fields that appear for the workflow.

1. Click Administration > Workflow Folder Definitions.  
    The Workflow Folder Definitions screen appears with several search results.   
    ![Search Folder Definition Screen](/assets/images/SearchFolderDefintion-screen.PNG "Search Folder Definition Screen")
2. Click Add New Workflow Folder Definitions.  
    The Create Folder Definition window appears.  
    ![Create Folder Definition Window](/assets/images/folder-definition-blank.png "Create Folder Definition Window")  
    Note that the options on the left of the screen may vary slightly based on your organization's Q-Action setup.  In particular, if your organization has [Records Management](/docs/records-management), then you will see a **Retention** tab in addition to the tabs pictured above.
    
3. Enter a Folder Name and Description. You will want to leave the Status field as Active.
    
4. In the Owner field, select the organization that handles this process.
    
5. Keep the default settings for the Application Administrator and Process Administrator.
    
6. Click Save.
    
You have now created a very basic folder definition in the system.  However the folder is not going to be very useful without further configuration.  The next important step is [Configuring Folder Fields](/docs/administrator-roles/process-admin#configuring-folder-fields), and you may also want to [configure a workflow](/docs/administrator-roles/process-admin#configuring-a-workflow-for-a-folder) as well in order to include tasks for users to work within the folder. Improve how the folder and workflow search screens function when the folder type is selected by configuring [Priority Search Fields](/docs/administrator-roles/priority-search-fields) for the folder definition.

## Configuring Folder Fields
On the [Create/Modify Folder Definition screen](/docs/administrator-roles/process-admin#creating-folder-definitions), click the Folder Fields tab on the left.  
![](/assets/images/folder-definition-folder-fields-QAction.png)

### Folder Label
The Folder Label field at the top lets you customize how the system displays the name of the folder that users will click on in search results to open it.  The example above shows fields from the folder itself in brackets{}, so the label for each individual folder will vary depending on the values of those fields.  Below shows how a folder with this configuration might appear in a search result - the blue text is determined by the **Folder Label** field.  
![](/assets/images/folder-definition-label-example.png)  
  
To select folder fields to include in the label, click **Add Field** to the right of the **Folder Label** field. This opens a window where you can look for the fields you want in a drop-down menu.  
![](/assets/images/add-field-to-label.PNG)

### Tabs
Tabs can be used to organize different folder fields into different sections. All folders have a **Default Tab**. Additional tabs can be added using the **Add Tab** link.  The names of different tabs can be edited using the edit icon (![](/assets/images/pencil-icon.PNG)) for the tab.  Tabs can be deleted using the remove icon (![](/assets/images/Icons/remove-icon.png)).

Click on different tabs to configure the folder fields that display in each one.

### Folder Fields
Folder fields give users information and enable users to search for folders by specific data. 

When adding or modifying an index field on the folder, you will have the following options:
- **Display Name** customizes the label of the field that will appear on the folder
- **Span Columns** makes the field the entire width of the folder instead of sticking to one column.
- **Required** indicates whether the user must input a value for the field when saving the folder.
- **View Mode Mask** modifies how the value of the field appears on the folder.
- **Validation** allows you to input a **pattern** that the value for the field must match when saving the folder, and a **Failure Message** to display to the user if the value doesn't match the pattern.

Custom object fields have a blue Plus (+) button to add related subfields. When adding or editing a subfield, you can choose whether or not to make it editable on the folder.

Drag any of the fields between Column 1 and Column 2 to alter how the fields are organized when a user is viewing the folder. 

### Additional Options
- Show Folder Due Date checkbox - Selecting a field for the Base Due Date on field, and enter a number of days in the Days allowed field (select either business days or calendar days).
- Select Field 1, Field 2, Field 3 section - Select the three most important fields, and those appear first in a search. 
- Include Documents in Folder by Field Values checkbox -  Add fields and then those selected fields connect future documents via matching values to this folder. End-users can then open a folder, click the Documents tab, and view documents that were added directly to that individual folder, as well as documents related to that folder according to the fields configured here by the administrator. For more information, refer to [Configuring Folders to View Field-Related Documents](https://docs.qflow.com/docs/workflows-and-tasks/viewing-a-folder#viewing-the-field-related-documents-in-your-folder).
- Provide a List of Similar Folders by Field Values checkbox - Add fields so that users can easily find related folders based on sharing the same values for those fields.  Select this checkbox and when the folder is opened by an end-user, a View Similar Folders (![](/assets/images/view-similar-folders-button.JPG)) button appears which the user can click to view a list of related folders.

## Configuring Folders to View Field-Related Documents

This task must be performed by a process administrator.

Administrators can configure a Folder Definition to automatically pull in documents to a folder based on certain Field Values and Classification/Document Type(s).  To view the field-related documents in your folders, refer to the [Viewing the Field-Related Documents in Your Folders](/docs/workflows-and-tasks/viewing-a-folder#viewing-the-field-related-documents-in-your-folder) topic under Workflow Functionality.

1. Click Administration > Folder Configuration.  
    The Search Folder Definition screen appears with several search results.
2. Locate the folder definition and click the title.  
    The folder definition window for the selected folder definition appears.  
    ![](/assets/images/folder-definition-QAction.PNG)
3. Click the Folder Fields tab.  
    ![](/assets/images/folder-definition-folder-fields-QAction.png)
4. In this window, select the Include Documents in Folder by Field Values checkbox in the bottom-right.  
    By default this option is not selected. Selecting the checkbox connects documents to the folder by configured field values.
5. Click Add Field beneath the **Include Documents in Folder by Field Values** checkbox.  
    ![](/assets/images/folder-definition-folder-fields-add-field-QAction.png)
6. From the left drop-down list, select a Folder Field.  
    A folder field must be selected from the left drop-down before the right drop-down is available. Once a folder field is selected, the right drop-down is available to select document fields that match the data type of the folder field selected. For example, if a date field is selected from the (left) folder field drop-down, only date fields appear in the (right) document field drop-down.
7. From the second drop-down list, select a Document Field.
8. Click OK.  
    The fields appear under the checkbox.  
    ![](/assets/images/folder-definition-folder-fields-include-documents-field-added-QAction.png)
9. Click Add Document Filter.  
    ![](/assets/images/folder-definition-filter-documents.png)
10. Select a Classification and optionally one or more Document Types, then click Save.  
    The selected Classification/Document Type(s) will appear beneath the selected Field Values.
11. Click Save.  
    Any folders with the definition you just edited will include documents added directly to the folder on the _Documents_ tab like normal, as well as now including documents of the selected Classification/Document Type(s) where the field on the document matches the field on the folder.
12. Close the folder definition window.

## Configuring a Workflow for a Folder
When [creating a folder definition](/docs/administrator-roles/process-admin#creating-folder-definitions), there are two ways to configure a workflow for the folder:  
- Specific documents can be configured to automatically kick off a workflow when they are added to the system.  These can be set up on the **Initiating Docs** tab of the folder definition screen.
- You can allow users to manually kick off a workflow using the **Create On Demand** tab of the folder screen.

Review how to configure these options in the sections below.

### Initiating Documents
1. Click the Initiating Docs tab, and click Add Initiating Document Settings.  
    The Initiating Documents Setting window appears.  
    ![Create Folder Definition Window - Initiating Docs Tab](/assets/images/initiating-doc-settings.jpeg "Create Folder Definition Window - Initiating Docs Tab")
2. In this window, review the options:
    1. Classification field - Select or enter a classification. This field and the Document Types field are connected.
    2. Document Types field - Either select specific document types in the field to limit the options, or click the All Document Types not Configured as Initiating Documents option so that when a document is added under this classification, all of the document types are available. If a document is added to the system with the selected Document Type and Classification, it starts the workflow connected to this folder.
    3. Allow the following routing options for new documents section - Select one or more of the checkboxes. When a document is added to the system with the same classification and document type configured above, a routing process begins. If two or more of the checkboxes are selected, then the Route window appears immediately after the document is added.
        - Create New Folder checkbox - When selected, you must select a workflow template to use (recommended) or manually set up a folder workflow. When a document is routed, it will follow the workflow defined here. If this checkbox is the only one selected, then the document added under this classification launches a task that is automatically routed and appears in your Active Tasks tab in your Inbox (no Route window appears after the document is added).
            - Choose Field Values to Copy From Documents to Folder link - Select fields to pull those field values from the document and to automatically add those fields to this folder when a new folder workflow begins (i.e., copy the field values from the document to the folder).
        - Add to an Existing Folder checkbox - When selected, click Choose Folder Lookup Fields to choose fields. Select a Document Field and/or Folder Field and click Add Selected > OK. Then when the end-user adds a document to this folder later, the Route window automatically appears. The end-user must choose an existing folder that has field values matching the selected Document Field and/or Folder Field in order to route the document.
            - Choose Folder Lookup Fields link - Select fields so that later the user can filter the folders by these fields when prompted on the Route window to choose a folder. The user can view all of the folders with the same field values.
            - **Auto Route On Folder Found** checkbox - If exactly one folder is found with matching folder fields to the document, the system will automatically add the document to that one existing folder.  If multiple folders are found, then the user will receive a Route Document task as normal. If no folders are found at all and the Create New Folder option is checked, then the system will automatically create a new folder.
        - Add to Repository Only checkbox - When selected, the document is added to the system without launching a workflow. If this checkbox is the only one selected, then the document added under this classification is automatically added to the system (no Route window appears after the document is added).
    4. When more then one option is available to route an incoming document, who determines the appropriate route? section - In the first field, select an organization, position, or user. This selection is assigned the Route Document task if the document must be routed. Alternately, you can leave it blank with the The person filing the document (Indexing, Add Electronic Document, Create Bar Code) option selected, so that the person adding the document automatically decides how it is routed.
    5. Allow Backfiling of Documents without Initiating Workflow checkbox - When selected and an end user adds a document, the Back File checkbox appears on the Add Document window. Then the end user can skip the Route window, and the document is automatically added to the repository only, regardless of what is selected in the Routing Options above.
3. Select values for the fields, and click Save.  
    The Initiating Documents Settings window closes. The document settings are added to the Initiating Documents tab.

### Create on Demand
1. Click the Create On Demand tab.  
    If users, roles, or organizations are given Create Folder privileges on the Security tab, then on the Create On Demand tab, you must define what workflow is initiated when those users create an on-demand folder.  
    ![Create On Demand Tab](/assets/images/create-on-demand.jpeg "Create On Demand Tab")
2. For the Workflow Options, select a workflow template to use (recommended) or manually set up a folder workflow.
3. Click Save.  
    The window closes and the folder is created.

## Configuring Folder Security
1. Click the Security tab.  
    ![Security Tab](/assets/images/security-tab-check-processing.jpeg "Security Tab")
2. Review the existing user roles listed and their privileges.
3. Click Add New ACL Entry to add a new user, role, or organization to specify unique privileges.
4. Review the privileges for each of the columns:
    - **View Folder** - Users can find and view folders.
    - **Edit Folder** - Users can edit any folder field.
    - **Delete Folder** - Users can delete folders from the system.
    - **Create Folder** - Users can create new folders on demand (without an initiating document).  
        Users with this privilege can create workflows with the [Creating Folders](/docs/workflows-and-tasks/launch-workflows) procedure.
    - **Edit Workflow** - Users can edit the workflow tasks to be completed for existing folders.
    - **Edit Security** - Users can edit the security privileges for existing folders.
    - **Deactivate/Reactivate** - Users can deactivate and reactivate the workflow for existing folders.