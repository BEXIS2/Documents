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
5. Click **Save** (floppy) button) to apply your changes.

> **Note:** If the unit is already assigned to a variable, changes will take effect immediately wherever that unit is used. Be cautious when editing units that are used in multiple places.



### Deleting a Unit

You can also remove units that are not used in the system. To remove a unit:

1. Go to the main menu and select **Manage Units** under **Settings** to open the Manage Units page.  
2. In the table, select the unit you want to delete.  
3. Click the **Delete** icon.  
4. Confirm the deletion in the confirmation popup.

> **Note:** Units that are already used in a dataset cannot be deleted until those assignments are removed. Always check whether a unit is in use before attempting to delete it. If you try to delete a unit that is in use, an error message will appear, and the unit cannot be deleted.

### Best Practices for Managing Units
- Use clear, standardized names and abbreviations based on international conventions.
-  Avoid creating duplicate units.
- Use the same schema for derived units (kg·m/s²)
- Provide meaningful descriptions to help users select the correct unit.  
- Assign the correct data types and dimensions to prevent misuse.  
- Only delete units after confirming they are not in use.



## Constraints
## Dimensions
## Meanings
## External Links
## Prefix Categories
