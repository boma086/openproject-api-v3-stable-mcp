# MembershipsService

A list of all methods in the `MembershipsService` service. Click on the method name to view detailed information about that method.

| Methods                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| :------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listMemberships](#listmemberships)                                 | Returns a collection of memberships. The client can choose to filter the memberships similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain memberships, for which the requesting client has sufficient permissions (_view_members_, _manage_members_).                                                                                                                                                                                                                                                 |
| [createMembership](#createmembership)                               | Creates a new membership applying the attributes provided in the body. You can use the form and schema to retrieve the valid attribute values and by that be guided towards successful creation. By providing a `notificationMessage` within the `_meta` block of the payload, the client can include a customized message to the user of the newly created membership. In case of a group, the message will be sent to every user belonging to the group. By including `{ "sendNotifications": false }` within the `_meta` block of the payload, no notifications is send out at all. |
| [getMembershipsAvailableProjects](#getmembershipsavailableprojects) | Gets a list of projects in which a membership can be created in. The list contains all projects in which the user issuing the request has the manage members permissions.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [formCreateMembership](#formcreatemembership)                       | Requests and validates the creation form for memberships. The request payload, if sent, is validated. The form endpoint itself does not create a membership.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [getMembershipSchema](#getmembershipschema)                         | Retrieves the schema for the membership resource object.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [getMembership](#getmembership)                                     | Retrieves a membership resource identified by the given id.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [updateMembership](#updatemembership)                               | Updates the given membership by applying the attributes provided in the body. By providing a `notificationMessage` within the `_meta` block of the payload, the client can include a customized message to the user of the updated membership. In case of a group, the message will be sent to every user belonging to the group. By including `{ "sendNotifications": false }` within the `_meta` block of the payload, no notifications is send out at all.                                                                                                                          |
| [deleteMembership](#deletemembership)                               | Deletes the membership.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [formUpdateMembership](#formupdatemembership)                       | Requests and validates the update form for a membership identified by the given id. The request payload, if sent, is validated. The form endpoint itself does not change the membership.                                                                                                                                                                                                                                                                                                                                                                                               |

## listMemberships

Returns a collection of memberships. The client can choose to filter the memberships similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain memberships, for which the requesting client has sufficient permissions (_view_members_, _manage_members_).

- HTTP Method: `GET`
- Endpoint: `/api/v3/memberships`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + any_name_attribute: filters memberships based on the name of the principal. All possible name variants (and also email and login) are searched. + blocked: reduces the result set to all memberships that are temporarily blocked or that are not blocked temporarily. + group: filters memberships based on the name of a group. The group however is not the principal used for filtering. Rather, the memberships of the group are used as the filter values. + name: filters memberships based on the name of the principal. Note that only the name is used which depends on a setting in the OpenProject instance. + principal: filters memberships based on the id of the principal. + project: filters memberships based on the id of the project. + role: filters memberships based on the id of any role assigned to the membership. + status: filters memberships based on the status of the principal. + created_at: filters memberships based on the time the membership was created. + updated_at: filters memberships based on the time the membership was updated last. |
| sortBy  | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported sorts are: + id: Sort by primary key + name: Sort by the name of the principal. Note that this depends on the setting for how the name is to be displayed at least for users. + email: Sort by the email address of the principal. Groups and principal users, which do not have an email, are sorted last. + status: Sort by the status of the principal. Groups and principal users, which do not have a status, are sorted together with the active users. + created_at: Sort by membership creation datetime + updated_at: Sort by the time the membership was updated last                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |

**Return Type**

`MembershipCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createMembership

Creates a new membership applying the attributes provided in the body. You can use the form and schema to retrieve the valid attribute values and by that be guided towards successful creation. By providing a `notificationMessage` within the `_meta` block of the payload, the client can include a customized message to the user of the newly created membership. In case of a group, the message will be sent to every user belonging to the group. By including `{ "sendNotifications": false }` within the `_meta` block of the payload, no notifications is send out at all.

- HTTP Method: `POST`
- Endpoint: `/api/v3/memberships`

**Parameters**

| Name | Type                                                      | Required | Description       |
| :--- | :-------------------------------------------------------- | :------- | :---------------- |
| body | [MembershipWriteModel](../models/MembershipWriteModel.md) | ❌       | The request body. |

**Return Type**

`MembershipReadModel`

**Example Usage Code Snippet**

```mcp

```

## getMembershipsAvailableProjects

Gets a list of projects in which a membership can be created in. The list contains all projects in which the user issuing the request has the manage members permissions.

- HTTP Method: `GET`
- Endpoint: `/api/v3/memberships/available_projects`

**Return Type**

`ProjectCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## formCreateMembership

Requests and validates the creation form for memberships. The request payload, if sent, is validated. The form endpoint itself does not create a membership.

- HTTP Method: `POST`
- Endpoint: `/api/v3/memberships/form`

**Parameters**

| Name | Type                                                      | Required | Description       |
| :--- | :-------------------------------------------------------- | :------- | :---------------- |
| body | [MembershipWriteModel](../models/MembershipWriteModel.md) | ❌       | The request body. |

**Return Type**

`MembershipFormModel`

**Example Usage Code Snippet**

```mcp

```

## getMembershipSchema

Retrieves the schema for the membership resource object.

- HTTP Method: `GET`
- Endpoint: `/api/v3/memberships/schema`

**Return Type**

`MembershipSchemaModel`

**Example Usage Code Snippet**

```mcp

```

## getMembership

Retrieves a membership resource identified by the given id.

- HTTP Method: `GET`
- Endpoint: `/api/v3/memberships/{id}`

**Parameters**

| Name | Type   | Required | Description   |
| :--- | :----- | :------- | :------------ |
| id   | number | ✅       | Membership id |

**Return Type**

`MembershipReadModel`

**Example Usage Code Snippet**

```mcp

```

## updateMembership

Updates the given membership by applying the attributes provided in the body. By providing a `notificationMessage` within the `_meta` block of the payload, the client can include a customized message to the user of the updated membership. In case of a group, the message will be sent to every user belonging to the group. By including `{ "sendNotifications": false }` within the `_meta` block of the payload, no notifications is send out at all.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/memberships/{id}`

**Parameters**

| Name | Type                                                      | Required | Description       |
| :--- | :-------------------------------------------------------- | :------- | :---------------- |
| body | [MembershipWriteModel](../models/MembershipWriteModel.md) | ❌       | The request body. |
| id   | number                                                    | ✅       | Membership id     |

**Return Type**

`MembershipReadModel`

**Example Usage Code Snippet**

```mcp

```

## deleteMembership

Deletes the membership.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/memberships/{id}`

**Parameters**

| Name | Type   | Required | Description   |
| :--- | :----- | :------- | :------------ |
| id   | number | ✅       | Membership id |

**Example Usage Code Snippet**

```mcp

```

## formUpdateMembership

Requests and validates the update form for a membership identified by the given id. The request payload, if sent, is validated. The form endpoint itself does not change the membership.

- HTTP Method: `POST`
- Endpoint: `/api/v3/memberships/{id}/form`

**Parameters**

| Name | Type                                                      | Required | Description       |
| :--- | :-------------------------------------------------------- | :------- | :---------------- |
| body | [MembershipWriteModel](../models/MembershipWriteModel.md) | ❌       | The request body. |
| id   | number                                                    | ✅       | Membership id     |

**Return Type**

`MembershipReadModel`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
