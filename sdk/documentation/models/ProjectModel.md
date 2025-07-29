# ProjectModel

**Properties**

| Name              | Type                          | Required | Description                                                                                             |
| :---------------- | :---------------------------- | :------- | :------------------------------------------------------------------------------------------------------ |
| \_type            | ProjectModelType              | ❌       |                                                                                                         |
| id                | number                        | ❌       | Projects' id                                                                                            |
| identifier        | string                        | ❌       |                                                                                                         |
| name              | string                        | ❌       |                                                                                                         |
| active            | boolean                       | ❌       | Indicates whether the project is currently active or already archived                                   |
| statusExplanation | ProjectModelStatusExplanation | ❌       | A text detailing and explaining why the project has the reported status                                 |
| public            | boolean                       | ❌       | Indicates whether the project is accessible for everybody                                               |
| description       | Formattable                   | ❌       |                                                                                                         |
| createdAt         | string                        | ❌       | Time of creation. Can be writable by admins with the `apiv3_write_readonly_attributes` setting enabled. |
| updatedAt         | string                        | ❌       | Time of the most recent change to the project                                                           |
| \_links           | ProjectModelLinks             | ❌       |                                                                                                         |

# ProjectModelType

**Properties**

| Name    | Type   | Required | Description |
| :------ | :----- | :------- | :---------- |
| PROJECT | string | ✅       | "Project"   |

# ProjectModelStatusExplanation

A text detailing and explaining why the project has the reported status

**Properties**

| Name   | Type                     | Required | Description                                        |
| :----- | :----------------------- | :------- | :------------------------------------------------- |
| format | StatusExplanationFormat1 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string                   | ❌       | The raw text, as entered by the user               |
| html   | string                   | ❌       | The text converted to HTML according to the format |

# StatusExplanationFormat1

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# ProjectModelLinks

**Properties**

| Name                         | Type                                 | Required | Description                                                                                                                                                               |
| :--------------------------- | :----------------------------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| self                         | \_LinksSelf39                        | ✅       | This project **Resource**: Project                                                                                                                                        |
| categories                   | \_LinksCategories1                   | ✅       | Categories available in this project **Resource**: Collection                                                                                                             |
| types                        | \_LinksTypes2                        | ✅       | Types available in this project **Resource**: Collection # Conditions **Permission**: view work packages or manage types                                                  |
| versions                     | \_LinksVersions1                     | ✅       | Versions available in this project **Resource**: Collection # Conditions **Permission**: view work packages or manage versions                                            |
| memberships                  | \_LinksMemberships2                  | ✅       | Memberships in the project **Resource**: Collection # Conditions **Permission**: view members                                                                             |
| workPackages                 | \_LinksWorkPackages2                 | ✅       | Work Packages of this project **Resource**: Collection                                                                                                                    |
| update                       | \_LinksUpdate5                       | ❌       | Form endpoint that aids in updating this project # Conditions **Permission**: edit project                                                                                |
| updateImmediately            | \_LinksUpdateImmediately5            | ❌       | Directly update this project # Conditions **Permission**: edit project                                                                                                    |
| delete                       | \_LinksDelete9                       | ❌       | Delete this project # Conditions **Permission**: admin                                                                                                                    |
| createWorkPackage            | \_LinksCreateWorkPackage1            | ❌       | Form endpoint that aids in preparing and creating a work package # Conditions **Permission**: add work packages                                                           |
| createWorkPackageImmediately | \_LinksCreateWorkPackageImmediately1 | ❌       | Directly creates a work package in the project # Conditions **Permission**: add work packages                                                                             |
| parent                       | \_LinksParent4                       | ❌       | Parent project of the project **Resource**: Project # Conditions **Permission** edit project                                                                              |
| status                       | \_LinksStatus4                       | ❌       | Denotes the status of the project, so whether the project is on track, at risk or is having trouble. **Resource**: ProjectStatus # Conditions **Permission** edit project |
| storages                     | \_LinksStorages1[]                   | ❌       |                                                                                                                                                                           |
| projectStorages              | \_LinksProjectStorages1              | ❌       | The project storage collection of this project. **Resource**: Collection # Conditions **Permission**: view_file_links                                                     |
| ancestors                    | \_LinksAncestors3[]                  | ❌       |                                                                                                                                                                           |

# \_LinksSelf39

This project **Resource**: Project

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

# \_LinksCategories1

Categories available in this project **Resource**: Collection

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

# \_LinksTypes2

Types available in this project **Resource**: Collection # Conditions **Permission**: view work packages or manage types

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

# \_LinksVersions1

Versions available in this project **Resource**: Collection # Conditions **Permission**: view work packages or manage versions

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

# \_LinksMemberships2

Memberships in the project **Resource**: Collection # Conditions **Permission**: view members

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

# \_LinksWorkPackages2

Work Packages of this project **Resource**: Collection

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

# \_LinksUpdate5

Form endpoint that aids in updating this project # Conditions **Permission**: edit project

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

# \_LinksUpdateImmediately5

Directly update this project # Conditions **Permission**: edit project

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

# \_LinksDelete9

Delete this project # Conditions **Permission**: admin

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

# \_LinksCreateWorkPackage1

Form endpoint that aids in preparing and creating a work package # Conditions **Permission**: add work packages

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

# \_LinksCreateWorkPackageImmediately1

Directly creates a work package in the project # Conditions **Permission**: add work packages

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

# \_LinksParent4

Parent project of the project **Resource**: Project # Conditions **Permission** edit project

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

# \_LinksStatus4

Denotes the status of the project, so whether the project is on track, at risk or is having trouble. **Resource**: ProjectStatus # Conditions **Permission** edit project

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

# \_LinksStorages1

The link to a storage that is active for this project. **Resource**: Storage # Conditions **Permission**: view_file_links

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

# \_LinksProjectStorages1

The project storage collection of this project. **Resource**: Collection # Conditions **Permission**: view_file_links

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

# \_LinksAncestors3

The link to an ancestor project. **Resource**: Project

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
