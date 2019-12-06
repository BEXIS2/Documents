# Business Adminstration (v2.13)

## A: Overview

Party package is managing all kinds of entities such as people, organizations, projects and etc. it is also managing the relationship between them. For example, one person is a part of a project for a certain duration. Furthermore, it is able to connect to the other modules which now it is connected to the security module and also it is able to import the definitions such as “partytypes”, “customattributes” and “relationshiptype” from an XML file.

## B: Manual for users

### Manage profile data
...

## C: Manual for administrators

### 1 XML-Schema

The schema is defined in the file *PartyTypes.xml* which is located in the workspace under *…\Workspace\Modules\BAM*. 
Here you can define the *party types* and their *custom attribues* together with *realtionship types*.

**[ ]** optional attributes
 
#### 1.1 PartyType attributes

|         |           |
| ------- |:--------| 
| **Name:** | Party type name should be unique among the other party types. It is better to avoid spaces and special characters.
| **[DisplayName]** | Name shown in the UI. If not set, the **Name** is used, which might be not very user-friendly.

#### 1.2 Attribute attributes:
Each party type has some custom attributes.

|         |           |
| ------- |:--------| 
| **Name:** | Name of the custom attribute.
| **[DisplayName]** | Name shown in the UI. If not set, the **Name** is used, which might be not very user-friendly.
| **[Type]** | By default it is considered as “String” and will show a text box to user. It could be “bool” which shows two radio buttons with true/false values to user.
| **[IsMain]** |every party should have a name and it comes from its custom attributes. If there are more than one “IsMain” attribute it will merge them together by space. In the picture above for “PersonMember”, name and family are the main fields for example. It is false by default.
| **[ValidValues]** |If a dropdownlist needs , this attribute is useful. Values should be separated by a “,”.
| **[IsUnique]** | By default it is false but if it is set to true it means that this attribute of this party should be unique among the other parties which has the same party type. 
| **[IsValueOptional]** |  By default it is true but if it is set to false user has to fill this field.
| **[Description]** | Shows some extra information as a tooltip to user.

  
#### 1.3 PartyRelationshipType attributes**

|         |         |
| ------- |:--------| 
| **Name** | PartyrelationshipType name should be unique among the others. It is better to avoid spaces and special characters.
| **[DisplayName]** | Name shown in the UI. If not set, the **Name** is used, which might be not very user-friendly.
| **[Description]** | It shows some info about this type to user in a tooltip.
| **[IndicatesHierarchy]** | If it is set to true it means that there is a hierarchy relationship between all the pairs as the source is root and target is the child of it.
| **[MaxCardinality]** |  By default it is unlimited and if it is set to a number it forces the user to not have more than this number relationships.
| **[MinCardinality]** | By default it is unlimited and if it is set to a number it forces the user to have at least this number relationships.

#### 1.4 PartyTypePair attributes

|         |         |
| ------- |:--------| 
| **Title**  | The title of this pair.
| **AllowedSource** | source party type is obligatory and should be exactly the same name as we defined for partytype.
| **AllowedTarget** | Target party type is obligatory and should be exactly the same name as we defined for partytype.
| **[Description]** | It shows some info about this type to user in a tooltip.



### 2 Manage parties
The user can see, create, edit and delete the parties

In this page, you can see all the available entities and manage them. The red warning icon in action-required column shows that this party needs some relationships to be valid.
 
#### 2.1 Create and Edit
In first step, you should select party type and its date range. Click on Next you will navigate to the next step.
 
Here depends on the selected party type you will see some additional attributes. You have to fill the required fields. 
 
For Some party types, you have to make relationships. If you do not do, that party will be saved but it is not valid. You can add relationship later as well.
 
To edit a party you will navigate to this page again. You are able to change all the fields except party type.

#### 2.1 Delete
 
### 3 Manage Relationships
#### 3.1 Create
Every party could have some relationships with the other parties. Party relationships tab in edit or create party is to manage these relationships. 
  To create a new relationship, click on create and you see the following window. Here you see all the available party relationship types depend on the definitions, which we already defined. The numbers in parentheses shows the number of current relationships and the maximum relationships that this party to this relationship type can have. 

 
Clicking on one of them, you see some more options and available parties to make relationship. 
 
Selecting a party, it asks you to enter some information and by default, it fills some of the fields. Title here is the title of this relationship, start and end date are important and will set the duration of this relationship. This duration should be fit to the duration of source party and the target party otherwise, you will face to an error.
 
You will face to this error if there is no party or party relationship type defined.
 

#### 3.2 Edit and view a relationship
Clicking on edit icon (pencil figure) on last column of each relationships, you are able to edit the relationship. Moreover, clicking on the view icon (eye figure), you are able to see the detail of a relationship.
 
 
 

#### 3.3 Delete a relationship
Clicking on delete icon (trash figure) on last column of each relationships, you are able to delete a relationship if the minimum cardinality of its relationship type preserved.
 



## Account registration

After creating an account, other information of user will save in party package . Before using this page we shoud set some configuration to clear the allowed party types which are related to the account and also the relationships which you want to ask user in registration page.
 
### Configuration
Party types related to the account should be defined in setting.xml, which you can find it in BAM workspace folder. A comma should separate party types and each of them could have zero or multi allowed relationship. If the relationship type has one ‘partytypepair’, the registration page will populate all the parties, which has the same party type as this type pair. If the relationship type has more than one 'partytypepair', it will populate the allowed target of the 'partytypepair' which has "partyrelationshiptypedefault==true" this attribute and if it doesn’t have this attribute it will use the first party type pair by default.

```
Example: 
PartyType1:PartyRelationshipTypeTitle1-PartyRelationshipTypeTitle2, PartyType2
```
 
