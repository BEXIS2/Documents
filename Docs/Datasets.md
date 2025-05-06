---
title: "Datasets"
description: "Manage Datasets in the BEXIS2 system"
position: 3
tags: ["javascript", "markdown", "metadata"]
---

# Create & Edit Datasets
>[!ROLE]
>__Role:__ [User](../docs/General/#roles)

## Create a Dataset

To create a new dataset, click on  __Create__ in the main menu. A list of dataset types will be displayed (e.g., file, observation, publications). Each dataset type may have a specific metadata schema, allowed file types, and other characteristics. To choose the most appropriate dataset type for your data:

* __Check its description__
* __Verify the accepted file types:__ If no file types are listed, you can upload any format supported by BEXIS2 (see the complete list here (link will be added))

To select a dataset type, simply click on it. If you're unsure about the best option or your file type is not accepted, please contact your data curator or manager.


![Create dataset I](https://github.com/BEXIS2/Documents/raw/master/Docs/Images/crreate_create_dataset1.png)

After selecting a dataset type, an input area will appear either on the right side or below. Enter the required metadata - such as the title and description - into the appropriate fields. Once all mandatory fields are completed, you can create the dataset by clicking the green plus sign in the bottom-right corner.

![Create dataset II](https://github.com/BEXIS2/Documents/raw/master/Docs/Images/crreate_create_dataset2.png)

This action opens the dataset's general editing page, where you can proceed in several ways:

* Upload data
* Select an existing Data Structure
* Add a new Data Structure
* Edit the metadata

By default, in most BEXIS2 instances, newly created datasets are only visible to you (the author) and users with editing permissions based on their roles - typically co-authors and data managers. For information on how to make your dataset accessible to all users, refer to the [versioning](../docs/MyData/#dataset-versioning) section.


### Dataset Edit Page (user)

The Dataset Edit Page is your workspace for managing and customizing your dataset. It provides tools for editing metadata, uploading files, defining Data Structures, adding attachments, and linking datasets. Use it to ensure your dataset is comprehensive, organized, and ready for sharing. Depending on the chosen dataset type, not all features might be available.

There are several ways to access the Dataset Edit Page, depending on your workflow:

1. __After creating a dataset__: The edit page opens automatically when you create a new dataset.
2. __From the dataset view page__: If you're viewing a dataset, use the edit button to switch to the edit page.
3. __From ‘My Data’__: Locate your dataset under the My Data section, then click the pen icon.
4. __Using search__: If the dataset is at least internally open, search for it, view it, and switch to the edit mode using the toggle (similar to option 2).

The Dataset Edit Page of every dataset includes the following parts, though some features may not be available for a dataset type or in an instance.

1. __[Metadata](#metadata)__ _(mandatory)_: Click on the pencil button to include the dataset's essential information in the metadata.
2. __[File upload](#file-upload):__ Upload your data files into this section by drag and drop or click to select.
3. __Data Structure__ _(some dataset types)_: Define the variables of the tabular data. The easiest way is to create the Data Structure by uploading your data first.
4. __Attachments__ _(some dataset types)_: Add supplementary files to support your dataset.
5. __Link:__ Connect your dataset to others within your instance.

With the __View__ button in the upper right corner, you can switch to the dataset view.

[image]




### Metadata

To edit the metadata, click on the pen icon on the Dataset Edit Page. The metadata form for your dataset will open in a new window.

Use the tabs at the top of the form to navigate the specific sections. Familiarize yourself with the icons and their functions to streamline data entry (icons will be added soon).


[image]


Please remember that you can return to edit the metadata form at any time to make updates. Ensure your metadata is complete and comprehensive, as this improves data discoverability and reuse, and guarantees you receive proper credit for your work.

After editing the metadata, scroll to the end of the form. There, you can provide brief information about your changes in a text box. Additionally, you can validate, save, or cancel your changes.

The validation process checks if all mandatory fields are filled and comply with the metadata standard. Errors and missing content will be highlighted in red. Clicking the Save button also triggers validation. Once your metadata is saved, you will be directed to the view mode.

If you want to update your dataset further (e.g., metadata, data, etc.), click on the button in the upper right corner of the page, and you will be redirected to the Dataset Edit Page.


[image]





### File Upload

To add your data, drag and drop your file(s) to the upload box or click the upload icon to select file(s) from your computer. We distinguish two different options for the file upload.

(1) __Upload and storage of tabular data__: One or more files with identical Data Structures can be uploaded per dataset. The data can be viewed and filtered in BEXIS2. If this option is possible, the edit page will contain the section [data structure](#data-structure).

Once you have uploaded the file(s), they will be listed. You can now add a description or comment to the file, delete the file(s), or submit them as part of your dataset. To upload the file(s), you will need to select a [data structure](#data-structure).


<[image]


(2) __Upload data__ (e.g., images, GIS files) __that are not saved in a tabular structure__ in BEXIS2: Several files can be uploaded. A Data Structure is not needed for this case.

Once you have uploaded the file(s), they will be listed. You can now add a description or comment to the file, delete the file(s), or submit them as part of your dataset. Only after pressing the submit button will the data be part of your dataset.



[image]



### Data Structure

A Data Structure defines all the variables of the data you wish to upload. Before uploading the primary data, the Data Structure must be determined. On the Dataset Edit Page, it can be created via the "Data Structure" drop-down menu. The following options are available:

1. __[Structure](#reusing-data-structures):__ Based on an existing Data Structure. We recommend reusing existing Data Structures whenever possible!
2. __[File data](#data-structure-based-on-file):__ Based on the uploaded file. This option is recommended if you cannot reuse an existing Data Structure.
3. __[Options](#create-a-new-structure):__ Create a new Data Structure.



[image]


After creating the Data Structure, you need to define your variables on the [data structure edit page](#data-structure-edit-page) page if you have chosen option (1) based on an existing Data Structure or (2) based on a file.


#### Reusing Data Structures

The reuse of Data Structures within BEXIS2 ensures consistency and efficiency. This scenario applies, for example, for monitoring data or data from data loggers. Defined Data Structures can and should be reused for recurring data, such as data of a data logger. This data often shares similar structures (e.g., timestamp, sensor readings).

__Method 1: Direct selection of an existing Data Structure__

1. Access the Dataset Edit Page
2. Search and select the Data Structure
* On the edit page, open the dropdown list labeled "Data Structure".
* Begin typing the name of the desired Data Structure.
* Select the correct Data Structure from the list.

__Method 2: Creating a new dataset based on an existing dataset__

1. Access "My Data"
2. Select the source dataset
* Select datasets and view the tab “Own/Edit”
* From the list of datasets, locate the dataset whose Data Structure you want to reuse.
* You only see the dataset where you have permission to edit this dataset (data creator or edit rights).

3. Create a new dataset
* Click on the copy symbol on the right side
* BEXIS2 will automatically create a new dataset based on the copied one
* You will be automatically directed to the Dataset Edit Page for the newly created dataset

4. Customization _(optional)_:
* After the new dataset is created, you can customize metadata (e.g., descriptions) as needed.
* You can also add new data without altering the underlying Data Structure.


#### Data Structure Based on File

If you need a new Data Structure, we strongly recommend creating it based on the file you want to upload.

__1. Uploading your file and selecting it for Data Structure creation__
* Upload: [Upload your file](#file-upload).
* Select for Data Structure: After the file is uploaded, select the uploaded file as the basis for your new Data Structure under Data Structure.
* Automatic analysis: The system will automatically analyze your file's structure. You will be directed to the next page.

__2. Verifying and adjusting file structure information__
* Review pre-filled settings: The system will pre-fill file structure information such as delimiter, decimal separator, text marker, and encoding.
* Verify accuracy: Carefully review these settings to ensure they accurately reflect your file's format.
* Make adjustments: If necessary, modify any of the pre-filled settings to match your file's characteristics.



[image]


__3. Handling Missing Values:__
* System default: BEXIS2 has a predefined default Missing Value.
* Administrator modification: An administrator can modify the default Missing Value.
* Customize Missing Values:
    * You can delete the existing Missing Value (bin icon).
    * You can edit the existing Missing Value.
    * You can add additional Missing Values (plus icon).
* Variable-specific Missing Values:
    * If you need different Missing Values for other variables, include this information in your uploaded file and mark the row containing this information.
    * Define these variable-specific Missing Values on the [data structure edit page](#data-structure-edit-page).

__4. Defining variables:__
* Variable information: Each variable in your data should have a name and a description. Optionally, you can also define a unit and a placeholder for Missing Values.
* Optimize creation: For efficient Data Structure creation, include variable information (description, unit) directly in your uploaded file.
* Row selection:
    * To specify which rows contain variable information (e.g., variable name, description), double-click the corresponding row or click the arrow and select the appropriate button (e.g., variable, unit).
    * At a minimum, you must select the row containing the variable name and the first row of data.
* Reset selection:__ Use the "reset" button to undo any selections.
* Delete and return: To delete the Data Structure and return to the Dataset Edit Page, click the "x" button.

__5. Selecting columns for upload _(optional)___
* Column selection: If you only want to upload specific columns, you can select them.
* Upload filter: Only the selected columns will be uploaded.

__6. Saving the Data Structure:__
* Mandatory information: Ensure you have provided the mandatory information: variable names and the first row of data.
* Save action: Once the mandatory information is provided, the "save" button (floppy disk icon) will be enabled. Click it to save.
* Data Structure Edit Page: After saving, you will be redirected to the [data structure edit page](#data-structure-edit-page).



[image]

#### Create a new structure

There is also the option to create a Data Structure from scratch.

* Access the Dataset Edit Page
* Select "Create New": Select "Create New" from the drop-down list under Data Structure. You will be redirected to the [data structure edit page](#data-structure-edit-page).


#### Data Structure Edit Page

On the Data Structure Edit Page, you define the variables for your data. Whether you choose the "Data Structure Based on File" or "Create a New Structure" is a crucial step in the Data Structure creation process.

The Data Structure Edit Page consists of three main sections:
* General information
* Required actions _(optional)_
* Variables

__1. General information of a Data Structure__
* __Data Structure title:__ provide a meaningful title for your data. This could be based on the dataset ID or the content.
* __Primary key:__ Each table row must contain a unique record. A Primary Key, consisting of one or more columns, serves as a unique identifier. This enables the updating of the dataset.

__2. Section with required actions__
This section lists the actions required to complete the Data Structure if the Data Structure already contains variables. This may include:
* Defining the Primary Key.
* Revising the listed variables. These are variables that are still incomplete or incorrectly defined. You will be directed to the corresponding editing area by clicking on a variable.



[image]

__3. Defining your Variables__

The next step is to define your variables. If you created your Data Structure from a file, some information may already be pre-filled, such as variable name, data type, description, and unit if they were defined in the prior step (LINK).  If your file contains only the variable name, BEXIS2 will attempt to select a suitable template automatically.

 You have the following options to specify your variable. If not mentioned differently, the information is mandatory:
* __Variable name:__ Is given if the Data Structure is created based on a file. Otherwise, it must be entered in the same way as it is in the file you want to upload.
* __Template__ _(optional, depending on your instance settings)_: Select a variable template from the provided list. Templates group relate variables by content (e.g., the "temperature" template includes soil, water, and air temperature).  If you create the Data Structure based on a file, BEXIS2 will attempt to select a suitable template automatically.
* __Data Type:__ Select the appropriate Data Type.
* __Meaning__ _(optional)_: (If available) Select the specific meaning of the variable.
* __Constraints__ _(optional)_: These may be pre-filled based on the chosen template or meaning. But you can also define them.
* __Missing Value and description__ _(optional)_: Define how Missing Values are represented and described. If you created the Data Structure based on a file, these fields are pre-filled
* __Primary Key (slider):__ Mark a variable as part of the Primary Key.
* __Make Values optional (slider):__
    * It is strongly recommended to leave this option unchecked for data integrity.
    * Exceptions may include columns containing comments or notes.
    * If unchecked, BEXIS2 will validate during upload that all cells are filled and report any empty cells.

[image]

__Creating a new Data Structure or modifying a Data Structure__

If you create a Data Structure from scratch or if you modify a copy of an existing Data Structure, you also have the following options.
* __Add empty variable:__ use the plus button at the end of the page to add new variables.
* __Copy a variable:__ use the copy button to insert copies of an existing variable. Do not forget to modify the variable name based on the variables in our file.
* __Copy the variable's characteristic to the next variable:__ the xxx button allows you to copy all variable attributes (e.g., description, template, unit) to the following variable in your list. The variable name is not copied.
* __Copy the variable's characteristic to all following variables:__ the xxx button allows you to copy all variable attributes (e.g., description, template, unit) to all following variables in your list. The variable name is not copied.
* __Delete variable:__ use the bin button to delete a variable.


### Attachments

You can upload additional material to your dataset as an attachment. To add attachments, drag and drop your file(s) into the upload box or click the upload icon to select files from your computer. Enter a description or comment for each attachment in the box behind the file. The files will be uploaded to your dataset immediately. To delete an attachment, click the delete button.



[image]


### Links (optional)

__Note:__ Currently, you can't set links between datasets on the Dataset Edit Page. However, they can be added on the dataset view page in the Link tab.

It is possible to link datasets independently of the dataset type (e.g., dataset, publication). Links always refer to a specific version of a dataset.

The page shows links from the current dataset to another dataset (link to) and links from another dataset to the current dataset (link from). This shows the link's direction and clearly defines the source and target. The table also shows the relationship between the linked dataset and comments (optional).

The links are always between specific versions of datasets. You have the option to view this specific version of the linked dataset (eye button) or the latest version of the linked dataset (... button).



[image]
