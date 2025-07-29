# NotificationCollectionModel

**Properties**

| Name       | Type                                | Required | Description                                               |
| :--------- | :---------------------------------- | :------- | :-------------------------------------------------------- |
| \_type     | NotificationCollectionModelType     | ✅       |                                                           |
| total      | number                              | ✅       | The total amount of elements available in the collection. |
| count      | number                              | ✅       | Actual amount of elements in this response.               |
| \_links    | NotificationCollectionModelLinks    | ✅       |                                                           |
| \_embedded | NotificationCollectionModelEmbedded | ✅       |                                                           |

# NotificationCollectionModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# NotificationCollectionModelLinks

**Properties**

| Name       | Type               | Required | Description                                                                             |
| :--------- | :----------------- | :------- | :-------------------------------------------------------------------------------------- |
| self       | \_LinksSelf46      | ✅       | This notification collection **Resource**: NotificationCollectionModel                  |
| jumpTo     | \_LinksJumpTo4     | ❌       | The notification collection at another offset **Resource**: NotificationCollectionModel |
| changeSize | \_LinksChangeSize4 | ❌       | The notification collection with another size **Resource**: NotificationCollectionModel |

# \_LinksSelf46

This notification collection **Resource**: NotificationCollectionModel

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

# \_LinksJumpTo4

The notification collection at another offset **Resource**: NotificationCollectionModel

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

# \_LinksChangeSize4

The notification collection with another size **Resource**: NotificationCollectionModel

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

# NotificationCollectionModelEmbedded

**Properties**

| Name           | Type                | Required | Description |
| :------------- | :------------------ | :------- | :---------- |
| elements       | NotificationModel[] | ✅       |             |
| detailsSchemas | SchemaModel[]       | ✅       |             |

<!-- This file was generated by liblab | https://liblab.com/ -->
