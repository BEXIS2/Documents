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

Click __Create__ in the main menu to start creating a new dataset. You will see a list of dataset types which may include file, observation and publication. Each type is defined by a specific metadata schema, the allowed file types and additional characteristics relevant for this type of data. To choose the most suitableate dataset type for your data, consider the following::

* Read the dataset type description to understand its intended use
* Check the accepted file types. If no file types are listed, you can upload any supported file format supported

To select a dataset type, simply click on it. If you are unsure which dataset type to choose or if your file type is not supported, contact your data curator or adminstrator for guidance.

Note: The screenshots in this manual are taken from the BEXIS2 demo instance. Depending on customizations made by your administrator, the appearance in your local instance may differ slightly.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset01.png" alt="Select an appropriate dataset typ to start creating a dataset" style="border:1px solid #bee1da; padding:10px;">

After selecting a dataset type, a metadata input area will appear either on the right side or below he list. Enter the required metadata (e.g., title, description). Once all mandatory fields are completed, click the "Create and Continue" button to create the dataset.

Once all mandatory fields are completed, click the green plus icon to create the dataset.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset02.png" alt="Fill in the required metadata (e.g., title, description)" style="border:1px solid #bee1da; padding:10px;">


After creation, you are taken to the dataset’s general editing page. From here, you can:

* Edit the metadata
* Upload data
* Select an existing data structure or crate a new data structure


