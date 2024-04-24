---
layout: default
title: Release Notes
nav_order: 2
has_children: false
---
# Release Notes

## 5.22
----

### New Features

1.  Index Queue Re-Route option now filters to only organizations that contain users who will be able to take over the task.\--ENG-980
2.  User suggestions now work with hierarchy process variables that are anchored to a specific place in the hierarchy.\--ENG-975
3.  Object and multi-value type subfields can now be made editable on folders.\--ENG-949
4.  Improved administrative user experience for Document Type customization.\--ENG-950
5.  New copy capability on LOV Maintenance administrative screen.\--ENG-957
6.  Users can now download batches to their computer from the Index Documents screen.\--ENG-1099

### Bug Fixes

1.  Re-Route option in batch assembly now works correctly.\--ENG-956
2.  Variable task assignees from folder fields now assign to the user under the correct group for the field rather than the general users group.\--ENG-976
3.  The user who actually assembled and indexed a document from the index queue is now set as the "Create user" for the document.\--ENG-979
4.  PDFs that have been rotated now display correctly.\--ENG-1003
5.  Multi-value fields now work correctly when a user clicks "Add" multiple times in a row and then makes all their selections after.\--ENG-1020
6.  Pop-up search screens now display correctly for users who have grid view turned on by default.\--ENG-1062

### Under-the-Hood Enhancements

1.  Improved script task & configuration maintenance capabilities.\--ENG-951

## 5.21
----

### New Features

1.  Users can now add a cover sheet to all documents on the batch and split screen.\--ENG-752
2.  New user preference to preview PDF initiating documents instead of downloading them.\--ENG-859
3.  New ability to add a special Assign User Next Task interface to complete task options in the BPMN editor.\--ENG\-870
4.  Using the "Related Folders" field to create a new folder is now a more seamless experience.\--ENG-871
5.  Values in LOV drop-downs can now display with a configured ordering besides just alphabetical.\--ENG-514

### Customizations

1.  Improved sync process with external data feed.\--ENG-611
2.  Updated custom fax import software to send documents to Q-Action where users can split & assemble the faxes.

### Bug Fixes

1.  Users can now use the Add icon to add new primary field objects when indexing documents.\--ENG-462
2.  PDF preview now properly displays large-size PDFs–ENG-496
3.  Fixed issue with removing process variables after a complete task interface in the BPMN editor.\--ENG-819
4.  Removed non-functional buttons from informational administrative screen.\--ENG-857

### Under-the-Hood Enhancements

1.  Improved caching performance.\--ENG-806

## 5.20
----

### New Features

1.  Folder subfields can now be made editable directly on a folder.–ENG-628
2.  Folder subfields can now be selected as complete task parameters in the BPMN workflow editor.–ENG-629
3.  Alphanumeric fields can now be given a custom display mask.–ENG-662
4.  Added an additional automation option in initiating documents settings.\--ENG-751
5.  BPMN workflow tasks can now have a variable number of days to complete based on a Numeric folder field.\--ENG-792

### Customizations

1.  Added ability to display historical workflow data migrated from other systems.–ENG-621
2.  Certain custom objects have been set up to automatically launch related folders upon creation where relevant.–ENG-660, ENG-667

### Bug Fixes

1.  InActive users will no longer be suggested in assign next task fields.–ENG-788
2.  Assign user next task functionality can now be used before a decision gateway in BPMN editor.–ENG-741
3.  Fixed issue with modify security action on multiple documents–ENG-694
4.  Remove from Folder option now correctly displays without requiring a folder refresh.–ENG-670
5.  Add icon now correctly displays for business object fields on Modify Indexes screen.–ENG-668
6.  Fixed list of values csv file import.\--ENG-846

## 5.19
----

### New Features

1.  Users can now preview PDFs on the Upload Documents screen by clicking on the preview (![](assets/images/images/Icons/preview-icon.png)) icon–case 31292
2.  Accessibility updates including:\--ENG-46
    1.  User can now close modal pop-ups with the Escape key + other keyboard accessibility improvements–ENG-29, ENG-23
    2.  Expanded screen reader support–ENG-25
3.  Updated top search field label–case 29773

### Bug Fixes

1.  Fixed issue with copying documents that have a Primary Field–ENG-734
2.  Fixed error with adding organizational document templates–case 30710
3.  Fixed issue with viewing similar folders–case 30815

### Under-the-Hood Enhancements

1.  Updated dependencies to improve security posture–case 29600, case 31061, case 31246, case 31266, case 31268, case 30872, case 30906, case 30872, case 29324
2.  Optimized document upload efficiency–case 28657

## 5.18.10
-------

### Customizations

1.  Improvements to custom process for a specific customer.

## 5.18.9
------

### Under-the-Hood Enhancements

1.  Updated dependencies\--ENG-315

# 5.18.8
------

### Customizations

1.  New functionality for a specific customer.

### Bug Fixes

1.  Assemble Batch task name queries now work correctly.\--ENG-193

## 5.18.7
------

### Bug Fixes

1.  Users can now search for the last name of a task's create user again.\--ENG-119
2.  Fixed issue with process to automatically take folders off hold\--ENG-115