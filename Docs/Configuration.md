---
title: "Configuration"
description: "Configuration of the BEXIS2 system"
position: 7
tags: ["javascript", "markdown", "metadata"]
---


# Configuration UI

>[!ROLE]
>__Role:__ [Administrator](../docs/General#roles)

## General

>[!SETTING]
>__Application Name__ (_Settings -> Application Settings -> General_)(_default: BEXIS2_)

(Short) name of the BEXIS2 instance. The name is, e.g., used in the breadcrumb or as a prefix in emails sent via the system. Avoid special characters or too-long names.

### Landing Page

The landing page is the first page a user sees when opening the base URL of the BEXIS2 instance. There are three types of landing pages which can be configured:

- __User is not logged in__:

>[!SETTING]
>__Landing Page__ (_Settings -> Application Settings -> General_) (_default: ddm, publisearch, index_)

Per default, the public search is shown. If nothing is specified, the `landingpage.htm` is loaded from the `tenant/content/landingpage.htm`. In this case, you can also hide the menu, header, and footer.

- __User logged in with permission to see the page__:

>[!SETTING]
>__Landing Page for Users__ (_Settings -> Application Settings -> General_) (_default: ddm, Home, index_)

This page is shown if the user has permission to see this (internal) page. It must point to a module, not to the shell.

- __User logged in without permission to see the page__:

>[!SETTING]
>__Landing Page for Users with no Permission__ (_Settings -> Application Settings -> General_) (_default: ddm, Home, nopermission_)

### Authentication

>[!SETTING]
>__LDAP Configurations__ (_Settings -> Application Settings -> General_) (_default: not set and active_)

BEXIS2 can connect to multiple LDAP servers. Details need to be filled out according to the items given.

>[!SETTING]
>__JWT__ (_Settings -> Application Settings -> General_) (_default: default values_)

???

### E-Mail
>
>[!SETTING]
>__System E-Mail Address__ (_Settings -> Application Settings -> General_) (_default: default values_)

An e-mail address used by the system to send all system notifications. This information is required to run a BEXIS2 instance. Otherwise the system will not work at all.

>[!SETTING]
>__SMTP__ (_Settings -> Application Settings -> General_) (_default: default values_)

The following section is the configuration of a smtp server so that the system is able to send out e-mails. This information is required to run a BEXIS2 instance. Otherwise the system will not work at all. Please ensure that the settings do not contain any "//" comments. Otherwise the system will not be able to read this section correctly. The comments in the following section are only included for better understanding and documentation.

```JSON
{
  // The name/address of the SMTP server.
  "hostName": "smtp.uni-jena.de",

  // The port under which the SMTP service runs on the above-mentioned host.
  "hostPort": 587,

  // If the SMTP service supports the sending of e-mails without authentication, set the value to “true”. Otherwise, leave it at “false” and enter the corresponding user information at "accountName" and "accountPassword".
  "hostAnonymous": false,

  // Provides a way of specifying the SSL and/or TLS encryption that should be used for a connection. [0] No SSL or TLS encryption should be used. [1] Allow the IMailService to decide which SSL or TLS options to use (default). If the server does not support SSL or TLS, then the connection will continue without any encryption. [2] The connection should use SSL or TLS encryption immediately. [3] Elevates the connection to use TLS encryption immediately after reading the greeting and capabilities of the server. If the server does not support the STARTTLS extension, then the connection will fail and a NotSupportedException will be thrown. [4] Elevates the connection to use TLS encryption immediately after reading the greeting and capabilities of the server, but only if the server supports the STARTTLS extension.
  "hostSecureSocketOptions": 1,

  // Set whether connecting via SSL/TLS should check certificate revocation. Normally, the value of this property should be set to true (the default) for security reasons, but there are times when it may be necessary to set it to false. For example, most Certificate Authorities are probably pretty good at keeping their CRL and/or OCSP servers up 24/7, but occasionally they do go down or are otherwise unreachable due to other network problems between the client and the Certificate Authority. When this happens, it becomes impossible to check the revocation status of one or more of the certificates in the chain resulting in an SslHandshakeException being thrown in the Connect method. If this becomes a problem, it may become desirable to set CheckCertificateRevocation to false.
  "hostCertificateRevocation": false,

  // In case of '"hostAnonymous": false', please enter the username of the e-mail account you want to use.
  "accountName": "username",

  // Similar to the field above '"accountName"'. But instead, enter the password.
  "accountPassword": "password",

  // Please provide a meaningful name, that will appear as "sender" information within the e-mails.
  "fromName": "BEXIS2 Instance",

  // Similar to the field above '"fromName"'. But instead of the name, enter the e-mail address that should appear.
  "fromAddress": "bexis2-your-instance@provider.com"
}
```

>[!SETTING]
>__Send Exceptions?__ (_Settings -> Application Settings -> General_) (_default: false_)

This value determines whether information about exceptions are sent to the system e-mail address or not. If set to false, exceptions are thrown silently. The user may see an error message on the screen (within the browser or another client), but the system won't send an e-mail with stack information about the issue to the deposited e-mail address separately. If the value is set to true, this is of course the case.

>[!SETTING]
>__Use Multimedia Module?__(_Settings -> Application Settings -> General_)(_default: false_)

If set to true, the multimedia module is activated. This allows the visualization of multimedia files, such as images, videos, etc., in the system.

>[!SETTING]
>__FAQ__ (_Settings -> Application Settings -> General_) (_default: [false](https://github.com/BEXIS2/Core/wiki/FAQ)_)

??

## Visibility & Versions (Dataset Discovery)

>[!SETTING]
>__Check Public Metadata__ (_Settings -> Application Settings -> Dataset Discovery_) (_default: true_)

Set true to enable to show metadata for not-logged in users, if the dataset is not public.

>[!SETTING]
>__Reduce Versions Select for Logged-in Users__ (_Settings -> Application Settings -> Dataset Discovery_) (_default: true_)

Set true to reduce the versions select for logged in users.

>[!SETTING]
>__Restrict to Latest Version for Logged-in Users__ (_Settings -> Application Settings -> Dataset Discovery_) (_default: true_)

Set true to restrict the version select to the latest version for logged in users.

>[!SETTING]
>__Activate Tags to Summarize Versions__ (_Settings -> Application Settings -> Dataset Discovery_) (_default: false_)

Enable to possibility for Users to define a combination of versions to a tag.

>[!SETTING]
>__Use Minor Tags__ (_Settings -> Application Settings -> Dataset Discovery_) (_default: false_)


Activate minor tags in order to be able to show the changes more granularly.


## Dataset Creation

>[!SETTING]
>__Number of cells for direct upload instead of async__ (_Settings -> Application Settings -> Dataset Creation_) (_default: 2000_)

This number of cells determines whether an upload of structured data should be executed directly or async.

>[!SETTING]
>__fileuploadDescription__ (_Settings -> Application Settings -> Dataset Creation_) (_default: required_)

If "active", adding a description per file is possible.
If "required", adding a descriptor per file is mandatory.
If "none", adding a description per file is not possible.


>[!SETTING]
>__Multiple file upload__ (_Settings -> Application Settings -> Dataset Creation_) (_default: true_)

Allow multiple files to be uploaded at the same time.

>[!SETTING]
>__attachmentDescription__ (_Settings -> Application Settings -> Dataset Creation_) (_default: active_)

If "active", adding a description per file is possible.
If "required", adding a descriptor per file is mandatory.
If "none", adding a description per file is not possible.

>[!SETTING]
>__Multiple attachment upload__ (_Settings -> Application Settings -> Dataset Creation_) (_default: false_)

Allow multiple files to be uploaded at the same time.

>[!SETTING]
>__Use external metadata form__ (_Settings -> Application Settings -> Dataset Creation_) (_default: false_)

Enables the loading of an external metadata form when editing entities. This is useful for external metadata forms that are not part of the BEXIS2 system. The external metadata form must be loaded from a URL. The URL must be accessible from the BEXIS2 instance.

>[!SETTING]
>__External metadata form destination URL__ (_Settings -> Application Settings -> Dataset Creation_) (_default: ""_)

Define the origin from where the external metadata form should be loaded.


## Users & Parties

### Link user email to party email

>[!SETTING]
>__Use Person E-Mail Attribute Name__ (_Settings -> Application Settings -> General_) (_default: false_)

>[!SETTING]
>__Person E-Mail Attribute Name__ (_Settings -> Application Settings -> General_) (_default: Email_)

To activate the linkage between a user email and a party email, set _Use Person E-Mail Attribute Name_ to true and define the party attribute. If one of the email addresses is changed, the other is also changed.

### Owner of a dataset

>[!SETTING]
>__Party Relationship Type for Owner__ (_Settings -> Application Settings -> Administration_) (_default: Owner_)

Define the party relationship type for the owner of a dataset. If this type is mapped to a metadata field, the selected user is automatically set as the dataset's owner. The owner will also receive notifications about the dataset and requests.

### Party Relationships
>[!SETTING]
>__Party Relationship Types for Account__ (_Settings -> Application Settings -> Administration_)

The party relationship types define the relationship between the user account and the party. The defined types will be used in the registration form.

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

>[!SETTING]
> __Former Member Role/Group__ (_key: formerMemberRole_) (_default: alumni_)

The role/group that is assigned to a user when he/she is no longer a member of the project.

>[!SETTING]
> __Former Member Mail: Title__ (_key: mailTextTitle_) (_default: Dear_)

Title for mails.

>[!SETTING]
> __Former Member Mail: Subject__ (_key: mailTextSubject_) (_default: mailTextSubject_)

Alternative subject for mails. If empty per default the instance short name as for all system mails as well.

>[!SETTING]
> __Former Member Mail: Main Text (applied)__ (_key: mailTextMainApplied_) (_default: This implies that your access to some features in BExIS will be restricted. You have full access to your datasets and publications._)

Main text for former members mails (applied).

>[!SETTING]
> __Former Member Mail: Main Text (revoked)__ (_key: mailTextMainRevoked_) (_default: This implies that your previous access rights to features and datasets in BEXIS have been re-applied._)

Main text for former members mails (revoked).

>[!SETTING]
> __Former Member Mail: Closing__ (_key: mailTextClosing_) (_default: Sincerely yours, System Team_)

Closing for former members mails.

## Data Upload

### File Analyze

The more analyzed rows, the more accurate the data type detection is. However, the analysis process will take longer. Rows are randomly selected from the file.

>[!SETTING]
> __Minimum row number__ (_Settings -> Application Settings -> Data Structure_) (default: 100)

The minimum number of rows that are used to analyze the file.

>[!SETTING]
> __Maximum row number__ (_Settings -> Application Settings -> Data Structure_) (default: 10000)

The maximum number of rows that are used to analyze the file.

>[!SETTING]
> __Percentage of rows__ (_Settings -> Application Settings -> Data Structure_) (default: 50)

The percentage of rows used to analyze the file.

>[!SETTING]
>__Similarity Threshold (0-100%)__ (_Settings -> Application Settings -> Data Structure_) (default: 60)

While analyzing a file to create a data structure, templates, and units are checked against the input using algorithms. The threshold specifies the minimum value that must be reached for the objects to be marked as suggestions. Set a value between 0-100% to define the similarity threshold. The higher the value, the more similar the objects must be to be marked as suggestions.

## Data Structure
>[!SETTING]
> __Enforce Primary Key__ (_Settings -> Application Settings -> Data Structure_) (default: true)

If set to true, it is required that a primary key is defined for the data structure.

>[!SETTING]
> __Primary Key changeable?__ (_Settings -> Application Settings -> Data Structure_) (default: false)

If set to true, the primary key can be changed after creating the data structure.

>[!SETTING]
> __Set optional as default__ (_Settings -> Application Settings -> Data Structure_) (default: false)

If set to true, variables are set to optional default when the data structure is created. Setting false to enforce NULL values are not allowed.

>[!SETTING]
> __Missing values__ (_Settings -> Application Settings -> Data Structure_) (default: na (not available))

Multiple key-value pairs for missing values can be defined. The key is the placeholder, and the value is the description.

>[!SETTING]
> __Template Support__ (_Settings -> Application Settings -> Data Structure_) (default: true)

If the template support is activated, then empty unit & data type fields with information from the template are set when the data structure is created.

>[!SETTING]
> __Show -Create Variable Template- on data structure edit__ (_Settings -> Application Settings -> Data Structure_) (default: false)

Show -Create Variable Template- on data structure edit form. This allows the user to create a variable template from the data structure.
(deprecated)

>[!SETTING]
> __Link variables to templates__ (_Settings -> Application Settings -> Data Structure_) (default: false)

If set to true, the variable must be linked to a template.

>[!SETTING]
> __Link variables to meanings__ (_Settings -> Application Settings -> Data Structure_) (default: false)

If set to true, the variable must be linked to a meaning.

>[!SETTING]
> __Update Variable Description by Template selection__ (_Settings -> Application Settings -> Data Structure_) (default: true)

If the template support is activated, then empty unit & datatype fields with information from the template are set when the data structure is created.

## Data Dissemination
>[!SETTING]
>__DataCite DOI Placeholders__ (_Settings -> Application Settings -> Data Dissemination_) (default: "")

DataCite DOI placeholders are used to create a DOI for a dataset.

```JSON
[
  {
  "{DatasetId}": "{DatasetId}",
  "{VersionId}": "{VersionId}",
  "{VersionNumber}": "{VersionNumber}",
  "{VersionName}": "{VersionName}",
  "{Tag}": "{Tag}"
  }
]
```

>[!SETTING]
>__DataCite DOI Mappings__ (_Settings -> Application Settings -> Data Dissemination_) (default: "")



```JSON
[
  {
  "URL": "{DatasetId}?version={VersionNumber}",
  "Version": "{VersionName}"
  }
]
```

>[!SETTING]
>__gbifCollectionArea__ (_Settings -> Application Settings -> Data Dissemination_) (default: "export/gbif")

All created Darwin Core archive dataset exports are saved in this specified directory. It starts from the predefined data folder as default. It is also possible to specify a sequential folder path. default: {Data}/export/gbif".

>[!SETTING]
>__GBIF API Credentials__ (_Settings -> Application Settings -> Data Dissemination_) (default: "export/gbif")

GBIF API credentials are used to connect to the GBIF API. The credentials are used to authenticate the user and to authorize access to the GBIF API.

```JSON
[
  {
  "organisationKey": "",
  "installationKey": "",
  "username": "",
  "password": "",
  "server": "http://api.gbif-uat.org/v1"
}
]
```

## Search

_Settings -> Manage Search_

 The search manager allows adding, editing, and deleting search components. The search manager is divided into two sections: the search components and the search attributes. The search components are the search fields displayed in the search UI as a facet or in the search result table as a column. The search attributes are the fields that are indexed in the search engine. The search attributes are mapped to metadata elements in the metadata schema.

>[!SETTING]
> __Refresh Search__ (_Settings -> Manage Search -> Refresh Search_)

Click on the _Refresh Search_ , to reindex the search components based on the current configuration.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/searchManager.png)

To add a new search component, click the _Create Search Attribute_ button. Click the edit or delete button to edit or delete a search component.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/searchattribute.png)

### Search Attribute

__Display Name:__ This is the name that is displayed in the search UI for the field.

__Source Name:__ This is the field's name in the index.

__Metadata Node:__  Add one or more xpaths from the metadata elements to be mapped against the field.

__Header Item:__  Tick if this item should be available as a category (e.g. as a grid column).

__Default Header Item:__ This item is displayed by default in the search result table.

__Search Component Type:__ This specifies the search pattern used against this field (as discussed in the introduction).
Therefore, the value of this attribute can be any of “Category” for creating a category-based search field, “Facet” for making a faceted search field, “Property” for creating a property search field, and “General” which creates an indexed field which is not displayed in the UI, but however, searched.

__Data Type:__ This specifies the primitive data type of the value to be indexed. E.g. string, integer, double, date.

__Store:__ This specifies if the field value should be stored. If the field is not stored, you can only search against the terms in the field, however, you cannot retrieve the value. For minimal display of the search result, it is recommended that some fields be stored. This value of the store attribute can be either yes or no.

__MultiValue:__ This specifies if a metadata element has several values in a given field. E.g. if a dataset can have several owners in metadata, then, the owner's field in the index, in this case, will be multi-valued
Analyzed: This specifies if the field should be interpreted or not. Only the analyzed fields can be searched.

__Norm:__ This can have a yes or no value and is used to specify if a norm should be created for the field. Norms can be used for similarity searches between documents. They can also significantly increase index sizes. So, you must take care of what field should contain norms

__Boost:__ This specifies the importance or weight of a field relative to others in a search. E.g. you may want the terms in “title” of a document to carry more weight than the content of the “footnotes” while indexing and searching.

__UI Component Type:__ Choose a UI component Type according to the number of options (1-3  = item, 3-15 = list, >15= range).

__Selection Type:__ Choose a selection type based on how many choices should be allowed (single, multiple).

__Direction:__ Default sort direction for this item (ascending, descending).

## Mapping

The mapping tool in BEXIS2 provides the predefined keys and party types for the metadata structures created in the system.

- Keys are attributes such as title or description.
- Party types are defined objects such as persons, institutes, organizations, or workshops.

For more information about party types see the manual about parties.

Mapping a metadata structure has two main advantages:

1. While publishing a dataset, BEXIS2 retrieves information from the metadata. The more keys and party types in the system defined, the better the information can be prepared for publication.
2. The BEXIS2 has party types like people, projects, etc.

    According to the mapping, appropriate results are suggested in the metadata form. All matching persons are available for selection if a user encapsulates a person in the metadata form. This simplifies the input of metadata. The following image shows autocomplete for the field of project title.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/mapping_tool2.png)

