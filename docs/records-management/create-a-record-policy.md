---
layout: default
title: Create a Record Policy
nav_order: 2
parent: Records Management
has_toc: false
---
# Creating a Record Policy

Only Application Administrators can manage Record Policies.

To create a Record Policy, open the appropriate Administration screen to locate and then edit the Custom Object Definition, Folder Definition, or Classification you wish to create the policy for.  If Records Management is enabled, there is a Retention Tab on the Add/Modify screen.

Retention Tab on an Example Custom Object Definition Screen  
![](/assets/images/retention-tab-custom-object.png)

Click Add Policy to create a Record Policy for the Definition/Classification you are editing.

Create Record Policy Screen  
![](/assets/images/create-record-policy-blank.png)  

Record Category is the human-readable description of the Policy you are creating.  Learn more in [Understanding Record Categories](/docs/records-management/policies-categories.html).

Filter Criteria are any additional data about the Record that determine whether this Policy applies to the Record.  Any Index Field on the Definition/Classification can be used as a Filter Criteria for a Record Policy.  If there are no Filter Criteria on the Policy, then the Policy will apply to every Object or Folder with the Definition you are editing, or every document in the Classification you are editing.

The other fields on this screen can be roughly grouped into two different categories:

- Launching [Disposition Approval Workflows](https://qaprod.qflow.com/QAction_help//Understanding_Disposition_Approval_Workflows.htm)
- Calculating the [Disposition Date](https://qaprod.qflow.com/QAction_help//Understanding_the_Disposition_Date.htm) for a given record

## Disposition Approval Workflows

Disposition Launch Frequency determines how often the system will launch a Disposition Approval Workflow for relevant Records under this Policy.

Workflow is the specific Workflow Template for the Disposition Approval Workflow that should be launched.

Records Officer and Custodian are the user groups who will need to complete tasks in the selected Disposition Approval Workflow whenever it launches.  The Custodian may not always be required.

Disposition Action determines what the system will do with the Record after its Disposition Approval Workflow is complete.

## Disposition Date

Retention Begin Date is the date field associated with the record that the system should use to determine when the Retention Period for the record should begin.  

The Retention Period Cutoff instructs the system to round off the Retention Begin Date, such as to the end of the fiscal or calendar year.

Retention Period is the length of time following the Retention Period Start Date, or the optional Cutoff following that date, after which the record will become eligible for disposition.