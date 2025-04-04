---
title: "General"
description: "This section provides an overview of the BEXIS2 system, including its terms, roles, and general information about datasets and data management."
tags: ["javascript", "markdown", "metadata"]
position: 0

---

# General

## Terms
__BEXIS2__: The name BEXIS2 originates from the previous implementation done within and for BExIS, which is the data repository of the Biodiversity Exploratories. BEXIS2 is a reimplementation of BExIS to serve the data management needs of multiple research projects as an underlying software.

__Entities__: Within BEXIS2, different types of entities (digital objects) e.g., datasets and publications, can be managed. Entities are associated with certain features, permissions, or even modules. Within the code, the administration part of BEXIS2, and the API, the term entity is used to express the independence of the content.

__Dataset__: The term dataset in BEXIS2 has a dual usage. On the general level, it describes the container object consisting of at least metadata with its internal unique identifier. On the specific level, it also describes one of the most common combinations, which is metadata and tabular or unstructured data.

__Dataset Types__: Dataset types in BEXIS2 are subcategories of certain entities (e.g., datasets or publications). These are fixed combinations of a certain metadata schema with or without data (e.g., observations, sampling data, publications, GIS data, …) and related settings (e.g., default values).


## Roles
In BEXIS2, access to features and stored data is based on fine-grained user and permission management. At least there are three different general roles - visitor, user, and administrator/data curator (further called admin). In the manual, four categories are used to categorize the access to features and data.

__Visitor__: An unregistered user with access to public features and data.

__User__: A registered person allowed to create and upload datasets.

__Advanced user__: A user with rights defined by the instance, potentially including features available to data curators and admins.

__Admin__: Administrators and data curators with advanced rights to manage entities, users, permissions, and configure BEXIS2.
