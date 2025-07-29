# GroupsService

A list of all methods in the `GroupsService` service. Click on the method name to view detailed information about that method.

| Methods                     | Description                                                                                                                                                                                                                                                                                                                 |
| :-------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listGroups](#listgroups)   | Returns a collection of groups. The client can choose to filter the groups similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain groups, for which the requesting client has sufficient permissions (_view_members_, _manage_members_).     |
| [createGroup](#creategroup) | Creates a new group applying the attributes provided in the body.                                                                                                                                                                                                                                                           |
| [getGroup](#getgroup)       | Fetches a group resource.                                                                                                                                                                                                                                                                                                   |
| [updateGroup](#updategroup) | Updates the given group by applying the attributes provided in the body. Please note that the `members` array provided will override the existing set of members (similar to a PUT). A client thus has to provide the complete list of members the group is to have after the PATCH even if only one member is to be added. |
| [deleteGroup](#deletegroup) | Deletes the group.                                                                                                                                                                                                                                                                                                          |

## listGroups

Returns a collection of groups. The client can choose to filter the groups similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain groups, for which the requesting client has sufficient permissions (_view_members_, _manage_members_).

- HTTP Method: `GET`
- Endpoint: `/api/v3/groups`

**Parameters**

| Name   | Type   | Required | Description                                                                                                                                                                                                                                                                                                             |
| :----- | :----- | :------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| sortBy | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported sorts are: + id: Sort by primary key + created_at: Sort by group creation datetime + updated_at: Sort by the time the group was updated last |
| select | string | ❌       | Comma separated list of properties to include.                                                                                                                                                                                                                                                                          |

**Return Type**

`GroupCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createGroup

Creates a new group applying the attributes provided in the body.

- HTTP Method: `POST`
- Endpoint: `/api/v3/groups`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [GroupWriteModel](../models/GroupWriteModel.md) | ❌       | The request body. |

**Return Type**

`GroupModel`

**Example Usage Code Snippet**

```mcp

```

## getGroup

Fetches a group resource.

- HTTP Method: `GET`
- Endpoint: `/api/v3/groups/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Group id    |

**Return Type**

`GroupModel`

**Example Usage Code Snippet**

```mcp

```

## updateGroup

Updates the given group by applying the attributes provided in the body. Please note that the `members` array provided will override the existing set of members (similar to a PUT). A client thus has to provide the complete list of members the group is to have after the PATCH even if only one member is to be added.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/groups/{id}`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [GroupWriteModel](../models/GroupWriteModel.md) | ❌       | The request body. |
| id   | number                                          | ✅       | Group id          |

**Return Type**

`GroupModel`

**Example Usage Code Snippet**

```mcp

```

## deleteGroup

Deletes the group.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/groups/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Group id    |

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
