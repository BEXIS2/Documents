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
- open a dataset to view metadata and data, and download the dataset

The search is based on dataset metadata and data structure definitions. The content of primary data files is currently not searchable.

> **Access rights:**  
> Search results depend on your **login status** and your **permissions** .  
> - **Not logged-in users** can view and download all public datasets. They may be also able to view the metadata of internal datasets.  
> - **Logged-in users** (e.g., project members) can see public and internal datasets; data access depends on permissions.


## Search Interface

Use the search page to explore all available datasets in your BEXIS2 instance. The exact layout may differ depending on your [instance configuration](#configuration-ui/manage-search).

Search results are shown either as:

- **List view** (tiles), or
- **Table view** (rows and columns)

You can switch between both views in the upper-right corner.

The main components of the search are:
- [Free-text search](#free-text-search) - available in both views, 
- [Search categories](#search-categories) - available in both views,
- [Filter and sorting option](#filter-and-sorting-options)  -  only available in the table view. 


 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search01_CardView_V4.2.1.png" alt="Search card view" style="border:1px solid #bee1da; padding:10px;">



### Free-Text Search

Use the search bar at the top of the page to search metadata.

- Select a metadata field (e.g. title, owner) from the dropdown menu.
- Enter a keyword or phrase. Autocomplete suggestions appear after three characters.
- Active search terms are displayed below the search field and can be removed by clicking on them.

### Search Categories

Categories on the left side allow you to refine results based on metadata such as persons or projects.

- Numbers next to the keyword indicate how many datasets nclude that term.
- Click **more** to see all terms in a category.
- Categories update automatically based on your current search.

Selected categories appear below the free-text search and can be removed at any time. If you select more than three terms from the same category, only the category name is shown. Click the number next to it to see all selected terms.


 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search02_CardView_V4.2.1.png" alt="Search card view" style="border:1px solid #bee1da; padding:10px;">

### Refine Results - Filter and Sorting Options

In Table View, you can further refine results:
- **Filter:** Click the filter icon in a column header and enter a search term and operation (e.g., contains, equals).
- **Sort:** Click a column header to sort results.


## Open a Dataset

To open a dataset:
- **Table View:** Click [[!LINK_VIEW]](../docs/General#roles) to open the dataset.
- **List View:** Click the dataset **tile**.

The dataset opens on its landing page, showing metadata and available content. Depending on the dataset and your permissions, the following **tabs** may be available:

- Data: 
    - Tabular data: shown as a searchable table
    - Non-tabular data: listed as files
- [Data structure](DataDescription.md#data-structures): Variable definitions for tabular data
- [Link](Datasets.md#dlinks): References to related datasets 
- [Attachment](Datasets.md#attachments): Additional materials such as documents or images

 <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/Search03_DatasetLandingPage_V4.2.1" alt="Search card view" style="border:1px solid #bee1da; padding:10px;">


## Download a Dataset

Depending on your permissions, you can download:
- Metadata only  
- The complete dataset (metadata, data, and related files)

You can download data directly from the dataset landing page:
- **Download Metadata:** Button on the left side of the metadata page. Downloads metadata as HTML or XML.

- **Download Dataset:** Button in the upper-right corner. Downloads the complete dataset. The downloaded ZIP file includes:
    - Metadata files,
    - Data structure files,
    - Dataset summary information (general_metadata.json),
    - Metadata schema definitions (schema folder),
    - The instance’sterms and conditions.

> **Note:**
If you are not allowed to access the data, the **Download Dataset** button is not available.

## Request Access to Restricted Data

If a dataset is restricted (e.g., embargo):

- Click Request Access on the dataset page.
- Provide a short justification (required).
- You will be notified once access is granted.
- You can view all your requests under My Data.

> **Note:**
If the request button is not shown, you may not have permission to request access. Please contact your instance administrator for support.


### Download via API

The API for dataset download is already available.
Detailed instructions and examples will be added to this manual in a future update.


## Cite a Dataset

Each dataset provides a ready-to-use citation at the top of its landing page.

You may also download the citation using the **Download Citation** button (if available) in citation formats BibTeX, RIS and plain text.


## Advanced Download Options 
Download via API

An API for downloading datasets is available for advanced use cases.
Detailed instructions and examples will be added in a future update of this manual.