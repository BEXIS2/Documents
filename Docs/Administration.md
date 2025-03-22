---
title: "Administration"
position: 6
---

# Administration
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles)

## Manage User

User accounts are used to assign permissions and track actions like creating a dataset. Accounts can be linked to the party module and the actual user name is shown instead of the account name.

![users](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/users.png)

### Create a user

In addition to the self-registration procedure, the administrator can also create accounts. This feature is available here: *Settings > Manage Users > Create User*. The system supports you with the validation of all entered information.

![create_user](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/create_user.png)

### Edit or Delete a user

Under *Settings > Manage Users* it is possible to view, modify, and delete user information using the following options:

| Button | Description
|-|-
| Edit | Not all fields can be modified for security and usability reasons (e.g., user name).
| Group | show the membership in a group <br/> status can be changed by (un)selecting the corresponding checkbox
| Delete | Delete a user account (exception: user accounts already used)

![edit_user](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/edit_user.png)

## Manage Groups

Groups combine a set of permissions for their members. Users can be assigned to different groups.

![groups](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/groups.png) 

### Create a group

This feature is available under *Settings > Manage Groups > Create Group*. A new group can be defined.

![create_group](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/create_group.png) 

### Edit or Delete a group

Under *Settings > Mange Groups* it is possible to view and modify group information.

| Button | Description
|-|-
| Edit | Change group name or description
| Group | Members of a group can be (un)selected
| Delete | Delete a group (exception: Groups already used)

![edit_group](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/edit_group.png) 



## Manage Parties
An administrator can see, create, edit, and delete parties. Parties are the central smaller entities in BEXIS2. They can be persons, organizations, projects, etc.

On the overview page, you can see and manage all the available entities. The red warning icon in the "action-required" column shows that this party needs some relationships to be valid.

<figure class="image">
  <img src="https://github.com/BEXIS2/Documents/raw/master/Manuals/BAM/Images/view_parties.png" alt="Overview parties">
  <figcaption style="display: block; text-align: center;">Overview parties</figcaption>
</figure>

### Create and Edit
A new party can be created under *Settings > Manage Parties > Create Party*. In the first step, select a party type and its date range, if applicable. Click on Next to continue.

In the next step, you will see additional attributes based on the selected party type. Required fields are marked with a red asterisk. Click on Save or on Next to continue.

In some party types, you must create relationships with others (e.g., a person belongs to an organization). If you do not do it, the party will be saved, but it is invalid. You can also add a relationship  later.

To edit a party, click on "Edit" in the party overview. You can change all the fields except for the party type.

