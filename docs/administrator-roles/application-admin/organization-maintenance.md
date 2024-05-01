---
layout: default
title: Organization Maintenance
nav_order: 2
parent: Application Administrators
grand_parent: Administrator Roles
has_toc: false
---
# Organization Maintenance
{: .no_toc }
The following sections describe the various activities that a application administrator role can perform.

## Outline
{: .no_toc .text-delta }
1. TOC
{:toc}

# Organization Maintenance Screen

Use this screen to do the following:

- Create organizational structure, both complex and simple.
- Create departmental or organizational roles within your structure.
- Add users to roles or departments.
- Create working groups (i.e., shortcuts) to organize and access content that is shared across your organizational structure.

The icons indicate various information about type of folder you are viewing:

|   |   |
|---|---|
|Icon|Description|
|![](/assets/images/organizational-folder-icon.PNG)|Organization Folder (indicated by the O on the folder icon)|
|![](/assets/images/WorkinGroup-folder-icon.PNG)|Working Group Folder (indicated by the WG on the folder icon)|
|![](/assets/images/organization-shortcut-icon.PNG)|Shortcut to an Organization Folder (indicated by the arrow on the folder icon)|
|![](/assets/images/Position-icon-folder.PNG)|Position Folder (indicated by the P on the folder icon)|
|![](/assets/images/roles-icon.PNG)|Role Folder (indicated by the R on the folder icon)|
|![](/assets/images/user-checked-out-doc-icon.png)|User|

# Creating Organizations, Positions, and Roles

The following task is an example scenario for using this screen.

1. Click Administration > Organizations and Positions.  
    The Organization Maintenance screen appears.

2. Right-click the first Organization Folder icon (![](/assets/images/organizational-folder-icon.PNG)).  
    The following options appear:
    - Add Child Organization
    - Add Position
    - Edit Organization
    - Print

3. Expand the folder, and right-click an Organization Folder icon.  
    The same options appear, plus the Move Organization option.

4. Right-click a Position Folder icon (![](/assets/images/Position-icon-folder.PNG)).  
    The following options appear: Add User, Edit Position, and Print.

5. Right-click a Working Group Folder icon (![](/assets/images/WorkinGroup-folder-icon.PNG)).  
    The following options appear:
    - Add Child Working Group
    - Edit Working Group
    - Add User
    - Select Organization(s) -- Refer to the [Adding Organizations to Working Group](/docs/administrator-roles/application-admin/organization-maintenance#adding-organizations-to-working-groups)s topic for more information.
    - Move Working Group
    - Delete Working Group
    - Print

6. Right-click a Shortcut Folder icon for an organization folder (![](/assets/images/organization-shortcut-icon.PNG)).  
    The following options appear: Remove organization and Print.

7. Right-click a Role Folder icon (![](/assets/images/roles-icon.PNG)).  
    The following options appear: Add User and Print.

8. Right-click a User icon (![](/assets/images/user-checked-out-doc-icon.png)).  
    The following options appear: Maintain User Account and Print.

# Creating Working Groups

Working groups can be configured to help managers distribute saved searches to users across an organization.

Create a working group and a child working group:

1. In the top-right of the application, click Administration > Organizations and Positions.  
    ![Administration Menu](/assets/images/Admin-options.png "Administration Menu")
    
    The Organization Maintenance screen appears.  
    ![Organization Maintenance Window - Document Indexing WG Folder](/assets/images/organizatons-and-positions-screen.png "Organization Maintenance Window - Document Indexing WG Folder")
    
2. Right-click the Working Groups folder, and click Add Working Group.  
    The Add Working Group window appears.
3. In the Name and Abbreviation fields, enter values, and click Save.  
    The new working groups folder appears with the name you entered and a WG Folder (![](/assets/images/WorkinGroup-folder-icon.PNG)) icon by it.
4. Locate the working group folder you created.
5. To nest a new working group folder under the folder, right-click the folder, and click Add Child Working Group.
6. In the Name and Abbreviation fields, enter values, and click Save.  
    The new working groups folder appears with the name you entered and a WG Folder (![](/assets/images/WorkinGroup-folder-icon.PNG)) icon by it.
7. To add organizations to this working group, refer to the [Adding Organizations to Working Groups](/docs/administrator-roles/application-admin/organization-maintenance#adding-organizations-to-working-groups) procedure.

{: .note}
Adding organizations to working groups can help Save Search Managers create organizational searches. Managers distribute these organizational searches to everyone within a working group. This step eliminates the need to create an organizational search for each organization folder and its users.

# Adding Organizations to Working Groups

Working groups can be configured to help managers distribute saved searches to users across an organization.

Review this procedure to do the following:

- To add organization folders to an existing working group.
    
- To nest a new working group folder under an existing working group folder.
    
{: .note}
Adding organizations to working groups can help Save Search Managers create organizational searches. This step eliminates the need to create an organizational search for each organization folder and its users.

1. In the top-right of the application, click Administration > Organizations and Positions.  
    ![Administration Menu](/assets/images/Admin-options.png "Administration Menu")
    
2. Expand the Working Groups folder and any relevant subfolders until the correct WG folder (![](/assets/images/WorkinGroup-folder-icon.PNG)) is visible.

3. To add organization folders to the working group, right-click the folder, and click Select Organization(s). The Select Organization(s) window appears.

4. In the Type here to filter results field, enter an organization name, abbreviation, or path to filter the results.

5. Press Ctrl on your keyboard to select multiple organizations or positions.

    {: .note}
    If an organization is selected, then all of the positions directly under that organization will be included in the working group.

6. When you are finished, click Select.

    {: .highlight}
    Under a working group, the folder icons for organizations or positions have a small arrow in the corner to indicate it's a shortcut to the original folder (![](/assets/images/organization-shortcut-icon.PNG)).

7. Back on the Organization Maintenance screen, to nest a new working group folder under the folder, right-click the folder, and click Add Child Working Group. The Add Child Working Group window appears.

8. In the Name field, enter a name for the working group folder. If you like you can also enter an abbreviation for the folder.

9. When you are finished, click Save.

10. To remove an organization from a working group, right-click the organization, and click Remove organization.  

    {: .note}
    If you add a top-level position or organization, and you try to remove an embedded organization or position (that is set up in the organization structure originally, and not set up through the working group), then you cannot remove it; the only option available will be to print it.

# Adding Users to Working Groups

After [creating a new user](/docs/administrator-roles/application-admin/manage-users#creating-a-new-person-entry) in the system, you can add them to working groups by following the steps below.

1. In the top-right of the application, click Administration > Organizations and Positions.
    
    ![Administration Menu](/assets/images/Admin-options.png "Administration Menu")
    
2. Expand the Working Groups folder.

3. Expand any subgroups needed to find the working group you want to add the user to.

4. Right-click the desired working group, and click Add User.
    
    {: .note}
    The Select User(s) window appears with the same search setup that can be seen throughout the website.
    
5. In the main Search field, enter a user social security number or last name, and click Search. ![Select User(s) Window - Social Security Number Entered](/assets/images/select-users-window.jpeg "Select User(s) Window - Social Security Number Entered")
    
6. Select the intended user. The window closes, and the user appears under the Pension Corporate folder.