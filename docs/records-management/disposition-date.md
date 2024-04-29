---
layout: default
title: Disposition Date
nav_order: 3
parent: Records Management
has_toc: false
---
# Understanding the Disposition Date

The Disposition Date for a given record is the date on which that record becomes eligible for disposition.  The system uses this date to automatically kick off [Disposition Approval Workflows](https://qaprod.qflow.com/QAction_help//Understanding_Disposition_Approval_Workflows.htm) for records with a Disposition Date in the past.

This date is automatically calculated by the system using three values defined in the [Record Policy](https://qaprod.qflow.com/QAction_help//Creating_a_Record_Policy.htm) (or Policies) that a given record falls under:

- Retention Period Start Date - the date field associated with the record that the system will use to calculate the Disposition Date.
- Retention Period Cutoff - an optional offset for the Retention Period to begin at a set time after the Retention Period Start Date.  This will usually be something like the end of the fiscal or calendar year.
- Retention Period - the length of time following the Retention Period Start Date, or the optional Cutoff following that date, after which the record will become eligible for disposition.

The system calculates (and/or recalculates) the Disposition Date for a Record whenever the Retention Period Start Date is set or changes.

## Example

Suppose there is a Record Policy on a Document Classification called Timesheets, to destroy records 7 years after the end of the calendar year for their Week Ending Date.  To break that down:
- This policy applies to all documents in the Timesheets Classification.
- The Retention Period Start Date is the Week Ending Date, an index field on documents in the Timesheets Classification.
- The Retention Period Cutoff is the end of the calendar year.
- The Retention Period is 7 years.
    

So if a particular Timesheet document has a Week Ending Date of 05/10/2020, then the system will calculate the Disposition Date to be 7 years after the end of the 2020 calendar year.  This means that the system will launch a Disposition Approval Workflow for the Timesheet document on or after December 31st, 2027, depending on the frequency set for Disposition Approval Workflows in the Record Policy.

If for some reason the Week End Date for a given Timesheet Document is changed - say, perhaps it was input into the system incorrectly at first - then the system will re-calculate the Disposition Date based on the updated Week End Date.