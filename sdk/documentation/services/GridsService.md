# GridsService

A list of all methods in the `GridsService` service. Click on the method name to view detailed information about that method.

| Methods                           | Description                                                                                                                                                                                                                                            |
| :-------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listGrids](#listgrids)           | Lists all grids matching the provided filters and being part of the selected query page. The grids returned will also depend on the permissions of the requesting user.                                                                                |
| [createGrid](#creategrid)         | Creates a new grid applying the attributes provided in the body. The constraints applied to the grid depend on the page the grid is placed in which is why the create form end point should be used to be guided when wanting to create a grid.        |
| [gridCreateForm](#gridcreateform) |                                                                                                                                                                                                                                                        |
| [getGrid](#getgrid)               | Fetches a single grid identified by its id.                                                                                                                                                                                                            |
| [updateGrid](#updategrid)         | Updates the given grid by applying the attributes provided in the body. The constraints applied to the grid depend on the page the grid is placed in which is why the create form end point should be used to be guided when wanting to update a grid. |
| [gridUpdateForm](#gridupdateform) |                                                                                                                                                                                                                                                        |

## listGrids

Lists all grids matching the provided filters and being part of the selected query page. The grids returned will also depend on the permissions of the requesting user.

- HTTP Method: `GET`
- Endpoint: `/api/v3/grids`

**Parameters**

| Name     | Type   | Required | Description                                                                                                                                                                                                                     |
| :------- | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| offset   | number | ❌       | Page number inside the requested collection.                                                                                                                                                                                    |
| pageSize | number | ❌       | Number of elements to display per page.                                                                                                                                                                                         |
| filters  | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: - page: Filter grid by work package |

**Return Type**

`GridCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createGrid

Creates a new grid applying the attributes provided in the body. The constraints applied to the grid depend on the page the grid is placed in which is why the create form end point should be used to be guided when wanting to create a grid.

- HTTP Method: `POST`
- Endpoint: `/api/v3/grids`

**Parameters**

| Name | Type                                          | Required | Description       |
| :--- | :-------------------------------------------- | :------- | :---------------- |
| body | [GridWriteModel](../models/GridWriteModel.md) | ❌       | The request body. |

**Return Type**

`GridReadModel`

**Example Usage Code Snippet**

```mcp

```

## gridCreateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/grids/form`

**Example Usage Code Snippet**

```mcp

```

## getGrid

Fetches a single grid identified by its id.

- HTTP Method: `GET`
- Endpoint: `/api/v3/grids/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Grid id     |

**Return Type**

`GridReadModel`

**Example Usage Code Snippet**

```mcp

```

## updateGrid

Updates the given grid by applying the attributes provided in the body. The constraints applied to the grid depend on the page the grid is placed in which is why the create form end point should be used to be guided when wanting to update a grid.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/grids/{id}`

**Parameters**

| Name | Type                                          | Required | Description       |
| :--- | :-------------------------------------------- | :------- | :---------------- |
| body | [GridWriteModel](../models/GridWriteModel.md) | ❌       | The request body. |

**Return Type**

`GridReadModel`

**Example Usage Code Snippet**

```mcp

```

## gridUpdateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/grids/{id}/form`

**Parameters**

| Name | Type   | Required | Description                   |
| :--- | :----- | :------- | :---------------------------- |
| id   | number | ✅       | ID of the grid being modified |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
