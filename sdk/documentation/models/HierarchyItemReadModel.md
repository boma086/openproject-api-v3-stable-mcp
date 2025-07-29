# HierarchyItemReadModel

**Properties**

| Name    | Type                        | Required | Description                                          |
| :------ | :-------------------------- | :------- | :--------------------------------------------------- |
| \_type  | HierarchyItemReadModelType  | ❌       |                                                      |
| id      | number                      | ❌       | Hierarchy item identifier                            |
| label   | string                      | ❌       | The label of the hierarchy item                      |
| short   | string                      | ❌       | The short name of the hierarchy item                 |
| depth   | number                      | ❌       | The hierarchy depth. The root item has a depth of 0. |
| \_links | HierarchyItemReadModelLinks | ❌       |                                                      |

# HierarchyItemReadModelType

**Properties**

| Name           | Type   | Required | Description     |
| :------------- | :----- | :------- | :-------------- |
| HIERARCHY_ITEM | string | ✅       | "HierarchyItem" |

# HierarchyItemReadModelLinks

**Properties**

| Name     | Type               | Required | Description                                                                                     |
| :------- | :----------------- | :------- | :---------------------------------------------------------------------------------------------- |
| self     | \_LinksSelf15      | ❌       | This hierarchy item **Resource**: HierarchyItem                                                 |
| parent   | \_LinksParent2     | ❌       | The hierarchy item that is the parent of the current hierarchy item **Resource**: HierarchyItem |
| children | \_LinksChildren2[] | ❌       |                                                                                                 |

# \_LinksSelf15

This hierarchy item **Resource**: HierarchyItem

**Properties**

| Name       | Type    | Required | Description                                                            |
| :--------- | :------ | :------- | :--------------------------------------------------------------------- |
| href       | string  | ✅       | URL to the referenced resource (might be relative)                     |
| title      | string  | ❌       | Representative label for the resource                                  |
| templated  | boolean | ❌       | If true the href contains parts that need to be replaced by the client |
| method     | string  | ❌       | The HTTP verb to use when requesting the resource                      |
| payload    | any     | ❌       | The payload to send in the request to achieve the desired result       |
| identifier | string  | ❌       | An optional unique identifier to the link object                       |
| type       | string  | ❌       | The MIME-Type of the returned resource.                                |

# \_LinksParent2

The hierarchy item that is the parent of the current hierarchy item **Resource**: HierarchyItem

**Properties**

| Name       | Type    | Required | Description                                                            |
| :--------- | :------ | :------- | :--------------------------------------------------------------------- |
| href       | string  | ✅       | URL to the referenced resource (might be relative)                     |
| title      | string  | ❌       | Representative label for the resource                                  |
| templated  | boolean | ❌       | If true the href contains parts that need to be replaced by the client |
| method     | string  | ❌       | The HTTP verb to use when requesting the resource                      |
| payload    | any     | ❌       | The payload to send in the request to achieve the desired result       |
| identifier | string  | ❌       | An optional unique identifier to the link object                       |
| type       | string  | ❌       | The MIME-Type of the returned resource.                                |

# \_LinksChildren2

A hierarchy item that is a child of the current hierarchy item **Resource**: HierarchyItem

**Properties**

| Name       | Type    | Required | Description                                                            |
| :--------- | :------ | :------- | :--------------------------------------------------------------------- |
| href       | string  | ✅       | URL to the referenced resource (might be relative)                     |
| title      | string  | ❌       | Representative label for the resource                                  |
| templated  | boolean | ❌       | If true the href contains parts that need to be replaced by the client |
| method     | string  | ❌       | The HTTP verb to use when requesting the resource                      |
| payload    | any     | ❌       | The payload to send in the request to achieve the desired result       |
| identifier | string  | ❌       | An optional unique identifier to the link object                       |
| type       | string  | ❌       | The MIME-Type of the returned resource.                                |

<!-- This file was generated by liblab | https://liblab.com/ -->
