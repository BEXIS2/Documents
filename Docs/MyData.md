---
title: "MyData"
description: "This section provides information about managing datasets, including versioning, requests, and exporting data."
tags: [search, download, citation, data access]
position: 4

---

# My Data
> [!ROLE]
> __Role:__ [User](../docs/General/#roles)
>
> 
My Data is your personal dashboard providing an overview of all datasets you have access to. It serves as the central point for:
 * viewing and editing your datasets ([My Datasets](#my-datasets))
 * tracking your data access requests ([My Requests](#my-requests))
 * managing access requests from other users for your datasets ([Decisions](decisions))



## Dashboard

The **My Data** dashboard opens when you click **My Data** in the main menu in the header. Depending on the configuration of your BEXIS2 instance, the dashboard may contain a single section (e.g., datasets) or multiple sections (e.g., datasets, publications). **My Data** gives you with an overview of all datasets you can access and is the main starting point for viewing and managing them. 

Within each section, datasets are organized in tab baseds on your permission level. By default, the following permission groups are used:

* __Own:__ Full access, including the ability to grant access to the dataset to other users
* __Edit:__ Access that allows the user to edit the dataset
* __Download:__ Read-only access with download permission

> Note: Permission groups and their names may vary depending on the configuration of your BEXIS2 instance.


### My Datasets

Within **My Datasets** in the tab **own**, you can see general information about your datasets (e.g., ID, title). The action buttons on the right provide the following options:

* __View ([[!LINK_VIEW]](../docs/General#roles)):__ Opens the dataset landing page 
* __Edit ([[!LINK_EDIT]](../docs/General#roles)):__ Opens the [dataset edit page](../docs/Datasets/#metadata-edit-page)
* __Copy:__ Creates a duplicate of your dataset and opens the [dataset edit page](../docs/Datasets/#metadata-edit-page) for the new dataset. The copied dataset includes the same metadata and data structure but does not include primary data, attachments, and links. Use this option to reuse metadata and/or data structures.
* __Versioning__ _(not available in all instances)_: Only, if advanced dataset versioning is enabled in your BEXIS2 instance, this button is visible. This option allows you - depending on your permissions - to request a dataset release or open the [version table](#dataset-versioning) of the dataset.

> Note: Datasets highlighted in red indicate incomplete or missing mandatory metadata.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/MyData_01_Own_V4.2.1.png" alt="My Data dashboard showing datasets grouped by permission level. My Data is your personal dashboard providing an overview of all datasets you have access to." style="border:1px solid #bee1da; padding:10px;">

### My Requests
My Requests lists all your pending and answered data access requests. Pending requests can be withdrawn if they are no longer needed by clicking ([[!LINK_DELETE]](../docs/General#roles)) on the right.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/MyData_02_Request_V4.2.1(BExIS).png" alt="My Data dashboard showing a list of pending and answered data access requests." style="border:1px solid #bee1da; padding:10px;">


### Decision
In Decisions, you can review all pending and answered access requests for your datasets. Pending requests can be approved (✓) or rejected (−). The requester is automatically informed of your decision via email.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/MyData_03_Decision_V1.18.png" alt="My Data dashboard showing a list of pending and answered data access requests." style="border:1px solid #bee1da; padding:10px;">

## Permissions & Visibility

### Permissions
> **Note:** This section is currently being created. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

### Visibility
> **Note:** This section is currently being created. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

## Dataset Versioning
In BEXIS2, every change to a dataset creates a new dataset version. This includes changes such as editing metadata, uploading or updating data files, and adding or deleting attachments.

How these versions are handled and displayed depends on the versioning configuration of your BEXIS2 instance.
This [configuration](#../docs/Configuration/visibility-&-versions-(dataset-discovery)) is defined by the administrators of your instance.

BEXIS2 supports two versioning modes:

* Versioning without minor/major versions
  * The dataset becomes **searchable immediately after creation**.
  * No explicit release action is required.
  * **Every version** created by any change in the dataset is shown on the dataset landing page.
* Versioning with minor/major versions (releases)
   * Before release, the dataset is visible **only to users with editing permissions** (e.g., dataset authors or administrators) in the My Data dashboard.
   * A dataset becomes **searchable only after a major/minor version** has been released.
   * Only released major/minor versions are visible on the dataset landing page.

### How to Request or Manage a Dataset Release

A dataset should be released as a major version when:
 * the metadata is complete and comprehensive
 * the data has been uploaded and reviewed


To manage dataset releases (major/minor versions):

  1.  Open My Data from the main menu
  2.  Locate your dataset under My Datasets
  3.  Click the versioning button. Depending on your permissions, you can:
      * Request a dataset release. Therefore, provide a short release message describing the changes. The request is sent to your instance’s data curator or adminstrator.
      * Open the [version table](#dataset-version-table). Select and release the desired version as a major or minor release.


  <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/MyData_10_Versioning03_VersiontableV4.2.1.png" alt="My Data dashboard showing a list of pending and answered data access requests." style="border:1px solid #bee1da; padding:10px;">


After a dataset has been released:

* Subsequent metadata changes are included in the released version automatically.
* Data changes require the release of a new major version.
* A minor release can be applied for substantial metadata changes. (Depending on the instance configuration, only major releases may be available.)

### Dataset Version Table

> **Note:** This section is currently being created. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

## Publishing Data

> **Note:** This section is currently being created. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

### DOI
### GBIF
### Other