![Create party](https://github.com/BEXIS2/Documents/raw/master/Manuals/BAM/Images/create_party.png)

### Delete
Only parties not in use or linked can be deleted under *Settings > Manage Parties*.

## Manage Relationships
### Create
Every party could have relationships with the other parties. The party relationships tab in Edit or create a party is to manage these relationships.
  To create a new relationship, click Create and see the following window. Here, you see all the available party relationship types, which depend on the definitions we already have. The numbers in parentheses show the number of current relationships and the maximum number of relationships that this party to this relationship type can have.


Clicking on one of them shows more options and available parties to make a relationship.

Selecting a party asks you to enter some information; by default, it fills some fields. Title here is the title of this relationship, start and end date are essential and will set the duration of this relationship. This duration should fit the source and target parties' duration; otherwise, you will face an error.

You will face this error if no party or party relationship type is defined.


### Edit and view a relationship
You can edit the relationship by clicking on the edit icon (pencil figure) on the last column of each relationship. Moreover, by clicking on the view icon (eye figure), you are able to see the details of a relationship.




### Delete a relationship
Clicking on the delete icon (trash figure) on the last column of each relationship, you can delete a relationship if the minimum cardinality of its relationship type is preserved.




## Manage Former Members

Former member management allows you to change rights for users no longer active in your project. The feature also allows you to undo the changes. The precondition for using this feature is a specific role in BEXIS, to which you assign all the rights that former members should have.

### Set user to a former member

This feature is available under *Settings > Manage Former Members.

Former member management uses the end date of a user party to find, e.g., users who have not been project members for a certain period of time. By using the end date filter, time-related queries can be made to users. The checkbox in the *is former member column* must be set to set a user as a former member. The system admin and the user will then receive a confirmation email. With the activation of the former member status, all feature and role rights are removed from the user. The user has been added to the former member group.

![formerMembers](https://github.com/BEXIS2/Documents/blob/master/Manuals/SAM/Images/set_former_member.png)


To customize the confirmation email the text blocks of the email can be changed in the SAM settings file. The file is located at "...\Workspace\Modules\SAM". If the subject remains empty, the default subject of BEXIS2 is used.

![formerMembersSettings](https://github.com/BEXIS2/Documents/blob/master/Manuals/SAM/Images/sam_settings.png)


### Revoke the user as a former member

To undo the former member status the checkbox must be deactivated. This means that the former member role will be removed from the user and his previous rights will be activated again. A confirmation email will be sent when the change is made.



## Permission

Permissions contain specific security regulations. The security system of BEXIS2 distinguishes between two types of permissions. The *feature permission* allows or prohibits access to the application's well-defined and delimited area, so-called Features. The *data permission* provides the option to protect all datasets.

### Feature permission

Under *Settings > Manage Feature Permissions*, you can customize feature permissions.

Selecting a checkbox in the navigation tree (e.g., *Search*) will make that feature accessible without authentication (*public access*). **Please use it with care!**

Clicking on a feature name opens a table on the right side. This table contains all subjects (users and groups) and their feature permission status. Using the radio buttons, you may grant or deny permissions for individual users or groups. Permission can be inherited from up-level features if it is not explicitly set (*none*). Inherited permissions are shown in the first column as *effective* permissions.

![features](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/features.png) 

### Entity Permission

To manage access to entities (datasets and publications) go to *Settings > Manage Entity Permissions*.

By selecting a dataset (by clicking on the row), a new table displays all subjects (users and groups) and their different data permission statuses regarding the selected dataset. Here, you can also change permissions for the selected dataset.

Selecting the checkbox in the first column (*IsPublic*) gives the public access to that dataset without any authentication.

![datasets](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/Help_img10.png) 

In general, BEXIS2 distinguishes different data permission types:

* Read: allows to read & download to primary data and attachments
* Update: enables changes (upload and update) of primary data and metadata
* Delete: allows to delete the whole dataset
* Grant: allows to give permission to other users or groups

## Manage datasets

Display the list of datasets under *Settings > Manage Datasets*. In this list, you can see the status of each dataset and do some useful actions to maintain datasets.

There are two ways to delete a dataset (1) *delete* and (2) *purge*.

![maintenance](https://github.com/BEXIS2/Documents/raw/master/Manuals/SAM/Images/Help_img11.png) 

There are two ways to delete a dataset:

*Delete* tags a data record to exclude it from nearly all features of BEXIS2 (e.g., search). But you are still able to restore the data record – if needed.

*Purge* deletes a dataset completely. The data record **can not be restored**.



## Manage Metadata Structure

Metadata structures (schemas or profiles) are typically created and imported by a data manager or administrator of the system. Thus, this import function is available under the Setup > Import Metadata Structure. The wizard will be able to help you in importing your metadata structure into the BEXIS2\. A metadata structure must be defined in an XSD schema file.

When importing a metadata schema, each element of the XSD file(s) is analyzed for its type, name, annotations, attributes, data types, constraints, etc. Based on this information a form is automatically being created. For example, if an element is of data type Date, a date picker UI component will be used in the form. Also, all names and descriptions are used exactly as they are in the XSD file(s).

NOTE: There are metadata standards available for almost any domain or type of data. It is good practice to follow one of them to ensure interoperability later on. However, although technically possible, most standards are very complex and should not be used as a whole. Users would be overwhelmed and may need only a small selection of elements to describe their data. Standards are designed to cover a great range of use cases, and data managers (in collaboration with their community) should make an effort to define a set of feasible metadata elements in a profile (XSD file).

IMPORTANT: Please check whether the XSD schema files have any dependencies on other files. You can find the dependencies in the import or include tags.

![Metadata1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/metadata1.png)

The system requires all referenced files to be locally available on the server (no URL to external resources). So you may need to store all references first in a local folder, change the schema location path in every file (e.g. ./fileName.xsd), and then upload all files to the server. (See section [Push Big File](#_push_big_file)).

![metadata2](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/metadata2.png)

![metadata3](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/metadata3.png) 

Upload a Metadata Structure follows the following steps:

### Select File

In the first step, an existing file containing your data must be selected. You can choose either an XSD file from your local computer or a file that has been uploaded to the server before starting the Wizard. You may use the "Push big data to server" function to upload multiple related XSD files in the Collect menu.

Note: Please upload a valid XSD structure. BEXIS2 does not check this kind of validation.

![Select XSD File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/select_xsd.png) 

### Read Source

Please specify a name (i.e. display name) for the new metadata structure. You may also enter a root node if only a part of the XSD will be used (optional).

![Read XSD File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/read_xsd.png)

To find the root node, open the XSD Schema file and look at the element tags. The example of ABCD looks like this:

![img27](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/metadata4.png)

If no root node is selected, the wizard will automatically select the first element, a complex type. However, it is also possible to define the element "DataSet" as the root node, and the metadata structure starts from this element. The Name of a metadata structure must be unique, and the root node must exist.

### Set Parameters

For the system to handle a dataset, at least the title and a description are needed. In this step, these two elements, typically available in all metadata structures, should be identified and made explicit to the system.

![Set XSD Parameters](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/set_xsd_parameters.png) 

### Summary

The Summary page is an overview of the created metadata structure.

![Summary](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/summary_xsd.png)

## Manage Requests

Requests are used to ask for permission to access a dataset. The request is sent to the dataset owner and in copy to the administrator. The request can be accepted or rejected.