### Mapping Overview

The "Mapping tool" is accessible through the _Settings -> Manage Metadata Structure_ view by clicking on the arrow buttons. Mapping could be defined to or from the system.

The page of Metadata Structure Mapping is divided into three sections. The source is displayed on the left and the target on the right. All created mappings are shown in the middle.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/mapping.png)

The source and target on the left and right sides include two parts: simple and complex blocks. First name, last name, or full name of a person are examples of simple elements. A complex element could be a person. A separate search box is provided for each side (source or target).

Mappings are connections between the source and the target. There are different connection possibilities between the simple attributes. Generally, only the connection between the two simple attributes is considered.

With the help of a transformation rule, it is possible to cover a wide range of cases. A transformation rule consists of a [RegEx](https://msdn.microsoft.com/de-de/library/az24scfc(v=vs.110).aspx) and a mask. With an example, you can check the values and the expected result.

### Mapping Examples

Here are some examples of one-to-one, one-to-many, and many-to-one mapping.

__Example: One to One__

This example creates a connection between the two titles. A RegEx separates all words and then arranges them differently via the mask.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/one_to_one.png)

__EXAMPLE: One to Many__

This example creates a connection between a name on one side and the FirstName and the LastName on the other side. In the transformation rule, the first and last names are separated from each other by a RegEx and then positioned in the mask via the variable.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/one_to_many.png)

