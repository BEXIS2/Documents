# Data Dissemination & Mapping

<!-- TOC -->

- [A: Overview](#a-overview)

- [B: Manual for users](#b-manual-for-users)
	- [1 Metadata Export](#1-metadata-export)
	- [2. Publishing a Dataset](#2-publishing-a-dataset)
		- [2.1 Publish](#21-publish)
		- [2.2 GFBIO](#22-gfbio)
- [C: Manual for administrators](#c-manual-for-administrators)

- [1 Mapping tool](#1-mapping-tool)
	- [1.1 Mapping Overview](#11-mapping-overview)
	- [1.2 Mapping Examples](#12-mapping-examples)
	- [1.3 Create a mapping](#13-create-a-mapping)
	- [1.4 Key overview](#14-key-overview)

<!-- /TOC -->

## A: Overview
There are different ways to extract, publish or export data from the system. One option is to export the metadata of several datasets for further local analysis or processing. Datasets can also directly be published to other repositories. Therefore it is necessary to map elements between different schemas, party types or the system values. A mapping tool provides a graphical interface to create these relations.

## B: Manual for users
### 1 Metadata Export
"Export Metadata" (*Settings > Export Metadata*) provides a tool to export metadata to a standard compliant XML file. For every metadata structure in the system, there is one tab in the tab strip. The data grid in each tab shows all datasets belonging to the selected metadata structure. Select one or more checkboxes for datasets you would like to export. Clicking on the Export button creates the metadata XML files and provides in-line download links.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/help_img1.png)

### 2 Publishing a Dataset 
Datasets can be published based on the current version of a dataset if the metadata is valid. Currently, there are two brokers and three data repositories available.

*   Brokers:
    *   GFBIO
    *   Pensoft
*   Data Repositories:
    *   GFBIO – Collections
    *   Pangaea
    *   Pensoft (GBIF metadata structure required)

*Please, note this tool might be deactivated or not accessible for users within your BEXIS instance.*

#### 2.1 Publish
Publish a dataset is available through the *Publish* tab on the dataset view.

All available data centers are listed in a dropdown. After selecting a data center, the system tries to convert the data and the metadata as defined in the submissionConfig.xml. This file has to be configured by the system administrator and includes a mapping between the source XML schema and the target schema. If something fails, a warning message will be displayed.

Possible failures:
-  The system is not able to convert the data. Please contact your system administrator. 

![img3](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/publish.png)


### 2.2 GFBIO

Via the GFBIO portal, you can start a submission and publish your dataset. There are different main Types. Choose one, which fits best with your data.

*   Pangaea
*   Collections
*   ENA

Each data repository has different data requirements. BEXIS2 offers an export for Pangea and Collections.

The data for the collections are stored in a zip file and includes:

1.  Schema - XSD Schema for the metadata
2.  Data.*** - Primary Data
3.  Data structure - Structure of the primary data
4.  Manifest File - General information’s about the Dataset
5.  Metadata - Metadata information’s about the dataset

For the Pangea, the metadata and primary data are stored in a text file.

## C: Manual for administrators

### 1 Mapping tool

The mapping tool in BEXIS2 provides the predefined keys and party types for the metadata structures, which are created in the system.

*   Keys are attributes such as title or description.
*   Party types are defined objects such as persons, institutes, organization or workshops.

for more information about party types see the manual about parties.

Mapping a metadata structure hast two main advantages:

1.  While publishing a dataset, BEXIS2 retrieve information from the metadata. The more keys and party types in the system defined, the better the information can be prepared for publication.
2.  In the BEXIS2 there are party types like people, project, etc.

    In the metadata form, according to the mapping, appropriate results are suggested. If a user encapsulates a person in the metadata form, all matching persons are made available for selection. This simplifies the input of metadata. The following image shows autocomplete for the fild of project title.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/mapping_tool2.png)


#### 1.1 Mapping Overview

The "Mapping tool" is accessible through the *Settings -> Manage Metadata Structure* view by clicking on the arrow buttons. Mapping could be defined to or from the system.

The page of Metadata Structure Mapping is divided into 3 sections. The source is displayed on the left and the target on the right side. All created mappings are displayed in the middle.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/mapping.png)

Source and target on the left and right side include two parts: simple and complex blocks. First name, last name or full name of a person are examples of simple elements. A complex element could be a person. A search box is provided for each side (source or target) separately.

Mappings are connections between the source and the target. There are different connection possibilities between the simple attributes. Generally, only the connection between the two simple attributes is considered.

With the help of a transformation rule, it is possible to cover a wide range of different cases. A transformation rule consists of a [RegEx](https://msdn.microsoft.com/de-de/library/az24scfc(v=vs.110).aspx) and a mask. With an example, you can check the values and the expected result.

#### 1.2 Mapping Examples

Here are some examples of a one to one, one to many and many to one mapping.

**Example: One to One**

This example creates a connection between two titles. All words are separated by a RegEx and then arranged differently via the mask.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/one_to_one.png)

**EXAMPLE: One to Many**

This example creates a connection between a name on one side and the FirstName and the LastName on the other side. In the transformation rule, the first and last names are separated from each other by a RegEx and then positioned in the mask via the variable.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/one_to_many.png)

**EXAMPLE: Many to One**

This example creates a connection between the FirstName and LastName by a name. Here is no RegEx needed, but the mask ordered from both variables.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/many_to_one.png)

#### 1.3 Create a mapping

1.  Choose a simple or complex element from the source.
2.  Add an element to the middle section by clicking the orange arrow next to the element.
3.  Choose a simple or complex element from the target.
4.  Create the mapping by clicking on the create button.
5.  All available simple elements are listed in the mapping container for this mapping. Draw a line by clicking on one simple element from the source side and drag it to a simple element on the target side.
6.  If needed, add RegEx and mask to the transformation rule.
7.  Press on the save button after entering values in the blocks.

#### 1.4 Key overview

![key_overview](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/key_overview.PNG)



[Go to top](#a-overview)
