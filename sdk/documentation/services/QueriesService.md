# QueriesService

A list of all methods in the `QueriesService` service. Click on the method name to view detailed information about that method.

| Methods                                                     | Description                                                                                                                                                                                                                                                                                                                                                                          |
| :---------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [viewDefaultQueryForProject](#viewdefaultqueryforproject)   | Same as [viewing an existing, persisted Query](https://www.openproject.org/docs/api/endpoints/queries/#list-queries) in its response, this resource returns an unpersisted query and by that allows to get the default query configuration. The client may also provide additional parameters which will modify the default query. The query will already be scoped for the project. |
| [viewSchemaForProjectQueries](#viewschemaforprojectqueries) | Retrieve the schema for project queries.                                                                                                                                                                                                                                                                                                                                             |
| [listQueries](#listqueries)                                 | Returns a collection of queries. The collection can be filtered via query parameters similar to how work packages are filtered. Please note however, that the filters are applied to the queries and not to the work packages the queries in turn might return.                                                                                                                      |
| [createQuery](#createquery)                                 | When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. The required fields of a Query can be found in its schema, which is embedded in the respective form. Note that it is only allowed to provide properties or links supporting the write operation.                                        |
| [availableProjectsForQuery](#availableprojectsforquery)     | Gets a list of projects that are available as projects a query can be assigned to.                                                                                                                                                                                                                                                                                                   |
| [viewDefaultQuery](#viewdefaultquery)                       | Same as [viewing an existing, persisted Query](https://www.openproject.org/docs/api/endpoints/queries/#list-queries) in its response, this resource returns an unpersisted query and by that allows to get the default query configuration. The client may also provide additional parameters which will modify the default query.                                                   |
| [queryCreateForm](#querycreateform)                         |                                                                                                                                                                                                                                                                                                                                                                                      |
| [viewSchemaForGlobalQueries](#viewschemaforglobalqueries)   | Retrieve the schema for global queries, those, that are not assigned to a project.                                                                                                                                                                                                                                                                                                   |
| [viewQuery](#viewquery)                                     | Retrieve an individual query as identified by the id parameter. Then end point accepts a number of parameters that can be used to override the resources' persisted parameters.                                                                                                                                                                                                      |
| [editQuery](#editquery)                                     | When calling this endpoint the client provides a single object, containing the properties and links that it wants to change, in the body. Note that it is only allowed to provide properties or links supporting the **write** operation.                                                                                                                                            |
| [deleteQuery](#deletequery)                                 | Delete the query identified by the id parameter                                                                                                                                                                                                                                                                                                                                      |
| [queryUpdateForm](#queryupdateform)                         |                                                                                                                                                                                                                                                                                                                                                                                      |
| [starQuery](#starquery)                                     |                                                                                                                                                                                                                                                                                                                                                                                      |
| [unstarQuery](#unstarquery)                                 |                                                                                                                                                                                                                                                                                                                                                                                      |

## viewDefaultQueryForProject

Same as [viewing an existing, persisted Query](https://www.openproject.org/docs/api/endpoints/queries/#list-queries) in its response, this resource returns an unpersisted query and by that allows to get the default query configuration. The client may also provide additional parameters which will modify the default query. The query will already be scoped for the project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects/{id}/queries/default`

**Parameters**

| Name            | Type    | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :-------------- | :------ | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| id              | number  | ✅       | Id of the project the default query is requested for                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| filters         | string  | ❌       | JSON specifying filter conditions. The filters provided as parameters are not applied to the query but are instead used to override the query's persisted filters. All filters also accepted by the work packages endpoint are accepted. If no filter is to be applied, the client should send an empty array (`[]`).                                                                                                                                                                                                                             |
| offset          | number  | ❌       | Page number inside the queries' result collection of work packages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| pageSize        | number  | ❌       | Number of elements to display per page for the queries' result collection of work packages.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| sortBy          | string  | ❌       | JSON specifying sort criteria. The sort criteria is applied to the query's result collection of work packages overriding the query's persisted sort criteria.                                                                                                                                                                                                                                                                                                                                                                                     |
| groupBy         | string  | ❌       | The column to group by. The grouping criteria is applied to the to the query's result collection of work packages overriding the query's persisted group criteria.                                                                                                                                                                                                                                                                                                                                                                                |
| showSums        | boolean | ❌       | Indicates whether properties should be summed up if they support it. The showSums parameter is applied to the to the query's result collection of work packages overriding the query's persisted sums property.                                                                                                                                                                                                                                                                                                                                   |
| timestamps      | string  | ❌       | Indicates the timestamps to filter by when showing changed attributes on work packages. Values can be either ISO8601 dates, ISO8601 durations and the following relative date keywords: "oneDayAgo@HH:MM+HH:MM", "lastWorkingDay@HH:MM+HH:MM", "oneWeekAgo@HH:MM+HH:MM", "oneMonthAgo@HH:MM+HH:MM". The first "HH:MM" part represents the zero paded hours and minutes. The last "+HH:MM" part represents the timezone offset from UTC associated with the time. Values older than 1 day are accepted only with valid Enterprise Token available. |
| timelineVisible | boolean | ❌       | Indicates whether the timeline should be shown.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| showHierarchies | boolean | ❌       | Indicates whether the hierarchy mode should be enabled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewSchemaForProjectQueries

Retrieve the schema for project queries.

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects/{id}/queries/schema`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Project id  |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## listQueries

Returns a collection of queries. The collection can be filtered via query parameters similar to how work packages are filtered. Please note however, that the filters are applied to the queries and not to the work packages the queries in turn might return.

- HTTP Method: `GET`
- Endpoint: `/api/v3/queries`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                        |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Currently supported filters are: + project: filters queries by the project they are assigned to. If the project filter is passed with the `!*` (not any) operator, global queries are returned. + id: filters queries based on their id + updated_at: filters queries based on the last time they where updated |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## createQuery

When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. The required fields of a Query can be found in its schema, which is embedded in the respective form. Note that it is only allowed to provide properties or links supporting the write operation.

- HTTP Method: `POST`
- Endpoint: `/api/v3/queries`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [QueryCreateForm](../models/QueryCreateForm.md) | ❌       | The request body. |

**Return Type**

`QueryModel`

**Example Usage Code Snippet**

```mcp

```

## availableProjectsForQuery

Gets a list of projects that are available as projects a query can be assigned to.

- HTTP Method: `GET`
- Endpoint: `/api/v3/queries/available_projects`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewDefaultQuery

Same as [viewing an existing, persisted Query](https://www.openproject.org/docs/api/endpoints/queries/#list-queries) in its response, this resource returns an unpersisted query and by that allows to get the default query configuration. The client may also provide additional parameters which will modify the default query.

- HTTP Method: `GET`
- Endpoint: `/api/v3/queries/default`

**Parameters**

| Name              | Type    | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| :---------------- | :------ | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters           | string  | ❌       | JSON specifying filter conditions. The filters provided as parameters are not applied to the query but are instead used to override the query's persisted filters. All filters also accepted by the work packages endpoint are accepted. If no filter is to be applied, the client should send an empty array (`[]`).                                                                                                                                                                                                                                                                                                                          |
| offset            | number  | ❌       | Page number inside the queries' result collection of work packages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| pageSize          | number  | ❌       | Number of elements to display per page for the queries' result collection of work packages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| sortBy            | string  | ❌       | JSON specifying sort criteria. The sort criteria is applied to the query's result collection of work packages overriding the query's persisted sort criteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| groupBy           | string  | ❌       | The column to group by. The grouping criteria is applied to the to the query's result collection of work packages overriding the query's persisted group criteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| showSums          | boolean | ❌       | Indicates whether properties should be summed up if they support it. The showSums parameter is applied to the to the query's result collection of work packages overriding the query's persisted sums property.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| timestamps        | string  | ❌       | Indicates the timestamps to filter by when showing changed attributes on work packages. Values can be either ISO8601 dates, ISO8601 durations and the following relative date keywords: "oneDayAgo@HH:MM+HH:MM", "lastWorkingDay@HH:MM+HH:MM", "oneWeekAgo@HH:MM+HH:MM", "oneMonthAgo@HH:MM+HH:MM". The first "HH:MM" part represents the zero paded hours and minutes. The last "+HH:MM" part represents the timezone offset from UTC associated with the time, the offset can be positive or negative e.g."oneDayAgo@01:00+01:00", "oneDayAgo@01:00-01:00". Values older than 1 day are accepted only with valid Enterprise Token available. |
| timelineVisible   | boolean | ❌       | Indicates whether the timeline should be shown.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| timelineZoomLevel | string  | ❌       | Indicates in what zoom level the timeline should be shown. Valid values are `days`, `weeks`, `months`, `quarters`, and `years`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| showHierarchies   | boolean | ❌       | Indicates whether the hierarchy mode should be enabled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## queryCreateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/queries/form`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [QueryCreateForm](../models/QueryCreateForm.md) | ❌       | The request body. |

**Example Usage Code Snippet**

```mcp

```

## viewSchemaForGlobalQueries

Retrieve the schema for global queries, those, that are not assigned to a project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/queries/schema`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewQuery

Retrieve an individual query as identified by the id parameter. Then end point accepts a number of parameters that can be used to override the resources' persisted parameters.

- HTTP Method: `GET`
- Endpoint: `/api/v3/queries/{id}`

**Parameters**

| Name                  | Type    | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| :-------------------- | :------ | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id                    | number  | ✅       | Query id                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| filters               | string  | ❌       | JSON specifying filter conditions. The filters provided as parameters are not applied to the query but are instead used to override the query's persisted filters. All filters also accepted by the work packages endpoint are accepted. If no filter is to be applied, the client should send an empty array (`[]`).                                                                                                                                                                                                                                                                                                                          |
| offset                | number  | ❌       | Page number inside the queries' result collection of work packages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| pageSize              | number  | ❌       | Number of elements to display per page for the queries' result collection of work packages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| columns               | string  | ❌       | Selected columns for the table view.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| sortBy                | string  | ❌       | JSON specifying sort criteria. The sort criteria is applied to the query's result collection of work packages overriding the query's persisted sort criteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| groupBy               | string  | ❌       | The column to group by. The grouping criteria is applied to the to the query's result collection of work packages overriding the query's persisted group criteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| showSums              | boolean | ❌       | Indicates whether properties should be summed up if they support it. The showSums parameter is applied to the to the query's result collection of work packages overriding the query's persisted sums property.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| timestamps            | string  | ❌       | Indicates the timestamps to filter by when showing changed attributes on work packages. Values can be either ISO8601 dates, ISO8601 durations and the following relative date keywords: "oneDayAgo@HH:MM+HH:MM", "lastWorkingDay@HH:MM+HH:MM", "oneWeekAgo@HH:MM+HH:MM", "oneMonthAgo@HH:MM+HH:MM". The first "HH:MM" part represents the zero paded hours and minutes. The last "+HH:MM" part represents the timezone offset from UTC associated with the time, the offset can be positive or negative e.g."oneDayAgo@01:00+01:00", "oneDayAgo@01:00-01:00". Values older than 1 day are accepted only with valid Enterprise Token available. |
| timelineVisible       | boolean | ❌       | Indicates whether the timeline should be shown.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| timelineLabels        | string  | ❌       | Overridden labels in the timeline view                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| highlightingMode      | string  | ❌       | Highlighting mode for the table view.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| highlightedAttributes | string  | ❌       | Highlighted attributes mode for the table view when `highlightingMode` is `inline`. When set to `[]` all highlightable attributes will be returned as `highlightedAttributes`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| showHierarchies       | boolean | ❌       | Indicates whether the hierarchy mode should be enabled.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |

**Return Type**

`QueryModel`

**Example Usage Code Snippet**

```mcp

```

## editQuery

When calling this endpoint the client provides a single object, containing the properties and links that it wants to change, in the body. Note that it is only allowed to provide properties or links supporting the **write** operation.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/queries/{id}`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [QueryUpdateForm](../models/QueryUpdateForm.md) | ❌       | The request body. |
| id   | number                                          | ✅       | Query id          |

**Return Type**

`QueryModel`

**Example Usage Code Snippet**

```mcp

```

## deleteQuery

Delete the query identified by the id parameter

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/queries/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Query id    |

**Example Usage Code Snippet**

```mcp

```

## queryUpdateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/queries/{id}/form`

**Parameters**

| Name | Type                                            | Required | Description       |
| :--- | :---------------------------------------------- | :------- | :---------------- |
| body | [QueryUpdateForm](../models/QueryUpdateForm.md) | ❌       | The request body. |
| id   | number                                          | ✅       | Query id          |

**Example Usage Code Snippet**

```mcp

```

## starQuery

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/queries/{id}/star`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Query id    |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## unstarQuery

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/queries/{id}/unstar`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Query id    |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