__EXAMPLE: Many to One__

This example creates a connection between the FirstName and LastName by a name. There is no RegEx needed, but the mask is ordered from both variables.

![img1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/many_to_one.png)

### Create a mapping

1. Choose a simple or complex element from the source.
2. Add an element to the middle section by clicking the orange arrow next to the component.
3. Choose a simple or complex element from the target.
4. Create the mapping by clicking on the Create button.
5. All available simple elements are listed in the mapping container for this mapping. Draw a line by clicking on one simple element from the source side and drag it to a simple element on the target side.
6. If needed, add RegEx and mask to the transformation rule.
7. Press the save button after entering values in the blocks.

### Key overview

![key_overview](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/key_overview.PNG)

### Mapping Concepts

Besides system mapping, there are other mapping possibilities, which we call concepts.
Concepts are a list of mapping keys needed to provide features with the appropriate information.

![gbif-conceptexample](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/gbif-conceptexample.PNG)

- Additionally, the keys contain the information that must be mapped.
- the required keys are marked with a red star
- before the functions are enabled, all required mappings must exist. A flag is displayed at the top, showing how many mappings are still missing.
- click on the key name for further information, in the best case an external URL is provided

### DOI (DataCite)

>
>[!SETTING]
>__DataCite DOI Placeholders__ (_Settings -> Application Settings -> Data Dissemination_) (_default: default values_)

