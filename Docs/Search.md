---
title: "Search and Download Data"
description: "This section provides information about searching and downloading data, including citation and data access requests."
tags: [search, download, citation, data access]
position: 2

---

# Search & Download Data
> [!ROLE]
> __Role:__ [User](../General/#roles)

Under construction. We are working on it.

## Overview
Use the search to explore all datasets and other entities such as publications available in your BEXIS2 instance. You can search by keywords, filter by categories, or sort results to quickly locate the data most relevant to your work.

The search is based on the information provided in the metadata of datasets and their data structures. The content of the primary data is not yet searchable.

> Note: Search results will depend on your user status. 
> - **Not logged-in users** can view and download only public datasets. 
> - **Logged-in user**, typically project members, can view all datasets. They have access to the metadata and, depending on their permissions, also to primary data and attachments.

## Search

The search interface is configured by your BEXIS2 instance administrator (see [Manage Search](#configuration-ui/manage-search)) and may therefore look different from the example shown in this manual. However, the main components — [Free-Text Search](#free-text-search), [Categories](#search-categories), and [Filter](#filter-and-sorting-options) — are available in all instances.


### Free-Text Search

Use the search field at the top of the page to search for keywords or phrases.

- The left dropdown field allows you to restrict the search to a specific topic (e.g., title, owner name).
- In the second field, enter your search term. An autocomplete function suggests words and phrases based on  metadata after entering at least three characters.

Your active keywords appear below the search field. You can remove any of them by clicking on the term.

### Search Categories

The search categories on the left side of the page are based on metadata details such as person, or projects.


> Notes:
> - Categories may contain more than five terms — click **More** to view the complete list.
> - The number next to each term indicates how many datasets contain that term.
> - The available categories and terms are automatically update based on your current selections.

Selected category filters are displayed below the free-text search field. If you select more than three terms from the same category, only the category name is shown. Click on the number next to the category to open a window showing all selected terms for that category. Filters can be removed by clicking on them.

### Filter and Sorting Options

The dataset overview in the center of the page can be displayed either as a **Table** or a **List**. It shows all searchable datasets and other entities (if available) based on your account permissions (e.g., guest or member). You can switch between the two views in the upper-right corner of the page.

The columns shown in the **Table View** depend on your instance configuration and may include ID, type, title, and other metadata categories.

Available sorting and filtering options:
- Click the **Filter Icon** in a column header to **Filter** its content. Enter a search term and choose an option (e.g., contains, is equal to).
- Click the **Column Header** to **Sort** by that column.
- When applying free-text search or category filters, the table automatically updates to display matching results.

The **List View** provides a more comprehensive overview of each dataset. The main components of the tiles usually include the title, authors, entity type (e.g., dataset, publication), license, DOI, and primary data type (e.g., tabular data, file).

## View a Dataset
When you find a dataset you are interested in, you can open it as follows:
- In the Table View: Click the **Eye Icon** to open the dataset.
- In the List View:  Click the **Tile** to open the dataset.

The dataset opens on a new page. Depending on the dataset’s content, your user permissions, and the configuration of your BEXIS2 instance, different tabs are displayed.

Usually, you will see at least the **Metadata** and **Data** tabs. Additional tabs may include **Data Structure**, **Links**, **Attachments**, **Permissions**, **Submit**, **Publish**, and **Quality**.

## Download a Dataset

You can download a dataset either directly from the **Dataset Page** or via the **API**.

### Download via Datset Page

On the dataset page,  the following download options are available:

- Download Metadata - Button on the left side of the metadata page: Downloads only the metadata as an HTML or XML file.
- Download Dataset - Button on the right upper corner: Download the entire dataset, including primary data. For tabular data, you can select a preferred format (e.g., CSV, TSV). The downloaded **ZIP File** contains:
    - Metadata as an **XML File**
    - Metadata as an **HTML File**
    - A **Schema Folder** containing the metadata XSD
    - A **general_metadata.json File** with key information about the dataset (ID, version, title, source, download date, etc.)


> Note: If you don’t have permission to view the data of a dataset, the Download Dataset button will not be available. As logged-in user you have option to request access via the **Request dataset** button.

### Download via API

The API for dataset download is already available.
Detailed instructions and examples will be added to this manual in a future update.


## Cite a Dataset

A copyable citation suggestion is provided at the top of the dataset page. It includes all necessary information (e.g., authors, title, year, version, DOI) to correctly reference the dataset.

In addition, you may have the option to download the citation in different formats via the **Download Citation** button. Available formats are BibTeX, RIS, and plain text.


## Request Data Access

As looged in user you can request access to data which is not yet freely available. Do so by clicking the Request Access button on  the right side of the dataset page. You will be notified when access was granted to you. You can view your open request under My Data (#)