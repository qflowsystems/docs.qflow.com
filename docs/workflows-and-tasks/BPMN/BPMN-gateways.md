---
layout: default
title: BPMN Gateways
nav_order: 3
parent: BPMN Process Workflows
grand_parent: Workflows and Tasks
has_children: false
has_toc: false
---
# BPMN Gateways
## Decision Gateway
A decision gateway marks the point in a workflow where a route decision is made either by the user or automatically by the system. These decisions can take one or many different routes. (Note: Currently in QAction we only support one route, also called an exclusive gateway)

## User Driven Exclusive Gateway
A user driven gateway requires a manually decision by the user when completing the previous task. The decisions are named based on the name of the sequence edges coming out of the decision gateway.

![](/assets/images/bpmn-user-driven-gateway.png)

**Required**
1. An exclusive decision gateway with at least two outgoing sequence edges
2. One sequence edge must be marked as “default”. This is used by the workflow prediction engine as the path to follow when a decision has not yet been made.
    - The sequence edge is set to default by selecting the edge, clicking the modification wrench icon, and choosing “Default Flow”
        

**Restrictions**
- A user decision gateway cannot be directly follow by another user decision gateway.
    

**Optional**
- See the Sequence Edge section for information on setting up optional properties
    

## Data Driven Exclusive Gateway
A data driven gateway requires no decision to be made by the user. The system will automatically choose the correct route based on some criteria. This criteria can be enter by the user on the previous task or taken from the process data that is enter upon creation or at another previous time in the workflow process.

![](/assets/images/bpmn-data-driven-gateway.png)

In the above scenario, when the “Enter Amount” task is completed the system will automatically route to the next task based on the amount entered. If there is no amount entered or the criteria doesn’t match, then the default route will be chosen.

**Required**
1. An exclusive decision gateway with at least two outgoing sequence edges
2. One sequence edge must be marked as “default”. This is used by the workflow prediction engine as the path to follow when a decision has not yet been made.
    - The sequence edge is set to default by selecting the edge, clicking the modification wrench icon, and choosing “Default Flow”
3. Data driven sequence edges must have a “Script” value. This is entered in the property panel for the sequence edge under the advanced tab when the data driven option is selected.
    1. The script must return a boolean value.
    2. To access the value of a folder field, use the system name of the folder field, which you can find to copy & paste when editing the folder field on the folder definition screen.
    3. For objects and LOVs, the value of the folder field will be the ID of the object/LOV. In order to access subfields on an object folder field, a more complicated script is required to load the object using its ID.
    4. To check if a value is null, you need to use the [Groovy binding object](https://docs.groovy-lang.org/3.0.8/html/gapi/groovy/lang/Binding.html), e.g.  
        return (!binding.variables.containsKey("ApplicationID"));

**Restrictions**
- A data decision gateway cannot be directly follow by a user decision gateway.

**Optional**
1. Data driven gateways may be chained together. Meaning a data driven gateway can be followed by another data driven gateway.
2. See the Sequence Edge section for information on setting up optional properties

## Parallel Gateway
Every time tasks are parallel (i.e., they occur at the same time instead of sequentially), there must always be an starting Parallel Gateway and a ending Parallel Gateway. Think of it as a Start Event and End Event for an embedded workflow. See the following image example.  
![](/assets/images/bpmn-parallel-workflow.PNG)