The placeholders are necessary to adopt dataset-specific values into the data model, which is sent to DataCite. As the system cannot assume that these values exist in the metadata, they must be extracted directly from the data record.

```JSON
{
  // 
  "{DatasetId}": "{DatasetId}",
  "{VersionId}": "{VersionId}",
  "{VersionNumber}": "{VersionNumber}",
  "{VersionName}": "{VersionName}",
  "{Tag}": "{Tag}"
}
```

>[!SETTING]
>__SMTP__ (_Settings -> Application Settings -> General_) (_default: default values_)

The following section is the configuration of a smtp server so that the system is able to send out e-mails. This information is required to run a BEXIS2 instance. Otherwise the system will not work at all. Please ensure that the settings do not contain any "//" comments. Otherwise the system will not be able to read this section correctly. The comments in the following section are only included for better understanding and documentation.

```JSON
{
  // The name/address of the SMTP server.
  "hostName": "smtp.uni-jena.de",

  // The port under which the SMTP service runs on the above-mentioned host.
  "hostPort": 587,

  // If the SMTP service supports the sending of e-mails without authentication, set the value to “true”. Otherwise, leave it at “false” and enter the corresponding user information at "accountName" and "accountPassword".
  "hostAnonymous": false,

  // Provides a way of specifying the SSL and/or TLS encryption that should be used for a connection. [0] No SSL or TLS encryption should be used. [1] Allow the IMailService to decide which SSL or TLS options to use (default). If the server does not support SSL or TLS, then the connection will continue without any encryption. [2] The connection should use SSL or TLS encryption immediately. [3] Elevates the connection to use TLS encryption immediately after reading the greeting and capabilities of the server. If the server does not support the STARTTLS extension, then the connection will fail and a NotSupportedException will be thrown. [4] Elevates the connection to use TLS encryption immediately after reading the greeting and capabilities of the server, but only if the server supports the STARTTLS extension.
  "hostSecureSocketOptions": 1,

  // Set whether connecting via SSL/TLS should check certificate revocation. Normally, the value of this property should be set to true (the default) for security reasons, but there are times when it may be necessary to set it to false. For example, most Certificate Authorities are probably pretty good at keeping their CRL and/or OCSP servers up 24/7, but occasionally they do go down or are otherwise unreachable due to other network problems between the client and the Certificate Authority. When this happens, it becomes impossible to check the revocation status of one or more of the certificates in the chain resulting in an SslHandshakeException being thrown in the Connect method. If this becomes a problem, it may become desirable to set CheckCertificateRevocation to false.
  "hostCertificateRevocation": false,

  // In case of '"hostAnonymous": false', please enter the username of the e-mail account you want to use.
  "accountName": "username",

  // Similar to the field above '"accountName"'. But instead, enter the password.
  "accountPassword": "password",

  // Please provide a meaningful name, that will appear as "sender" information within the e-mails.
  "fromName": "BEXIS2 Instance",

  // Similar to the field above '"fromName"'. But instead of the name, enter the e-mail address that should appear.
  "fromAddress": "bexis2-your-instance@provider.com"
}
```