> **Note:** By default, in most BEXIS2 instances, newly created datasets are only visible to you (the author) and to users with editing permissions based on their roles (e.g., co-authors and data curators). o make your dataset visible to other users or publicly accessible see the section on [versioning](../docs/MyData/#dataset-versioning) section.

### Best Practices to Create a Dataset

✅ Select the **dataset type that best matches** your data.   
✅ Provide **clear and meaningful key information**, such as a descriptive title and a concise abstract.



### Dataset Edit Page

The Dataset Edit Page is the central area for managing a dataset. Here you can edit metadata, upload files, define the data structure, add attachments, and create links to other datasets. Depending on the dataset type, some features may not be available.

There are several ways to open the Dataset Edit Page, depending on your workflow:

* __After creating a dataset__: The edit page opens automatically.
* __From My Data__: Find the dataset and click [[!LINK_VIEW]](../docs/General#roles).
* __Via search__:  Search for the dataset, open it by clicking [[!LINK_VIEW]](../docs/General#roles), and switch to edit mode by clicking the **Edit Button** and go to the dataset edit page.
* __From the dataset landing page__: Click the **Edit Button** to switch to edit mode.

The Edit Page gives you access to all options for updating and managing your dataset. Depending on the dataset type, you may see some or all of the following sections:

* __[Metadata](#metadata)__ _(mandatory)_: Click [[!LINK_EDIT]](../docs/General#roles) to add or update the metadata of your dataset.
* __[File upload](#file-upload):__ Upload data files using drag-and-drop or file selection.
* __[Data Structure](#data-structure)__ _(some dataset types)_: Define the variables of your tabular data. Often, the easiest way is to upload your data first so the structure can be created semi-automatically.
* __[Attachments](#attachments)__ _(some dataset types)_: Add supporting files such as documents or images.
* __[Links](#links):__ Connect your dataset to related datasets or publications.

With the __View__ button in the upper right corner, you can switch to the dataset view.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset03_DatasetEditPage.png" alt="The Dataset Edit Page is the central area for managing a dataset. Here you can edit metadata, upload files, define the data structure, add attachments, and create links to other datasets. Depending on the dataset type, some features may not be available." style="border:1px solid #bee1da; padding:10px;">

## Edit Metadata

Metadata are “data about data”. They describe essential information about a dataset — such as who collected the data, when, where, how, and for what purpose. Good metadata provide context (e.g., methods) so that others can correctly interpret, and reuse the data.. Well-structured metadata also make datasets easier to find, understand, and reuse, supporting the FAIR principles.

1. __Open the metadata page:__. There are several ways to open the Metadata Edit Page, depending on your workflow:
There are several ways to access the Metadata Edit Page, depending on your workflow:
    * __From My Data__: Locate your dataset and click [[!LINK_EDIT]](../docs/General#roles).
    * __Via search__:  Search for the dataset, open it via [[!LINK_VIEW]](../docs/General#roles), then switch to edit mode by clicking the **Edit Button**.
    * __From the dataset edit page__: To edit the metadata, click [[!LINK_EDIT]](../docs/General#roles). The metadata form opens in a new window.
    * __From the dataset landing page__: Click [[!LINK_EDIT]](../docs/General#roles) to switch to edit mode.
2. __Fill in your metadata:__. Use the tabs at the top of the form to navigate  through different sections.  Icons in the form help indicate field types and available actions.

    | Icon | Description |
    |------|-------------|
    | ℹ️ | Offers help when filling out the metadata fields; the info-button on the top shows all help texts |
    | <span style="color:red;">*</span> | Indicates mandatory fields |
    | ![info](./35aa291f-fe83-45f0-9363-a1892230bec7.png)  | Opens or closes subsections. |
    | + / - | Adds or deletes an additional field |
    | ▼ / ▲ | Reorders items in a list |
    | ☐ | Subsections are closed by default; ticking opens the subsection |

3. __Provide change message:__ After making edits, scroll to the bottom and briefly describe what you changed. This helps maintain a transparent version history.
4. __Validate metadata__ _(optional)_: Click the __Validation button__ to check whether all mandatory fields are filled in and whether your entries follow the required metadata standard.Missing or invalid information is highlighted in red.
5. __Save or cancel:__ Save your edits or discard them. Saving also triggers validation. After saving, you will be redirected to the dataset landing page.

> **Note:** You can return to the metadata form at any time to update your dataset.

### Best Practices for Metadata

✅ Provide **complete and clear** metadata to increase discoverability, usability, and scientific credit.  
✅ Use a **meaningful title**, a **concise descriptive abstract**, and **clear descriptions of methods and workflows**.  
✅ Ensure terminology,naming, and units are **consistent** across the dataset.  
✅ Add enough context so others (and your future self) can **understand the data without additional explanation**.

## Upload File

There are two options for file upload:

(1) Tabular data: Data can be viewed and filtered directly in BEXIS2. If this option is available, the dataset edit page will include the section [data structure](#data-structure).  
(2) Non-tabluar data (e.g., documents, images, scripts)

### Upload Tabluar Data
1. Open the dataset edit page of your dataset (see [dataset edit page](#dataset-edit-page))
2. Drag and drop your file(s) into the upload box or click the upload icon to select files from your computer. Once uploaded, the files will be listed.
3. Add a description or comment for each file. You can also delete files.
4. To finalize the upload, create or select a [data structure](#data-structure).

> **Note:** All files must share the same data structure. One or more files with identical variables can be uploaded per dataset. These files can be viewed and filtered in BEXIS2.

### Upload Non-Tabluar Data
1. Open the dataset edit page of your dataset (see [dataset edit page](#dataset-edit-page))
2. Drag and drop your file(s) into the upload box or click the upload icon to select files from your computer. Once uploaded, the files will be listed.
3. Add a description or comment for each file. You can also delete files.
4. Delete the file(s), or submit them. You have to confirm the submission.

### Best Practices for File Upload
✅ **Prepare your files** to ensure they have the correct structure before uploading.   
✅ **Provide meaningful comments** for each file to improve reuse.

## Create Data Structure

A Data Structure defines all variables in the data you want to upload. Before uploading your tabluar primary data, you must define the Data Structure. On the Dataset Edit Page, you can create it using the Data Structure drop-down menu. The following options are available:

* __[Structure](#reusing-data-structures):__ Based on an existing Data Structure. Best Practice: Reuse existing Data Structures whenever possible to ensure consistency and save time.
* __[File data](#data-structure-based-on-file):__ Based on the uploaded file. Best Practice: Recommended if you cannot reuse an existing structure. Make sure your file includes variable names, units, and variable description for easier setup.
* __[Options](#create-a-new-structure):__ Create a new Data Structure from scratch.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset05_CreateDataStructure01.png" alt="Before uploading your tabluar primary data, you must define the Data Structure. On the Dataset Edit Page, you can create it using the Data Structure drop-down menu." style="border:1px solid #bee1da; padding:10px;">



### Best Practices for Data Structures

✅ **Reuse first** - Always check if an existing Data Structure fits your dataset.   
✅ Prepare your file and **include variable names, descriptions, and units** in your file for automatic detection.



### Reusing Data Structures

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


### Data Structure Based on File

If you need a new Data Structure, we strongly recommend creating it based on the file you want to upload.

__1. Uploading your file and selecting it for Data Structure creation__
* Upload: [Upload](#file-upload) your file.
* Select for Data Structure: After the file is uploaded, select the uploaded file as the basis for your new Data Structure under Data Structure.
* Automatic analysis: The system will automatically analyze your file's structure. You will be directed to the next page.

__2. Verifying and adjusting file structure information__
* Review pre-filled settings: The system will pre-fill file structure information such as delimiter, decimal separator, text marker, and encoding.
* Verify accuracy: Carefully review these settings to ensure they accurately reflect your file's format.
* Make adjustments: If necessary, modify any of the pre-filled settings to match your file's characteristics.

__3. Handling Missing Values:__
* System default: BEXIS2 has a predefined default Missing Value.
* Administrator modification: An administrator can modify the default Missing Value.
* Customize Missing Values:
    * You can delete the existing Missing Value (bin icon).
    * You can edit the existing Missing Value.
    * You can add additional Missing Values (plus icon).
* Variable-specific Missing Values:
    * If you need different Missing Values for other variables, include this information in your uploaded file and mark the row containing this information.
    * Define these variable-specific Missing Values on the [Data Structure Edit Page](#data-structure-edit-page).
 
> **Note**: The boolean data type does not support Missing Values.

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



![DatasetEditPage](https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset06_CreateDataStructure02.png)

### Create a new structure

There is also the option to create a Data Structure from scratch.

* Access the Dataset Edit Page
* Select "Create New": Select "Create New" from the drop-down list under Data Structure. You will be redirected to the [data structure edit page](#data-structure-edit-page).


### Data Structure Edit Page

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
* __Template__ _(optional, depending on your instance settings)_: Select a [Variable Template](DataDescription.md#variable-template) from the provided list. Templates group related variables by content (e.g., the "temperature" template includes soil, water, and air temperature).  If you create the Data Structure based on a file, BEXIS2 will attempt to select a suitable template automatically.
* __Data Type:__ Select the appropriate [Data Type](DataDescription.md#data-types).
* __Meaning__ _(optional)_: (If available) Select the specific Meaning of the variable. [Meanings](DataDescription.md#meanings) can be modified and created in the Settings.
* __Constraints__ _(optional)_: These may be pre-filled based on the chosen template or meaning. But you can also define [Constraints](DataDescription.md#constraints).
* __Missing Value and description__ _(optional)_: Define how Missing Values are represented and described. If you created the Data Structure based on a file, these fields are pre-filled
* __Primary Key (slider):__ Mark a variable as part of the Primary Key.
* __Make Values optional (slider):__
    * It is strongly recommended to leave this option unchecked for data integrity.
    * Exceptions may include columns containing comments or notes.
    * If unchecked, BEXIS2 will validate during upload that all cells are filled and report any empty cells.
 
> **Note**: The boolean data type does not support Missing Values.

[image]

__Creating a new Data Structure or modifying a Data Structure__

If you create a Data Structure from scratch or if you modify a copy of an existing Data Structure, you also have the following options.
* __Add empty variable:__ use the plus button at the end of the page to add new variables.
* __Copy a variable:__ use the copy button to insert copies of an existing variable. Do not forget to modify the variable name based on the variables in our file.
* __Copy the variable's characteristic to the next variable:__ the xxx button allows you to copy all variable attributes (e.g., description, template, unit) to the following variable in your list. The variable name is not copied.
* __Copy the variable's characteristic to all following variables:__ the xxx button allows you to copy all variable attributes (e.g., description, template, unit) to all following variables in your list. The variable name is not copied.
* __Delete variable:__ use the bin button to delete a variable.


## Attachments

You can upload additional material to a dataset as attachments. To add attachments, drag and drop one or more files into the upload box or click the upload icon to select files from your computer. For each attachment, you can enter a description or comment in the field next to the file. The files are uploaded to the dataset immediately. To remove an attachment, click [[!LINK_DELETE]](../docs/General#roles).

### Best Practices

✅ Choose **meaningful file names** for your attachments.   
✅ Provide a **clear description or comment** for each uploaded attachment. 






## Links
> __Note:__ Links between datasets cannot currently be created on the [Dataset Edit Page](#dataset-edit-page). To add links, open the dataset view and switch to the **Link** tab.

You can link datasets regardless of their type (e.g. dataset, publication). Each link always refers to a specific version of a dataset.

The links page displays:
- **Links to** other datasets (outgoing links)
- **Links from** other datasets to the current one (incoming links)

This makes the direction of each link explicit and clearly defines the source and target. For each link, the table shows the relationship between the datasets and any optional comments.

Because links are version-specific, you can:
- open the linked **referenced version** clicking [[!LINK_VIEW]](../docs/General#roles)
- navigate to the **latest version** of the linked dataset using skip icon

### Best Practices

✅ Link datasets when there is a **clear and meaningful relationship** between them.  
✅ Choose the **appropriate relationship type** to clearly describe how the datasets are connected.  