# Search UI, Data Discovery Module

<!-- TOC -->
- [A: Overview](#a-overview)

- [B: Manual for users](#b-manual-for-users)
	- [1 Search UI](#1-search-ui)
		- [1.1 Categories](#11-categories)
		- [1.2 Properties](#12-properties)
		- [1.3 Free text search with Autocomplete](#13-free-text-search-with-autocomplete)
		- [1.4 Selected Filter](#14-selected-filter)
		- [1.5 Results](#15-results)
	- [2 Dataset Components](#2-data-components)
		- [2.1 Metadata](#21-metadata)
		- [2.2 Primary Data](#22-primary-data)
		- [2.3 Data Structure](#23-data-structure)
		- [2.4 Links](#24-links)
		- [2.5 Dataset Permissions](#25-dataset-permissions)
		- [2.6 Publish a Dataset Version](#26-publish-a-dataset-version)
		- [2.7 Attachments](#27-attachments)	
	- [3 Dashboard](#3-dashboard)
		- [3.1 My Datasets](#31-my-datasets)
		- [3.2 My Requests](#32-my-requests)
		- [3.3 Decision](#33-decision)

- [C: Manual for administrators](#c-manual-for-administrators)
	- [1 Search Manager](#1-search-manager)
	- [2 Dataset tabs display](#2-dataset-tabs-display)
	

<!-- /TOC -->

## B: Manual for users

### 1 Search UI

Search UI contains some parts to make search easier. In this way, you are able to look for all details of datasets, but not for the uploaded data. You can control the search UI via search manager explained in section 3.


![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/searchui.png)

#### 1.1 Categories 
Categories are defined by number 1 in the image above. The main nodes like _Project Name_ are based on nodes in the metadata. The elements are values in the metadata from a main node and can be used to restrict the current selection. The numbers next to the elements and main nodes show the number of existing data sets in the database. This list changes according to the current selection. After selection the results and the facets updated. With the “more” button it is possible to select more than one element at the same time.

#### 1.2 Properties 
Number 2 in the image above is related with properties. In this section there are predefined UI Components like dropdown, radio button or slider to filter the data. There is only one possible choice for every component. After selection the results and the facets are updated accordingly. 

#### 1.3 Free text search with Autocomplete
The free text search, number 3 in the image above, works as in any common search engine. It includes Autocomplete where words or phrases are being predicted once three letters or figures are entered. It supports also different languages.

#### 1.4 Selected Filter
You can find selected filter part by number 4 in the image above. Every filter applied from section 1.1-1.3 is displayed here. Filters can be deselected just by clicking on it. In point 1 by the categories you are able to select more than one option to a category. If there are more than 2 you will see only the category. Click on the category and a window will open to define your selection for this category.

#### 1.5 Results
The matching results are displayed in a table or in the list view. It marks by number 5 in the image above. Basic functions like sorting, filtering, paging are available in the table header. By right clicking on the header, you can change visibility of columns.
The details button opens the detailed view of the selected dataset.

---

### 2 Dataset Components
Datasets in BEXIS consist of the following components: Metadata, Primary data, Data structure, Links, and Attachments. Depending on access rights for a dataset (e.g., guest, member, owner), you are authorized to view some or all components of a data record. If you have no access rights to a component, the tab of this element is grey or not visible.

#### 2.1 Metadata
The metadata contains all necessary information about a dataset (e.g., title, owner, contact, methods, or keywords). The metadata can be downloaded as HTML or XML.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/metadata.png)

#### 2.2 Primary Data
Tabular data is displayed as a table in the *primary data* tab. It is possible to sort the data by clicking on the variable name and filter the data using the funnel button next to the variable. It is possible to download the complete data or a subset in different formats (excel, comma-separated as a csv file, or tab-separated as txt or tsv file).

For non-tabular data such as GIS-files, images, or documents, the content of the primary data tab is shown as a list of all files.


![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/primarydata.png)

#### 2.3 Data Structure
The data structure provides information about primary data. For non-tabular data, it shows the file type. For tabular data, the data structure (or data dictionary) describes the variables (e.g., name, description, unit).

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/structure.png)

#### 2.4 Links
The links section gives an overview of related datasets and their relationship to each other.

#### 2.5 Dataset Permissions
The dataset permission section allows to view and assign edit and download permissions for a dataset.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/datapermissions.png)

#### 2.6 Publish a Dataset Version
On this tab you are able to publish the latest version of your dataset. In this Version a Zip file will be generated and prepared for download for a specific defined datacenter. More information can be found in the data dissemination manual.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/publish.png)


#### 2.7 Attachments
Under this tab, all attachments of the dataset are listed and can be downloaded.


![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/attachments.png)


### 3 Dashboard
#### 3.1 My Datasets
Overview on all datasets the currently logged in user has access. Datasets are groups by permission: Own (full permission including granting permission), Edit, and download.
Datasets marked in red have incomplete metadata.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/dashboard.png)


#### 3.2 My Requests
List of all your pending and answered requests for data access permissions. Pending requests can be withdrawn/delete, if the request is not anymore valid.
![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/Requests.png)

 
#### 3.3 Decision
List of all answered and pending requests related to your datasets. You can accept (hook) or reject (minus) pending requests. The requesting person will be informed via email about your decision. 

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/decision.png)

## C: Manual for administrators

### 1 Search Manager
With the help of the search manager, you can make search UI more operative. This part is available from **Setup > Manage search**. 
You need to click on the Refresh Search button, to make the search result effective.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/searchManager.png)

To add a new search component, click on the Create Search Attribute button. The configuration files consist of one element – the field element, and several attributes. The element represent each lucene field and its attribute are used to configure indexing, searching, and display. Take mouse over each question mark near by a field and you can see the help information.

You can use the buttons for edit and delete a search component. 

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/searchattribute.png)


We, therefore, go through each of the elements attributes of the configuration file.

**Display Name:** This is the name which is displayed in the search UI for the field.

**Source Name:** This is the name of the field in the lucene index.

**Metadata Node:**  Add one or more xpaths from the metadata elements to be mapped against the lucene field.

**Header Item:** 	Tick if this item should be available as a category (e.g. as a grid column).

**Default Header Item:** The header item is be visible upon page load.

**Search Component Type:** This specifies the search pattern that will be should be used against this field (as discussed in the introduction). 
Therefore, the value of this attribute can be any of “Category” for creating a category-based search field, “Facet” for creating faceted search field, “Property” for creating a property search field, and “General” which creates an indexed field which is not displayed in the UI, but however, searched.

**Data Type:** This specifies the primitive data type of the value to be indexed. E.g. string, integer, double, date.

**Store:** This specifies if the field value should be stored. If the field is not stored, you can only search against the terms in the field, however, you cannot retrieve the value. For minimal display of the search result, it is recommended that some fields be store. This value of the store attribute can be either yes or no.

**Multi Value:** This specifies if there are several values of a metadata element in a given field. E.g. if a dataset can have several owners in a metadata, then, the owners field in the index in this case, will be multi-valued
Analyzed: This specifies if the field should be analyzed or not. Only analyzed field can be searched.

**Norm:** This can have a value of yes or no and it is used to specify if a norm should be created for the field. Norms can be used for similarities search between documents. They can also significantly increase index sizes. So, you must take care to of what field should contain norms 

**Boost:** This specifies the importance or weight of a field relative to others in a search. E.g. you may want the terms in “title” of a document to carry more weight than the content of the “footnotes” while indexing and searching.

**UI Component Type:** Choose a UI component Type according to the number of options (1-3  = item, 3-15 = list, >15= range).

**Selection Type:** Choose a selection type based how many choices should be allowed (single, multiple).

**Direction:** Default sort direction for this item (ascending, descending).

### 2 Dataset tabs display
To hide tabs permanantly (show_xx = false) and to hide deactivated tabs (& and some button) change the settings in the *areas/DDM/Ddm.settings.xml* / *Workspace/Modules/DDM/Ddm.settings.xml*

```XML
<entry key="show_primary_data_tab" value="true" type="String"/>
<entry key="show_data_structure_tab" value="true" type="String"/>  
<entry key="show_link_tab" value="true" type="String"/>
<entry key="show_permission_tab" value="true" type="String"/>
<entry key="show_publish_tab" value="true" type="String"/>
<entry key="show_attachments_tab" value="true" type="String"/>
  
<entry key="show_tabs_deactivated" value="true" type="String"/>
```    



[Go to top](#a-overview)
