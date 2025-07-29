# CategoriesByProjectModel

**Properties**

| Name       | Type                             | Required | Description                                               |
| :--------- | :------------------------------- | :------- | :-------------------------------------------------------- |
| \_type     | CategoriesByProjectModelType     | ✅       |                                                           |
| total      | number                           | ✅       | The total amount of elements available in the collection. |
| count      | number                           | ✅       | Actual amount of elements in this response.               |
| \_links    | CategoriesByProjectModelLinks    | ✅       |                                                           |
| \_embedded | CategoriesByProjectModelEmbedded | ✅       |                                                           |

# CategoriesByProjectModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# CategoriesByProjectModelLinks

**Properties**

| Name | Type          | Required | Description                                                  |
| :--- | :------------ | :------- | :----------------------------------------------------------- |
| self | \_LinksSelf11 | ✅       | The categories collection **Resource**: CategoriesCollection |

# \_LinksSelf11

The categories collection **Resource**: CategoriesCollection

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

# CategoriesByProjectModelEmbedded

**Properties**

| Name     | Type                  | Required | Description |
| :------- | :-------------------- | :------- | :---------- |
| elements | \_EmbeddedElements3[] | ❌       |             |

# \_EmbeddedElements3

Collection of Categories

**Properties**

| Name    | Type           | Required | Description   |
| :------ | :------------- | :------- | :------------ |
| id      | number         | ❌       | Category id   |
| name    | string         | ❌       | Category name |
| \_links | ElementsLinks3 | ❌       |               |

# ElementsLinks3

**Properties**

| Name            | Type                    | Required | Description                                                            |
| :-------------- | :---------------------- | :------- | :--------------------------------------------------------------------- |
| self            | \_LinksSelf12           | ✅       | This category **Resource**: Category                                   |
| project         | \_LinksProject3         | ✅       | The project of this category **Resource**: Project                     |
| defaultAssignee | \_LinksDefaultAssignee2 | ❌       | Default assignee for work packages of this category **Resource**: User |

# \_LinksSelf12

This category **Resource**: Category

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

# \_LinksProject3

The project of this category **Resource**: Project

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

# \_LinksDefaultAssignee2

Default assignee for work packages of this category **Resource**: User

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
