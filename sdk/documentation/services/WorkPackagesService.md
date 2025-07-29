# WorkPackagesService

A list of all methods in the `WorkPackagesService` service. Click on the method name to view detailed information about that method.

| Methods                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| :------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [getProjectWorkPackageCollection](#getprojectworkpackagecollection) | Returns the collection of work packages that are related to the given project.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [createProjectWorkPackage](#createprojectworkpackage)               | When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. The required fields of a WorkPackage can be found in its schema, which is embedded in the respective form. Note that it is only allowed to provide properties or links supporting the write operation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [formCreateWorkPackageInProject](#formcreateworkpackageinproject)   | This endpoint allows you to validation a new work package creation body in a specific project. It works similarly to the `/api/v3/work_packages/form` endpoint, but already specifies the work package's project in the path, so that it does not have to be defined in the request body.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [projectAvailableAssignees](#projectavailableassignees)             | Gets a list of users that can be assigned to work packages in the given project.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [listWorkPackages](#listworkpackages)                               | Returns a collection of work packages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [createWorkPackage](#createworkpackage)                             | When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. The required fields of a WorkPackage can be found in its schema, which is embedded in the respective form. Note that it is only allowed to provide properties or links supporting the write operation. A project link must be set when creating work packages through this route. When setting start date, finish date, and duration together, their correctness will be checked and a 422 error will be returned if one value does not match with the two others. You can make the server compute a value: set only two values in the request and the third one will be computed and returned in the response. For instance, when sending `{ "startDate": "2022-08-23", duration: "P2D" }`, the response will include `{ "dueDate": "2022-08-24" }`.                                                                                                        |
| [formCreateWorkPackage](#formcreateworkpackage)                     | When calling this endpoint, the client provides a single object containing the properties and links to be created, in the body. The input is validated and a schema response is returned. If the validation errors of the response is empty, the same payload can be used to create a work package. Only the properties of the work package write model are allowed to set on a work package on creation. When setting start date, finish date, and duration together, their correctness will be checked and a validation error will be returned if one value does not match with the two others. You can make the server compute a value: set only two values in the request and the third one will be computed and returned in the response. For instance, when sending `{ "startDate": "2022-08-23", duration: "P2D" }`, the response will include `{ "dueDate": "2022-08-24" }`.                                                                                                                      |
| [listWorkPackageSchemas](#listworkpackageschemas)                   | List all work package schemas that match the given filters. This endpoint does not return a successful response, if no filter is given.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [viewWorkPackageSchema](#viewworkpackageschema)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [viewWorkPackage](#viewworkpackage)                                 | Returns the specified work package.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [updateWorkPackage](#updateworkpackage)                             | When calling this endpoint the client provides a single object, containing the properties and links that it wants to change, in the body. Note that it is only allowed to provide properties or links supporting the **write** operation. Additionally to the fields the client wants to change, it is mandatory to provide the value of `lockVersion` which was received by the `GET` request this change originates from. The value of `lockVersion` is used to implement [optimistic locking](https://en.wikipedia.org/wiki/Optimistic_concurrency_control).                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [deleteWorkPackage](#deleteworkpackage)                             | Deletes the work package, as well as: - all associated time entries - its hierarchy of child work packages                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [listWorkPackageActivities](#listworkpackageactivities)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [commentWorkPackage](#commentworkpackage)                           | Creates an activity for the selected work package and, on success, returns the updated activity.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [workPackageAvailableAssignees](#workpackageavailableassignees)     | Gets a list of users that can be assigned to the given work package.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [availableProjectsForWorkPackage](#availableprojectsforworkpackage) | Gets a list of projects that are available as projects to which the work package can be moved.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [listAvailableRelationCandidates](#listavailablerelationcandidates) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [availableWatchers](#availablewatchers)                             | Gets a list of users that are able to be watchers of the specified work package.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [listWorkPackageFileLinks](#listworkpackagefilelinks)               | Gets all file links of a work package. As a side effect, for every file link a request is sent to the storage's origin to fetch live data and patch the file link's data before returning, as well as retrieving permissions of the user on this origin file.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [createWorkPackageFileLink](#createworkpackagefilelink)             | Creates file links on a work package. The request is interpreted as a bulk insert, where every element of the collection is validated separately. Each element contains the origin meta data and a link to the storage, the file link is about to point to. The storage link can be provided as a resource link with id or as the host url. The file's id and name are considered mandatory information. The rest of the origin meta data SHOULD be provided by the client. The _mimeType_ SHOULD be a standard mime type. An empty mime type will be handled as unknown. To link a folder, the custom mime type `application/x-op-directory` MUST be used. Up to 20 file links can be submitted at once. If any element data is invalid, no file links will be created. If a file link with matching origin id, work package, and storage already exists, then it will not create an additional file link or update the meta data. Instead the information from the existing file link will be returned. |
| [formEditWorkPackage](#formeditworkpackage)                         | When calling this endpoint, the client provides a single object containing the properties and links to be edited, in the body. The input is validated and a schema response is returned. If the validation errors of the response is empty, the same payload can be used to edit the work package. Only the properties of the work package write model are allowed to set on a work package on editing. When setting start date, finish date, and duration together, their correctness will be checked and a validation error will be returned if one value does not match with the two others. You can make the server compute a value: set only two values in the request and the third one will be computed and returned in the response. For instance, when sending `{ "startDate": "2022-08-23", duration: "P2D" }`, the response will include `{ "dueDate": "2022-08-24" }`.                                                                                                                        |
| [revisions](#revisions)                                             | Gets a list of revisions that are linked to this work package, e.g., because it is referenced in the commit message of the revision. Only linked revisions from repositories are shown if the user has the view changesets permission in the defining project.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [reminders](#reminders)                                             | Gets a list of your upcoming reminders for this work package.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [listWatchers](#listwatchers)                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [addWatcher](#addwatcher)                                           | Adds a watcher to the specified work package. The request is expected to contain a single JSON object, that contains a link object under the `user` key. The response will be user added as watcher. In case the user was already watching the work package an `HTTP 200` is returned, an `HTTP 201` if the user was added as a new watcher.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [removeWatcher](#removewatcher)                                     | Removes the specified user from the list of watchers for the given work package. If the request succeeds, the specified user is not watching the work package anymore. _Note: This might also be the case, if the specified user did not watch the work package prior to the request._                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

## getProjectWorkPackageCollection

Returns the collection of work packages that are related to the given project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects/{id}/work_packages`

**Parameters**

| Name     | Type    | Required | Description                                                                                                                                                                                                                             |
| :------- | :------ | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id       | number  | ✅       | Project id                                                                                                                                                                                                                              |
| offset   | number  | ❌       | Page number inside the requested collection.                                                                                                                                                                                            |
| pageSize | number  | ❌       | Number of elements to display per page.                                                                                                                                                                                                 |
| filters  | string  | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. If no filter is to be applied, the client should send an empty array (`[]`). |
| sortBy   | string  | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint.                                                                                  |
| groupBy  | string  | ❌       | The column to group by.                                                                                                                                                                                                                 |
| showSums | boolean | ❌       | Indicates whether properties should be summed up if they support it.                                                                                                                                                                    |
| select   | string  | ❌       | Comma separated list of properties to include.                                                                                                                                                                                          |

**Return Type**

`WorkPackagesModel`

**Example Usage Code Snippet**

```mcp

```

## createProjectWorkPackage

When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. The required fields of a WorkPackage can be found in its schema, which is embedded in the respective form. Note that it is only allowed to provide properties or links supporting the write operation.

- HTTP Method: `POST`
- Endpoint: `/api/v3/projects/{id}/work_packages`

**Parameters**

| Name   | Type                                              | Required | Description                                                                                                                                                                                                                             |
| :----- | :------------------------------------------------ | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| body   | [WorkPackageModel](../models/WorkPackageModel.md) | ❌       | The request body.                                                                                                                                                                                                                       |
| id     | number                                            | ✅       | Project id                                                                                                                                                                                                                              |
| notify | boolean                                           | ❌       | Indicates whether change notifications (e.g. via E-Mail) should be sent. Note that this controls notifications for all users interested in changes to the work package (e.g. watchers, author and assignee), not just the current user. |

**Return Type**

`WorkPackageModel`

**Example Usage Code Snippet**

```mcp

```

## formCreateWorkPackageInProject

This endpoint allows you to validation a new work package creation body in a specific project. It works similarly to the `/api/v3/work_packages/form` endpoint, but already specifies the work package's project in the path, so that it does not have to be defined in the request body.

- HTTP Method: `POST`
- Endpoint: `/api/v3/projects/{id}/work_packages/form`

**Parameters**

| Name | Type                                                        | Required | Description                                                 |
| :--- | :---------------------------------------------------------- | :------- | :---------------------------------------------------------- |
| body | [WorkPackageWriteModel](../models/WorkPackageWriteModel.md) | ❌       | The request body.                                           |
| id   | number                                                      | ✅       | ID of the project in which the work package will be created |

**Return Type**

`WorkPackageFormModel`

**Example Usage Code Snippet**

```mcp

```

## projectAvailableAssignees

Gets a list of users that can be assigned to work packages in the given project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects/{id}/available_assignees`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Project id  |

**Return Type**

`AvailableAssigneesModel`

**Example Usage Code Snippet**

```mcp

```

## listWorkPackages

Returns a collection of work packages.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages`

**Parameters**

| Name       | Type    | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| :--------- | :------ | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| offset     | number  | ❌       | Page number inside the requested collection.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| pageSize   | number  | ❌       | Number of elements to display per page.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| filters    | string  | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. If no filter is to be applied, the client should send an empty array (`[]`), otherwise a default filter is applied. A Currently supported filters are (there are additional filters added by modules): - assigned_to - assignee_or_group - attachment_base - attachment_content - attachment_file_name - author - blocked - blocks - category - comment - created_at - custom_field - dates_interval - description - done_ratio - due_date - duplicated - duplicates - duration - estimated_hours - file_link_origin_id - follows - group - id - includes - linkable_to_storage_id - linkable_to_storage_url - manual_sort - milestone - only_subproject - parent - partof - precedes - principal_base - priority - project - relatable - relates - required - requires - responsible - role - search - start_date - status - storage_id - storage_url - subject - subject_or_id - subproject - type - typeahead - updated_at - version - watcher - work_package |
| sortBy     | string  | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| groupBy    | string  | ❌       | The column to group by.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| showSums   | boolean | ❌       | Indicates whether properties should be summed up if they support it.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| select     | string  | ❌       | Comma separated list of properties to include.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| timestamps | string  | ❌       | In order to perform a [baseline comparison](/docs/api/baseline-comparisons), you may provide one or several timestamps in ISO-8601 format as comma-separated list. The timestamps may be absolute or relative, such as ISO8601 dates, ISO8601 durations and the following relative date keywords: "oneDayAgo@HH:MM+HH:MM", "lastWorkingDay@HH:MM+HH:MM", "oneWeekAgo@HH:MM+HH:MM", "oneMonthAgo@HH:MM+HH:MM". The first "HH:MM" part represents the zero paded hours and minutes. The last "+HH:MM" part represents the timezone offset from UTC associated with the time, the offset can be positive or negative e.g."oneDayAgo@01:00+01:00", "oneDayAgo@01:00-01:00". Usually, the first timestamp is the baseline date, the last timestamp is the current date. Values older than 1 day are accepted only with valid Enterprise Token available.                                                                                                                                                                                                                                                                         |

**Return Type**

`WorkPackagesModel`

**Example Usage Code Snippet**

```mcp

```

## createWorkPackage

When calling this endpoint the client provides a single object, containing at least the properties and links that are required, in the body. The required fields of a WorkPackage can be found in its schema, which is embedded in the respective form. Note that it is only allowed to provide properties or links supporting the write operation. A project link must be set when creating work packages through this route. When setting start date, finish date, and duration together, their correctness will be checked and a 422 error will be returned if one value does not match with the two others. You can make the server compute a value: set only two values in the request and the third one will be computed and returned in the response. For instance, when sending `{ "startDate": "2022-08-23", duration: "P2D" }`, the response will include `{ "dueDate": "2022-08-24" }`.

- HTTP Method: `POST`
- Endpoint: `/api/v3/work_packages`

**Parameters**

| Name   | Type                                              | Required | Description                                                                                                                                                                                                                             |
| :----- | :------------------------------------------------ | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| body   | [WorkPackageModel](../models/WorkPackageModel.md) | ❌       | The request body.                                                                                                                                                                                                                       |
| notify | boolean                                           | ❌       | Indicates whether change notifications (e.g. via E-Mail) should be sent. Note that this controls notifications for all users interested in changes to the work package (e.g. watchers, author and assignee), not just the current user. |

**Return Type**

`WorkPackageModel`

**Example Usage Code Snippet**

```mcp

```

## formCreateWorkPackage

When calling this endpoint, the client provides a single object containing the properties and links to be created, in the body. The input is validated and a schema response is returned. If the validation errors of the response is empty, the same payload can be used to create a work package. Only the properties of the work package write model are allowed to set on a work package on creation. When setting start date, finish date, and duration together, their correctness will be checked and a validation error will be returned if one value does not match with the two others. You can make the server compute a value: set only two values in the request and the third one will be computed and returned in the response. For instance, when sending `{ "startDate": "2022-08-23", duration: "P2D" }`, the response will include `{ "dueDate": "2022-08-24" }`.

- HTTP Method: `POST`
- Endpoint: `/api/v3/work_packages/form`

**Parameters**

| Name | Type                                                        | Required | Description       |
| :--- | :---------------------------------------------------------- | :------- | :---------------- |
| body | [WorkPackageWriteModel](../models/WorkPackageWriteModel.md) | ❌       | The request body. |

**Return Type**

`WorkPackageFormModel`

**Example Usage Code Snippet**

```mcp

```

## listWorkPackageSchemas

List all work package schemas that match the given filters. This endpoint does not return a successful response, if no filter is given.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/schemas`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                 |
| :------ | :----- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ✅       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + id: The schema's id Schema id has the form `project_id-work_package_type_id`. |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewWorkPackageSchema

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/schemas/{identifier}`

**Parameters**

| Name       | Type   | Required | Description              |
| :--------- | :----- | :------- | :----------------------- |
| identifier | string | ✅       | Identifier of the schema |

**Example Usage Code Snippet**

```mcp

```

## viewWorkPackage

Returns the specified work package.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}`

**Parameters**

| Name       | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| :--------- | :----- | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id         | number | ✅       | Work package id                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| timestamps | string | ❌       | In order to perform a [baseline comparison](/docs/api/baseline-comparisons) of the work-package attributes, you may provide one or several timestamps in ISO-8601 format as comma-separated list. The timestamps may be absolute or relative, such as ISO8601 dates, ISO8601 durations and the following relative date keywords: "oneDayAgo@HH:MM+HH:MM", "lastWorkingDay@HH:MM+HH:MM", "oneWeekAgo@HH:MM+HH:MM", "oneMonthAgo@HH:MM+HH:MM". The first "HH:MM" part represents the zero paded hours and minutes. The last "+HH:MM" part represents the timezone offset from UTC associated with the time, the offset can be positive or negative e.g."oneDayAgo@01:00+01:00", "oneDayAgo@01:00-01:00". Usually, the first timestamp is the baseline date, the last timestamp is the current date. Values older than 1 day are accepted only with valid Enterprise Token available. |

**Return Type**

`WorkPackageModel`

**Example Usage Code Snippet**

```mcp

```

## updateWorkPackage

When calling this endpoint the client provides a single object, containing the properties and links that it wants to change, in the body. Note that it is only allowed to provide properties or links supporting the **write** operation. Additionally to the fields the client wants to change, it is mandatory to provide the value of `lockVersion` which was received by the `GET` request this change originates from. The value of `lockVersion` is used to implement [optimistic locking](https://en.wikipedia.org/wiki/Optimistic_concurrency_control).

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/work_packages/{id}`

**Parameters**

| Name   | Type                                              | Required | Description                                                                                                                                                                                                           |
| :----- | :------------------------------------------------ | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| body   | [WorkPackageModel](../models/WorkPackageModel.md) | ❌       | The request body.                                                                                                                                                                                                     |
| id     | number                                            | ✅       | Work package id                                                                                                                                                                                                       |
| notify | boolean                                           | ❌       | Indicates whether change notifications should be sent. Note that this controls notifications for all users interested in changes to the work package (e.g. watchers, author and assignee), not just the current user. |

**Return Type**

`WorkPackagePatchModel`

**Example Usage Code Snippet**

```mcp

```

## deleteWorkPackage

Deletes the work package, as well as: - all associated time entries - its hierarchy of child work packages

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/work_packages/{id}`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | Work package id |

**Example Usage Code Snippet**

```mcp

```

## listWorkPackageActivities

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/activities`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | Work package id |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## commentWorkPackage

Creates an activity for the selected work package and, on success, returns the updated activity.

- HTTP Method: `POST`
- Endpoint: `/api/v3/work_packages/{id}/activities`

**Parameters**

| Name   | Type                                                                | Required | Description                                                                                                                                                                                                                             |
| :----- | :------------------------------------------------------------------ | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| body   | [CommentWorkPackageRequest](../models/CommentWorkPackageRequest.md) | ❌       | The request body.                                                                                                                                                                                                                       |
| id     | number                                                              | ✅       | Work package id                                                                                                                                                                                                                         |
| notify | boolean                                                             | ❌       | Indicates whether change notifications (e.g. via E-Mail) should be sent. Note that this controls notifications for all users interested in changes to the work package (e.g. watchers, author and assignee), not just the current user. |

**Example Usage Code Snippet**

```mcp

```

## workPackageAvailableAssignees

Gets a list of users that can be assigned to the given work package.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/available_assignees`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | Work package id |

**Return Type**

`AvailableAssigneesModel`

**Example Usage Code Snippet**

```mcp

```

## availableProjectsForWorkPackage

Gets a list of projects that are available as projects to which the work package can be moved.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/available_projects`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | work package id |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## listAvailableRelationCandidates

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/available_relation_candidates`

**Parameters**

| Name     | Type   | Required | Description                                                                                                                                                   |
| :------- | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| id       | number | ✅       | Project id                                                                                                                                                    |
| pageSize | number | ❌       | Maximum number of candidates to list (default 10)                                                                                                             |
| filters  | string | ❌       | JSON specifying filter conditions. Accepts the same filters as the [work packages](https://www.openproject.org/docs/api/endpoints/work-packages/) endpoint.   |
| query    | string | ❌       | Shortcut for filtering by ID or subject                                                                                                                       |
| type     | string | ❌       | Type of relation to find candidates for (default "relates")                                                                                                   |
| sortBy   | string | ❌       | JSON specifying sort criteria. Accepts the same sort criteria as the [work packages](https://www.openproject.org/docs/api/endpoints/work-packages/) endpoint. |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## availableWatchers

Gets a list of users that are able to be watchers of the specified work package.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/available_watchers`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | work package id |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## listWorkPackageFileLinks

Gets all file links of a work package. As a side effect, for every file link a request is sent to the storage's origin to fetch live data and patch the file link's data before returning, as well as retrieving permissions of the user on this origin file.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/file_links`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                               |
| :------ | :----- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id      | number | ✅       | Work package id                                                                                                                                                                                           |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. The following filters are supported: - storage |

**Return Type**

`FileLinkCollectionReadModel`

**Example Usage Code Snippet**

```mcp

```

## createWorkPackageFileLink

Creates file links on a work package. The request is interpreted as a bulk insert, where every element of the collection is validated separately. Each element contains the origin meta data and a link to the storage, the file link is about to point to. The storage link can be provided as a resource link with id or as the host url. The file's id and name are considered mandatory information. The rest of the origin meta data SHOULD be provided by the client. The _mimeType_ SHOULD be a standard mime type. An empty mime type will be handled as unknown. To link a folder, the custom mime type `application/x-op-directory` MUST be used. Up to 20 file links can be submitted at once. If any element data is invalid, no file links will be created. If a file link with matching origin id, work package, and storage already exists, then it will not create an additional file link or update the meta data. Instead the information from the existing file link will be returned.

- HTTP Method: `POST`
- Endpoint: `/api/v3/work_packages/{id}/file_links`

**Parameters**

| Name | Type                                                                      | Required | Description       |
| :--- | :------------------------------------------------------------------------ | :------- | :---------------- |
| body | [FileLinkCollectionWriteModel](../models/FileLinkCollectionWriteModel.md) | ❌       | The request body. |
| id   | number                                                                    | ✅       | Work package id   |

**Return Type**

`FileLinkCollectionReadModel`

**Example Usage Code Snippet**

```mcp

```

## formEditWorkPackage

When calling this endpoint, the client provides a single object containing the properties and links to be edited, in the body. The input is validated and a schema response is returned. If the validation errors of the response is empty, the same payload can be used to edit the work package. Only the properties of the work package write model are allowed to set on a work package on editing. When setting start date, finish date, and duration together, their correctness will be checked and a validation error will be returned if one value does not match with the two others. You can make the server compute a value: set only two values in the request and the third one will be computed and returned in the response. For instance, when sending `{ "startDate": "2022-08-23", duration: "P2D" }`, the response will include `{ "dueDate": "2022-08-24" }`.

- HTTP Method: `POST`
- Endpoint: `/api/v3/work_packages/{id}/form`

**Parameters**

| Name | Type                                                        | Required | Description                           |
| :--- | :---------------------------------------------------------- | :------- | :------------------------------------ |
| body | [WorkPackageWriteModel](../models/WorkPackageWriteModel.md) | ❌       | The request body.                     |
| id   | number                                                      | ✅       | ID of the work package being modified |

**Return Type**

`WorkPackageFormModel`

**Example Usage Code Snippet**

```mcp

```

## revisions

Gets a list of revisions that are linked to this work package, e.g., because it is referenced in the commit message of the revision. Only linked revisions from repositories are shown if the user has the view changesets permission in the defining project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/revisions`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | Work package id |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## reminders

Gets a list of your upcoming reminders for this work package.

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/reminders`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | Work package id |

**Return Type**

`ReminderModel`

**Example Usage Code Snippet**

```mcp

```

## listWatchers

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/watchers`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | Work package id |

**Return Type**

`WatchersModel`

**Example Usage Code Snippet**

```mcp

```

## addWatcher

Adds a watcher to the specified work package. The request is expected to contain a single JSON object, that contains a link object under the `user` key. The response will be user added as watcher. In case the user was already watching the work package an `HTTP 200` is returned, an `HTTP 201` if the user was added as a new watcher.

- HTTP Method: `POST`
- Endpoint: `/api/v3/work_packages/{id}/watchers`

**Parameters**

| Name | Type                                                | Required | Description       |
| :--- | :-------------------------------------------------- | :------- | :---------------- |
| body | [AddWatcherRequest](../models/AddWatcherRequest.md) | ❌       | The request body. |
| id   | number                                              | ✅       | Work package id   |

**Example Usage Code Snippet**

```mcp

```

## removeWatcher

Removes the specified user from the list of watchers for the given work package. If the request succeeds, the specified user is not watching the work package anymore. _Note: This might also be the case, if the specified user did not watch the work package prior to the request._

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/work_packages/{id}/watchers/{user_id}`

**Parameters**

| Name   | Type   | Required | Description     |
| :----- | :----- | :------- | :-------------- |
| id     | number | ✅       | Work package id |
| userId | number | ✅       | User id         |

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
