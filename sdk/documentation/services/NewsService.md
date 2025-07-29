# NewsService

A list of all methods in the `NewsService` service. Click on the method name to view detailed information about that method.

| Methods                   | Description                                                                                                                                                                                                                                                       |
| :------------------------ | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listNews](#listnews)     | Lists news. The news returned depend on the provided parameters and also on the requesting user's permissions.                                                                                                                                                    |
| [createNews](#createnews) | Creates a news entry. Only administrators and users with "Manage news" permission in the given project are eligible. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. |
| [viewNews](#viewnews)     |                                                                                                                                                                                                                                                                   |
| [updateNews](#updatenews) | Updates the news's writable attributes. When calling this endpoint the client provides a single object, containing the properties and links to be updated, in the body.                                                                                           |
| [deleteNews](#deletenews) | Permanently deletes the specified news entry.                                                                                                                                                                                                                     |

## listNews

Lists news. The news returned depend on the provided parameters and also on the requesting user's permissions.

- HTTP Method: `GET`
- Endpoint: `/api/v3/news`

**Parameters**

| Name     | Type   | Required | Description                                                                                                                                                                                                                                                  |
| :------- | :----- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| offset   | number | ❌       | Page number inside the requested collection.                                                                                                                                                                                                                 |
| pageSize | number | ❌       | Number of elements to display per page.                                                                                                                                                                                                                      |
| sortBy   | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported sorts are: + id: Sort by primary key + created_at: Sort by news creation datetime |
| filters  | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + project_id: Filter news by project                             |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## createNews

Creates a news entry. Only administrators and users with "Manage news" permission in the given project are eligible. When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body.

- HTTP Method: `POST`
- Endpoint: `/api/v3/news`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [NewsCreateModel](../models/NewsCreateModel.md) | ❌       | The request body. |

**Return Type**

`NewsModel`

**Example Usage Code Snippet**

```mcp

```

## viewNews

- HTTP Method: `GET`
- Endpoint: `/api/v3/news/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | news id     |

**Return Type**

`NewsModel`

**Example Usage Code Snippet**

```mcp

```

## updateNews

Updates the news's writable attributes. When calling this endpoint the client provides a single object, containing the properties and links to be updated, in the body.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/news/{id}`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [NewsCreateModel](../models/NewsCreateModel.md) | ❌       | The request body. |
| id   | number                                          | ✅       | News id           |

**Return Type**

`NewsModel`

**Example Usage Code Snippet**

```mcp

```

## deleteNews

Permanently deletes the specified news entry.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/news/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | News id     |

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
