---
layout: default
title: Content Collector Email Setup
nav_order: 7
parent: Application Administrators
grand_parent: Administrator Roles
has_toc: false
---
# Content Collector Email Setup Screen
Use this screen to do the following:
- Collect emails from indicated users.  
- Select how to store the collected emails.
- Modify or delete an existing content collector listing.
- Export content collector information in a PDF or an Excel sheet.
    

## Adding Content Collector Emails
This functionality uses the IBM Collective Content Services in the background to collect and store emails in QAction, so that important emails can be automatically backed up. Fields like Classification and Document Type are defined so that emails are backed up and stored using that index information. If a user has the necessary privileges, they can locate the stored emails using these fields values to filter the search.

The content collector services uses the email addresses entered to locate end-user email inboxes and then it automatically backs up and indexes the emails in QAction using the fields and values you selected in the previous steps.

The following task is an example scenario for using this screen.

1. Click Administration > Email Content Collector Setup.  
    The Content Collector Email Setup screen appears.  
    ![Content Collector Email Setup Screen](/assets/images/Content-CollectorEmailScreen.PNG "Content Collector Email Setup Screen")

2. Click Add and the _Add Content Collector Email_ form appears. 
    ![](/assets/images/add-content-collector-email.PNG)
    
3. Enter or locate criteria for the Classification, Document Type, User, and Organization fields. 

    {: .note}
    > After the user is selected, the Organization field populates with the user's organization.  
    >
    > These fields determine where emails are backed up and stored. If a user has the necessary privileges, they can locate the stored emails using these fields values to filter the search.
    
4. Enter an email address.  
    
    {: .note}
    Content collector services uses this email address to locate end-user email inboxes and then it automatically backs up and indexes the emails in QAction using the fields and values you selected in the previous steps.
    
5. Click **Save**.  

6. Click the new row in the grid, and click **Modify**.  
    
7. Update any of the fields, and click **Save**.