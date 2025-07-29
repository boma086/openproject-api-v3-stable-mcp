# ActionsCapabilitiesService

A list of all methods in the `ActionsCapabilitiesService` service. Click on the method name to view detailed information about that method.

| Methods                                 | Description                                                                                                                                                                                                                                                                                                                 |
| :-------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listActions](#listactions)             | Returns a collection of actions. The client can choose to filter the actions similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain actions, for which the requesting client has sufficient permissions.                                     |
| [viewAction](#viewaction)               | Returns an individual action.                                                                                                                                                                                                                                                                                               |
| [listCapabilities](#listcapabilities)   | Returns a collection of actions assigned to a principal in a context. The client can choose to filter the actions similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain actions, for which the requesting client has sufficient permissions |
| [viewGlobalContext](#viewglobalcontext) | Returns the global capability context. This context is necessary to consistently link to a context even if the context is not a project.                                                                                                                                                                                    |
| [viewCapabilities](#viewcapabilities)   |                                                                                                                                                                                                                                                                                                                             |

## listActions

Returns a collection of actions. The client can choose to filter the actions similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain actions, for which the requesting client has sufficient permissions.

- HTTP Method: `GET`
- Endpoint: `/api/v3/actions`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                           |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + id: Returns only the action having the id or all actions except those having the id(s). |
| sortBy  | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported sorts are: + _No sort supported yet_                                                                       |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewAction

Returns an individual action.

- HTTP Method: `GET`
- Endpoint: `/api/v3/actions/{id}`

**Parameters**

| Name | Type   | Required | Description                               |
| :--- | :----- | :------- | :---------------------------------------- |
| id   | string | ✅       | action id which is the name of the action |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## listCapabilities

Returns a collection of actions assigned to a principal in a context. The client can choose to filter the actions similar to how work packages are filtered. In addition to the provided filters, the server will reduce the result set to only contain actions, for which the requesting client has sufficient permissions

- HTTP Method: `GET`
- Endpoint: `/api/v3/capabilities`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. + action: Get all capabilities of a certain action + principal: Get all capabilities of a principal + context: Get all capabilities within a context. Note that for a project context the client needs to provide `p{id}`, e.g. `p5` and for the global context a `g` |
| sortBy  | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported sorts are: + id: Sort by the capabilities id                                                                                                                                                                                                          |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewGlobalContext

Returns the global capability context. This context is necessary to consistently link to a context even if the context is not a project.

- HTTP Method: `GET`
- Endpoint: `/api/v3/capabilities/context/global`

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## viewCapabilities

- HTTP Method: `GET`
- Endpoint: `/api/v3/capabilities/{id}`

**Parameters**

| Name | Type   | Required | Description   |
| :--- | :----- | :------- | :------------ |
| id   | string | ✅       | capability id |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
