# ListAvailableParentProjectCandidatesModel

**Properties**

| Name       | Type                                              | Required | Description                                               |
| :--------- | :------------------------------------------------ | :------- | :-------------------------------------------------------- |
| \_type     | ListAvailableParentProjectCandidatesModelType     | ✅       |                                                           |
| total      | number                                            | ✅       | The total amount of elements available in the collection. |
| count      | number                                            | ✅       | Actual amount of elements in this response.               |
| \_links    | ListAvailableParentProjectCandidatesModelLinks    | ✅       |                                                           |
| \_embedded | ListAvailableParentProjectCandidatesModelEmbedded | ✅       |                                                           |

# ListAvailableParentProjectCandidatesModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# ListAvailableParentProjectCandidatesModelLinks

**Properties**

| Name | Type          | Required | Description                                            |
| :--- | :------------ | :------- | :----------------------------------------------------- |
| self | \_LinksSelf52 | ✅       | The project collection **Resource**: ProjectCollection |

# \_LinksSelf52

The project collection **Resource**: ProjectCollection

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

# ListAvailableParentProjectCandidatesModelEmbedded

**Properties**

| Name     | Type                  | Required | Description |
| :------- | :-------------------- | :------- | :---------- |
| elements | \_EmbeddedElements6[] | ❌       |             |

# \_EmbeddedElements6

Collection of projects

**Properties**

| Name              | Type                      | Required | Description                                                                                             |
| :---------------- | :------------------------ | :------- | :------------------------------------------------------------------------------------------------------ |
| \_type            | ElementsType2             | ❌       |                                                                                                         |
| id                | number                    | ❌       | Projects' id                                                                                            |
| identifier        | string                    | ❌       |                                                                                                         |
| name              | string                    | ❌       |                                                                                                         |
| active            | boolean                   | ❌       | Indicates whether the project is currently active or already archived                                   |
| statusExplanation | ElementsStatusExplanation | ❌       | A text detailing and explaining why the project has the reported status                                 |
| public            | boolean                   | ❌       | Indicates whether the project is accessible for everybody                                               |
| description       | Formattable               | ❌       |                                                                                                         |
| createdAt         | string                    | ❌       | Time of creation. Can be writable by admins with the `apiv3_write_readonly_attributes` setting enabled. |
| updatedAt         | string                    | ❌       | Time of the most recent change to the project                                                           |
| \_links           | ElementsLinks4            | ❌       |                                                                                                         |

# ElementsType2

**Properties**

| Name    | Type   | Required | Description |
| :------ | :----- | :------- | :---------- |
| PROJECT | string | ✅       | "Project"   |

# ElementsStatusExplanation

A text detailing and explaining why the project has the reported status

**Properties**

| Name   | Type                     | Required | Description                                        |
| :----- | :----------------------- | :------- | :------------------------------------------------- |
| format | StatusExplanationFormat2 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string                   | ❌       | The raw text, as entered by the user               |
| html   | string                   | ❌       | The text converted to HTML according to the format |

# StatusExplanationFormat2

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# ElementsLinks4

**Properties**

| Name                         | Type                                 | Required | Description                                                                                                                                                               |
| :--------------------------- | :----------------------------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| self                         | \_LinksSelf53                        | ✅       | This project **Resource**: Project                                                                                                                                        |
| categories                   | \_LinksCategories2                   | ✅       | Categories available in this project **Resource**: Collection                                                                                                             |
| types                        | \_LinksTypes3                        | ✅       | Types available in this project **Resource**: Collection # Conditions **Permission**: view work packages or manage types                                                  |
| versions                     | \_LinksVersions2                     | ✅       | Versions available in this project **Resource**: Collection # Conditions **Permission**: view work packages or manage versions                                            |
| memberships                  | \_LinksMemberships3                  | ✅       | Memberships in the project **Resource**: Collection # Conditions **Permission**: view members                                                                             |
| workPackages                 | \_LinksWorkPackages3                 | ✅       | Work Packages of this project **Resource**: Collection                                                                                                                    |
| update                       | \_LinksUpdate7                       | ❌       | Form endpoint that aids in updating this project # Conditions **Permission**: edit project                                                                                |
| updateImmediately            | \_LinksUpdateImmediately10           | ❌       | Directly update this project # Conditions **Permission**: edit project                                                                                                    |
| delete                       | \_LinksDelete13                      | ❌       | Delete this project # Conditions **Permission**: admin                                                                                                                    |
| createWorkPackage            | \_LinksCreateWorkPackage2            | ❌       | Form endpoint that aids in preparing and creating a work package # Conditions **Permission**: add work packages                                                           |
| createWorkPackageImmediately | \_LinksCreateWorkPackageImmediately2 | ❌       | Directly creates a work package in the project # Conditions **Permission**: add work packages                                                                             |
| parent                       | \_LinksParent5                       | ❌       | Parent project of the project **Resource**: Project # Conditions **Permission** edit project                                                                              |
| status                       | \_LinksStatus5                       | ❌       | Denotes the status of the project, so whether the project is on track, at risk or is having trouble. **Resource**: ProjectStatus # Conditions **Permission** edit project |
| storages                     | \_LinksStorages2[]                   | ❌       |                                                                                                                                                                           |
| projectStorages              | \_LinksProjectStorages2              | ❌       | The project storage collection of this project. **Resource**: Collection # Conditions **Permission**: view_file_links                                                     |
| ancestors                    | \_LinksAncestors4[]                  | ❌       |                                                                                                                                                                           |

# \_LinksSelf53

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

# \_LinksCategories2

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

# \_LinksTypes3

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

# \_LinksVersions2

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

# \_LinksMemberships3

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

# \_LinksWorkPackages3

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

# \_LinksUpdate7

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

# \_LinksUpdateImmediately10

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

# \_LinksDelete13

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

# \_LinksCreateWorkPackage2

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

# \_LinksCreateWorkPackageImmediately2

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

# \_LinksParent5

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

# \_LinksStatus5

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

# \_LinksStorages2

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

# \_LinksProjectStorages2

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

# \_LinksAncestors4

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
