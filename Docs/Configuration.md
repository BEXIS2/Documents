---
title: "Configuration"
description: "Configuration of the BEXIS2 system"
position: 2
tags: ["javascript", "markdown", "metadata"]
---


# Configuration
>[!ROLE]
>__Role:__ [Administrator]("General/#roles")

## General
>[!SETTING]
>__Application Name__ (_default: BEXIS2_) (_Settings -> Application Settings -> General_)

(Short) name of the BEXIS2 instance. The name is e.g., used in the breadcrumb or as prefix in emails sent via the system. Avoid special characters or to long names.

### Landing Page
The landing page is the first page a user sees when opening the base URL of the BEXIS2 instance. There are three types of landing pages, which can be configured:

- **User is not logged in**:
>[!SETTING]
>__Landing Page__ (_Settings -> Application Settings -> General_) (_default: ddm, publisearch, index_)

By default, the public search is shown. If nothing is specified, the `landingpage.htm` is loaded from the `tenant/content/landingpage.htm`. In this case, you can also hide the menu, header, and footer.

- **User logged in with permission to see the page**:
>[!SETTING]
>__Landing Page for Users__ (_Settings -> Application Settings -> General_) (_default: ddm, Home, index_)

This page is shown if the user has permission to see this (internal) page. It must point to a module, not to the shell.


- **User logged in without permission to see the page**:
>[!SETTING]
>__Landing Page for Users with no Permission__ (_Settings -> Application Settings -> General_) (_default: ddm, Home, nopermission_)

### Authentication
>[!SETTING]
>__LDAP Configurations__ (_Settings -> Application Settings -> General_) (_default: not set and active_)

BEXIS2 can connect to multiple LDAP server. Details need to be filled according to the given items.
>[!SETTING]
>__JWT__ (_Settings -> Application Settings -> General_) (_default: default values_)

???

### Mail
>[!SETTING]
>__System E-Mail Address__ (_Settings -> Application Settings -> General_) (_default: default values_)

Email address all system emails are sent to. This is required, to run a BEXIS2 instance.

>[!SETTING]
>__SMTP__ (_Settings -> Application Settings -> General_) (_default: default values_)

SMTP server configuration for sending emails. This is required, to run a BEXIS2 instance.

```JSON
{
  "hostName": "smtp.uni-jena.de",
  "hostPort": 587,
  "hostAnonymous": false,
  "hostSecureSocketOptions": 1,
  "hostCertificateRevocation": false,
  "accountName": "",
  "accountPassword": ".",
  "fromName": "",
  "fromAddress": "
}
```
>[!SETTING]
>__Send Exceptions?__ (_Settings -> Application Settings -> General_) (_default: false_)

 ???
>[!SETTING]
>__Use Multimedia Module?__
>(_default: false_)
>
>(_Settings -> Application Settings -> General_)

