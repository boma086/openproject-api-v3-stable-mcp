# FileLinksService

A list of all methods in the `FileLinksService` service. Click on the method name to view detailed information about that method.

| Methods                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| :-------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [viewFileLink](#viewfilelink)                                   | Gets a single file link resource of a work package.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [deleteFileLink](#deletefilelink)                               | Removes a file link on a work package. The request contains only the file link identifier as a path parameter. No request body is needed.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [openFileLink](#openfilelink)                                   | Creates a uri to open the origin file linked by the given file link. This uri depends on the storage type and is always located on the origin storage itself.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [downloadFileLink](#downloadfilelink)                           | Creates a uri to download the origin file linked by the given file link. This uri depends on the storage type and is always located on the origin storage itself.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [listProjectStorages](#listprojectstorages)                     | Gets a collection of all project storages that meet the provided filters and the user has permission to see them.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [getProjectStorage](#getprojectstorage)                         | Gets a project storage resource. This resource contains all data that is applicable on the relation between a storage and a project.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [openProjectStorage](#openprojectstorage)                       | Gets a redirect to the location of the project storage's remote origin. If the project storage has a project folder, it is opened at this location. If not, the storage root is opened.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [listStorages](#liststorages)                                   | Returns a collection of storages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [createStorage](#createstorage)                                 | Creates a storage resource. When creating a storage, a confidential OAuth 2 provider application is created automatically. The oauth client id and secret of the created OAuth application are returned in the response. **IMPORTANT:** This is the only time, the oauth client secret is visible to the consumer. After that, the secret is hidden. To update the storage with OAuth client credentials, which enable the storage resource to behave as an OAuth 2 client against an external OAuth 2 provider application, another request must be made to create those, see `POST /api/v3/storages/{id}/oauth_client_credentials`. |
| [getStorage](#getstorage)                                       | Gets a storage resource. As a side effect, a live connection to the storages origin is established to retrieve connection state data.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [updateStorage](#updatestorage)                                 | Updates a storage resource. Only data that is not generated by the server can be updated. This excludes the OAuth 2 application data.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [deleteStorage](#deletestorage)                                 | Deletes a storage resource. This also deletes all related records, like the created oauth application, client, and any file links created within this storage.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [getStorageFiles](#getstoragefiles)                             | Gets a collection of files from a storage. If no `parent` context is given, the result is the content of the document root. With `parent` context given, the result contains the collections of files/directories from within the given parent file id. If given `parent` context is no directory, `400 Bad Request` is returned.                                                                                                                                                                                                                                                                                                     |
| [prepareStorageFileUpload](#preparestoragefileupload)           | Executes a request that prepares a link for a direct upload to the storage. The background here is, that the client needs to make a direct request to the storage instance for file uploading, but should not get access to the credentials, which are stored in the backend. The response contains a link object, that enables the client to execute a file upload without the real credentials.                                                                                                                                                                                                                                     |
| [createStorageFolder](#createstoragefolder)                     | Creates a new folder under the given parent                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [createStorageOauthCredentials](#createstorageoauthcredentials) | Inserts the OAuth 2 credentials into the storage, to allow the storage to act as an OAuth 2 client. Calling this endpoint on a storage that already contains OAuth 2 client credentials will replace them.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [openStorage](#openstorage)                                     | Gets a redirect to the location of the storage's remote origin. The storage's files root should be the target location.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

## viewFileLink

Gets a single file link resource of a work package.

- HTTP Method: `GET`
- Endpoint: `/api/v3/file_links/{id}`

**Parameters**

| Name | Type   | Required | Description  |
| :--- | :----- | :------- | :----------- |
| id   | number | ✅       | File link id |

**Return Type**

`FileLinkReadModel`

**Example Usage Code Snippet**

```mcp

```

## deleteFileLink

Removes a file link on a work package. The request contains only the file link identifier as a path parameter. No request body is needed.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/file_links/{id}`

**Parameters**

| Name | Type   | Required | Description  |
| :--- | :----- | :------- | :----------- |
| id   | number | ✅       | File link id |

**Example Usage Code Snippet**

```mcp

```

## openFileLink

Creates a uri to open the origin file linked by the given file link. This uri depends on the storage type and is always located on the origin storage itself.

- HTTP Method: `GET`
- Endpoint: `/api/v3/file_links/{id}/open`

**Parameters**

| Name     | Type    | Required | Description                                                                                      |
| :------- | :------ | :------- | :----------------------------------------------------------------------------------------------- |
| id       | number  | ✅       | File link id                                                                                     |
| location | boolean | ❌       | Boolean flag indicating, if the file should be opened directly or rather the directory location. |

**Example Usage Code Snippet**

```mcp

```

## downloadFileLink

Creates a uri to download the origin file linked by the given file link. This uri depends on the storage type and is always located on the origin storage itself.

- HTTP Method: `GET`
- Endpoint: `/api/v3/file_links/{id}/download`

**Parameters**

| Name | Type   | Required | Description  |
| :--- | :----- | :------- | :----------- |
| id   | number | ✅       | File link id |

**Example Usage Code Snippet**

```mcp

```

## listProjectStorages

Gets a collection of all project storages that meet the provided filters and the user has permission to see them.

- HTTP Method: `GET`
- Endpoint: `/api/v3/project_storages`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                         |
| :------ | :----- | :------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: - project_id - storage_id - storage_url |

**Return Type**

`ProjectStorageCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## getProjectStorage

Gets a project storage resource. This resource contains all data that is applicable on the relation between a storage and a project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/project_storages/{id}`

**Parameters**

| Name | Type   | Required | Description        |
| :--- | :----- | :------- | :----------------- |
| id   | number | ✅       | Project storage id |

**Return Type**

`ProjectStorageModel`

**Example Usage Code Snippet**

```mcp

```

## openProjectStorage

Gets a redirect to the location of the project storage's remote origin. If the project storage has a project folder, it is opened at this location. If not, the storage root is opened.

- HTTP Method: `GET`
- Endpoint: `/api/v3/project_storages/{id}/open`

**Parameters**

| Name | Type   | Required | Description        |
| :--- | :----- | :------- | :----------------- |
| id   | number | ✅       | Project storage id |

**Example Usage Code Snippet**

```mcp

```

## listStorages

Returns a collection of storages.

- HTTP Method: `GET`
- Endpoint: `/api/v3/storages`

**Return Type**

`StorageCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createStorage

Creates a storage resource. When creating a storage, a confidential OAuth 2 provider application is created automatically. The oauth client id and secret of the created OAuth application are returned in the response. **IMPORTANT:** This is the only time, the oauth client secret is visible to the consumer. After that, the secret is hidden. To update the storage with OAuth client credentials, which enable the storage resource to behave as an OAuth 2 client against an external OAuth 2 provider application, another request must be made to create those, see `POST /api/v3/storages/{id}/oauth_client_credentials`.

- HTTP Method: `POST`
- Endpoint: `/api/v3/storages`

**Parameters**

| Name | Type                                                | Required | Description       |
| :--- | :-------------------------------------------------- | :------- | :---------------- |
| body | [StorageWriteModel](../models/StorageWriteModel.md) | ❌       | The request body. |

**Return Type**

`StorageReadModel`

**Example Usage Code Snippet**

```mcp

```

## getStorage

Gets a storage resource. As a side effect, a live connection to the storages origin is established to retrieve connection state data.

- HTTP Method: `GET`
- Endpoint: `/api/v3/storages/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Storage id  |

**Return Type**

`StorageReadModel`

**Example Usage Code Snippet**

```mcp

```

## updateStorage

Updates a storage resource. Only data that is not generated by the server can be updated. This excludes the OAuth 2 application data.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/storages/{id}`

**Parameters**

| Name | Type                                                | Required | Description       |
| :--- | :-------------------------------------------------- | :------- | :---------------- |
| body | [StorageWriteModel](../models/StorageWriteModel.md) | ❌       | The request body. |
| id   | number                                              | ✅       | Storage id        |

**Return Type**

`StorageReadModel`

**Example Usage Code Snippet**

```mcp

```

## deleteStorage

Deletes a storage resource. This also deletes all related records, like the created oauth application, client, and any file links created within this storage.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/storages/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Storage id  |

**Example Usage Code Snippet**

```mcp

```

## getStorageFiles

Gets a collection of files from a storage. If no `parent` context is given, the result is the content of the document root. With `parent` context given, the result contains the collections of files/directories from within the given parent file id. If given `parent` context is no directory, `400 Bad Request` is returned.

- HTTP Method: `GET`
- Endpoint: `/api/v3/storages/{id}/files`

**Parameters**

| Name   | Type   | Required | Description                |
| :----- | :----- | :------- | :------------------------- |
| id     | number | ✅       | Storage id                 |
| parent | string | ❌       | Parent file identification |

**Return Type**

`StorageFilesModel`

**Example Usage Code Snippet**

```mcp

```

## prepareStorageFileUpload

Executes a request that prepares a link for a direct upload to the storage. The background here is, that the client needs to make a direct request to the storage instance for file uploading, but should not get access to the credentials, which are stored in the backend. The response contains a link object, that enables the client to execute a file upload without the real credentials.

- HTTP Method: `POST`
- Endpoint: `/api/v3/storages/{id}/files/prepare_upload`

**Parameters**

| Name | Type                                                                                | Required | Description       |
| :--- | :---------------------------------------------------------------------------------- | :------- | :---------------- |
| body | [StorageFileUploadPreparationModel](../models/StorageFileUploadPreparationModel.md) | ❌       | The request body. |
| id   | number                                                                              | ✅       | Storage id        |

**Return Type**

`StorageFileUploadLinkModel`

**Example Usage Code Snippet**

```mcp

```

## createStorageFolder

Creates a new folder under the given parent

- HTTP Method: `POST`
- Endpoint: `/api/v3/storages/{id}/folders`

**Parameters**

| Name | Type                                                            | Required | Description       |
| :--- | :-------------------------------------------------------------- | :------- | :---------------- |
| body | [StorageFolderWriteModel](../models/StorageFolderWriteModel.md) | ❌       | The request body. |
| id   | number                                                          | ✅       | Storage id        |

**Return Type**

`StorageFileModel`

**Example Usage Code Snippet**

```mcp

```

## createStorageOauthCredentials

Inserts the OAuth 2 credentials into the storage, to allow the storage to act as an OAuth 2 client. Calling this endpoint on a storage that already contains OAuth 2 client credentials will replace them.

- HTTP Method: `POST`
- Endpoint: `/api/v3/storages/{id}/oauth_client_credentials`

**Parameters**

| Name | Type                                                                              | Required | Description       |
| :--- | :-------------------------------------------------------------------------------- | :------- | :---------------- |
| body | [OAuthClientCredentialsWriteModel](../models/OAuthClientCredentialsWriteModel.md) | ❌       | The request body. |
| id   | number                                                                            | ✅       | Storage id        |

**Return Type**

`StorageReadModel`

**Example Usage Code Snippet**

```mcp

```

## openStorage

Gets a redirect to the location of the storage's remote origin. The storage's files root should be the target location.

- HTTP Method: `GET`
- Endpoint: `/api/v3/storages/{id}/open`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Storage id  |

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
