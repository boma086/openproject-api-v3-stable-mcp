# TimeEntriesService

A list of all methods in the `TimeEntriesService` service. Click on the method name to view detailed information about that method.

| Methods                                                             | Description                                                                                                                                                                                                                    |
| :------------------------------------------------------------------ | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listTimeEntries](#listtimeentries)                                 | Lists time entries. The time entries returned depend on the filters provided and also on the permission of the requesting user.                                                                                                |
| [createTimeEntry](#createtimeentry)                                 | Creates a new time entry applying the attributes provided in the body. Please note that while there is a fixed set of attributes, custom fields can extend a time entries' attributes and are accepted by the endpoint.        |
| [timeEntryUpdateForm](#timeentryupdateform)                         |                                                                                                                                                                                                                                |
| [availableProjectsForTimeEntries](#availableprojectsfortimeentries) | Gets a list of projects in which a time entry can be created in or be assigned to on update. The list contains all projects in which the user issuing the request has the necessary permissions.                               |
| [timeEntryCreateForm](#timeentrycreateform)                         |                                                                                                                                                                                                                                |
| [viewTimeEntrySchema](#viewtimeentryschema)                         |                                                                                                                                                                                                                                |
| [getTimeEntry](#gettimeentry)                                       | Retrieves a single time entry identified by the given id.                                                                                                                                                                      |
| [updateTimeEntry](#updatetimeentry)                                 | Updates the given time entry by applying the attributes provided in the body. Please note that while there is a fixed set of attributes, custom fields can extend a time entries' attributes and are accepted by the endpoint. |
| [deleteTimeEntry](#deletetimeentry)                                 | Permanently deletes the specified time entry.                                                                                                                                                                                  |

## listTimeEntries

Lists time entries. The time entries returned depend on the filters provided and also on the permission of the requesting user.

- HTTP Method: `GET`
- Endpoint: `/api/v3/time_entries`

**Parameters**

| Name     | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| :------- | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| offset   | number | ❌       | Page number inside the requested collection.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| pageSize | number | ❌       | Number of elements to display per page.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| sortBy   | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported sorts are: + id: Sort by primary key + hours: Sort by logged hours + spent_on: Sort by spent on date + created_at: Sort by time entry creation datetime + updated_at: Sort by the time the time entry was updated last                                                                                                                                                                                                             |
| filters  | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + work_package: Filter time entries by work package + project: Filter time entries by project + user: Filter time entries by users + ongoing: Filter for your ongoing timers + spent_on: Filter time entries by spent on date + created_at: Filter time entries by creation datetime + updated_at: Filter time entries by the last time they where updated + activity: Filter time entries by time entry activity |

**Return Type**

`TimeEntryCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createTimeEntry

Creates a new time entry applying the attributes provided in the body. Please note that while there is a fixed set of attributes, custom fields can extend a time entries' attributes and are accepted by the endpoint.

- HTTP Method: `POST`
- Endpoint: `/api/v3/time_entries`

**Parameters**

| Name | Type                                          | Required | Description       |
| :--- | :-------------------------------------------- | :------- | :---------------- |
| body | [TimeEntryModel](../models/TimeEntryModel.md) | ❌       | The request body. |

**Return Type**

`TimeEntryModel`

**Example Usage Code Snippet**

```mcp

```

## timeEntryUpdateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/time_entries/{id}/form`

**Parameters**

| Name | Type   | Required | Description              |
| :--- | :----- | :------- | :----------------------- |
| body | number | ✅       | The request body.        |
| id   | number | ✅       | Time entries activity id |

**Example Usage Code Snippet**

```mcp

```

## availableProjectsForTimeEntries

Gets a list of projects in which a time entry can be created in or be assigned to on update. The list contains all projects in which the user issuing the request has the necessary permissions.

- HTTP Method: `GET`
- Endpoint: `/api/v3/time_entries/available_projects`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## timeEntryCreateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/time_entries/form`

**Example Usage Code Snippet**

```mcp

```

## viewTimeEntrySchema

- HTTP Method: `GET`
- Endpoint: `/api/v3/time_entries/schema`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## getTimeEntry

Retrieves a single time entry identified by the given id.

- HTTP Method: `GET`
- Endpoint: `/api/v3/time_entries/{id}`

**Parameters**

| Name | Type   | Required | Description   |
| :--- | :----- | :------- | :------------ |
| id   | number | ✅       | time entry id |

**Return Type**

`TimeEntryModel`

**Example Usage Code Snippet**

```mcp

```

## updateTimeEntry

Updates the given time entry by applying the attributes provided in the body. Please note that while there is a fixed set of attributes, custom fields can extend a time entries' attributes and are accepted by the endpoint.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/time_entries/{id}`

**Parameters**

| Name | Type   | Required | Description   |
| :--- | :----- | :------- | :------------ |
| id   | number | ✅       | Time entry id |

**Return Type**

`TimeEntryModel`

**Example Usage Code Snippet**

```mcp

```

## deleteTimeEntry

Permanently deletes the specified time entry.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/time_entries/{id}`

**Parameters**

| Name | Type   | Required | Description   |
| :--- | :----- | :------- | :------------ |
| id   | number | ✅       | Time entry id |

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
