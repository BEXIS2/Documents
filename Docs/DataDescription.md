---
title: "Data Description"
description: "Mange Data Description of the BEXIS2 system"
position: 5
tags: ["javascript", "markdown", "metadata"]
---

# Manage Data Description

>[!ROLE]
>__Role:__ [Advanced User](../docs/General/#roles)

## Overview

This section is under construction. Please be patient with us as we work on it.

## Entity Templates
## Data Structures
## Variable Templates
## Data Types
## Units
### Overview

Units in BEXIS2 describe the measurement context for variable values in datasets.  For example, a value like 25 becomes meaningful when it is known to represent *25 degrees Celsius* or *25 meters*.  By assigning units to variables, measurements and quantities can be stored, interpreted, processed, and reused consistently and accurately.

In BEXIS2 instances managed by a data management team, only administrators typically have permission to manage units.  Once defined, units are available system-wide and can be assigned to variables during the creation or editing of a [Data Structure](Dataset.md#datda-structure).



### Units
To view, edit, create, or delete a unit, navigate __Settings -> Manage Units__. On this page, you will find a table listing all units and their properties in your BEXIS2 instance. Each unit is defined by the following information:

* __Name:__ The full name of the unit (e.g., meter, second, degree Celsius) based on international standards such as the __International System of Units (SI)__. Abbreviations or internal codes should be avoided.
* __Description:__ A short explanation of what this unit measures and in which context it is used. For example: *Standard unit of temperature on the Celsius scale.*
* __Abbreviation__ (required): The internationally standardized symbol or abbreviation of the unit (e.g., m, s, °C). This abbreviation will be displayed to users alongside variable names and values.
* __Dimension:__ The physical dimension of the unit expressed in terms of base quantities (e.g., length [L], mass [M], time [T]). [Dimensions](#dimensions) are defined under __Settings -> Manage Dimensions__ .
* __Data Type:__ Defines which data types can be associated with values using this unit. [Data types](#data-types) can be defined under __Settings -> Manage Data Types__.
* __Measurement System__ (optional): Defines the measurement system the unit belongs to, such as the Metric or Imperial system.
* __External Link__ (optional): A link to an external definition or reference (e.g., a standard vocabulary or ontology).



### Creating a New Unit

To create a new unit that users can later assign to variables:
1. Go to the main menu and select  *Manage Units* under Settings to open the Manage Unit page.
2. On the Manage Unit page, click the + button to create a new unit.
3. Fill out the required and optional fields in the form. Fields marked with a red asterisk (*) are mandatory:
* __Name__ (required): Enter the internationally standardized name of the unit (e.g., meter, second, degree Celsius). Do not use abbreviations or internal codes.
* __Abbreviation__ (required): Enter the internationally standardized symbol or abbreviation of the unit (e.g., m, s, °C). This abbreviation will be shown to users alongside variable names and values.
* __Description__ (required): Provide a short explanation of what this unit measures and in which context it is used. For example: “Standard unit of temperature on the Celsius scale.”
* __[Data type](#data-types)__ (required): Select __all__ data types that are compatible with this unit, such as integer, decimal, or double. This ensures the unit is only used with appropriate value types.
* __[Dimension](#dimensions)__ (required): Choose the physical dimension of the unit, expressed in terms of base quantities (e.g., length, mass, time). Select 'none' if no standard dimension applies (e.g., for ratios or counts). If the required dimension is not available in the list, create it under __Settings -> Manage Dimensions__.
* __Measurement System__ (optional): Optionally indicate the measurement system the unit belongs to, such as Metric, Imperial, or Nautical.
* __External Link__ (optional): Select a link to an external definition or reference from the list, if needed (e.g., a standard vocabulary or ontology).

The **Save** (Floppy) button becomes active only after all required information has been entered. You can then save the unit by clicking the button. Once the unit is successfully created, a confirmation message appears in the top right corner of the screen.

![Create dataset I](https://github.com/BEXIS2/Documents/raw/master/Docs/Images/DataDescription_CreateUnit.png)


### Editing a Unit

You can update an existing unit to correct or clarify its information.

1. Go to the main menu and select **Manage Units** under **Settings** to open the Manage Units page.  
2. In the Units table, locate the unit you want to update.  
3. Click the **Edit** icon on the right.  
4. Make the necessary changes to the relevant fields.  
5. Click **Save** (floppy button) to apply your changes.

> **Note:** If the unit is already assigned to a variable, changes will take effect immediately wherever that unit is used. Be cautious when editing units that are used in multiple places.



### Deleting a Unit

You can also remove units that are not used in the system. To remove a unit:

1. Go to the main menu and select **Manage Units** under **Settings** to open the Manage Units page.  
2. In the table, select the unit you want to delete.  
3. Click the **Delete** icon.  
4. Confirm the deletion in the confirmation popup.

> **Note:** Units that are already used in a dataset cannot be deleted until those assignments are removed. Always check whether a unit is in use before attempting to delete it. If you try to delete a unit that is in use, an error message will appear, and the unit cannot be deleted.

### Best Practices for Managing Units
- ✅ Use **descriptive and standardized names** to ensure clarity and reuse.  
- ✅ Write **concise, meaningful descriptions** to make constraints easy to understand.  
- ✅ **Test regular expressions (regex)** thoroughly to avoid unexpected validation issues.  
- ✅ Define **range constraints** with clear minimum/maximum values and use appropriate data types.  
- ✅ Provide **domain values** that are unambiguous, relevant, and well-suited to the variable they constrain.  
- ✅ **Check dependencies** before deleting a constraint, and only remove it if it is no longer in use.



## Constraints
### Overview

Constraints in BEXIS2 are rules that define acceptable values for a variable. They help ensure data consistency, enforce formats, and guide users in entering valid information. Constraints are created and managed centrally by administrators and are available throughout the system when designing or editing data structures. Constraints can also be assigned to variable templates under **Settings → Manage Variable Templates**, which is a common use case for ensuring consistent rules across datasets.

To access the constraints management section, go to **Settings → Manage Constraints**.

### Types of Constraints

There are three main types of constraints:

- **Pattern**: Ensures values match a specific format (e.g., a date or identifier) defined using regular expressions..
  - Example: To allow only dates in the format `YYYY-MM-DD`, use the regex pattern:  `^\d{4}-\d{2}-\d{2}$`
- **Range**: Limits acceptable values to a defined numeric range.
  - Example: A constraint with a minimum of `1` and a maximum of `100` allows only values within that range.
- **Domain**: Specifies a list of valid values. There are three ways to provide domain values:
  - Enter values manually (one per line).
  - Upload a text file containing values.
  - Select a dataset and extract values from one of its variables.

### Creating a New Constraint

To create a new constraint:

1. Navigate to **Settings → Manage Constraints**.
2.  On the **Manage Constraints** page, click the **plus icon (+)** to create a new dimension.
3. Fill out the fields in the form:

   - **Name (required)**: A unique name for the constraint, visible when assigning it to variables.
   - **Description (required)**: A short explanation of the constraint’s purpose.
   - **Formal Description (auto-generated)**: Automatically created based on the selected type and its settings.
   - **Constraint Type (required)**: Select between *Pattern*, *Range*, or *Domain*.
  
### Reload and Cancel Buttons

- The **Reload** button (circular arrow icon) resets the form to its original state.
- The **Cancel** button exits the form without saving any changes.

### Editing a Constraint

To edit a constraint:

1. Go to **Settings → Manage Constraints**.
2. Find the constraint in the list and click the **Edit** icon.
3. Update the relevant fields and click **Save** (floppy disk icon) to apply the changes.

### Deleting a Constraint

To delete a constraint:

1. Go to **Settings → Manage Constraints**.
2. Find the constraint in the list and click the **Delete** icon.
3. Confirm deletion in the popup window.

> **Note**: Constraints currently in use in a dataset cannot be deleted until they are removed from those datasets.

### Best Practices

- ✅ Use **descriptive and consistent names** to make constraints easy to identify and understand.  
- ✅ Provide **concise and meaningful descriptions** to clarify the purpose of each constraint.  
- ✅ **Thoroughly test regular expressions (regex)** to ensure they behave as expected and avoid unintended validation results.  
- ✅ Define **range constraints** with clearly specified minimum and maximum values, and ensure they match the correct data type.  
- ✅ Use **domain values** that are unambiguous, relevant, and context-appropriate for the variable they constrain.  
- ✅ Only delete constraints after confirming they are **no longer referenced or in use** elsewhere in the system.

## Dimensions

>[!ROLE]
>__Role:__ [Administrator](../docs/General/#roles)

**Dimensions** in BEXIS2 refer to fundamental physical properties such as *length*, *time*, or *mass*. They provide the structural foundation for defining units, which give precise meaning to the values in a dataset. For example, the unit *meter* is based on the dimension *Length*, while *second* is based on *Time*. Linking variables to dimensions through units ensures that measurement values are grounded in scientifically accepted principles.

Each dimension in BEXIS2 is described using a structured combination of base quantities. This enables the system to consistently support a wide range of scientific measurements. Dimensions are defined using a dimension string such as `L(1,0)M(0,0)T(0,0)I(0,0)Θ(0,0)N(0,0)J(0,0)`. This format facilitates unit conversion and makes it easier to compare data across studies and disciplines.

Usually, only administrators can create or modify dimensions. Once defined, these dimensions are available system-wide and are automatically referenced when users assign units to variables during dataset creation or editing. This design ensures consistency and prevents redundant definitions of measurement concepts.


### Creating a New Dimension

To define a new dimension:

1. Navigate to **Settings → Manage Dimensions**.  
2. On the **Manage Dimensions** page, click the **plus icon (+)** to create a new dimension.  
3. Fill out the form with the required and optional fields. Fields marked with a red asterisk (*) are mandatory:

   - **Name (required)**: Provide a clear and unique name, preferably based on international standards such as the *International System of Units (SI)*. Avoid abbreviations or internal codes.
   - **Specification (required)**: Define the mathematical structure using base units.  
     Example: `L(1,0)M(0,0)T(0,0)I(0,0)Θ(0,0)N(0,0)J(0,0)`
   - **Description (required)**: Briefly describe the context or usage of the dimension, e.g., _"Used for time-based units like seconds or minutes."_
     
> **Note**:  
> Dimensions refer to the physical properties of variables. In BEXIS2, a dimension consists of base dimension abbreviations (e.g., L, M) followed by a pair of exponents (positive, negative).

#### Base Dimension Components

| Symbol | Component              |
|--------|------------------------|
| **L**  | Length                 |
| **M**  | Mass                   |
| **T**  | Time                   |
| **I**  | Electric Current       |
| **Θ**  | Temperature            |
| **N**  | Amount of Substance    |
| **J**  | Luminous Intensity     |

Once all required fields are completed, the **Save** button (floppy disk icon) becomes active. Click it to save the new dimension.

To cancel the entry, click the **X** (cancel icon).

![Create dataset I](https://github.com/BEXIS2/Documents/raw/master/Docs/Images/DataDescription_ManageDimension.png)

### Editing a Dimension

> **Note**: Editing is only possible if the dimension is not currently in use.

1. Navigate to **Settings → Manage Dimensions**.  
2. Locate the dimension in the list and click the **Edit icon** on the right-hand side.  
3. Make your changes and click **Save** to apply them.


### Deleting a Dimension

> **Note**: Deletion is only possible if the dimension is not referenced by any unit.

1. Navigate to **Settings → Manage Dimensions**.  
2. Find the dimension and click the **Delete icon** on the right-hand side.  
3. A confirmation dialog appears showing the dimension’s name and specification.  
4. Click **Confirm** to permanently delete the dimension.

### Best Practices for Managing Dimensions

- ✅ Use **standardized and descriptive names** for better clarity and reuse.  
- ✅ **Check existing entries** to avoid duplicates.  
- ✅ Follow the **SI system structure** when defining specifications.  
- ✅ Keep **descriptions concise but informative**.  
- ✅ Regularly **review and remove unused dimensions**.



## Meanings
## External Links
## Prefix Categories
