---
layout: default
title: BPMN Process Workflows
nav_order: 7
parent: Workflows and Tasks
has_children: true
has_toc: true
---
# Overview
To create a workflow that contains decision trees (i.e., a workflow with conditional tasks), create a BPMN process workflow. For example, if Option A occurs, send the workflow to Person 1, but if Option B occurs, send the workflow to Person 2.

The Workflow Folder must be set up by a Process Administrator (Administration > Folder Configuration) before you can proceed.

![](/assets/images/bpmn-naming-your-workflow-template.PNG)

Use a pen and paper to draw out the map before you begin. What flow do you want to see? Who starts and ends the workflow? What tasks need to be completed? Who are the actors? Are there any fields that affect where the document goes? Mark those conditions.

{: .important}
Save frequently on the Bpmn Editor screen to avoid losing data if you are timed out of the application.

## Basic Two Step Workflow
![](/assets/images/bpmn-basic-workflow-example.png)

This example shows the workflow for a basic “Review and Approve” process. The workflow begins with a Review task assigned to the Review Group. This task has one complete option. Once the Review task is completed an Approve task is created and assigned to the Approval Group. The Approve task is followed by a user driven exclusive gateway. This means there is a decision to be made by the user when completing this task. The Approve task will have two complete options. The default option is to approve the task and end the workflow. The second option is to send the workflow back to the Review task. If the “More Information Required” option is chosen when completing the Approve task, the workflow will create a new Review task and assign it to the Review Group.

### Modeler Overview  
![Bpmn Editor Screen](/assets/images/bpmn-editor-screen%20-%20callouts.png "Bpmn Editor Screen")

Screen descriptions:
1. **Lasso tool** - Click and drag to select one or several parts of your workflow at once.
2. **Create or Remove Space tool** - Click a workflow field barrier and drag to expand or decrease the white space.
3. **Create Start Event tool** - Insert this symbol to begin a workflow (by default, this symbol automatically appears in the workflow field).
4. **Create End Event tool** - Insert this symbol to complete a path in the workflow.
5. **Create Exclusive Gateway tool** - Insert this symbol to create a conditional decision path.
6. **Create Intermediate Throw Event tool** - Insert this symbol to create a workflow event.
7. **Create User Task tool** - Insert this symbol to create a user task within the workflow.
8. **Create Script Task tool** - Insert this symbol to create script task within the workflow.
9. **Call Activity tool** - Insert this symbol to create a call activity that inserts another BPMN process into the current proces.
10. **Save button** - Save the workflow.
11. **Save SVG button** - Save the workflow as an SVG image to your local drive.
12. **Workflow Title Bar** - Enter the name of the workflow.
13. **Workflow pool**- Insert all workflow nodes here.
14. **Start Event symbol** - Represents the start of the workflow.
15. **Properties panel** - Customize fields and information for each node.
16. **Mini Map** - Used for navigation of the canvas.

### Node Options
Clicking on a workflow node will display some operations that can be performed for the specific node.

![](/assets/images/bpmn-node-options.png)

![](/assets/images/bpmn-swimlane-options.png)

1. Add a node after the selected node (ex: Task, Gateway, End Event)
2. Add a comment box to the node
3. Node Modifications
    1. Wrench - Change the type of the node
    2. Trashcan - Delete the node
4. Add a sequence edge from the selected node
5. Add a swim lane to the pool
    1. If a task needs a different user, group, or organization assigned to perform it, then the task must exist in its own swimlane. Each lane is assigned unique a user, group, or organization.

{: .important}
Using a position or organization is ideal for these workflows (instead of an individual user). Assigning a position or organization is better for handing off work when there is a position change. Additionally, the flow of the tasks may be interrupted if an individual user is selected.