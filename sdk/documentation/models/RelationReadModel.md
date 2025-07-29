# RelationReadModel

**Properties**

| Name        | Type                      | Required | Description                                                            |
| :---------- | :------------------------ | :------- | :--------------------------------------------------------------------- |
| \_type      | RelationReadModelType1    | ❌       |                                                                        |
| id          | number                    | ❌       | Relation ID                                                            |
| name        | string                    | ❌       | The internationalised name of this type of relation                    |
| type        | RelationReadModelType2    | ❌       | The relation type.                                                     |
| reverseType | ReverseType               | ❌       | The type of relation from the perspective of the related work package. |
| description | string                    | ❌       | A descriptive text for the relation.                                   |
| lag         | number                    | ❌       | The lag in days between closing of `from` and start of `to`            |
| \_embedded  | RelationReadModelEmbedded | ❌       |                                                                        |
| \_links     | RelationReadModelLinks    | ❌       |                                                                        |

# RelationReadModelType1

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| RELATION | string | ✅       | "Relation"  |

# RelationReadModelType2

The relation type.

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| RELATES    | string | ✅       | "relates"    |
| DUPLICATES | string | ✅       | "duplicates" |
| DUPLICATED | string | ✅       | "duplicated" |
| BLOCKS     | string | ✅       | "blocks"     |
| BLOCKED    | string | ✅       | "blocked"    |
| PRECEDES   | string | ✅       | "precedes"   |
| FOLLOWS    | string | ✅       | "follows"    |
| INCLUDES   | string | ✅       | "includes"   |
| PARTOF     | string | ✅       | "partof"     |
| REQUIRES   | string | ✅       | "requires"   |
| REQUIRED   | string | ✅       | "required"   |

# ReverseType

The type of relation from the perspective of the related work package.

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| RELATES    | string | ✅       | "relates"    |
| DUPLICATES | string | ✅       | "duplicates" |
| DUPLICATED | string | ✅       | "duplicated" |
| BLOCKS     | string | ✅       | "blocks"     |
| BLOCKED    | string | ✅       | "blocked"    |
| PRECEDES   | string | ✅       | "precedes"   |
| FOLLOWS    | string | ✅       | "follows"    |
| INCLUDES   | string | ✅       | "includes"   |
| PARTOF     | string | ✅       | "partof"     |
| REQUIRES   | string | ✅       | "requires"   |
| REQUIRED   | string | ✅       | "required"   |

# RelationReadModelEmbedded

**Properties**

| Name | Type             | Required | Description |
| :--- | :--------------- | :------- | :---------- |
| from | WorkPackageModel | ❌       |             |
| to   | WorkPackageModel | ❌       |             |

# RelationReadModelLinks

**Properties**

| Name              | Type                       | Required | Description                                                                                                     |
| :---------------- | :------------------------- | :------- | :-------------------------------------------------------------------------------------------------------------- |
| self              | \_LinksSelf68              | ❌       | This relation **Resource**: Relation # Conditions **Permission**: view work packages                            |
| updateImmediately | \_LinksUpdateImmediately16 | ❌       | Updates the relation between two work packages # Conditions **Permission**: manage work package relations       |
| delete            | \_LinksDelete16            | ❌       | Destroys the relation between the two work packages # Conditions **Permission**: manage work package relations  |
| from              | From\_                     | ❌       | The emanating work package **Resource**: WorkPackage # Conditions **Permission**: view work packages            |
| to                | \_LinksTo1                 | ❌       | The work package the relation ends in **Resource**: WorkPackage # Conditions **Permission**: view work packages |

# \_LinksSelf68

This relation **Resource**: Relation # Conditions **Permission**: view work packages

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

# \_LinksUpdateImmediately16

Updates the relation between two work packages # Conditions **Permission**: manage work package relations

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

# \_LinksDelete16

Destroys the relation between the two work packages # Conditions **Permission**: manage work package relations

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

# From\_

The emanating work package **Resource**: WorkPackage # Conditions **Permission**: view work packages

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

# \_LinksTo1

The work package the relation ends in **Resource**: WorkPackage # Conditions **Permission**: view work packages

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
