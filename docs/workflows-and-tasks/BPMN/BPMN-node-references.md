---
layout: default
title: BPMN Node Reference
nav_order: 1
parent: BPMN Process Workflows
grand_parent: Workflows and Tasks
has_children: false
has_toc: false
---
# BPMN Node Reference

|---|---|---|---|---|
|**Basic Buttons or Symbols**|**Description**|**Properties**|**Incoming Edge Count**|**Outgoing Edge Count**|
|![](/assets/images/bpmn-pool-icon.png)|**Pool** - The container for the workflow process.|- Name<br>- Folder Type<br>- Organization|0|0|
|![](/assets/images/bpmn-swimlane-icon.png)|**Swim Lane** - Contains nodes assigned to a specific group/user in the workflow.|- Assignee<br>- Auto Assign to User|0|0|
|![](/assets/images/bpmn-sequence-edge-icon.png)|**Sequence Edge** - Connects nodes in a workflow process|- Name<br>- Sort Order<br>- Task Note Required<br>- Assign Next User|0|0|
|![](/assets/images/bpmn-start-event-button.PNG)|**Start Event** - The default starting point of a workflow. Each workflow must have one and only one of these.|- Name|0|1|
|![](/assets/images/bpmn-signal-start-event-icon.png)|**Signal Start Event** - Used for Re-Activate events. A workflow can have any number of these.|- Name<br>- Re-Activate to last completed task|0|1|
|![](/assets/images/bpmn-end-event-icon.PNG)|**End Event** - The end of a workflow process. All paths must end with one of these. A workflow must have at least one of these.||1|0|
|![](/assets/images/bpmn-user-task-symbol.PNG)|**User Task** - A task in the workflow that requires manual input from the user to complete.|- Name<br>- Days to Complete<br>- Day Type<br>- Days to Complete Field Path<br>- Holdable<br>- Hold Instructions<br>- Terminatable<br>- Cancellable<br>- Instructions<br>- Document Signature<br>- Launch Initiating Document<br>- Show Icon if Folder Has Documents<br>- Complete through API Services<br>- Open Task Default Behavior (View/Work Task)<br>- View Instructions<br>- Alert When Complete<br>- User Interface Key<br>- Work Task Default Action<br>- Custom Properties|1+|1|
|![](/assets/images/bpmn-script-task-symbol.PNG)|Script Task - A task in the workflow that is completed automatically by the system. These tasks execute some script code to perform system operations.|- Name<br>- Seconds to Complete<br>- Script<br>- Script Language<br>- Alert When Complete|1+|1|
|![](/assets/images/bpmn-call-activity.png)|**Call Activity** - Inserts another BPMN workflow process in place into the current process.|- Name<br>- External Process|1+|1|
|![](/assets/images/bpmn-exclusive-gateway-symbol.PNG)|**Exclusive Gateway** - Marks a decision point in the workflow. These can be data or user driven.|- Name|1|2+|
|![](/assets/images/bpmn-paralle-gateway-symbol.PNG)|**Parallel Gateway** - Marks the beginning of a parallel sequence in the workflow. These can be data or user driven. Must always be used as a set, a parallel sequence must have an end.|- Name|1|2+|
|![](/assets/images/bpmnevent-gateway-symbol.PNG)|**Event Based Gateway** - Represents a hold task in the system. Can have multiple incoming sequence edges and must have outgoing sequence edges followed by an intermediate catch event. Must include at least one conditional take off hold catch event and a timer catch event.|- Name<br>- Allow Dynamic Hold Time<br>- Dynamic Hold Time Required<br>- Hold Instructions<br>- Hold Reason Type<br>- Hold Reason List|1|2+|

## Catch Events
Catch Events are types of events that connect to Event Gateways. Catch Events must be set up to receive information from the Event Gateway and deliver the correct next task to the defined user or group.

Catch Events must be uniquely named within the system. Catch Events must have a matching QEvent record of type “ProcessIntermediate”??

|**Catch Events**|**Description**||||
|![](/assets/images/bpmn-intermediate-catch-event-email.PNG)|**Message Intermediate Throw Event** - Sends a configured email message.|- Name<br>- Sender<br>- Recipients<br>- CCs<br>- Subject<br>- Message|1+|1|
|![](/assets/images/bpmn-intermediate-catch-event-take-off-hold.PNG)|**Conditional Intermediate Catch Event** - Used in conjunction with an event based gateway. Executes when some condition in the workflow is met.|- Name<br>- Take Off Hold Event<br>- Document Event|1|1|
|![](/assets/images/bpmn-intermediate-catch-event-days-to-hold.PNG)|**Timer Intermediate Catch Event** - Used in conjunction with an event based gateway. Executes when a certain number of days has elapsed since the hold start date.|- Name<br>- Days to Hold<br>- Day Type|1|1|
|![](/assets/images/bpmn-intermediate-catch-event-triangle.PNG)|**Signal Intermediate Catch Event** - Used in conjunction with an event based gateway. Executes in response to a signal intermediate throw event or external event with the same name.|- Name|1|1|
|![](/assets/images/bpmn-intermediate-throw-event.png)|**Signal Intermediate Throw Event** - Fires a corresponding signal intermediate catch event with the same name.|- Name|1+|1|