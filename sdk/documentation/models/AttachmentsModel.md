# AttachmentsModel

**Properties**

| Name       | Type                     | Required | Description                                               |
| :--------- | :----------------------- | :------- | :-------------------------------------------------------- |
| \_type     | AttachmentsModelType     | ✅       |                                                           |
| total      | number                   | ✅       | The total amount of elements available in the collection. |
| count      | number                   | ✅       | Actual amount of elements in this response.               |
| \_links    | AttachmentsModelLinks    | ✅       |                                                           |
| \_embedded | AttachmentsModelEmbedded | ✅       |                                                           |

# AttachmentsModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# AttachmentsModelLinks

**Properties**

| Name | Type         | Required | Description                                                    |
| :--- | :----------- | :------- | :------------------------------------------------------------- |
| self | \_LinksSelf6 | ✅       | The attachments collection **Resource**: AttachmentsCollection |

# \_LinksSelf6

The attachments collection **Resource**: AttachmentsCollection

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

# AttachmentsModelEmbedded

**Properties**

| Name     | Type                  | Required | Description |
| :------- | :-------------------- | :------- | :---------- |
| elements | \_EmbeddedElements2[] | ❌       |             |

# \_EmbeddedElements2

Collection of Attachments

**Properties**

| Name        | Type                 | Required | Description                                     |
| :---------- | :------------------- | :------- | :---------------------------------------------- |
| title       | string               | ✅       | The name of the file                            |
| fileName    | string               | ✅       | The name of the uploaded file                   |
| description | ElementsDescription2 | ✅       | A user provided description of the file         |
| contentType | string               | ✅       | The files MIME-Type as determined by the server |
| digest      | string               | ✅       | A checksum for the files content                |
| createdAt   | string               | ✅       | Time of creation                                |
| id          | number               | ❌       | Attachment's id                                 |
| fileSize    | number               | ❌       | The size of the uploaded file in Bytes          |
| \_links     | ElementsLinks2       | ❌       |                                                 |

# ElementsDescription2

A user provided description of the file

**Properties**

| Name   | Type               | Required | Description                                        |
| :----- | :----------------- | :------- | :------------------------------------------------- |
| format | DescriptionFormat3 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string             | ❌       | The raw text, as entered by the user               |
| html   | string             | ❌       | The text converted to HTML according to the format |

# DescriptionFormat3

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# ElementsLinks2

**Properties**

| Name             | Type                     | Required | Description                                                                                                                             |
| :--------------- | :----------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| self             | \_LinksSelf7             | ✅       | This attachment **Resource**: Attachment                                                                                                |
| container        | \_LinksContainer2        | ✅       | The object (e.g. WorkPackage) housing the attachment **Resource**: Anything                                                             |
| author           | \_LinksAuthor3           | ✅       | The user who uploaded the attachment **Resource**: User                                                                                 |
| downloadLocation | \_LinksDownloadLocation2 | ✅       | Direct download link to the attachment **Resource**: -                                                                                  |
| delete           | \_LinksDelete3           | ❌       | Deletes this attachment # Conditions **Permission**: edit on attachment container or being the author for attachments without container |

# \_LinksSelf7

This attachment **Resource**: Attachment

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

# \_LinksContainer2

The object (e.g. WorkPackage) housing the attachment **Resource**: Anything

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

# \_LinksAuthor3

The user who uploaded the attachment **Resource**: User

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

# \_LinksDownloadLocation2

Direct download link to the attachment **Resource**: -

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

# \_LinksDelete3

Deletes this attachment # Conditions **Permission**: edit on attachment container or being the author for attachments without container

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
