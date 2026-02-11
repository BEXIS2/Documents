---
title: "Search and Download Data"
description: "This section provides information about searching and downloading data, including citation and data access requests."
tags: [search, download, citation, data access]
position: 2

---

# Search & Download Data
> [!ROLE]
> __Role:__ [User](../General/#roles)

This section explains how to find datasets, open  and download them, and request access to data in BEXIS2.

With the search you can:

- find datasets and other entities (e.g. publications),
- refine results using categories, keywords, and filters,
- open a dataset to view metadata and data, and download the dataset.

The search is based on dataset metadata and data structure definitions. The content of primary data files is currently not searchable.

> **Access rights:**  
> Search results depend on your **login status** and your **permissions** .  
> - **Not logged-in users** can view and download all public datasets. They may be also able to view the metadata of internal datasets.  
> - **Logged-in users** (e.g., project members) can see public and internal datasets. Data access depends on their permissions.

---
## Search Interface

Use the search page to explore all available datasets in your BEXIS2 instance. The exact layout may differ depending on your [instance configuration](configuration-ui/#manage-search).

Search results are shown either as:

- **List view** (tiles), or
- **Table view** (rows and columns)

You can switch between both views in the upper-right corner.

The main components of the search are:
- [Free-text search](#free-text-search) - available in both views, 
- [Search categories](#search-categories) - available in both views,
- [Filter and sorting option](#refine-results---filter-and-sorting-options)  -  only available in the table view. 


 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search01_CardView_V4.2.1.png" alt="Search card view" style="border:1px solid #bee1da; padding:10px;">



### Free-Text Search

Use the search bar at the top of the page to search metadata.

- Select a metadata field (e.g. title, owner) from the dropdown menu.
- Enter a keyword or phrase. Autocomplete suggestions appear after three characters.
- Active search terms are displayed below the search field and can be removed by clicking on them.

### Search Categories

Categories on the left side allow you to refine results based on metadata such as persons or projects.

- Numbers next to the keyword indicate how many datasets include that term.
- Click **more** to see all terms in a category.
- Categories update automatically based on your current search.

Selected categories appear below the free-text search and can be removed at any time. If you select more than three terms from the same category, only the category name is shown. Click the number next to it to see all selected terms.


 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search02_CardView_V4.2.1.png" alt="Search card view" style="border:1px solid #bee1da; padding:10px;">

### Refine Results - Filter and Sorting Options

In Table View, you can further refine results:
- **Filter:** Click the **filter icon** in a column header and enter a search term and operation (e.g., contains, equals).
- **Sort:** Click a **column header** to sort results.

 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search03_TableView_V4.2.1.png" alt="Search card view" style="border:1px solid #bee1da; padding:10px;">


---
## Open a Dataset

To open a dataset:
- **Table View:** Click [[!LINK_VIEW]](../docs/General#roles) to open the dataset.
- **List View:** Click the dataset **tile**.

The dataset opens on its landing page, showing metadata and available content. Depending on the dataset and your permissions, the following **tabs** may be available:

- **Data**: **Tabular data**: shown as a searchable table-. **Non-tabular data**: filea are listed.
- [**Data structure**](../docs/DataDescription#data-structures): Variable definitions for tabular data
- [**Link**](../docs/Datasets#links): References to related datasets 
- [**Attachments**](../docs/Datasets#attachments): Additional materials such as documents or images

 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search04_DatasetLandingPage_V4.2.1.png" alt="Search card view" style="border:1px solid #bee1da; padding:10px;">

---
## Download a Dataset

Depending on your permissions, you can download:
- Metadata only  
- The complete dataset

You can download data directly from the dataset landing page:
- **Download Metadata:** Button on the left side of the metadata page. Downloads metadata as HTML or XML.

- **Download Dataset or Download:** Button in the upper-right corner downloads the complete dataset. The downloaded ZIP file includes:
    - metadata files,
    - data file (use the filter option to download only part of the data)
    - data structure files,
    - dataset summary information (general_metadata.json),
    - metadata schema definitions (schema folder),
    - the instance’s terms and conditions.

> **Note:**
If you are not allowed to access the data, the **Download Dataset** button is not available. But you may be able to request access to the data. However, you may be able to **[request access](#request-access-to-restricted-data)** to the data. 

 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search05_Download_V4.2.1.png" alt="Download a dataset" style="border:1px solid #bee1da; padding:10px;">

---
## Request Access to Restricted Data

If a dataset is restricted (e.g., embargo):

- Click the **Request Access** button on the dataset page.
- Provide a brief justification (required).
- You will be notified once access is granted.
- You can view all your requests under [**My Data**](../docs/MyData#my-requests).

> **Note:**
If the request button is not shown, you may not have permission to request access. Please contact your instance administrator for support.

---
## Cite a Dataset

A citation suggestion may be provided depending on your BEXIS2 instance configuration:
- at the top of the dataset page,
- via the **Download Citation** button in BibTeX, RIS and plain text citation formats.



## Advanced Download Options (via API)

An API for downloading datasets is available for advanced use cases. Under your user name in the main menu, you find: 
- the link to the API
- your personal access token for datasets you are permitted to access (including internal datasets).

The API enables automated access to datasets.

 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search06_API01_V4.2.1.png" alt="API for dataset download" style="border:1px solid #bee1da; padding:10px;">