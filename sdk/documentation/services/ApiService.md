# ApiService

A list of all methods in the `ApiService` service. Click on the method name to view detailed information about that method.

| Methods                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :---------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [getCustomFieldItems](#getcustomfielditems)           | Retrieves the hierarchy of custom fields. The hierarchy is a tree structure of hierarchy items. It is represented as a flat list of items, where each item has a reference to its parent and children. The list is ordered in a depth-first manner. The first item is the requested parent. If parent was unset, the root item is returned as first element. Passing the `depth` query parameter allows to limit the depth of the hierarchy. If the depth is unset, the full hierarchy tree is returned. If the depth is set to `0`, only the requested parent is returned. Any other positive integer will return the number of children levels specified by this value. This endpoint only returns, if the custom field is of type `hierarchy`. |
| [getCustomFieldItem](#getcustomfielditem)             | Retrieves a single custom field item specified by its unique identifier.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [getCustomFieldItemBranch](#getcustomfielditembranch) | Retrieves the branch of a single custom field item specified by its unique identifier. A branch is list of all ancestors, starting with the root item and finishing with the item itself.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |

## getCustomFieldItems

Retrieves the hierarchy of custom fields. The hierarchy is a tree structure of hierarchy items. It is represented as a flat list of items, where each item has a reference to its parent and children. The list is ordered in a depth-first manner. The first item is the requested parent. If parent was unset, the root item is returned as first element. Passing the `depth` query parameter allows to limit the depth of the hierarchy. If the depth is unset, the full hierarchy tree is returned. If the depth is set to `0`, only the requested parent is returned. Any other positive integer will return the number of children levels specified by this value. This endpoint only returns, if the custom field is of type `hierarchy`.

- HTTP Method: `GET`
- Endpoint: `/api/v3/custom_fields/{id}/items`

**Parameters**

| Name   | Type   | Required | Description                                 |
| :----- | :----- | :------- | :------------------------------------------ |
| id     | number | ✅       | The custom field's unique identifier        |
| parent | number | ❌       | The identifier of the parent hierarchy item |
| depth  | number | ❌       | The level of hierarchy depth                |

**Return Type**

`HierarchyItemCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## getCustomFieldItem

Retrieves a single custom field item specified by its unique identifier.

- HTTP Method: `GET`
- Endpoint: `/api/v3/custom_field_items/{id}`

**Parameters**

| Name | Type   | Required | Description                               |
| :--- | :----- | :------- | :---------------------------------------- |
| id   | number | ✅       | The custom field item's unique identifier |

**Return Type**

`HierarchyItemReadModel`

**Example Usage Code Snippet**

```mcp

```

## getCustomFieldItemBranch

Retrieves the branch of a single custom field item specified by its unique identifier. A branch is list of all ancestors, starting with the root item and finishing with the item itself.

- HTTP Method: `GET`
- Endpoint: `/api/v3/custom_field_items/{id}/branch`

**Parameters**

| Name | Type   | Required | Description                               |
| :--- | :----- | :------- | :---------------------------------------- |
| id   | number | ✅       | The custom field item's unique identifier |

**Return Type**

`HierarchyItemCollectionModel`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
