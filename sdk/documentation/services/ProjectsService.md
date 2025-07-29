# ProjectsService

A list of all methods in the `ProjectsService` service. Click on the method name to view detailed information about that method.

| Methods                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| :---------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listProjects](#listprojects)                                                 | Returns a collection of projects. The collection can be filtered via query parameters similar to how work packages are filtered. In addition to the provided filter, the result set is always limited to only contain projects the client is allowed to see.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [createProject](#createproject)                                               | Creates a new project, applying the attributes provided in the body. You can use the form and schema to be retrieve the valid attribute values and by that be guided towards successful creation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [projectCreateForm](#projectcreateform)                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [viewProjectSchema](#viewprojectschema)                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [viewProject](#viewproject)                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [updateProject](#updateproject)                                               | Updates the given project by applying the attributes provided in the body.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [deleteProject](#deleteproject)                                               | Deletes the project permanently. As this is a lengthy process, the actual deletion is carried out asynchronously. So the project might exist well after the request has returned successfully. To prevent unwanted changes to the project scheduled for deletion, it is archived at once.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [projectUpdateForm](#projectupdateform)                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [createProjectCopy](#createprojectcopy)                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [projectCopyForm](#projectcopyform)                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [viewProjectStatus](#viewprojectstatus)                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [listAvailableParentProjectCandidates](#listavailableparentprojectcandidates) | Lists projects which can become parent to another project. Only sound candidates are returned. For instance a project cannot become parent of itself or its children. To specify the project for which a parent is queried for, the `of` parameter can be provided. If no `of` parameter is provided, a new project is assumed. Then, the check for the hierarchy is omitted as a new project cannot be part of a hierarchy yet. Candidates can be filtered. Most commonly one will want to filter by name or identifier. You can do this through the `filters` parameter which works just like the work package index. For instance to find all parent candidates with "rollout" in their name: `?filters=[{"name_and_identifier":{"operator":"~","values":["rollout"]}}]` |
| [listProjectsWithVersion](#listprojectswithversion)                           | This endpoint lists the projects where the given version is available. The projects returned depend on the sharing settings of the given version, but are also limited to the projects that the current user is allowed to see.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

## listProjects

Returns a collection of projects. The collection can be filtered via query parameters similar to how work packages are filtered. In addition to the provided filter, the result set is always limited to only contain projects the client is allowed to see.

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| :------ | :----- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + active: based on the active property of the project + ancestor: filters projects by their ancestor. A project is not considered to be its own ancestor. + available*project_attributes: filters projects based on the activated project project attributes. + created_at: based on the time the project was created + id: based on projects' id. + latest_activity_at: based on the time the last activity was registered on a project. + project_phase_any: based on the project phases active in a project. + name_and_identifier: based on both the name and the identifier. + parent_id: filters projects by their parent. + principal: based on members of the project. + storage_id: filters projects by linked storages + storage_url: filters projects by linked storages identified by the host url + type_id: based on the types active in a project. + user_action: based on the actions the current user has in the project. + visible: based on the visibility for the user (id) provided as the filter value. This filter is useful for admins to identify the projects visible to a user. There might also be additional filters based on the custom fields that have been configured. Each defined lifecycle step will also define a filter in this list endpoint. Given that the elements are not static but rather dynamically created on each OpenProject instance, a list cannot be provided. Those filters follow the schema: + project_start_gate*[id]: a filter on a project phase's start gate active in a project. The id is the id of the phase the gate belongs to. + project*finish_gate*[id]: a filter on a project phase's finish gate active in a project. The id is the id of the phase the gate belongs to. + project*phase*[id]: a filter on a project phase active in a project. The id is the id of the phase queried for. |
| sortBy  | string | ❌       | JSON specifying sort criteria. Currently supported orders are: + id + name + typeahead (sorting by hierarchy and name) + created_at + public + latest_activity_at + required_disk_space There might also be additional orders based on the custom fields that have been configured.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| select  | string | ❌       | Comma separated list of properties to include.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

**Return Type**

`ProjectCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createProject

Creates a new project, applying the attributes provided in the body. You can use the form and schema to be retrieve the valid attribute values and by that be guided towards successful creation.

- HTTP Method: `POST`
- Endpoint: `/api/v3/projects`

**Parameters**

| Name | Type                                      | Required | Description       |
| :--- | :---------------------------------------- | :------- | :---------------- |
| body | [ProjectModel](../models/ProjectModel.md) | ❌       | The request body. |

**Return Type**

`ProjectModel`

**Example Usage Code Snippet**

```mcp

```

## projectCreateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/projects/form`

**Parameters**

| Name | Type | Required | Description       |
| :--- | :--- | :------- | :---------------- |
| body | any  | ❌       | The request body. |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewProjectSchema

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects/schema`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewProject

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Project id  |

**Return Type**

`ProjectModel`

**Example Usage Code Snippet**

```mcp

```

## updateProject

Updates the given project by applying the attributes provided in the body.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/projects/{id}`

**Parameters**

| Name | Type                                      | Required | Description       |
| :--- | :---------------------------------------- | :------- | :---------------- |
| body | [ProjectModel](../models/ProjectModel.md) | ❌       | The request body. |
| id   | number                                    | ✅       | Project id        |

**Return Type**

`ProjectModel`

**Example Usage Code Snippet**

```mcp

```

## deleteProject

Deletes the project permanently. As this is a lengthy process, the actual deletion is carried out asynchronously. So the project might exist well after the request has returned successfully. To prevent unwanted changes to the project scheduled for deletion, it is archived at once.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/projects/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Project id  |

**Example Usage Code Snippet**

```mcp

```

## projectUpdateForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/projects/{id}/form`

**Parameters**

| Name | Type   | Required | Description       |
| :--- | :----- | :------- | :---------------- |
| body | any    | ❌       | The request body. |
| id   | number | ✅       | Project id        |

**Example Usage Code Snippet**

```mcp

```

## createProjectCopy

- HTTP Method: `POST`
- Endpoint: `/api/v3/projects/{id}/copy`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Project id  |

**Example Usage Code Snippet**

```mcp

```

## projectCopyForm

- HTTP Method: `POST`
- Endpoint: `/api/v3/projects/{id}/copy/form`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Project id  |

**Example Usage Code Snippet**

```mcp

```

## viewProjectStatus

- HTTP Method: `GET`
- Endpoint: `/api/v3/project_statuses/{id}`

**Parameters**

| Name | Type   | Required | Description       |
| :--- | :----- | :------- | :---------------- |
| id   | string | ✅       | Project status id |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## listAvailableParentProjectCandidates

Lists projects which can become parent to another project. Only sound candidates are returned. For instance a project cannot become parent of itself or its children. To specify the project for which a parent is queried for, the `of` parameter can be provided. If no `of` parameter is provided, a new project is assumed. Then, the check for the hierarchy is omitted as a new project cannot be part of a hierarchy yet. Candidates can be filtered. Most commonly one will want to filter by name or identifier. You can do this through the `filters` parameter which works just like the work package index. For instance to find all parent candidates with "rollout" in their name: `?filters=[{"name_and_identifier":{"operator":"~","values":["rollout"]}}]`

- HTTP Method: `GET`
- Endpoint: `/api/v3/projects/available_parent_projects`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                          |
| :------ | :----- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions.                                                                                                                                                                                                   |
| of      | string | ❌       | The id or identifier of the project the parent candidate is determined for                                                                                                                                                           |
| sortBy  | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint and allows all the filters and sortBy supported by the project list end point. |

**Return Type**

`ListAvailableParentProjectCandidatesModel`

**Example Usage Code Snippet**

```mcp

```

## listProjectsWithVersion

This endpoint lists the projects where the given version is available. The projects returned depend on the sharing settings of the given version, but are also limited to the projects that the current user is allowed to see.

- HTTP Method: `GET`
- Endpoint: `/api/v3/versions/{id}/projects`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Version id  |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
