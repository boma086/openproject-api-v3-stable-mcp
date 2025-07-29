# VersionModel

**Properties**

| Name        | Type                    | Required | Description                                   |
| :---------- | :---------------------- | :------- | :-------------------------------------------- |
| name        | string                  | ✅       | Version name                                  |
| status      | string                  | ✅       | The current status of the version             |
| sharing     | string                  | ✅       | The current status of the version             |
| createdAt   | string                  | ✅       | Time of creation                              |
| updatedAt   | string                  | ✅       | Time of the most recent change to the version |
| id          | number                  | ❌       | Version id                                    |
| description | VersionModelDescription | ❌       |                                               |
| startDate   | string                  | ❌       |                                               |
| endDate     | string                  | ❌       |                                               |
| \_links     | VersionModelLinks       | ❌       |                                               |

# VersionModelDescription

**Properties**

| Name   | Type                | Required | Description                                        |
| :----- | :------------------ | :------- | :------------------------------------------------- |
| format | DescriptionFormat10 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string              | ❌       | The raw text, as entered by the user               |
| html   | string              | ❌       | The text converted to HTML according to the format |

# DescriptionFormat10

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# VersionModelLinks

**Properties**

| Name                | Type                        | Required | Description                                                                                                           |
| :------------------ | :-------------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------- |
| self                | \_LinksSelf66               | ✅       | This version **Resource**: Version                                                                                    |
| availableInProjects | \_LinksAvailableInProjects2 | ✅       | Projects where this version can be used **Resource**: Projects                                                        |
| update              | \_LinksUpdate10             | ❌       | Form endpoint that aids in preparing and performing edits on the version # Conditions **Permission**: manage versions |
| updateImmediately   | \_LinksUpdateImmediately15  | ❌       | Directly perform edits on the version # Conditions **Permission**: manage versions                                    |
| definingProject     | \_LinksDefiningProject2     | ❌       | The project to which the version belongs **Resource**: Project                                                        |

# \_LinksSelf66

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

# \_LinksAvailableInProjects2

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

# \_LinksUpdate10

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

# \_LinksUpdateImmediately15

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

# \_LinksDefiningProject2

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
