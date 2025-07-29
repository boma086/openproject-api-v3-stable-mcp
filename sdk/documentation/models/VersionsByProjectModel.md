# VersionsByProjectModel

**Properties**

| Name       | Type                           | Required | Description                                               |
| :--------- | :----------------------------- | :------- | :-------------------------------------------------------- |
| \_type     | VersionsByProjectModelType     | ✅       |                                                           |
| total      | number                         | ✅       | The total amount of elements available in the collection. |
| count      | number                         | ✅       | Actual amount of elements in this response.               |
| \_links    | VersionsByProjectModelLinks    | ✅       |                                                           |
| \_embedded | VersionsByProjectModelEmbedded | ✅       |                                                           |

# VersionsByProjectModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# VersionsByProjectModelLinks

**Properties**

| Name | Type          | Required | Description                                              |
| :--- | :------------ | :------- | :------------------------------------------------------- |
| self | \_LinksSelf64 | ✅       | The versions collection **Resource**: VersionsCollection |

# \_LinksSelf64

The versions collection **Resource**: VersionsCollection

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

# VersionsByProjectModelEmbedded

**Properties**

| Name     | Type                   | Required | Description |
| :------- | :--------------------- | :------- | :---------- |
| elements | \_EmbeddedElements10[] | ❌       |             |

# \_EmbeddedElements10

Collection of Versions

**Properties**

| Name        | Type                 | Required | Description                                   |
| :---------- | :------------------- | :------- | :-------------------------------------------- |
| name        | string               | ✅       | Version name                                  |
| status      | string               | ✅       | The current status of the version             |
| sharing     | string               | ✅       | The current status of the version             |
| createdAt   | string               | ✅       | Time of creation                              |
| updatedAt   | string               | ✅       | Time of the most recent change to the version |
| id          | number               | ❌       | Version id                                    |
| description | ElementsDescription3 | ❌       |                                               |
| startDate   | string               | ❌       |                                               |
| endDate     | string               | ❌       |                                               |
| \_links     | ElementsLinks8       | ❌       |                                               |

# ElementsDescription3

**Properties**

| Name   | Type               | Required | Description                                        |
| :----- | :----------------- | :------- | :------------------------------------------------- |
| format | DescriptionFormat9 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string             | ❌       | The raw text, as entered by the user               |
| html   | string             | ❌       | The text converted to HTML according to the format |

# DescriptionFormat9

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# ElementsLinks8

**Properties**

| Name                | Type                        | Required | Description                                                                                                           |
| :------------------ | :-------------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------- |
| self                | \_LinksSelf65               | ✅       | This version **Resource**: Version                                                                                    |
| availableInProjects | \_LinksAvailableInProjects1 | ✅       | Projects where this version can be used **Resource**: Projects                                                        |
| update              | \_LinksUpdate9              | ❌       | Form endpoint that aids in preparing and performing edits on the version # Conditions **Permission**: manage versions |
| updateImmediately   | \_LinksUpdateImmediately14  | ❌       | Directly perform edits on the version # Conditions **Permission**: manage versions                                    |
| definingProject     | \_LinksDefiningProject1     | ❌       | The project to which the version belongs **Resource**: Project                                                        |

# \_LinksSelf65

This version **Resource**: Version

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

# \_LinksAvailableInProjects1

Projects where this version can be used **Resource**: Projects

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

# \_LinksUpdate9

Form endpoint that aids in preparing and performing edits on the version # Conditions **Permission**: manage versions

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

# \_LinksUpdateImmediately14

Directly perform edits on the version # Conditions **Permission**: manage versions

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

# \_LinksDefiningProject1

The project to which the version belongs **Resource**: Project

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
