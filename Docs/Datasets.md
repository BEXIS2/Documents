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


> **Note:** By default, in most BEXIS2 instances, newly created datasets are only visible to you (the author) and to users with editing permissions based on their roles (e.g., co-authors and data curators). To make your dataset visible to other users or publicly accessible see the section on [Versioning](../docs/MyData/#dataset-versioning) section.

### Best Practices to Create a Dataset

✅ Select the **dataset type that best matches** your data.   
✅ Provide **clear and meaningful key information**, such as a descriptive title and a concise abstract.



### Dataset Edit Page

The Dataset Edit Page is the central area for managing a dataset. Here you can edit metadata, upload and manage data files, define the data structure, and add attachments. Depending on the dataset type, some options may not be available.

#### How to Open the Dataset Edit Page
You can access the Dataset Edit Page in several ways, depending on your workflow:

* __After creating a dataset__: The Dataset Edit Page opens automatically.
* __From My Data__: Find the dataset and click [[!LINK_VIEW]](../docs/General#roles).
* __Via the Search__:  Search for the dataset in the Search menu, open it using [[!LINK_VIEW]](../docs/General#roles), then click the **Edit** button to switch to Dataset Edit Page.

> **Note:** Newly created datasets may not appear in search results immediately. In this case, open My data and request a dataset release by clicking the release tab (see [Versioning](../docs/MyData/#dataset-versioning)).

#### Available Sections on the Dataset Edit Page

The Dataset Edit Page provides access to all options for updating and managing your dataset. Depending on the dataset type, you may see some or all of the following sections:

* __[Metadata](#metadata)__: Click [[!LINK_EDIT]](../docs/General#roles) to add or update the dataset metadata.
* __[File upload](#file-upload):__ Upload data files using drag-and-drop or file selection.
* __[Data Structure](#data-structure)__: Define the variables of your tabular data. In many cases, uploading the data file first allows the data structure to be created semi-automatically.
* __Data__: A preview of the uploaded data table is displayed here.
* __[Attachments](#attachments)__: Add supplementary files such as documents, images, or additional material.

Use the __View__ button in the upper right corner to switch from edit mode to the dataset view.

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
3. Add a description for each file. You can also delete files.
4. Create or select a [data structure](#data-structure) for your file.
5. Once the Data Structure is validated, you can submit your file by clicking the **Submit button**. Variables that cannot be validated are highlighted in **red** and accompanied by an error message. Expand the message panel to read the full details and upaded the variable definition by adding the data structure.

> **Note:** All files must share the same data structure. One or more files with identical variables can be uploaded per dataset. These files can be viewed and filtered in BEXIS2.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset07_DataUpload.png"
     alt="Validation of data and datastructure" style="border:1px solid #bee1da; padding:10px;">

### Upload Non-Tabluar Data
1. Open the dataset edit page of your dataset (see [dataset edit page](#dataset-edit-page))
2. Drag and drop your file(s) into the upload box or click the upload icon to select files from your computer. Once uploaded, the files will be listed.
3. Add a description for each file. You can also delete files.
4. Delete the file(s), or submit them. You have to confirm the submission.

### Best Practices for File Upload
✅ **Prepare your files** to ensure they have the correct structure before uploading.   
✅ **Provide meaningful comments** for each file to improve reuse.

## Create Data Structure


A Data Structure defines all variables of the data you want to upload (e.g. names, data types, units, missing values). Before you can upload **tabular primary data**, a Data Structure must be defined.

You can create or assign a Data Structure on the [dataset edit page](#dataset-edit-page) using the Data Structure drop-down menu. The following options are available:

- **[Reuse an existing structure](#reusing-data-structures)**: Use an already defined Data Structure. **Best practice:** Reuse existing Data Structures whenever possible to ensure consistency and save time.
- **[Based on a file](#data-structure-based-on-a-file)**: Create a Data Structure from an uploaded file.  
  **Best practice:** Recommended if no suitable structure exists. Prepare your file with variable names, units, and descriptions for easier setup.
- **[Create from scratch](#create-a-new-structure-from-scratch)**: Manually define a new Data Structure.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset05_CreateDataStructure01.png" alt="Create a Data Structure on the Dataset Edit Page using the Data Structure drop-down menu." style="border:1px solid #bee1da; padding:10px;">


### Best Practices for Data Structures

✅ **Reuse first** - Check whether an existing Data Structure already fits your data.   
✅ **Prepare your file** – Include variable names, descriptions, and units to enable automatic detection.

---

### Reusing Data Structures

Reusing Data Structures in BEXIS2 improves consistency and efficiency. This is especially useful for **recurring or monitoring data**, such as measurements from data loggers, where datasets often share the same structure (e.g. timestamp, sensor values).


__Option 1: Direct selection of an existing Data Structure__

1. Open the [dataset edit page](#dataset-edit-page)
2. Open the **Data Structure** drop-down list and select the appropriate Data Structure. *Tip*: Start typing the name of the Data Structure to filter the list and find it faster.


__Option 2: Creating a new dataset based on an existing dataset__

1. Go to [my data](#MyData.md/) and select a dataset under [my datasets](#MyData.md/my-datasets) in the *Edit* or *Own* tab.
2. Click the **copy** icon on the right side. BEXIS2 creates a new dataset based on the selected one and redirects you to the [dataset edit page](#dataset-edit-page), where you can adjust metadata (e.g. title or description) as needed.


### Data Structure Based on a File

If you need a new Data Structure, we strongly recommend creating it **based on the file you want to upload**.

#### 1. Uploading your file and selecting it for Data Structure creation
-  Upload your file via [Upload](#file-upload).
- Select the uploaded file as the basis for the Data Structure. BEXIS2 automatically analyzes the file and forwards you to the next step.
  

#### 2. Verifying and adjusting file structure information
- Verify automatically detected settings for delimiter, decimal separator, text marker, and encoding. Adjust these settings if necessary.

#### 3. Handling Missing Values:
- System default: BEXIS2 uses a predefined default missing value (commonly `na`). Administrators can change this [default missing value](#configuration.md/#data-structure) in the configuration, so it may differ in your instances.
- Global missing values: You can edit or remove ([[!LINK_Delete]](../docs/General#roles)) predefined missing values and add additional ones (plus icon). These apply to all variables of your file.
    * Variable-specific missing values: If variables require specific missing values, either include them in your file and mark the corresponding row or define them later on the [data structure edit page](#data-structure-edit-page).
 
> **Note**: The boolean data type does not support Missing Values.

#### 4. Defining variables
- Mandatory selection: Select the row containing the **variable names** and the row containing the **first data record**. These two selections are required to continue. 
- How to select: Select a row by clicking on `>` or double-click on the row  and select the appropriate content (e.g., variable, unit) by clicking on the corresponding button. Use the "reset" button to undo any selections.
- Optional variable information: Each variable should have a description and may also include a unit and a placeholder value. For faster and more accurate setup, include this information directly in your uploaded file and assign the corresponding rows.
   * Delete and return: To discard the Data Structure and return to the Dataset Edit Page, click `×`.

#### 5. Selecting columns or rows for upload _(optional)_
* You may limit the upload to specific columns or rows. Only selected data will be imported.

#### 6. Saving the Data Structure:__
* Once all mandatory information is provided, ([[!LINK_SAVE]](../docs/General#roles)) button becomes active. Click it to store the Data Structure.
* You will be redirected to the [data structure edit page](#data-structure-edit-page).



<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset06_CreateDataStructure02.png"
     alt="Data Structure creation – variable definition step" style="border:1px solid #bee1da; padding:10px;">


#### Best Practices for Data Structures
✅ **Review detected settings** for file structure and missing values carefully.  
✅ **Prepare files in advance** to minimize manual addtions.



### Create a New Structure from Scratch

You can also create a Data Structure manually.

1. Open the [dataset edit page](#dataset-edit-page).
2. In the **Data Structure** drop-down list, select **Create New**. You will be redirected to the [data structure edit page](#data-structure-edit-page), where you can define all variables manually.

---
### Data Structure Edit Page

On the **Data Structure Edit Page**, you define and manage the variables of your dataset. Regardless of whether you created the Data Structure [based on a file](#data-structure-based-on-a-file) or [from scratch](#create-a-new-structure-from-scratch), this page is the next step in the Data Structure creation process.


The page is divided into three main sections:
- **General information** (title and description)
- **Required actions** *(optional)*
- **Variable definitions** (detailed list of variables)

#### 1. General information
* **Title and description:** Provide a meaningful title and a short description of the Data Structure. This can be based on the dataset ID and/or the dataset content.


#### 2. Section with required actions__
This section highlights actions that must be completed before the Data Structure can be saved and used. It is shown when variables are already present and may include:
- **Define a primary key:** Each row must be uniquely identifiable. A primary key consists of one or more variables and is required to enable dataset updates.
- **Complete incomplete variables:** Variables with missing or invalid definitions are listed. Click the variable name to jump directly to it.
* **Darwin Core validation (optional):** If you plan to publish species data to GBIF, you can validate whether your Data Structure meets the requirements for a Darwin Core Occurrence dataset or extensions (e.g., Taxon, EMoF, Humboldt).


<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset06_CreateDataStructure03.png"
     alt="Data structure edit page – general information and requiered action section" style="border:1px solid #bee1da; padding:10px;">

#### 3. Defining your variables

In this step, you define the variables of your Data Structure. If the Data Structure was [created from a file](#data-structure-based-on-a-file), some information (e.g. variable name, data type, description, unit) may already be pre-filled. If only variable names are available, BEXIS2 attempts to select suitable defaults automatically.


The following settings are available. Unless stated otherwise, they are mandatory:
- **Variable name:**  Automatically set when created from a file; otherwise, enter it exactly as it appears in the upload file.
- **Template** _(optional, instance-dependent)_: Select a [Variable Template](DataDescription.md#variable-template) to group variables by content (e.g., temperature, mass). When creating from a file, BEXIS2 may preselect a suitable template.
- **Data type:** Choose the appropriate [Data Type](DataDescription.md#data-types). When possible, this is detected automatically.
**Meaning** _(optional, instance-dependent)_: Specify the semantic meaning of the variable, if available. [Meanings](DataDescription.md#meanings) are managed in the system settings, usually by an administrator.
- **Constraints** _(optional)_: These may be pre-filled based on the chosen template or meaning. But you can also define constraints. Accee my be limited. If you can not access [manage constraints](DataDescription.md#constraints) please contact your administrator and ask for assistance. 
- **Missing values** _(optional)_:   Define how missing values are represented and described. When created from a file, these values are pre-filled but can be adjusted.
- **Primary Key (toggle):** ark the variable as part of the primary key.
- **Make values optional (toggle):**   It is recommended to keep this disabled to ensure data integrity. Enable it only for variables such as comments or notes. If disabled, BEXIS2 validates that all cells are filled during upload.
- **Variable actions (icons):** Icons next to each variable allow you to:
    - copy the whole variale description except the name to the next variable
    - copy the whole variale description except the name to all following variables
    - copy the variable. A copy of the variable will be inserted after the varibale with the action
    - delete the variable
    - move the variable up and down
- **Add variable:** Use the **plus** button at the end of the list to add an empty variable.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/CreateDataset06_CreateDataStructure04.png"
     alt="Data structure edit page – Defining a variable" style="border:1px solid #bee1da; padding:10px;">

> **Note**: The boolean data type does not support Missing Values.

### Best Practices for the Data Structure Edit Page

✅ Select a **primary key that uniquely identifies each record** and is unlikely to change (e.g. timestamp + station ID). This is essential for updating datasets.
✅ **Avoid empty cells.** Required values improve data completeness and validation.
✅ Always **check pre-filled information** (data types, units, missing values) and adjust it if necessary.
✅ **Use existing variable templates** whenever possible to ensure consistency across datasets and reduce manual work.
✅ Provide **meaningful descriptions, correct data types, and appropriate units**. Well-defined variables improve data quality and reusability.

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