### GBIF

> Several requirements must be met for the export to work.

__Dataset__

- completed metadata
- primary data must be present
- data structure must be structured

__Setup__

- concept mapping to GBIF must be complete
- structure mapping file to Darwin Core Terms for data structure must exist

#### Mapping Concept

![gbif-conceptexample](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/gbif-conceptexample.PNG)

| Term                 | Status   |
| -------------------- | -------- |
| Alternate identifier | Required |
| Title                | Required |
| Pub Date             | Required |
| Language             | Required |
| Abstract             | Required |
| Keyword              | Optional |
| Intellectual Rights  | Required |
| Creator              | Required |
| Contact              | Required |
| Metadata provider    | Required |
| Geographic coverage  | Optional |
| Taxonomic coverage   | Optional |

#### Darwin Core Terms mapping

- In the current version of BEXIS2, one file per data structure is used for mapping variables to Darwin core archive terms.

- This file must be stored in the server's data folder.
 e.g. __[DATAFOLDER]\DataStructures\2__

The data structure must be either an Occurrence or a Sampling event.

For each type there is an example file in the workspace in the Folder: __[WORKSPACE]\Modules\DIM\structures__

![templates_dws_terms](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/templates_dws_terms.PNG)

> In this template, the required terms are already included, but of course, there are more!

