# GridReadModel

**Properties**

| Name        | Type               | Required | Description                                                                                  |
| :---------- | :----------------- | :------- | :------------------------------------------------------------------------------------------- |
| \_type      | GridReadModelType  | ✅       |                                                                                              |
| id          | number             | ✅       | Grid's id                                                                                    |
| rowCount    | number             | ✅       | The number of rows the grid has                                                              |
| columnCount | number             | ✅       | The number of columns the grid has                                                           |
| widgets     | GridWidgetModel[]  | ✅       | The set of `GridWidget`s selected for the grid. # Conditions - The widgets must not overlap. |
| \_links     | GridReadModelLinks | ✅       |                                                                                              |
| createdAt   | string             | ❌       | The time the grid was created.                                                               |
| updatedAt   | string             | ❌       | The time the grid was last updated.                                                          |

# GridReadModelType

**Properties**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| GRID | string | ✅       | "Grid"      |

# GridReadModelLinks

**Properties**

| Name              | Type                      | Required | Description                                                                                                                               |
| :---------------- | :------------------------ | :------- | :---------------------------------------------------------------------------------------------------------------------------------------- |
| self              | \_LinksSelf34             | ✅       | This grid. **Resource**: Grid                                                                                                             |
| scope             | \_LinksScope1             | ✅       | The location where this grid is used, usually represented as a relative URL.                                                              |
| attachments       | \_LinksAttachments5       | ❌       | The attachment collection of this grid. **Resource**: AttachmentCollection                                                                |
| addAttachment     | \_LinksAddAttachment4     | ❌       | Link for adding an attachment to this grid.                                                                                               |
| updateImmediately | \_LinksUpdateImmediately3 | ❌       | Directly perform edits on this grid. # Conditions **Permission**: depends on the page the grid is defined for                             |
| update            | \_LinksUpdate4            | ❌       | Validate edits on the grid via a form resource before committing # Conditions **Permission**: depends on the page the grid is defined for |
| delete            | \_LinksDelete7            | ❌       | Deletes this grid resource.                                                                                                               |

# \_LinksSelf34

This grid. **Resource**: Grid

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

# \_LinksScope1

The location where this grid is used, usually represented as a relative URL.

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

# \_LinksAttachments5

The attachment collection of this grid. **Resource**: AttachmentCollection

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

# \_LinksAddAttachment4

Link for adding an attachment to this grid.

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

# \_LinksUpdateImmediately3

Directly perform edits on this grid. # Conditions **Permission**: depends on the page the grid is defined for

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

# \_LinksUpdate4

Validate edits on the grid via a form resource before committing # Conditions **Permission**: depends on the page the grid is defined for

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

# \_LinksDelete7

Deletes this grid resource.

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
