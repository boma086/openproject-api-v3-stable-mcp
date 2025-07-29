# PrincipalsService

A list of all methods in the `PrincipalsService` service. Click on the method name to view detailed information about that method.

| Methods                                         | Description                                                                                                                                                                                                                                                                       |
| :---------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listPlaceholderUsers](#listplaceholderusers)   | List all placeholder users. This can only be accessed if the requesting user has the global permission `manage_placeholder_user` or `manage_members` in any project.                                                                                                              |
| [createPlaceholderUser](#createplaceholderuser) | Creates a new placeholder user. Only administrators and users with `manage_placeholder_user` global permission are allowed to do so. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. |
| [viewPlaceholderUser](#viewplaceholderuser)     | Return the placeholder user resource.                                                                                                                                                                                                                                             |
| [updatePlaceholderUser](#updateplaceholderuser) | Updates the placeholder user's writable attributes. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body.                                                                                  |
| [deletePlaceholderUser](#deleteplaceholderuser) | Set the specified placeholder user to deleted status.                                                                                                                                                                                                                             |
| [listPrincipals](#listprincipals)               | List all principals. The client can choose to filter the principals similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain principals who are members in projects the client is allowed to see.    |

## listPlaceholderUsers

List all placeholder users. This can only be accessed if the requesting user has the global permission `manage_placeholder_user` or `manage_members` in any project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/placeholder_users`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                  |
| :------ | :----- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: - name: filters placeholder users by the name. - group: filters placeholder by the group it is contained in. - status: filters placeholder by the status it has. |
| select  | string | ❌       | Comma separated list of properties to include.                                                                                                                                                                                                                                                                                                               |

**Return Type**

`PrincipalCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createPlaceholderUser

Creates a new placeholder user. Only administrators and users with `manage_placeholder_user` global permission are allowed to do so. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body.

- HTTP Method: `POST`
- Endpoint: `/api/v3/placeholder_users`

**Parameters**

| Name | Type                                                                  | Required | Description       |
| :--- | :-------------------------------------------------------------------- | :------- | :---------------- |
| body | [PlaceholderUserCreateModel](../models/PlaceholderUserCreateModel.md) | ❌       | The request body. |

**Return Type**

`PlaceholderUserModel`

**Example Usage Code Snippet**

```mcp

```

## viewPlaceholderUser

Return the placeholder user resource.

- HTTP Method: `GET`
- Endpoint: `/api/v3/placeholder_users/{id}`

**Parameters**

| Name | Type   | Required | Description             |
| :--- | :----- | :------- | :---------------------- |
| id   | string | ✅       | The placeholder user id |

**Return Type**

`PlaceholderUserModel`

**Example Usage Code Snippet**

```mcp

```

## updatePlaceholderUser

Updates the placeholder user's writable attributes. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/placeholder_users/{id}`

**Parameters**

| Name | Type                                                                  | Required | Description         |
| :--- | :-------------------------------------------------------------------- | :------- | :------------------ |
| body | [PlaceholderUserCreateModel](../models/PlaceholderUserCreateModel.md) | ❌       | The request body.   |
| id   | number                                                                | ✅       | Placeholder user id |

**Return Type**

`PlaceholderUserModel`

**Example Usage Code Snippet**

```mcp

```

## deletePlaceholderUser

Set the specified placeholder user to deleted status.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/placeholder_users/{id}`

**Parameters**

| Name | Type   | Required | Description         |
| :--- | :----- | :------- | :------------------ |
| id   | number | ✅       | Placeholder user id |

**Example Usage Code Snippet**

```mcp

```

## listPrincipals

List all principals. The client can choose to filter the principals similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain principals who are members in projects the client is allowed to see.

- HTTP Method: `GET`
- Endpoint: `/api/v3/principals`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :------ | :----- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: - type: filters principals by their type (_User_, _Group_, _PlaceholderUser_). - member: filters principals by the projects they are members in. - name: filters principals by the user or group name. - any_name_attribute: filters principals by the user or group first- and last name, email or login. - status: filters principals by their status number (active = _1_, registered = _2_, locked = _3_, invited = _4_) |
| select  | string | ❌       | Comma separated list of properties to include.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

**Return Type**

`PrincipalCollectionModel`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
