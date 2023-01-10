# User and Permission management

<!-- TOC -->
- [A: Overview](#a-overview)

- [B: Manual for users](#b-manual-for-users)

	- [1 Registration](#1-registration)
	- [2 Login](#2-login)
	- [3 Dataset permissions](#3-dataset-permissions)
	- [4 API Token](#4-api-token)
	
- [C: Manual for administrators](#c-manual-for-administrators)
	- [1 Manage User](#1-manage-user)
		- [1.1 Create a user](#11-create-a-user)
		- [1.2 Edit or Delete a user](#12-edit-or-delete-a-user)
	- [2 Manage groups](#2-manage-groups)
		- [2.1. Create a group](#21-create-a-group)
		- [2.2. Edit or Delelte a group](#22-edit-or-delete-a-group)
	- [3 Manage former members](#3-manage-former-members)
		- [3.1. Set user to former member](#31-set-user-to-former-member)
		- [3.2. Revoke user as former member](#32-Revoke-user-as-former-member)
	- [4 Permission](#4-permission)
		- [3.1. Feature permission](#41-feature-permission)
		- [3.2. Entity permission](#42-entity-permission)
	- [5 Manage datasets](#5-manage-datasets)
	

<!-- /TOC -->

## A: Overview

All features (e.g., search)  and all types of datasets are secured and managed via a user and permission management. Depending on the BEXIS2 configuration, some features (e.g., search) are also accessible for non-registered users, while others only for authorized users. After registration in BEXIS2, the system administrator assigns the appropriate permissions individually or by assigning the user to a permission group. In general, it is possible to add, remove, or modify existing permissions on features and all types of datasets. Each user can also grant permission for their datasets to others. Also, it is possible to generate a personal token for authentication to access BEXIS2 via API.

## B: Manual for users

### 1 Registration

The registration form is accessible via the Register button on the right side. All fields of the form are mandatory and it is required to agree on the *Terms and Conditions* and *Privacy Policy*. Then you are asked to confirm your email address. As the last step, you have to provide some information (e.g.,  name, affiliation to the project, organization). Based on the provided details, the project Team grants permissions within three days.

![registration](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/register.png)

### 2 Login

Press the *Login* button on the right side. BEXIS2 redirects you to the login form, where you have to enter your account credentials (email or user name and password). If the login is successful, the start page (e.g., *Dashboard* or *Search*) is loaded. Otherwise, you will see information about the status and reason for the failed login.

<a href="url" title="login"><img src="https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/login.png" align="center" height="300" ></a>


### 3 Dataset permissions

### 4 API Token

In general, two mechanisms, authentication, and authorization protect the APIs of BEXIS2. Unlike logon, which uses the usual credentials, the APIs use a personalized token for authentication. The token can be found in the user menu. 

![token](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/token.png) 

## C: Manual for administrators
### 1 Manage User

User accounts are used to assign permissions and track actions like the creation of a dataset. Accounts can be linked to the party module and the real user name is shown instead of the account name. 

![users](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/users.png)

#### 1.1. Create a user

In addition to the self-registration procedure, the administrator can also create accounts. This feature is available here: *Settings > Manage Users > Create User*. The system supports you with validation on all entered information.

![create_user](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/create_user.png)

#### 1.2. Edit or Delete a user

Under *Settings > Manage Users* it is possible to view, modify, and delete user information using the following options:

| Button | Description 
|-|-
| Edit | for security and usability reasons, not all fields can be modified (e.g., user name).  
| Group | show the membership in a group <br/> status can be changed by (un)selecting the corresponding checkbox 
| Delete | delete a user account (exception: user accounts already used)

![edit_user](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/edit_user.png)

## 2 Manage groups

Groups combine a set of permissions for its members. Users can be assigned to different groups.

![groups](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/groups.png) 

#### 2.1. Create a group

This feature is available under *Settings > Manage Groups > Create Group*. A new group can be defined.

![create_group](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/create_group.png) 

#### 2.2. Edit or Delete a group

Under *Settings > Mange Groups* it is possible to view and modify group information. 

| Button | Description 
|-|-
| Edit | change group name or description 
| Group | members of a group can be (un)selected
| Delete | delete a group (exception: Groups already used)

![edit_group](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/edit_group.png) 

### 3 Manage Former members

Former member management gives you the possibility to change rights in BEXIS for users who are no longer active in your project. The feature also allows you to undo the changes. The precondition for the use of this feature is a special role in BEXIS to which you then assign all the rights that former members should have.

#### 3.1 Set user to former member

This feature is available under *Settings > Manage Former Members. 

Former member management uses end date of a user party to find e.g. users who have not been project members for a certain period of time. By using the end date filter, time-related queries can be made to users. To set a user as former member the checkbox in the *is former member column* must be set. The system admin and the user will then receive a confirmation email. With the activation of the former member status, all feature and role rights are removed from the user. And the user is added to the former member role.

![formerMembers](https://github.com/BEXIS2/Documents/blob/master/Manuals/SAM/Images/set_former_member.png)


To customize the confirmation email the text blocks of the email can be changed in the SAM settings file. The file is located at "...\Workspace\Modules\SAM". If the subject remains empty, the default subject of BEXIS is used.

![formerMembersSettings](https://github.com/BEXIS2/Documents/blob/master/Manuals/SAM/Images/sam_settings.png)


#### 3.2 Revoke user as former member

To undo the former member status the checkbox must be deactivated. This means that the former member role will be removed from the user and his previous rights will be activated again. A confirmation email will be sent when the change is made.

### 4 Permission

Permissions contain specific security regulations. The security system of BEXIS2 distinguishes between two types of permissions. The *feature permission* allows or prohibits access to a well-defined and delimited area of the application, so-called Features. The *data permission* provides the option to protect all types of datasets.

#### 4.1 Feature permission

Under *Settings > Manage Feature Permissions* you can customize features permissions. 

Selecting a checkbox in the navigation tree (e.g., *Search*) will make that feature accessible without authentication (*public access*). **Please use it with care!**

Clicking on a feature name opens a table on the right side. This table contains all subjects (users and groups) and their feature permission status. You may grant or deny permissions for individual users or groups using the radio buttons. If permission is not explicitly set (*none*), it can be inherited from up-level features. Inherited permissions are shown in the first column as *effective* permissions.

![features](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/features.png) 

#### 4.2 Entity Permission

To manage access to entities (datasets and publications) go to *Settings > Manage Entity Permissions*.

By selecting a dataset (by clicking on the row of the dataset), a new table displays all subjects (users and groups) and their different data permission statuses regarding the selected dataset. Here you can also change permissions for the selected dataset.

Selecting the checkbox in the first column (*IsPublic*) gives public access to that dataset without any authentication.

![datasets](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/Help_img10.png) 

In general, BEXIS2 distinguishes different data permission types:

* Read: allows to read & download to primary data and attachments
* Update: enables changes (upload and update) of primary data and metadata
* Delete: allows to delete the whole dataset
* Grant: allows to give permission to other users or groups

### 5 Manage datasets

Display the list of datasets under *Settings > Manage Datasets*. In this list, you can see the status of each dataset and do some useful actions to maintain datasets.

There are two ways to delete a dataset (1) *delete* and (2) *purge*. 

![maintenance](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/Help_img11.png) 

There are two ways to delete a dataset:

*Delete* tags a data record to exclude it from nearly all features of BEXIS2 (e.g., search). But you are still able to restore the data record – if needed. 

*Purge* deletes a dataset completely. The data record **can not be restored**. 



[Go to top](#a-overview)
