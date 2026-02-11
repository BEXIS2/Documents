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
**My Data** is your personal workspace. Here you manage your datasets and handle access requests. Use **My Data** to:
 * view and edit your datasets ([My Datasets](#my-datasets)),
 * approve or reject requests for your datasets ([My Requests](#my-requests)),
 * manage dataset releases ([Decisions](#decision))

 Open **My Data** from the main menu.

Open **My Data** from the main menu. Depending on the configuration of your BEXIS2 instance, the dashboard may contain include one or more sections (e.g., datasets, publications). Within each section datasets are grouped into tabs based on your permission level.


## Overview

Open **My Data** from the main menu. Depending on the configuration of your BEXIS2 instance, the dashboard may contain include one or more sections (e.g., datasets, publications). Within each section datasets are grouped into tabs based on your permission level.


- **Own**: You can edit the dataset and **grant access** (e.g. contact person). 
- **Edit** : You can edit the dataset but cannot grant access.
- **Download** : You can view and download metadata and data.

### Manage my Dataset (My Datasets)

In **My Datasets** (tab: **edit**), you see key information such as dataset ID and title of your datasets

Within **My Datasets** in the tab **edit**, you can see general information about your datasets (e.g., ID, title).

Available actions:
* __View ([[!LINK_VIEW]](../docs/General#roles)):__ Open the dataset landing page 
* __Edit ([[!LINK_EDIT]](../docs/General#roles)):__ Open the [dataset edit page](../docs/Datasets#metadata-edit-page)
* __Copy:__ Create a new dataset based on existing metadata and data structure (without primary data, attachments, or links). Use this option to **reuse metadata and/or data structures**.
* __Versioning__ _(if enabled)_: Request the dataset release or manage its versions in the **[version table](#dataset-versioning)** of your dataset.

> Note: Datasets highlighted in red contain incomplete mandatory metadata.



<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/MyData_01_Own_V4.2.1.png" alt="My Data dashboard showing datasets grouped by permission level. My Data is your personal dashboard providing an overview of all datasets you have access to." style="border:1px solid #bee1da; padding:10px;">

### My Requests
This section lists all your pending and answered data access requests. Pending requests can be withdrawn by clicking ([[!LINK_DELETE]](../docs/General#roles)) on the right.


<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/MyData_02_Request_V4.2.1_BExIS.png" alt="My Data dashboard showing a list of pending and answered data access requests." style="border:1px solid #bee1da; padding:10px;">


### Decision
In Decisions, you can manage incoming access requests. You can approve requests (✓) or reject them (−). The requester is automatically notified by email.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/MyData_03_Decision_V1.18.png" alt="My Data dashboard showing a list of pending and answered data access requests." style="border:1px solid #bee1da; padding:10px;">

## Permissions & Visibility

### Permissions
> **Note:** This section is currently being created. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

### Visibility
> **Note:** This section is currently being created. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

## Dataset Versioning
Every change to a dataset (metadata, files, attachments) creates a new version. How these versions are handled and displayed depends on the versioning **[configuration](../docs/Configuration#visibility--versions-dataset-discovery)** of your BEXIS2 instance.

### Versioning Modes

#### 1. Simple Versioning
  * Dataset becomes **searchable immediately after creation**.
  * No explicit release action is required.
  * **All version** created by any change in the dataset are visible on the dataset landing page.
#### 2. Release-Based Versioning (Major/Minor)
   * Datasets are only **searchable after a release**.
   * Before release, datasets are visible **only to users with editing permissions** (e.g., dataset authors or administrators) in the [My Data dashboard](#my-data).
   * Only released major/minor versions are visible on the dataset landing page.

### Manage Dataset Releases (if enabled)

Release a dataset (major version) when:
- metadata is complete,
- data has been uploaded and reviewed.

To manage dataset releases (major/minor versions):

1. Open **[My Data](#my-data)**
2. Locate your dataset under **[My Datasets](#my-requests)**
3. Click the **Versioning** button. Depending on your permissions, you can:
  - Request a release (add a short release note), or
  - Open the [version table](#dataset-version-table).  Select and release the desired version as a major or minor release. 

  <img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/MyData_10_Versioning03_VersiontableV4.2.1.png" alt="My Data dashboard showing a list of pending and answered data access requests." style="border:1px solid #bee1da; padding:10px;">


After a dataset release:

* Subsequent metadata changes are included in the released version automatically.
* Data changes require a new major release.
* A minor release can be applied for substantial metadata changes (instance-dependent).

### Dataset Version Table

> **Note:** This section is currently being created. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

## Publishing Data

> **Note:** This section is currently being created. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

### DOI
### GBIF
### Other