If set to true, the multimedia module is activated. This allows the visualization of multimedia files like images, videos, etc.
>[!SETTING]
>__FAQ__ (_Settings -> Application Settings -> General_) (_default: [false](https://github.com/BEXIS2/Core/wiki/FAQ)_)

??



## Users & Parties

### Link user email to party email
>[!SETTING]
>__Use Person E-Mail Attribute Name__ (_Settings -> Application Settings -> General_) (_default: false_)

>[!SETTING]
>__Person E-Mail Attribute Name__ (_Settings -> Application Settings -> General_) (_default: Email_)

To activate the linkage between between user email and a party email set _Use Person E-Mail Attribute Name_ to true and define the party party attribute. If one of the email addresses is changed the other is changed as well.

### Owner of a dataset
>[!SETTING]
>__Party Relationship Type for Owner__ (_Settings -> Application Settings -> Administration_) (_default: Owner_)

Define the party relationship type for the owner of a dataset. If this type is mapped to a metadata field, the selected user is automatically set as the owner of the dataset. Owner will also receive notifications about the dataset and requests.


### Party Relationships

>__Party Relationship Types for Account__ (_Settings -> Application Settings -> Administration_)

The party relationship types are used to define the relationship between the user account and the party. Set defined types will be used in the registration form.

Example:

```JSON
[
  {
    "PartyType": "Person",
    "PartyRelationshiptypes": [
      "organizationEmployment",
      "projectMember",
      "consortiaMember"
    ]
  }
]
```

### Former Member

> __Help URL__ (_key: help_) (_default: help_)

> __Former Member Role/Group__ (_key: formerMemberRole_) (_default: alumni_)

> __Former Member Mail: Title__ (_key: mailTextTitle_) (_default: Dear_)

> __Former Member Mail: Subject__ (_key: mailTextSubject_) (_default: mailTextSubject_)

> __Former Member Mail: Main Text (applied)__ (_key: mailTextMainApplied_) (_default: This implies that your access to some features in BExIS will be restricted. You have full access to your datasets and publications._)

> __Former Member Mail: Main Text (revoked)__ (_key: mailTextMainRevoked_) (_default: This implies that your previous access rights to features and datasets in BEXIS have been re-applied._)

> __Former Member Mail: Closing__ (_key: mailTextClosing_) (_default: Sincerely yours, System Team_)



## Data Upload

### File Analyze

The more rows are analyzed, the more accurate the data type detection is. However, the analysis process will take longer. Rows are randomly selected from the file.

> __Minimum row number__ (_Settings -> Application Settings -> Data Structure_) (default: 100)

The minimum number of rows that are used to analyze the file.

> __Maximum row number__ (_Settings -> Application Settings -> Data Structure_) (default: 10000)

The maximum number of rows that are used to analyze the file.

> __Percentage of rows__ (_Settings -> Application Settings -> Data Structure_) (default: 50)

The percentage of rows used to analyze the file.

> __Similarity Threshold (0-100%)__ (_Settings -> Application Settings -> Data Structure_) (default: 60)

During the analysis of a file to create a data structure, templates and units are checked against the input using algorithms. The threshold specifies the minimum value that must be reached for the objects to be marked as suggestion. Set 0-100% to define the similarity threshold. The higher the value, the more similar the objects must be to be marked as suggestions.

## Data Structure
> __Enforce Primary Key__ (_Settings -> Application Settings -> Data Structure_) (default: true)

If set to true, it is required that a primary key is defined for the data structure.

> __Primary Key changeable?__ (_Settings -> Application Settings -> Data Structure_) (default: false)

If set to true, the primary key can be changed after the data structure is created.
> __Set optional as default__ (_Settings -> Application Settings -> Data Structure_) (default: false)

If set to true, variables are set to optional default when the data structure is created. Set false to enforce NULL values are not allowed.

> __Missing values__ (_Settings -> Application Settings -> Data Structure_) (default: na (not available))
>
Multiple key value pairs for missing values can be defined. The key is the placeholder and the value is the description.

> __Template Support__ (_Settings -> Application Settings -> Data Structure_) (default: true)

If the template support is activated, then empty unit & data type fields with information from the template are set when the data structure is created.


> __Show -Create Variable Template- on data structure edit__ (_Settings -> Application Settings -> Data Structure_) (default: false)

????

> __Link variables to templates__ (_Settings -> Application Settings -> Data Structure_) (default: false)

If set to true, it is required the variable is linked to a templates.

> __Link variables to meanings__ (_Settings -> Application Settings -> Data Structure_) (default: false)

If set to true, it is required the variable is linked to a meaning.


## Seed data definition

Under *Workspace/RPM/* several text files can be located to create seed data for attributes, datatypes, dimensions and units.

*attributes.csv*
```
Name;ShortName;Description;IsMultipleValue;IsBuiltIn;Owner;ContainerType;MeasurementScale;EntitySelectionPredicate;Self;DataType;Unit;Methodology;Constraints;ExtendedProperties;GlobalizationInfos;AggregateFunctions;REMARK
```
*datatypes.csv*
```
Name;Description;System Type;Display Pattern
```
*dimensions.csv*
```
id;name;syntax;description
```
*units*
```
Name;Abbreviation;Description;DimensionName;Measurement System;Data Types;used by;conversion to SI;remark
```

## Search
> _Settings -> Manage Search_

 The search manager allows you to add, edit, and delete search components. The search manager is divided into two sections: the search components and the search attributes. The search components are the search fields that are displayed in the search UI as facet or in the search result table as a column. The search attributes are the fields that are indexed in the search engine. The search attributes are mapped to metadata elements in the metadata schema.

> __Refresh Search__ (_Settings -> Manage Search -> Refresh Search_)

Click on the _Refresh Search_ , to reindex the search components based on the current configuration.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/searchManager.png)

To add a new search component, click on the _Create Search Attribute_ button. For editing or deleting a search component, click on the edit or delete button respectively.


![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/searchattribute.png)


### Search Attribute

**Display Name:** This is the name which is displayed in the search UI for the field.

**Source Name:** This is the name of the field in the index.

**Metadata Node:**  Add one or more xpaths from the metadata elements to be mapped against the field.

**Header Item:** 	Tick if this item should be available as a category (e.g. as a grid column).

**Default Header Item:** This item is displayed by default in the search result table.

**Search Component Type:** This specifies the search pattern that will be used against this field (as discussed in the introduction).
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



## Mapping

The mapping tool in BEXIS2 provides the predefined keys and party types for the metadata structures, which are created in the system.

*   Keys are attributes such as title or description.
*   Party types are defined objects such as persons, institutes, organization or workshops.

for more information about party types see the manual about parties.

Mapping a metadata structure hast two main advantages:

1.  While publishing a dataset, BEXIS2 retrieve information from the metadata. The more keys and party types in the system defined, the better the information can be prepared for publication.
2.  In the BEXIS2 there are party types like people, project, etc.

    In the metadata form, according to the mapping, appropriate results are suggested. If a user encapsulates a person in the metadata form, all matching persons are made available for selection. This simplifies the input of metadata. The following image shows autocomplete for the fild of project title.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/mapping_tool2.png)


#### Mapping Overview

The "Mapping tool" is accessible through the *Settings -> Manage Metadata Structure* view by clicking on the arrow buttons. Mapping could be defined to or from the system.

The page of Metadata Structure Mapping is divided into 3 sections. The source is displayed on the left and the target on the right side. All created mappings are displayed in the middle.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/mapping.png)

Source and target on the left and right side include two parts: simple and complex blocks. First name, last name or full name of a person are examples of simple elements. A complex element could be a person. A search box is provided for each side (source or target) separately.

Mappings are connections between the source and the target. There are different connection possibilities between the simple attributes. Generally, only the connection between the two simple attributes is considered.

With the help of a transformation rule, it is possible to cover a wide range of different cases. A transformation rule consists of a [RegEx](https://msdn.microsoft.com/de-de/library/az24scfc(v=vs.110).aspx) and a mask. With an example, you can check the values and the expected result.

#### Mapping Examples

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

#### Create a mapping

1.  Choose a simple or complex element from the source.
2.  Add an element to the middle section by clicking the orange arrow next to the element.
3.  Choose a simple or complex element from the target.
4.  Create the mapping by clicking on the create button.
5.  All available simple elements are listed in the mapping container for this mapping. Draw a line by clicking on one simple element from the source side and drag it to a simple element on the target side.
6.  If needed, add RegEx and mask to the transformation rule.
7.  Press on the save button after entering values in the blocks.

#### Key overview

![key_overview](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/key_overview.PNG)

### Mapping Concepts

Besides the system mapping there are also other mapping possibilities which we call concepts.
Concepts are a list of mapping keys that are needed to provide features with the appropriate information.

![gbif-conceptexample](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/gbif-conceptexample.PNG)

- Additionally, the keys contain the information that must be mapped.
- the required keys are marked with a red star
- before the functions are enabled, all required mappings must exist. for this, a flag is displayed at the top showing how many mappings are still missing.
- click on the key name for further information, in the best case an external url is provided

### GBIF

>There are several requirements that must be met for the export to work.


**Dataset**
- Completed metadata
- primary data must be present.
- datastructure must be structured

**Setup**
- concept mapping to gbif must be complete
- structure mapping file to Darwin Core Terms for data structure must exist

#### Mapping Concept

![gbif-conceptexample](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/gbif-conceptexample.PNG)

| Term |	Status |
|---|---|
| Alternate identifier |	Required |
| Title |	Required |
| Pub Date	| Required
| Language |	Required
| Abstract | 	Required
| Keyword |	Optional
| Intellectual Rights | Required
| Creator | 	Required
| Contact | 	Required
| Metadata provider |	Required
| Geographic coverage | Optional
| Taxonomic coverage | Optional

#### Darwin Core Terms mapping

- In the current version of BEXIS2, one file per data structure is used for mapping variables to darwin core archive terms.

- This file must be stored in the data folder on the server.
 e.g. **[DATAFOLDER]\DataStructures\2**

The data structure must be either an Occurrence or a Sampling event.

For each type there is an example file in the workspace in the Folder: **[WORKSPACE]\Modules\DIM\structures**

![templates_dws_terms](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/templates_dws_terms.PNG)

> In this templates the required terms are allready included but of cources there are more!

**Sampling Event**
> https://www.gbif.org/data-quality-requirements-occurrences

![dw_sample_json](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/dw_sample_json.PNG)

**Occurrence**
> https://www.gbif.org/data-quality-requirements-sampling-events

![dw_occurrence_json](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/dw_occurrence.PNG)

Use one of the templates to assign the Darwin core terms to the variables, with the index pointing to the location of the variable in the structure.

- The file must be adapted and extended if necessary.
- Then rename the file to **dw_terms.json**.
- Afterwards it must be stored in **[DATAFOLDER]\DataStructures\\{ID}\dw_terms.json**.




# Server Configuration

## Datasets
### Dataset Links
The reference types and descriptions can be configured under *Workspace/Modules/DCM/EntityReferenceConfig.Xml*. If the system contains also other entity types, which should be not allowed for linking, you can define a whitelist of shown datasets types.

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