# Data Collection: Metadata and Data


<!-- TOC -->

- [Data Collection: Metadata and Data](#data-collection-metadata-and-data)
	- [A: Overview](#a-overview)
	- [B: Manual for users](#b-manual-for-users)
		- [1 Create Dataset](#1-create-dataset)
			- [1.1 Metadata](#11-metadata)
			- [1.2 Dataset links](#12-dataset-links)
				- [Link via Metadata](#link-via-metadata)
				- [Direct links](#direct-links)
		- [2 Upload data](#2-upload-data)
			- [2.1 File upload](#21-file-upload)
			- [2.2 Tabular data import: Data Structure \& Validation](#22-tabular-data-import-data-structure--validation)
	- [C: Manual for administrators](#c-manual-for-administrators)
		- [1 Manage Metadata Structure](#1-manage-metadata-structure)
			- [1.1 Select File](#11-select-file)
			- [1.2 Read Source](#12-read-source)
			- [1.3 Set Parameters](#13-set-parameters)
			- [1.4 Summary](#14-summary)
		- [2 Configure dataset links](#2-configure-dataset-links)

<!-- /TOC -->

## A: Overview

The *Data Collection Module* provides tools to create new datasets consisting of metadata and data. The metadata is based on a schema defined by a metadata structure. The primary data can be tabular (structured) or files. They are described by a data structure which describes the variables and units of tabular data.

## B: Manual for users
### 1 Create Dataset

To create a new dataset, use the “Create” button on the main menu on top.

In the next step, the general type of your dataset needs to be selected. Check the description and allowed file types to choose the type that fits most. If you need clarification, contact your data curator/manager. Different metadata schemas or allowed file types are associated with each type and the (de)activation of specific features.

![Select Entity Type](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/Select_Entity_Type.png) 

After selecting a type, you will be asked for a few main metadata entries, e.g., the title of your dataset. You can improve it later, but please avoid dummy entries like “test” or “my data” here.

Once you click save, you will be forwarded to your new dataset's main edit page. The page is split into several sections (Metadata, File Upload, …).

![Edit Dataset](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/Edit_Dataset.png) 


#### 1.1 Metadata

Click on the pen icon to edit the metadata.

Only datasets with complete and comprehensive metadata qualify, e.g., for DOIs, and can be set publicly available. The better you describe your data, the better it can also be found and used by other researchers.

You can use the tabs on top of the page to navigate through the sections of the form. Fields marked with a red asterisk are mandatory. You can come back to edit this form at any time.

The content area is where you enter metadata describing your dataset. The forms provided here may look different and contain different attributes depending on the metadata schema (structure) you have chosen in the first step.

![Required](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/red_star.png)           Required attributes

![Add](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/plus.png)        Add an attribute

![Mines](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/mines.png)        Remove an attribute

![Up Down](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/up_down.png)  Change order of the attribute

![Expand](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/expand.png)![Collapse](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/collapse.png)      Expand / collapse

![Help](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/help.png)   	Show help information. The button on the right top hides / shows all help information.

![Create Dataset Metadata](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/Create%20Dataset%20Metadata.png) 

Once you are done, click the “Save” button at the bottom of the page. Alternatively, you can click the “Validate” button before to check whether all the required fields are filled in - the missing fields will be highlighted in red.

After saving, you can view your metadata and data in your dataset’s page. If you need to keep working on your dataset (e.g., to edit metadata or to upload files), activate the slider on the upper right corner of the page. You, and you will be redirected to the edit page of the dataset. At any point you wish to view your dataset (e.g., to check the metadata page, files, or attachments uploaded), activate the switch in the Edit page.


#### 1.2 Dataset links
It is possible to create relations between different datasets of one type or different types of datasets (e.g. dataset and publication). Links always refer to a specific version of a dataset. Dataset links are shown under *Links* and divided into *Links to* the dataset and *Links from* the dataset. This shows the direction of the link and clearly defines what is source and target, which might be relevant related to the type of the selected reference (e.g. parent, child ...).

There are two options to create relations / links between datasets:

##### Link via Metadata
Fields in the metadata form can contain lists of datasets stored within the system. If one is selected also a link in both directions based on the most current versions is created.

##### Direct links
Links can also be created directly under *Link > Create link*. Here you can also choose  which version you like to refer to and what kind of link it is. In addition, you can also give more details to it.

![Create links](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/create_links.png) 

### 2 Upload data

To add your data, drag or select your file(s). This is independent if you will only upload or import (tabular data only) your data. If tabular data import is generally possible, the section “Data Structure” (see …) will be shown (see Fig. XX). If not, only the file upload is visible and possible.


![File Upload](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/File_Upload.png) 


#### 2.1 File upload
A short description should be added at least for all file uploads (Fig. 6). Once you confirm the list of files you want to upload (“submit”), the files are added to the system (Note: NOT before!). You can view them under  ….


#### 2.2 Tabular data import: Data Structure & Validation
After adding your data (drag or select your file(s)), specify the related data structure on top. The system currently only supports reading from .csv files. Depending on the system configuration, you have up to 3 options:

 - Select an existing data structure
 - Create a new data structure based on your uploaded file
 - _Create a new data structure manually (currently not recommended due to missing na config options)_

Once a data structure is attached/created, it will be used for validation against the uploaded file(s). Expand the items to see more details. With every change (data or data structure), validation is repeated to show the new result (see example in Fig. ..).

__Select an existing data structure__

Create a new data structure based on your uploaded file
If no data structure exists for your data, this is the recommended way to create a new one.

The system will analyze your file structure (“File reader information”). If the data in your table looks fine, all parameters are detected correctly. If not, you can select other options until it looks fine.

At least select the rows with your variable name, and the first line of your data section starts following the instructions on the right. If available, you can also mark the row with your description, units, or missing value. Missing values can differ for each parameter, but it is often enough to define globally on top. You can define as many placeholders for missing values as you need.

Please note only the first ten rows are shown.

Once all mandatory information is provided, the save button (floppy disc icon) will be enabled, and in the next step, the data structure can be completed.

Data types are detected automatically (based on a subset). Please check and adjust if it does not fit. You will be also asked in case of date fields for the used display pattern.

Based on the provided information (name, units, …) the system tries to match known templates and meanings. Note: This can be wrong! Please check carefully and correct it!

Finally, let the system know about the variable(s) that identify each row and can be used as a key (“primary key”).

## C: Manual for administrators

### 1 Manage Metadata Structure

Metadata structures (also called schemas or profiles) are typically created and imported by a data manager or administrator of the system. Thus this import function is available under the Setup > Import metadata Structure. The wizard will assist you in importing your metadata structure into the BEXIS2\. A metadata structure must be defined in a XSD schema file.

When importing a metadata schema into BEXIS2, each element of the XSD file(s) is analyzed for its type, name, annotations, attributes, data types, constraints etc. Based on this information a form is automatically being created. For example, if an element is of data type Date, a date picker UI component will be used in the form. Also all names and descriptions are used exactly as they are in the XSD file(s).

NOTE: There are metadata standards available for almost any domain or type of data. It is good practice to follow one of them in order to ensure interoperability later on. However, although technical possible, most standards are very complex and should not be used as a whole. Users would just be overwhelmed and may need only a small selection of elements to describe their data. Standards are designed to cover a great range of use cases and data managers (in collaboration with their community) should make the effort in defining a set of feasible metadata elements in a profile (XSD file).

IMPORTANT: Please check, whether the XSD schema files have any dependencies to other files. You can find the dependencies in the import or include tags.

![Metadata1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/metadata1.png)

The current BEXIS2 system requires all referenced files to be locally available on the server (no URL to external resource). So you may need to store all references first to a local folder, change the schema location path in every file (e.g. ./fileName.xsd) and then upload all files to the server. (See section [Push Big File](#_push_big_file)).

![metadata2](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/metadata2.png)

![metadata3](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/metadata3.png) 

Upload a Metadata Structure follows the following steps:

#### 1.1 Select File

In the first step an existing file containing your data needs to be selected. You can either select a XSD file from your local computer or a file that has been uploaded to the server prior to starting the Wizard. You may use the "Push big data to server" function in the Collect menu to upload multiple related XSD files.

Note: Please upload a valid XSD structure. BEXIS2 does not check this kind of validation.

![Select XSD File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/select_xsd.png) 

#### 1.2 Read Source

Please specify a name (i.e. display name) for the new metadata structure. You may also enter a root node if only a part of the XSD is to be used (optional).

![Read XSD File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/read_xsd.png)

To find the root node open the XSD Schema file and have a look on the element tags. In the example of ABCD it looks like this.

![img27](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/metadata4.png)

If no root node is selected then the wizard will automatically select the first element which is a complex type. But it is also possible to define the element "DataSet" as root node and the metadata structure starts from this element. The Name of a metadata structure must be unique and the root node must exist.

#### 1.3 Set Parameters

For the system to handle a dataset at least the title and a description is needed. In this step these two elements, which are typically available in all metadata structures, should be identified and made explicit to the system.

![Set XSD Parameters](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/set_xsd_parameters.png) 

#### 1.4 Summary

The Summary page is an overview about the created metadata structure.

![Summary](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/summary_xsd.png)

### 2 Configure dataset links
The reference types and descriptons can be configured under *Workspace/Modules/DCM/EntityReferenceConfig.Xml*. If the system contains also other entity types, which should be not allowed for linking, you can define a whitelist of shown datasets types.

```XML
<config>
<referenceTypes>
    <referenceType description="">collection</referenceType>
    <referenceType description="">based on</referenceType>
    <referenceType description="">child of</referenceType>
    <referenceType description="">parent of</referenceType>
    <referenceType description="">link</referenceType>
</referenceTypes>
<!--Whitelist for entity types. Please configure, if you need to hide entities from the list
<entityTypes>
    <entityType description="">Dataset</entityType>
</entityTypes>-->
</config>

```






[Go to top](#_overview)
