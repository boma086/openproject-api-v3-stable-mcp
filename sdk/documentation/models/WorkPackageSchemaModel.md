# WorkPackageSchemaModel

A schema for a work package. This schema defines the attributes of a work package. TODO: Incomplete, needs to be updated with the real behaviour of schemas (when does which attribute appear?).

**Properties**

| Name                  | Type                        | Required | Description                         |
| :-------------------- | :-------------------------- | :------- | :---------------------------------- |
| \_type                | WorkPackageSchemaModelType  | ❌       |                                     |
| \_dependencies        | string[]                    | ❌       | TBD                                 |
| \_attributeGroups     | any[]                       | ❌       | TBD (WorkPackageFormAttributeGroup) |
| lockVersion           | SchemaPropertyModel         | ❌       |                                     |
| id                    | SchemaPropertyModel         | ❌       |                                     |
| subject               | SchemaPropertyModel         | ❌       |                                     |
| description           | SchemaPropertyModel         | ❌       |                                     |
| duration              | SchemaPropertyModel         | ❌       |                                     |
| scheduleManually      | SchemaPropertyModel         | ❌       |                                     |
| ignoreNonWorkingDays  | SchemaPropertyModel         | ❌       |                                     |
| startDate             | SchemaPropertyModel         | ❌       |                                     |
| dueDate               | SchemaPropertyModel         | ❌       |                                     |
| derivedStartDate      | SchemaPropertyModel         | ❌       |                                     |
| derivedDueDate        | SchemaPropertyModel         | ❌       |                                     |
| estimatedTime         | SchemaPropertyModel         | ❌       |                                     |
| derivedEstimatedTime  | SchemaPropertyModel         | ❌       |                                     |
| remainingTime         | SchemaPropertyModel         | ❌       |                                     |
| derivedRemainingTime  | SchemaPropertyModel         | ❌       |                                     |
| percentageDone        | SchemaPropertyModel         | ❌       |                                     |
| derivedPercentageDone | SchemaPropertyModel         | ❌       |                                     |
| readonly              | SchemaPropertyModel         | ❌       |                                     |
| createdAt             | SchemaPropertyModel         | ❌       |                                     |
| updatedAt             | SchemaPropertyModel         | ❌       |                                     |
| author                | SchemaPropertyModel         | ❌       |                                     |
| project               | SchemaPropertyModel         | ❌       |                                     |
| parent                | SchemaPropertyModel         | ❌       |                                     |
| assignee              | SchemaPropertyModel         | ❌       |                                     |
| responsible           | SchemaPropertyModel         | ❌       |                                     |
| type                  | SchemaPropertyModel         | ❌       |                                     |
| status                | SchemaPropertyModel         | ❌       |                                     |
| category              | SchemaPropertyModel         | ❌       |                                     |
| version               | SchemaPropertyModel         | ❌       |                                     |
| priority              | SchemaPropertyModel         | ❌       |                                     |
| \_links               | WorkPackageSchemaModelLinks | ❌       |                                     |

# WorkPackageSchemaModelType

**Properties**

| Name   | Type   | Required | Description |
| :----- | :----- | :------- | :---------- |
| SCHEMA | string | ✅       | "Schema"    |

# WorkPackageSchemaModelLinks

**Properties**

| Name | Type          | Required | Description                                   |
| :--- | :------------ | :------- | :-------------------------------------------- |
| self | \_LinksSelf56 | ❌       | This work package schema **Resource**: Schema |

# \_LinksSelf56

This work package schema **Resource**: Schema

**Properties**

| Name       | Type    | Required | Description                                                            |
| :--------- | :------ | :------- | :--------------------------------------------------------------------- |
| href       | string  | ✅       | URL to the referenced resource (might be relative)                     |
| title      | string  | ❌       | Representative label for the resource                                  |
| templated  | boolean | ❌       | If true the href contains parts that need to be replaced by the client |
| method     | string  | ❌       | The HTTP verb to use when requesting the resource                      |
| payload    | any     | ❌       | The payload to send in the request to achieve the desired result       |
| identifier | string  | ❌       | An optional unique identifier to the link object                       |
| type       | string  | ❌       | The MIME-Type of the returned resource.                                |

<!-- This file was generated by liblab | https://liblab.com/ -->
