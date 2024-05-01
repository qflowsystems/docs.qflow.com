---
layout: default
title: Disposition Approval Workflows
nav_order: 4
parent: Records Management
has_toc: false
---
# Understanding Disposition Approval Workflows

Each [Record Policy](/docs/records-management/create-a-record-policy) defines a frequency at which the system will launch a Disposition Approval Workflow for any records with a [Disposition Date](/docs/records-management/disposition-date) in the past.  Some records may be excluded if a different Record Policy also applies to that record, and defines a Disposition Date for the record that is still in the future.

The exact steps in a Disposition Approval Workflow may vary by Record Policy, but every Disposition Approval Workflow will at least contain a Review and Approve Records Disposition Task to be worked by the Record Custodian user group defined in the Policy.

After a Disposition Approval Workflow is completed, the system will kick off a background process to perform the Disposition Action defined in the Policy on each of the records for the Workflow, except those with a [Hold](/docs/records-management/record-holds).

Users who are assigned to work a task in a Disposition Approval Workflow can find that task in their [Inbox](/docs/workflows-and-tasks/workflow-screens#Inbox).

Disposition Approval Workflow Folders can also be searched for on the Search Folders screen by clicking Folders in the left-hand menu.

Records Managers can see Disposition Approval Workflows at various stages along with Record Policies and Records on a special [Records Disposition Dashboard screen](/docs/records-management/records-disposition-dashboard).