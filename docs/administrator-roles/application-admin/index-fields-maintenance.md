---
layout: default
title: Index Fields Maintenance
nav_order: 4
parent: Application Administrators
grand_parent: Administrator Roles
has_toc: false
---
# Index Fields Maintenance
Access the Index Fields Maintenance Screen from the Administration menu.

![](/assets/images/index-field-maintenance-screen.png)

{: .important}
> This maintenance screen is just informational to allow administrators to see all the index fields in the system and where they are used. 
>   
> Indexes themselves are added and modified in the context of the [Business Objects](https://qaprod.qflow.com/QAction_help//Object_Definitions_Screen.htm), [Document Classifications](https://qaprod.qflow.com/QAction_help//Classification_Maintenance_Screen.htm), and [Workflow Folder Definitions](https://qaprod.qflow.com/QAction_help//Creating_Folder_Definitions.htm) that use them.

Follow the steps below to add a new index field to a particular Business Object, Document Classification, or Workflow Folder Definition.

1. On a Business Object Definition, Classification, or Workflow Folder Definition, when adding a new index field to the configuration, click **Create New Data Field**.  
    The Add Index Field window appears.  
    ![Add Index Field Window](/assets/images/add-index-field.png "Add Index Field Window")
    
2. Review the options in the Add Index Field window:
    - **Display Name** - Enter a unique name.
    - **Data Type** - Click the drop-down list to see a variety of options, such as _Address, Alphanumeric, Boolean (Yes/No), Currency, Date, Document Type, Entity, List of Values, Numeric, Rich Text, Tag, User_, and various custom fields. The selection for this item affects the options later in the window.
    - **Multi-valued** - Select Yes to allow end-users to add multiple values to one field when adding documents or data. If No is selected, then a user can only choose one value. For example, it is not available for Boolean (Yes/No) as there are only two values, but it is available for Document Types as there are several values.  This option is not connected to adding multi-values on search screens. Learn more about [using multi-valued fields](https://qaprod.qflow.com/QAction_help//Types_of_Search_Filters.htm).
    - **Max Length** - Enter a numeric character limit for the field entries. For example, if generic Alphanumeric is selected for Data Type, then you can add a 10 character limit for the user entry.
    - **Visible Lines** - If Rich Text is selected for the Data Type, enter a value for how many lines can be shown before the user must scroll. This field is only available for Rich Text. For example, enter 2, and only the first two lines of text can be seen without scrolling.
    - **List of Values** - When List of Values is selected for the Data Type, click the drop-down list to choose a list of values created by an administrator on the [List of Values Maintenance](https://qaprod.qflow.com/QAction_help//List_of_Values_Maintenance_Screen.htm) screen. This field is only available for List of Values.
    - **System Name** - Revise the value if necessary, but exclude spaces. Based on your Display Name, the system provides a System Name that contains no spaces.
    - **View Mode Mask** - Will use an input Regular Expression to mask the contents of the field when displayed in the application.
        
3. Enter information in the available fields.
    
4. Click Save.  
    The new index field appears in the grid, from where you can add it to the Business Object, Classification, or Workflow Folder Definition you are working on.