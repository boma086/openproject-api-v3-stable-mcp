# VersionsService

A list of all methods in the `VersionsService` service. Click on the method name to view detailed information about that method.

| Methods                                                             | Description                                                                                                                                                                                                                                                                                                                                   |
| :------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listVersionsAvailableInAProject](#listversionsavailableinaproject) | This endpoint lists the versions that are _available_ in a given project. Note that due to sharing this might be more than the versions _defined_ by that project.                                                                                                                                                                            |
| [listVersions](#listversions)                                       | Returns a collection of versions. The client can choose to filter the versions similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain versions, for which the requesting client has sufficient permissions (_view_work_packages_).                             |
| [createVersion](#createversion)                                     | Creates a new version applying the attributes provided in the body. Please note that while there is a fixed set of attributes, custom fields can extend a version's attributes and are accepted by the endpoint. You can use the form and schema to be retrieve the valid attribute values and by that be guided towards successful creation. |
| [availableProjectsForVersions](#availableprojectsforversions)       | Gets a list of projects in which a version can be created in. The list contains all projects in which the user issuing the request has the manage versions permissions.                                                                                                                                                                       |
| [versionCreateForm](#versioncreateform)                             |                                                                                                                                                                                                                                                                                                                                               |
| [viewVersionSchema](#viewversionschema)                             |                                                                                                                                                                                                                                                                                                                                               |
| [viewVersion](#viewversion)                                         |                                                                                                                                                                                                                                                                                                                                               |
| [updateVersion](#updateversion)                                     | Updates the given version by applying the attributes provided in the body. Please note that while there is a fixed set of attributes, custom fields can extend a version's attributes and are accepted by the endpoint.                                                                                                                       |
| [deleteVersion](#deleteversion)                                     | Deletes the version. Work packages associated to the version will no longer be assigned to it.                                                                                                                                                                                                                                                |
| [versionUpdateForm](#versionupdateform)                             |                                                                                                                                                                                                                                                                                                                                               |

## listVersionsAvailableInAProject

This endpoint lists the versions that are _available_ in a given project. Note that due to sharing this might be more than the versions _defined_ by that project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects/{id}/versions`

**Parameters**

| Name | Type   | Required | Description                                     |
| :--- | :----- | :------- | :---------------------------------------------- |
| id   | number | ✅       | ID of the project whose versions will be listed |

**Return Type**

`VersionsByProjectModel`

**Example Usage Code Snippet**

```mcp

```

## listVersions

Returns a collection of versions. The client can choose to filter the versions similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain versions, for which the requesting client has sufficient permissions (_view_work_packages_).

- HTTP Method: `GET`
- Endpoint: `/api/v3/versions`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                |
| :------ | :----- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + sharing: filters versions by how they are shared within the server (_none_, _descendants_, _hierarchy_, _tree_, _system_).                                                                   |
| sortBy  | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported attributes are: + id: Sort by the version id + name: Sort by the version name using numeric collation, comparing sequences of decimal digits by their numeric value + semver_name: Deprecated, use name instead |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## createVersion

Creates a new version applying the attributes provided in the body. Please note that while there is a fixed set of attributes, custom fields can extend a version's attributes and are accepted by the endpoint. You can use the form and schema to be retrieve the valid attribute values and by that be guided towards successful creation.

- HTTP Method: `POST`
- Endpoint: `/api/v3/versions`

**Return Type**

`VersionModel`

**Example Usage Code Snippet**

```mcp

```

## availableProjectsForVersions

Gets a list of projects in which a version can be created in. The list contains all projects in which the user issuing the request has the manage versions permissions.

- HTTP Method: `GET`
- Endpoint: `/api/v3/versions/available_projects`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## versionCreateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/versions/form`

**Example Usage Code Snippet**

```mcp

```

## viewVersionSchema

- HTTP Method: `GET`
- Endpoint: `/api/v3/versions/schema`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewVersion

- HTTP Method: `GET`
- Endpoint: `/api/v3/versions/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Version id  |

**Return Type**

`VersionModel`

**Example Usage Code Snippet**

```mcp

```

## updateVersion

Updates the given version by applying the attributes provided in the body. Please note that while there is a fixed set of attributes, custom fields can extend a version's attributes and are accepted by the endpoint.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/versions/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Version id  |

**Return Type**

`VersionModel`

**Example Usage Code Snippet**

```mcp

```

## deleteVersion

Deletes the version. Work packages associated to the version will no longer be assigned to it.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/versions/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Version id  |

**Example Usage Code Snippet**

```mcp

```

## versionUpdateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/versions/{id}/form`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Project id  |

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
