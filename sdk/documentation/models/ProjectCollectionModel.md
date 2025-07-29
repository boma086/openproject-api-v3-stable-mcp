# ProjectCollectionModel

**Properties**

| Name       | Type                           | Required | Description                                                                                                     |
| :--------- | :----------------------------- | :------- | :-------------------------------------------------------------------------------------------------------------- |
| \_type     | ProjectCollectionModelType     | ✅       |                                                                                                                 |
| total      | number                         | ✅       | The total amount of elements available in the collection.                                                       |
| count      | number                         | ✅       | Actual amount of elements in this response.                                                                     |
| \_links    | ProjectCollectionModelLinks    | ✅       |                                                                                                                 |
| pageSize   | number                         | ✅       | The amount of elements per page. If not set by the request this value defaults to the server's system settings. |
| offset     | number                         | ✅       | The page offset indicating on which page the element collection starts.                                         |
| \_embedded | ProjectCollectionModelEmbedded | ✅       |                                                                                                                 |

# ProjectCollectionModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# ProjectCollectionModelLinks

**Properties**

| Name             | Type                    | Required | Description                                                                                            |
| :--------------- | :---------------------- | :------- | :----------------------------------------------------------------------------------------------------- |
| self             | \_LinksSelf42           | ✅       | This collection resource. **Resource**: Collection                                                     |
| jumpTo           | \_LinksJumpTo3          | ✅       | A templated link to jump to a given offset.                                                            |
| changeSize       | \_LinksChangeSize3      | ✅       | A templated link to change the current page size.                                                      |
| previousByOffset | \_LinksPreviousByOffset | ❌       | A link to the previous page of the collection. # Conditions - The collection is not on the first page. |
| nextByOffset     | \_LinksNextByOffset     | ❌       | A link to the next page of the collection. # Conditions - The collection is not on the last page.      |
| representations  | Representations[]       | ❌       |                                                                                                        |

# \_LinksSelf42

This collection resource. **Resource**: Collection

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

# \_LinksJumpTo3

A templated link to jump to a given offset.

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

# \_LinksChangeSize3

A templated link to change the current page size.

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

# \_LinksPreviousByOffset

A link to the previous page of the collection. # Conditions - The collection is not on the first page.

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

# \_LinksNextByOffset

A link to the next page of the collection. # Conditions - The collection is not on the last page.

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

# Representations

A project collection representation in a specific file format.

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

# ProjectCollectionModelEmbedded

**Properties**

| Name     | Type           | Required | Description |
| :------- | :------------- | :------- | :---------- |
| elements | ProjectModel[] | ✅       |             |

<!-- This file was generated by liblab | https://liblab.com/ -->
