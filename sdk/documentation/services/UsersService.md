# UsersService

A list of all methods in the `UsersService` service. Click on the method name to view detailed information about that method.

| Methods                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| :-------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listUsers](#listusers)           | Lists users. Only administrators or users with any of the following can access this resource: - `manage_members` - `manage_user` - `share_work_packages`                                                                                                                                                                                                                                                                                                                                                              |
| [createUser](#createuser)         | Creates a new user. Only administrators and users with manage_user global permission are allowed to do so. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. Valid values for `status`: 1) "active" - In this case a password has to be provided in addition to the other attributes. 2) "invited" - In this case nothing but the email address is required. The rest is optional. An invitation will be sent to the user. |
| [viewUserSchema](#viewuserschema) | The schema response use two exemplary custom fields that extend the schema response. Depending on your instance and custom field configuration, the response will look somewhat different.                                                                                                                                                                                                                                                                                                                            |
| [viewUser](#viewuser)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [updateUser](#updateuser)         | Updates the user's writable attributes. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body.                                                                                                                                                                                                                                                                                                                                  |
| [deleteUser](#deleteuser)         | Permanently deletes the specified user account.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [userUpdateForm](#userupdateform) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [lockUser](#lockuser)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [unlockUser](#unlockuser)         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

## listUsers

Lists users. Only administrators or users with any of the following can access this resource: - `manage_members` - `manage_user` - `share_work_packages`

- HTTP Method: `GET`
- Endpoint: `/api/v3/users`

**Parameters**

| Name     | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                        |
| :------- | :----- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| offset   | number | ❌       | Page number inside the requested collection.                                                                                                                                                                                                                                                                                                                                                                       |
| pageSize | number | ❌       | Number of elements to display per page.                                                                                                                                                                                                                                                                                                                                                                            |
| filters  | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + status: Status the user has + group: Name of the group in which to-be-listed users are members. + name: Filter users in whose first or last names, or email addresses the given string occurs. + login: User's login |
| sortBy   | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint.                                                                                                                                                                                                                                                             |
| select   | string | ❌       | Comma separated list of properties to include.                                                                                                                                                                                                                                                                                                                                                                     |

**Return Type**

`UserCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createUser

Creates a new user. Only administrators and users with manage_user global permission are allowed to do so. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. Valid values for `status`: 1) "active" - In this case a password has to be provided in addition to the other attributes. 2) "invited" - In this case nothing but the email address is required. The rest is optional. An invitation will be sent to the user.

- HTTP Method: `POST`
- Endpoint: `/api/v3/users`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [UserCreateModel](../models/UserCreateModel.md) | ❌       | The request body. |

**Return Type**

`UserModel`

**Example Usage Code Snippet**

```mcp

```

## viewUserSchema

The schema response use two exemplary custom fields that extend the schema response. Depending on your instance and custom field configuration, the response will look somewhat different.

- HTTP Method: `GET`
- Endpoint: `/api/v3/users/schema`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewUser

- HTTP Method: `GET`
- Endpoint: `/api/v3/users/{id}`

**Parameters**

| Name | Type   | Required | Description                                          |
| :--- | :----- | :------- | :--------------------------------------------------- |
| id   | string | ✅       | User id. Use `me` to reference current user, if any. |

**Return Type**

`UserModel`

**Example Usage Code Snippet**

```mcp

```

## updateUser

Updates the user's writable attributes. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/users/{id}`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [UserCreateModel](../models/UserCreateModel.md) | ❌       | The request body. |
| id   | number                                          | ✅       | User id           |

**Return Type**

`UserModel`

**Example Usage Code Snippet**

```mcp

```

## deleteUser

Permanently deletes the specified user account.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/users/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | User id     |

**Example Usage Code Snippet**

```mcp

```

## userUpdateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/users/{id}/form`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | User id     |

**Example Usage Code Snippet**

```mcp

```

## lockUser

- HTTP Method: `POST`
- Endpoint: `/api/v3/users/{id}/lock`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | User id     |

**Return Type**

`UserModel`

**Example Usage Code Snippet**

```mcp

```

## unlockUser

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/users/{id}/lock`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | User id     |

**Return Type**

`UserModel`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
