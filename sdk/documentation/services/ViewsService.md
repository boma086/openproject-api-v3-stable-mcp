# ViewsService

A list of all methods in the `ViewsService` service. Click on the method name to view detailed information about that method.

| Methods                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| :-------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listViews](#listviews)     | Returns a collection of Views. The collection can be filtered via query parameters similar to how work packages are filtered.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [viewView](#viewview)       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [createViews](#createviews) | When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. The required fields of a View can be found in its schema, which is embedded in the respective form. Note that it is only allowed to provide properties or links supporting the write operation. There are different subtypes of `Views` (e.g. `Views::WorkPackagesTable`) with each having its own endpoint for creating that subtype e.g. _ `/api/v3/views/work_packages_table` for `Views::WorkPackagesTable` _ `/api/v3/views/team_planner` for `Views::TeamPlanner` \* `/api/v3/views/work_packages_calendar` for `Views::WorkPackagesCalendar` **Not yet implemented** To get the list of available subtypes and by that the endpoints for creating a subtype, use the `  /api/v3/views/schemas` endpoint. |

## listViews

Returns a collection of Views. The collection can be filtered via query parameters similar to how work packages are filtered.

- HTTP Method: `GET`
- Endpoint: `/api/v3/views`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                     |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| filters | string | ❌       | JSON specifying filter conditions. Currently supported filters are: + project: filters views by the project their associated query is assigned to. If the project filter is passed with the `!*` (not any) operator, global views are returned. + id: filters views based on their id + type: filters views based on their type |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewView

- HTTP Method: `GET`
- Endpoint: `/api/v3/views/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | View id     |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## createViews

When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. The required fields of a View can be found in its schema, which is embedded in the respective form. Note that it is only allowed to provide properties or links supporting the write operation. There are different subtypes of `Views` (e.g. `Views::WorkPackagesTable`) with each having its own endpoint for creating that subtype e.g. _ `/api/v3/views/work_packages_table` for `Views::WorkPackagesTable` _ `/api/v3/views/team_planner` for `Views::TeamPlanner` \* `/api/v3/views/work_packages_calendar` for `Views::WorkPackagesCalendar` **Not yet implemented** To get the list of available subtypes and by that the endpoints for creating a subtype, use the `  /api/v3/views/schemas` endpoint.

- HTTP Method: `POST`
- Endpoint: `/api/v3/views/{id}`

**Parameters**

| Name | Type                                                  | Required | Description         |
| :--- | :---------------------------------------------------- | :------- | :------------------ |
| body | [CreateViewsRequest](../models/CreateViewsRequest.md) | ❌       | The request body.   |
| id   | string                                                | ✅       | The view identifier |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
