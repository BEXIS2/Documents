---
title: "Data Description"
description: "Mange Data Description of the BEXIS2 system"
position: 5
tags: ["javascript", "markdown", "metadata"]
---

# Manage Data Description

>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles), [Advanced User](../docs/General/#roles)

> **Note:** This section is currently being created. Some parts are not yet available. Content will be gradually added to ensure the documentation is complete and up to date. Thank you for your understanding.

## Overview


## Entity Templates
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles), [Advanced User](../docs/General/#roles)

## Data Structures
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles), [Advanced User](../docs/General/#roles)

## Variable Templates
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles), [Advanced User](../docs/General/#roles)

In BEXIS2, Variable Templates are predefined, reusable blueprints that define the properties and semantics of variables used in datasets. They specify key aspects such as data type (e.g., string, integer, date), unit (e.g., kg, m), and constraints (e.g., value ranges). These templates ensure consistency, comparability, and standardization across datasets by allowing users to apply the same variable definition to similar variables (e.g., temp, T, Tmin for temperature) without redefining it each time.

When defining a dataset’s [data structure](#data-structures), users can select an existing Variable Template. Its information is then automatically copied into the data structure, providing a consistent starting point while still allowing for adjustments if needed. This improves data integration and sharing, and supports semantic querying across datasets, standardization, and interoperability..

In most BEXIS2 instances, only administrators can create and manage Variable Templates. Once created, they are available system-wide and can be reused in any dataset where tabular data variables are defined.


### Create a Variable Template

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Variable Templates**.
2. On the Manage Variable Templates page, click  [[!LINK_CREATE]](../docs/General#roles) to open a new template.
3. Fill the following fields:
   - **Name**: Enter a clear, specific name. This name appears in the selection list when users choose a template.
   - **Description** (optional): Add a short description to help users identify the correct template.
   - **Unit** (optional): Select a [unit](#units) from the list if the variable has a physical unit.
   - **Data Type**: Choose the [data type](#data-types) that best matches the expected values.
   - **Meaning** (optional): Select a [meaning](#meanings), if available, to link the template to a defined concept.
   - **Constraint** (optional): Choose a constraint if values must follow certain rules (e.g., codes, ranges, or formats).
4. Once all required fields are completed, the **Save** button becomes active. 
5. A confirmation message appears in the upper right corner, and the new template is listed in the table.


### Edit a Variable Template

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Variable Templates**.
2. Find the template in the list and click  [[!LINK_EDIT]](../docs/General#roles).
3. Update any fields as needed (e.g., name, description, unit, data type, meaning, or constraints).
4. Click **Save** to apply the changes.

> **Note:** Changes affect only future use of the template. Existing datasets that already include variables based on this template are not updated automatically.


### Delete a Variable Template

1. Navigate to [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Variable Templates**.
2. Locate the template and click  [[!LINK_DELETE]](../docs/General#roles) next to it.
3. A confirmation dialog appears showing the template name. Confirm the deletion to permanently remove it.

> **Note:** Templates that are in use or required by the system cannot be deleted.


### Best Practices to Manage Variable Templates

✅ Use **clear and descriptive names** so users can easily identify the correct template.  
✅ Always add a **short description** explaining the intended use.  
✅ **Link units, meanings, and constraints** to support standardization and semantic clarity.  

>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles)

---------------------
## Units
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles), [Advanced User](../docs/General/#roles)


### Overview
Units in BEXIS2 describe the measurement context for variable values in datasets.  For example, a value like 25 becomes meaningful when it is known to represent *25 degrees Celsius* or *25 meters*.  By assigning units to variables, measurements and quantities can be stored, interpreted, processed, and reused consistently and accurately.

In BEXIS2 instances managed by a data management team, only administrators typically have permission to manage units.  Once defined, units are available system-wide and can be assigned to variables during the creation or editing of a [data structure](Dataset.md#datda-structure).


### Units
Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Units** to view, edit, create, or delete a unit. On this page, you will find a table listing all units and their properties in your BEXIS2 instance. Each unit is defined by the following information:
* __Name:__ The full name of the unit (e.g., meter, second, degree Celsius) based on international standards such as the *International System of Units (SI)*. Abbreviations or internal codes should be avoided.
* __Description:__ A short explanation of what this unit measures and in which context it is used (for example: standard unit of temperature on the Celsius scale.)
* __Abbreviation:__ The internationally standardized symbol or abbreviation of the unit (e.g., m, s, °C). This abbreviation will be displayed to users alongside variable names and values.
* __Dimension:__ The physical dimension of the unit expressed in terms of base quantities (e.g., length [L], mass [M], time [T]). [Dimensions](#dimensions) are defined under [[!LINK_CONFIGURE]](../docs/General#roles) **Settings -> Manage Dimensions**.
* __Data Type:__ Defines which [data types](#data-types) can be associated with values using this unit. This ensures the unit is only used with appropriate value types. Data types can be defined under [[!LINK_CONFIGURE]](../docs/General#roles) **Settings -> Manage Data Types**.
* __Measurement System__ (optional): Defines the measurement system the unit belongs to, such as the ,etric or imperial system.
* __External Link__ (optional): A link to an external definition or reference (e.g., a standard vocabulary or ontology).

### Create a Unit

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Units** to open the Manage Unit page.
2. On the Manage Unit page, click the **+ button** to create a new unit.
3. Fill out the required and optional fields in the form. Fields marked with a red asterisk (*) are mandatory:
   - __Name__: Enter the internationally standardized name of the unit (e.g., meter, second, degree Celsius). Do not use abbreviations or internal codes.
   - __Abbreviation__: Enter the internationally standardized symbol or abbreviation of the unit (e.g., m, s, °C).
   - __Description__: Provide a short explanation of what this unit measures and in which context it is used.
   - __Data type__: Select all [data types](#data-types) that are compatible with this unit, such as integer, decimal, or double. 
   - __Dimension__: Choose the physical [dimension](#dimensions) of the unit, expressed in terms of base quantities (e.g., length, mass, time). Select 'none' if no standard dimension applies (e.g., for ratios or counts). If the required dimension is not available in the list, create it under  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings -> Manage Dimensions**.
   - __Measurement System__ (optional): Indicate the measurement system the unit belongs to, such as metric, imperial, or nautical.
   - __External Link__ (optional): Select an [external link](#external-links) to an external definition or reference from the list, if needed (e.g., a standard vocabulary or ontology).
4. Once all required fields are completed, the **Save** (floppy) button becomes active. Save the unit by clicking the button.
5. A confirmation message appears in the upper right corner, and the new unit is successfully created.

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/DataDescription_CreateUnit.png" alt="Form to create a new unit" style="border:1px solid #bee1da; padding:10px;">


### Edit a Unit

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Units** to open the Manage Units page.
2. In the Units table, locate the unit you want to update and click  [[!LINK_EDIT]](../docs/General#roles) on the right.  
3. Make the necessary changes to the relevant fields.  
4. Click **Save** (floppy button) to apply your changes.

> **Note:** If the unit is already assigned to a variable, changes will take effect immediately wherever that unit is used. Be cautious when editing units that are used in multiple places.


### Delete a Unit

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Units** to open the Manage Units page.
2. In the table, select the unit you want to delete and click the  [[!LINK_DELETE]](../docs/General#roles) icon.   
3. Confirm the deletion in the confirmation popup.

> **Note:** Units that are already used in a dataset cannot be deleted until those assignments are removed. Always check whether a unit is in use before attempting to delete it. If you try to delete a unit that is in use, an error message will appear, and the unit cannot be deleted.


### Best Practices to Manage Units

✅ Use **descriptive and standardized names** to ensure clarity and reuse.  
✅ Write **concise, meaningful descriptions** to make constraints easy to understand.  
✅ **Test regular expressions (regex)** thoroughly to avoid unexpected validation issues.  
✅ Define **range constraints** with clear minimum/maximum values and use appropriate data types.  
✅ Provide **domain values** that are unambiguous, relevant, and well-suited to the variable they constrain.  
✅ **Check dependencies** before deleting a constraint, and only remove it if it is no longer in use.

---

## Constraints
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles), [Advanced User](../docs/General/#roles)

### Overview
Constraints in BEXIS2 are rules that define acceptable values for a variable. They help ensure data consistency, enforce formats, and guide users in entering valid information. Constraints are usually created and managed centrally by administrators and are available throughout the system when designing or editing data structures. Constraints can also be assigned to [variable templates](variable-templates) under [[!LINK_CONFIGURE]](../docs/General#roles) **Settings  → Manage Variable Templates**, which is a common use case for ensuring consistent rules across datasets.
To access the constraints management section, go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Constraints**.

### Types of Constraints
There are three main types of constraints:
- **Pattern**: Ensures values match a specific format (e.g., a date or identifier) defined using regular expressions.
  - Example: To allow only dates in the format *YYYY-MM-DD*, use the regex pattern:  *^\d{4}-\d{2}-\d{2}$*
- **Range**: Limits acceptable values to a defined numeric range.
  - Example: A constraint with a minimum of *1** and a maximum of *100*`* allows only values within that range.
- **Domain**: Specifies a list of valid values. There are three ways to provide domain values:
  - Enter values manually (one per line).
  - Upload a text file containing values.
  - Select a dataset and extract values from one of its variables.

### Create a Constraint

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Constraints**.
2. On the **Manage Constraints** page, click the **+ icon** to create a new dimension.
3. Fill out the fields in the form:
   - **Name**: A unique name for the constraint, visible when assigning it to variables.
   - **Description**: A short explanation of the constraint’s purpose.
   - **Formal Description** (auto-generated): Automatically created based on the selected type and its settings.
   - **Constraint Type**: Select between *Pattern*, *Range*, or *Domain*.
4. Further actions: **Save**, **Reload**, or **Cancel**
   - The **Save** button (floppy) becomes active only after all required information has been entered. Save the new constraint by clicking the button.
   - The **Reload** button (circular arrow icon) resets the form to its original state.
   - The **Cancel** button exits the form without saving any changes.

### Edit a Constraint

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Constraints**.
2. Find the constraint in the list and click [[!LINK_EDIT]](../docs/General#roles).
3. Update the relevant fields and click **Save** (floppy icon) to apply the changes.

### Delete a Constraint

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Constraints**.
2. Find the constraint in the list and click the  [[!LINK_DELETE]](../docs/General#roles) icon.
3. Confirm deletion in the popup window.

> **Note**: Constraints currently in use in a dataset cannot be deleted until they are removed from those datasets.

### Best Practices to Manage Constraints

✅ Use **descriptive and consistent names** to make constraints easy to identify and understand.  
✅ Provide **concise and meaningful descriptions** to clarify the purpose of each constraint.  
✅ **Thoroughly test regular expressions (regex)** to ensure they behave as expected and avoid unintended validation results.  
✅ Define **range constraints** with clearly specified minimum and maximum values, and ensure they match the correct data type.  
✅ Use **domain values** that are unambiguous, relevant, and context-appropriate for the variable they constrain.  
✅ Only delete constraints after confirming they are **no longer referenced or in use** elsewhere in the system.


---
## Dimensions
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles)

**Dimensions** in BEXIS2 refer to fundamental physical properties such as *length*, *time*, or *mass*. They provide the structural foundation for defining units, which give precise meaning to the values in a dataset. For example, the unit *meter* is based on the dimension *Length*, while *second* is based on *Time*. Linking variables to dimensions through units ensures that measurement values are grounded in scientifically accepted principles.

Each dimension in BEXIS2 is described using a structured combination of base quantities. This enables the system to consistently support a wide range of scientific measurements. Dimensions are defined using a dimension string such as *L(1,0)M(0,0)T(0,0)I(0,0)Θ(0,0)N(0,0)J(0,0)*. This format facilitates unit conversion and makes it easier to compare data across studies and disciplines.

The base compents of the dimensions are:
| Symbol | Component              |
|:--------|:------------------------|
| **L**  | Length                 |
| **M**  | Mass                   |
| **T**  | Time                   |
| **I**  | Electric Current       |
| **Θ**  | Temperature            |
| **N**  | Amount of Substance    |
| **J**  | Luminous Intensity     |

Usually, only administrators can create or modify dimensions. Once defined, these dimensions are available system-wide and are automatically referenced when users assign units to variables during dataset creation or editing. This design ensures consistency and prevents redundant definitions of measurement concepts.


### Create a Dimension

1. Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Dimensions**.
2. On the **Manage Dimensions** page, click the **+ button** to create a new dimension.  
3. Fill out the form with the required and optional fields. Fields marked with a red asterisk (*) are mandatory:
   - **Name**: Provide a clear and unique name, preferably based on international standards such as the *International System of Units (SI)*. Avoid abbreviations or internal codes.
   - **Specification**: Define the mathematical structure using base units.  
     Example: *L(1,0)M(0,0)T(0,0)I(0,0)Θ(0,0)N(0,0)J(0,0)*
   - **Description**: Briefly describe the context or usage of the dimension, e.g., _"Used for time-based units like seconds or minutes."_
4. Once all required fields are completed, the **Save** button (floppy icon) becomes active. Click it to save the new dimension. To cancel the entry, click the **X** (cancel icon).
     
> **Note**:  
> Dimensions refer to the physical properties of variables. In BEXIS2, a dimension consists of base dimension abbreviations (e.g., L, M) followed by a pair of exponents (positive, negative).

<img src="https://github.com/BEXIS2/Documents/raw/master/Docs/Images/DataDescription_ManageDimension.png" alt="Form to create a new dimension" style="border:1px solid #bee1da; padding:10px;">


### Edit a Dimension

1. Navigate to [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Dimensions**.  
2. Locate the dimension in the list and click [[!LINK_EDIT]](../docs/General#roles) on the right-hand side.  
3. Make your changes and click **Save** to apply them.

> **Note**: Editing is only possible if the dimension is not currently in use.


### Delete a Dimension

1. Navigate to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Dimensions**.  
2. Find the dimension and click the  [[!LINK_DELETE]](../docs/General#roles) icon on the right-hand side.  
3. A confirmation dialog appears showing the dimension’s name and specification.  
4. Click **Confirm** to permanently delete the dimension.

> **Note**: Deletion is only possible if the dimension is not referenced by any unit.

### Best Practices to Manage Dimensions

✅ Use **standardized and descriptive names** for better clarity and reuse.  
✅ **Check existing entries** to avoid duplicates.  
✅ Follow the **SI system structure** when defining specifications.  
✅ Keep **descriptions concise but informative**.  
✅ Regularly **review and remove unused dimensions**.



## Meanings
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles)

### Overview
**Meanings** in BEXIS2 describe the *semantic context* of variables used in datasets. They define what a variable represents beyond its name or data type.  
For example, a variable might be called *ID*, but the associated meaning could specify it as a *Specimen Identifier* or *Collection Code*. By assigning meanings, datasets become more interoperable and understandable across teams, disciplines, and systems.

In most BEXIS2 instances, only administrators have permission to manage meanings. Once defined, meanings are available system-wide and can be assigned to variables either directly or via [variable templates](#variable-templates). This promotes reuse of standard concepts and ensures consistent semantics across datasets.

### Meanings
To view, edit, create, or delete a meaning, go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Meanings**. On this page, you will find a table listing all defined meanings. Each entry contains the following fields:
- **Name**: The label used to identify the meaning. It should clearly describe what the variable represents (e.g., *Sample Identifier*, *Location Code*, *Observer Name*). Avoid vague or technical terms unless they are standardized.
- **Description**: A short explanation of what this meaning represents and how it is used. For example: *A unique identifier used to track a collected biological specimen.*  
- **Approved**: Indicates that a meaning was reviewed and approved by an administrator.
- **Selectable**: Indicates that users can select this meaning when assigning meanings to variables or [variable templates](variable-templates).

### Creat a Meaning
1.	Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Meanings**.  
2.	Click the **+ button** to open a new meaning form.
3.	Fill out the form fields:
   - **Name**: Provide a clear and descriptive name (e.g., *Observer ID*, *Collection Number*).  (e.g., *Specimen Identifier*)
   - **Description** (optional): Summarize when and how this meaning should be used.
   - **Relation** (optional): Click the + button to add a relation type and object (e.g., *has relation → occurrenceID*).
   - **Approved** (optional): Mark as reviewed and accepted for use.
   - **Selectable** (optional): Allow users to assign this meaning.
   - **Constraints** (optional): Select one or more [constraints](#constraints) that restrict the allowed values.
4. Click the **Save** button (floppy icon). A confirmation message appears at the top right of the screen.

### Edit a Meaning
1.	Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Meanings**.  
2.	Find the meaning in the list and click  [[!LINK_EDIT]](../docs/General#roles) on the right-hand side. 
3.	The form opens with the existing values 
4.	Make the necessary changes.  
5.	Click **Save** to apply the changes.

> **Note:** If a meaning is already assigned to variables, changes will automatically apply everywhere they are used. Modify widely used meanings with caution to avoid unintentional impact on existing datasets

### Delete a Meaning
1.	Go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Meanings**.  
2.	Select the meaning in the list and click the  [[!LINK_DELETE] ](../docs/General#roles) icon to delete the meaning.
3.	A confirmation dialog appears showing the name of the Meaning. Click **Confirm** to delete.

> **Note:** Only meanings not assigned to variables or templates can be deleted. Otherwise, an error message will appear.

### Best Practices to Manage Meanings
✅ Use **short, clear names** that describe the variable’s purpose.  
✅ Always provide a **description** for clarity.  
✅ Use **relations** to connect meanings with external (or internal) vocabularies.  
✅ Define **constraints** to enforce valid and consistent data.  


## External Links
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles)

In BEXIS2, External Links connect internal system elements such as variables to external vocabularies, standards, or reference systems. This improves interoperability and makes datasets easier to share and understand across platforms.
For example, you can link a variable to a Darwin Core term like *occurrenceID*. This makes the dataset clearer to others and ensures that it follows widely accepted standards.  

In most BEXIS2 instances, only administrators can manage External Links. Once created, an External Link is available system-wide and can be reused in meanings or constraints that reference external vocabularies.  

To access and manage external links, go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage External Links**. On the Manage External Links page, you will find a table listing all defined external links. Each entry contains the following fields:


- **ID**: A system-generated identifier for each external link.  
- **Name**: The internal label used to identify the external link. 
- **URI**: The web address or identifier that points to the external resource.  
- **Type**: Defines the kind of external resource. Options include prefix, link, entity, link, characteristics, vocabulary, relationship.
- **Prefix**: An optional namespace or prefix associated with the link.
- **Link Button**: Opens the used external source.
- **Edit & Delete**: Option to edit and delete the External Link

### Create an External Link

1. Navigate to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage External Links**.  
2. On the Manage External Links page, click the **+** button to open the creation form.  
3. Fill out the form fields:  
   - **Name**: Enter a clear label for the link (e.g., *dwc*, *hasDwcTerm*). This is how the link will be referenced in the system.  
   - **Type**: Select the appropriate type. Choosing the correct type is important, because it determines how BEXIS2 interprets the link.  
   - **Prefix** (optional): Add a prefix if needed, for example when defining vocabulary or namespaces.  
   - **Prefix Category** (optional):
   - **URI**: Provide a full URI (e.g., *http://rs.tdwg.org/dwc/terms/*). Using stable URIs ensures the link remains valid and interoperable.  

4. Once all required fields are filled, the **Save** button becomes active. Click **Save** to create the external link.  
5. A confirmation message will appear at the top-right of the screen.  

### Edit an External Link

1. Navigate to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → External Links**.
2. Locate the external link in the list and click  [[!LINK_EDIT]](../docs/General#roles) next to the entry.  
3. Update the relevant fields and click **Save** to apply the changes.  

> **Note:** If the link is already referenced in other parts of the system (for example in meanings or constraints), the changes will automatically apply wherever the link is used.  

### Delete an External Link

1. Navigate to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → External Links**.
2. Find the External Link and click the  [[!LINK_DELETE]](../docs/General#roles) icon next to the entry.    
3. A confirmation dialog will appear with the link’s name. Confirm the deletion.  

> **Note:** You can only delete external links that are not currently in use. If the link is referenced elsewhere in the system, deletion will be blocked, and an error message will appear.  

### Best Practices to Manage External Links

✅ Use **clear, descriptive names** that make it easy to identify the purpose of the link.  
✅ Choose the **correct type** to ensure the link behaves as expected.  
✅ Prefer **valid and persistent URIs** that point to stable external resources.  
✅ Check for existing entries to **avoid duplication**.  

## Prefix Categories
>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles)

In BEXIS2, Prefix Categories define the classification or context of prefixes used in [external links](#external-links). They help organize and interpret prefixes that relate to vocabularies, namespaces, or semantic references. This ensures that external links are consistently structured and clearly understood throughout the system.

In most BEXIS2 instances, only administrators can manage **Prefix Categories**. Once created, a Prefix Category is available system-wide and can be reused in External Links, particularly when linking to standardized vocabularies or metadata schemes.
To access and manage Prefix Categories, go to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Prefix Categories**. On this page, you will find a table listing all defined categories. Each entry contains the following fields:

- **ID**: A system-generated identifier for each prefix category.
- **Name**: The internal name used to identify the prefix category.
- **Description**: An explanation of the prefix category’s purpose or context.
- **Edit & Delete**: Options to modify or remove the prefix category if not in use.

### Create a Prefix Category

1. Navigate to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Prefix Categories**.
2. On the Prefix Category page, click the **+ button** to open the creation form.
3. Fill out the form fields:
   - **Name**: Enter a short and descriptive name for the category (e.g., *dwc*, *gbif*). This identifies the category within the system and will be shown when selecting prefixes.
   - **Description** (optional): Provide context or an explanation of how this prefix category should be used. This helps users understand its purpose when linking external resources.
4. Once all required fields are filled out, the **Save** button becomes active. Click **Save** to create the prefix category.
5. A confirmation message will appear, and the new category will be listed in the main table.

### Edit a Prefix Category

1. Navigate to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Prefix Categories**.
2. Locate the prefix category in the list and click [[!LINK_EDIT]](../docs/General#roles).
3. The prefix category form opens above the table. Update the desired fields and click **Save** to apply changes.

> **Note:** If the prefix category is already used in external links, all updates will automatically apply wherever it is referenced.

### Delete a Prefix Category

1. Navigate to  [[!LINK_CONFIGURE]](../docs/General#roles) **Settings → Manage Prefix Categories**.
2. Find the prefix category and click the  [[!LINK_DELETE]](../docs/General#roles) icon next to it.
3. A confirmation dialog will appear with the name of the prefix category. Confirm the deletion.

> **Note:** Only prefix categories that are not currently used in external links can be deleted.

### Best Practices to Manage Prefix Categories

✅ Use a **clear and descriptive names** to make categories easily identifiable.   
✅ Add **meaningful descriptions** to help other users understand their purpose.   
✅ Check for existing categories before creating new ones to **avoid duplication**.