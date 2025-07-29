# RelationsService

A list of all methods in the `RelationsService` service. Click on the method name to view detailed information about that method.

| Methods                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| :-------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [listRelations](#listrelations)   | Lists all relations according to the given (optional, logically conjunctive) filters and ordered by ID. The response only includes relations between work packages which the user is allowed to see.                                                                                                                                                                                                                                                                                                                                                                                                    |
| [getRelation](#getrelation)       | Get a single relation specified by its unique identifier.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [updateRelation](#updaterelation) | When calling this endpoint the client provides a single object, containing the properties and links that it wants to change, in the body. It is only allowed to provide properties or links supporting the **write** operation. Note that changing the `type` of a relation invariably also changes the respective `reverseType` as well as the "name" of it. The returned Relation object will reflect that change. For instance if you change a Relation's `type` to "follows" then the `reverseType` will be changed to `precedes`. It is not allowed to change a relation's involved work packages. |
| [deleteRelation](#deleterelation) | Deletes the relation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [createRelation](#createrelation) | Create a work package relation on the given work package. A successful creation will result in a relation between two work packages, thus appearing on both involved work package resources.                                                                                                                                                                                                                                                                                                                                                                                                            |

## listRelations

Lists all relations according to the given (optional, logically conjunctive) filters and ordered by ID. The response only includes relations between work packages which the user is allowed to see.

- HTTP Method: `GET`
- Endpoint: `/api/v3/relations`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Valid fields to filter by are: - id - ID of relation - from - ID of work package from which the filtered relations emanates. - to - ID of work package to which this related points. - involved - ID of either the `from` or the `to` work package. - type - The type of relation to filter by, e.g. "follows". |
| sortBy  | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint.                                                                                                                                                                                                                                                                                                                     |

**Return Type**

`RelationCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## getRelation

Get a single relation specified by its unique identifier.

- HTTP Method: `GET`
- Endpoint: `/api/v3/relations/{id}`

**Parameters**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| id   | number | ✅       | Relation id |

**Return Type**

`RelationReadModel`

**Example Usage Code Snippet**

```mcp

```

## updateRelation

When calling this endpoint the client provides a single object, containing the properties and links that it wants to change, in the body. It is only allowed to provide properties or links supporting the **write** operation. Note that changing the `type` of a relation invariably also changes the respective `reverseType` as well as the "name" of it. The returned Relation object will reflect that change. For instance if you change a Relation's `type` to "follows" then the `reverseType` will be changed to `precedes`. It is not allowed to change a relation's involved work packages.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/relations/{id}`

**Parameters**

| Name | Type                                                  | Required | Description       |
| :--- | :---------------------------------------------------- | :------- | :---------------- |
| body | [RelationWriteModel](../models/RelationWriteModel.md) | ❌       | The request body. |
| id   | number                                                | ✅       | Relation ID       |

**Return Type**

`RelationReadModel`

**Example Usage Code Snippet**

```mcp

```

## deleteRelation

Deletes the relation.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/relations/{id}`

**Parameters**

| Name | Type   | Required | Description                                    |
| :--- | :----- | :------- | :--------------------------------------------- |
| id   | number | ✅       | The unique identifier of the relation resource |

**Example Usage Code Snippet**

```mcp

```

## createRelation

Create a work package relation on the given work package. A successful creation will result in a relation between two work packages, thus appearing on both involved work package resources.

- HTTP Method: `POST`
- Endpoint: `/api/v3/work_packages/{id}/relations`

**Parameters**

| Name | Type                                                  | Required | Description       |
| :--- | :---------------------------------------------------- | :------- | :---------------- |
| body | [RelationWriteModel](../models/RelationWriteModel.md) | ❌       | The request body. |
| id   | number                                                | ✅       | Work package id   |

**Return Type**

`RelationReadModel`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
