# TypesByProjectModel

**Properties**

| Name       | Type                        | Required | Description                                               |
| :--------- | :-------------------------- | :------- | :-------------------------------------------------------- |
| \_type     | TypesByProjectModelType     | ✅       |                                                           |
| total      | number                      | ✅       | The total amount of elements available in the collection. |
| count      | number                      | ✅       | Actual amount of elements in this response.               |
| \_links    | TypesByProjectModelLinks    | ✅       |                                                           |
| \_embedded | TypesByProjectModelEmbedded | ✅       |                                                           |

# TypesByProjectModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# TypesByProjectModelLinks

**Properties**

| Name | Type          | Required | Description                                        |
| :--- | :------------ | :------- | :------------------------------------------------- |
| self | \_LinksSelf61 | ✅       | The types collection **Resource**: TypesCollection |

# \_LinksSelf61

The types collection **Resource**: TypesCollection

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

# TypesByProjectModelEmbedded

**Properties**

| Name     | Type                  | Required | Description |
| :------- | :-------------------- | :------- | :---------- |
| elements | \_EmbeddedElements9[] | ❌       |             |

# \_EmbeddedElements9

Collection of Types

**Properties**

| Name        | Type           | Required | Description                                          |
| :---------- | :------------- | :------- | :--------------------------------------------------- |
| id          | number         | ❌       | Type id                                              |
| name        | string         | ❌       | Type name                                            |
| color       | string         | ❌       | The color used to represent this type                |
| position    | number         | ❌       | Sort index of the type                               |
| isDefault   | boolean        | ❌       | Is this type active by default in new projects?      |
| isMilestone | boolean        | ❌       | Do work packages of this type represent a milestone? |
| createdAt   | string         | ❌       | Time of creation                                     |
| updatedAt   | string         | ❌       | Time of the most recent change to the user           |
| \_links     | ElementsLinks7 | ❌       |                                                      |

# ElementsLinks7

**Properties**

| Name | Type          | Required | Description                  |
| :--- | :------------ | :------- | :--------------------------- |
| self | \_LinksSelf62 | ✅       | This type **Resource**: Type |

# \_LinksSelf62

This type **Resource**: Type

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