__Sampling Event__
> <https://www.gbif.org/data-quality-requirements-occurrences>

![dw_sample_json](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/dw_sample_json.PNG)

__Occurrence__
> <https://www.gbif.org/data-quality-requirements-sampling-events>

![dw_occurrence_json](https://github.com/BEXIS2/Documents/raw/master/Manuals/DIM/Images/dw_occurrence.PNG)

Use one of the templates to assign the Darwin core terms to the variables, with the index pointing to the location of the variable in the structure.

- The file must be adapted and extended if necessary.
- Then rename the file to __dw_terms.json__.
- Afterwards it must be stored in __[DATAFOLDER]\DataStructures\\{ID}\dw_terms.json__.

# Configuration Server

## Changeable Settings

### Header & Footer

### Dataset Links

The reference types and descriptions can be configured under _Workspace/Modules/DCM/EntityReferenceConfig.Xml_. If the system also contains other entity types, which should not be allowed for linking, you can define a whitelist of shown dataset types.

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

## Initial Configuration

### Manage Parties

A party package manages all kinds of entities such as people, organizations, projects, etc. It also manages the relationship between them. For example, one person is a part of a project for a certain duration. Furthermore, it is able to connect to the other modules, which now it is connected to the security module, and it is also able to import the definitions such as “partytypes”, “customattributes,” and “relationshiptype” from an XML file.

#### XML-Schema

The schema is defined in the file _PartyTypes.xml_ which is located in the workspace under _…\Workspace\Modules\BAM_.
Here you can define the _party types_ and their _custom attributes_ together with _relationship types_.

__[ ]__ optional attributes

#### PartyType attributes

|                   |                                                                                                                |
| ----------------- | :------------------------------------------------------------------------------------------------------------- |
| __Name:__         | Party type name should be unique among the other party types. Spaces and special characters should be avoided. |
| __[DisplayName]__ | Name shown in the UI. If not set, the __Name__ is used, which might be not very user-friendly.                 |

#### Custom attributes

Each party type can have custom attributes.

|                       |                                                                                                                                                                                |
| --------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| __Name:__             | Name of the custom attribute.                                                                                                                                                  |
| __[DisplayName]__     | _default_: __Name__. The name is shown in the UI. If not set, the __Name__ is used, which might be not very user-friendly.                                                     |
| __[Type]__            | _default_: "string". Option: "bool" (two radio buttons with true/false).                                                                                                       |
| __[IsMain]__          | _default_: "false". Every party should have a general name, which comes from its custom attributes. If there is more than one “IsMain” attribute it will be merged by a space. |
| __[ValidValues]__     | List of values shown as a dropdown list. Values should be separated by “,”.                                                                                                    |
| __[IsUnique]__        | _default_: "false". "true" means that this attribute of this party should be unique among the other parties which have the same party type.                                    |
| __[IsValueOptional]__ | _default_: "true".  "false" means the user has to fill in this field.                                                                                                          |
| __[Description]__     | Shows some extra information as a tooltip to the user.                                                                                                                         |

#### PartyRelationshipType attributes

|                          |                                                                                                                                                            |
| ------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------- |
| __Name__                 | PartyrelationshipType name should be unique among the others. Spaces and special characters should be avoided.                                             |
| __[DisplayName]__        | Name shown in the UI. If not set, the __Name__ is used, which might be not very user-friendly.                                                             |
| __[Description]__        | Shows some extra information as a tooltip to the user.                                                                                                     |
| __[IndicatesHierarchy]__ | _default_: "false". "true" means that there is a hierarchy relationship between all the pairs as the source is the root and the target is the child of it. |
| __[MaxCardinality]__     | _default_: unlimited. If it is set to a number it forces the user to not have more than this number relationships.                                         |
| __[MinCardinality]__     | _default_: unlimited. If it is set to a number it forces the user to have at least this number of relationships.                                           |

#### PartyTypePair attributes

|                   |                                                                                                  |
| ----------------- | :----------------------------------------------------------------------------------------------- |
| __Title__         | The title of this pair.                                                                          |
| __AllowedSource__ | source party type is obligatory and should be exactly the same name as we defined for partytype. |
| __AllowedTarget__ | Target party type is obligatory and should be exactly the same name as we defined for partytype. |
| __[Description]__ | It shows some info about this type to the user in a tooltip.                                     |

### Datasets Seed Data

Under _Workspace/RPM/_, several text files can be located to create seed data for attributes, datatypes, dimensions, and units.

_attributes.csv_

```
Name;ShortName;Description;IsMultipleValue;IsBuiltIn;Owner;ContainerType;MeasurementScale;EntitySelectionPredicate;Self;DataType;Unit;Methodology;Constraints;ExtendedProperties;GlobalizationInfos;AggregateFunctions;REMARK
```

*datatypes.csv_

```
Name;Description;System Type;Display Pattern
```

*dimensions.csv_

```
id;name;syntax;description
```

*units_

```
Name;Abbreviation;Description;DimensionName;Measurement System;Data Types;used by;conversion to SI;remark
```
