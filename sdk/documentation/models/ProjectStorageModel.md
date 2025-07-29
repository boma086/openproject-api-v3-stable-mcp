# ProjectStorageModel

**Properties**

| Name              | Type                     | Required | Description                                           |
| :---------------- | :----------------------- | :------- | :---------------------------------------------------- |
| \_type            | ProjectStorageModelType  | ✅       |                                                       |
| id                | number                   | ✅       | The project storage's id                              |
| projectFolderMode | ProjectFolderMode        | ✅       |                                                       |
| createdAt         | string                   | ✅       | Time of creation                                      |
| updatedAt         | string                   | ✅       | Time of the most recent change to the project storage |
| \_links           | ProjectStorageModelLinks | ❌       |                                                       |

# ProjectStorageModelType

**Properties**

| Name            | Type   | Required | Description      |
| :-------------- | :----- | :------- | :--------------- |
| PROJECT_STORAGE | string | ✅       | "ProjectStorage" |

# ProjectFolderMode

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| INACTIVE | string | ✅       | "inactive"  |
| MANUAL   | string | ✅       | "manual"    |

# ProjectStorageModelLinks

**Properties**

| Name                      | Type                      | Required | Description                                                                                                                                                                              |
| :------------------------ | :------------------------ | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| self                      | \_LinksSelf28             | ✅       | This project storage. **Resource**: ProjectStorage                                                                                                                                       |
| creator                   | \_LinksCreator2           | ✅       | The user who created the project storage. **Resource**: User                                                                                                                             |
| storage                   | \_LinksStorage2           | ✅       | The storage resource, that is linked to a project with this project storage. **Resource**: Storage                                                                                       |
| project                   | \_LinksProject6           | ✅       | The project resource, that is linked to a storage with this project storage. **Resource**: Project                                                                                       |
| projectFolder             | ProjectFolder             | ❌       | The directory on the storage that is used as a project folder. **Resource**: StorageFile # Conditions Only provided, if the `projectFolderMode` is `manual` or `automatic`.              |
| open                      | \_LinksOpen2              | ❌       | A link to OpenProject strorage.                                                                                                                                                          |
| openWithConnectionEnsured | OpenWithConnectionEnsured | ❌       | A link to OpenProject storage with making sure user has access to it. # Conditions If the storage has not been configured(oauth client is missing, for instance), then the link is null. |

# \_LinksSelf28

This project storage. **Resource**: ProjectStorage

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

# \_LinksCreator2

The user who created the project storage. **Resource**: User

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

# \_LinksStorage2

The storage resource, that is linked to a project with this project storage. **Resource**: Storage

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

# \_LinksProject6

The project resource, that is linked to a storage with this project storage. **Resource**: Project

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

# ProjectFolder

The directory on the storage that is used as a project folder. **Resource**: StorageFile # Conditions Only provided, if the `projectFolderMode` is `manual` or `automatic`.

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

# \_LinksOpen2

A link to OpenProject strorage.

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

# OpenWithConnectionEnsured

A link to OpenProject storage with making sure user has access to it. # Conditions If the storage has not been configured(oauth client is missing, for instance), then the link is null.

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
