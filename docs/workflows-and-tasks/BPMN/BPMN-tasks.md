---
layout: default
title: BPMN Tasks
nav_order: 2
parent: BPMN Process Workflows
grand_parent: Workflows and Tasks
has_children: false
has_toc: false
---
# BPMN Tasks
## User Task
![](/assets/images/bpmn-user-task-symbol.PNG)
**Required**

- Name
- Days to complete
    - By default this is set to 1 business day
    - The day type can be changed between business and calendar
    - If a folder type is set for the workflow, then a custom object field can be selected to set the days to complete
        - The custom object field selected must be a numeric type
            
**Optional**
- Instructions - Text to display on the complete task screen
- Holdable - Creates a complete task option that allows the task to be put on hold
    - Hold Instructions - Display only while the task is on hold
    
    {: .note}
    To create a task that starts off On Hold, see the [Hold Tasks](/docs/workflows-and-tasks/BPMN/BPMN-tasks#hold-tasks) section.
        
- Terminatable - Creates a complete task option to immediately terminate the workflow
    - A complete task note is required when selecting Terminate
- Cancellable - Same as terminatable, but no note is required.
- Document Signature - Marks the task as a document signature task
- Launch Initiating Document - When the task is opened the document that initiated the workflow will display
- Show Icon if Folder has Documents - Displays an icon if the folder contains documents
- Completed Through API Services - Notates that the task is completed through an API integration rather than in the user interface
- Open Task Default Behavior
    - Work - When the task is opened, then it is started and assigned to the user that opened the task
    - View - When the task is opened, then view options are displayed. This allows the user to view the folder and task without working it.
        - View options will allow the user the option to start working the task
        - View Instructions are only displayed on the task in View Mode
- Alert When Complete - Group that receives an email notification when the task is completed
- User Interface Key - Applies a custom complete task user interface
- Work Task Default Action - The default complete option that will be selected when the task is opened
- Custom Properties - Attributes set on the task that are used for internal system operations. These are not displayed in the user interface.

## Sequence Edge
![](/assets/images/bpmn-sequence-edge-icon.png)

A sequence edge represents a route in the workflow process. A sequence edge is unidirectional (one-way).

![](/assets/images/bpmn-sequence-edge-general.png)

**Required**
1. A sequence edge must have a sort order (populated on the General tab). This is the order in which the complete task options will appear. The default value is 0.
2. All nodes with the exception of Start Events must have an incoming sequence edge.
3. All nodes with the exception of End Events must have an outgoing sequence edge.

**Optional**
General Tab (pictured above):
1. Sequence edges can be named. This name is used for the complete task option. If the edge is not named, then the default value is “Complete”.
2. Task Note Required - When this is checked a note will be required when selecting the edge when completing a task.
3. Assign Next User - Adds an interface to the complete task option for the user to select a specific assignee for the following task from the group for the swimlane the following task is in.

Advanced Tab:
![](/assets/images/bpmn-sequence-edge-advanced.png)

1. User/Data Driven - This only applies when used with a decision [gateway](/docs/workflows-and-tasks/BPMN/BPMN-gateways).
2. Workflow Variables - Used to apply parameters that can or must be captured when completing a user task.
3. Custom Properties - Values set for the edge that are used for system integration. 

**Restrictions**
1. All nodes with the exception of [gateways](/docs/workflows-and-tasks/BPMN/BPMN-gateways) can only have one outgoing sequence edge.

## Workflow Variables
Workflow variables are very useful for capturing specific data from the user when they complete a task.  When the user selects the complete task option for a specific sequence edge, they will see all of the workflow variables set up for that sequence edge.

To configure workflow variables for a sequence edge, open the **Advanced** tab for that edge and click the **Click to open editor** link under **Workflow Variables**.

This opens the _Process Variable Editor_ window.  Here you can add workflow variables of three different types:

1. **Folder** variables represent data fields on the folder.  When a user fills out a folder variable on a task, the workflow updates that field on the folder.
2. **Process** variables are just used by the workflow itself, e.g. a data-driven [gateway](/docs/workflows-and-tasks/BPMN/BPMN-gateways) later in the workflow may reference a process variable to determine which path to follow.
3. **Document** variables prompt for a document of the selected Classification and Document Type.  If a matching document is found in the folder, it will be shown, otherwise the user can upload a new document.

Each workflow variable added to an edge can be Required or optional.

When a [hierarchy field](/docs/performing-searches/types-of-search-filters#hierarchy-filters) is added as a workflow variable, it can be anchored to a specific location in the hierarchy so that users don't have to navigate through the whole hierarchy tree to find the group that is relevant to the workflow.  Hierarchy fields can also be configured to show users under the selected location (as opposed to just showing groups/positions/etc). 

Hierarchy workflow variables can be especially useful when a task later in the workflow should be assigned to a specific group, position, or user selected earlier in the workflow.  To accomplish this, the relevant swimlane just needs to be assigned to the same folder field as the workflow variable.

## Hold Tasks

A hold task in Q-Action is defined by a BPMN complex [gateway](/docs/workflows-and-tasks/BPMN/BPMN-gateways) node. This creates a user task that starts on hold, and unlike a “holdable” task, when it is taken off hold it must follow a sequence edge to another node.

![](/assets/images/bpmn-hold-task.png)

**Waiting for Something (1)**  
This is the hold task (complex gateway)

1. **Optional Properties**
    
    1. Allow Dynamic Hold Time - Adds a task parameter to the preceding user step that allows the user to define how long the task is on hold for
        * Dynamic Hold Time Required - Requires the above parameter to be entered
    2. Hold Instructions - Instructions displayed for the hold task
    3. Hold Reason Type - When entering a dynamic hold time, a hold reason is required. This defines whether the entry is free form text or a list of options
        * Hold Reason List - Defines the list of options for the above parameter
            
2. **Required Events**  
    A hold task must have only one of each of the following events
    1. Conditional Take Off Hold Event (2) - The event followed when a user manually takes the task off hold. This is also defined as the default edge for the gateway. Marked by checking the “Take Off Hold Event” checkbox on the conditional event node property
    2. Timer Event (4) - The event followed when the number of hold days expires
        
3. **Optional Events**  
    A hold can can have the following additional events
    1. Folder Document Event (3) - The event followed when a document that matches the folders initiating document configuration is received. This is marked by checking the “Document Event” checkbox on the conditional event node property. Only one of these events is allowed.
    2. Event Happened (5) - This is a signal event that is fired either from a throwing signal event within the workflow or a system event. The throwing event name must match this catching events name. Any number of these can be defined as long as they have a unique name.