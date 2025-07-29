# AttachmentModel

**Properties**

| Name        | Type                       | Required | Description                                     |
| :---------- | :------------------------- | :------- | :---------------------------------------------- |
| title       | string                     | ✅       | The name of the file                            |
| fileName    | string                     | ✅       | The name of the uploaded file                   |
| description | AttachmentModelDescription | ✅       | A user provided description of the file         |
| contentType | string                     | ✅       | The files MIME-Type as determined by the server |
| digest      | string                     | ✅       | A checksum for the files content                |
| createdAt   | string                     | ✅       | Time of creation                                |
| id          | number                     | ❌       | Attachment's id                                 |
| fileSize    | number                     | ❌       | The size of the uploaded file in Bytes          |
| \_links     | AttachmentModelLinks       | ❌       |                                                 |

# AttachmentModelDescription

A user provided description of the file

**Properties**

| Name   | Type               | Required | Description                                        |
| :----- | :----------------- | :------- | :------------------------------------------------- |
| format | DescriptionFormat4 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string             | ❌       | The raw text, as entered by the user               |
| html   | string             | ❌       | The text converted to HTML according to the format |

# DescriptionFormat4

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# AttachmentModelLinks

**Properties**

| Name             | Type                     | Required | Description                                                                                                                             |
| :--------------- | :----------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| self             | \_LinksSelf8             | ✅       | This attachment **Resource**: Attachment                                                                                                |
| container        | \_LinksContainer3        | ✅       | The object (e.g. WorkPackage) housing the attachment **Resource**: Anything                                                             |
| author           | \_LinksAuthor4           | ✅       | The user who uploaded the attachment **Resource**: User                                                                                 |
| downloadLocation | \_LinksDownloadLocation3 | ✅       | Direct download link to the attachment **Resource**: -                                                                                  |
| delete           | \_LinksDelete4           | ❌       | Deletes this attachment # Conditions **Permission**: edit on attachment container or being the author for attachments without container |

# \_LinksSelf8

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

# \_LinksContainer3

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

# \_LinksAuthor4

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

# \_LinksDownloadLocation3

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

# \_LinksDelete4

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
