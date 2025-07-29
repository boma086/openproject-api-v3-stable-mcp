# AttachmentsService

A list of all methods in the `AttachmentsService` service. Click on the method name to view detailed information about that method.

| Methods                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| :---------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [createAttachment](#createattachment)                       | Clients can create attachments without a container first and attach them later on. This is useful if the container does not exist at the time the attachment is uploaded. After the upload, the client can then claim such containerless attachments for any resource eligible (e.g. WorkPackage) on subsequent requests. The upload and the claiming _must_ be done for the same user account. Attachments uploaded by another user cannot be claimed and once claimed for a resource, they cannot be claimed by another. The upload request must be of type `multipart/form-data` with exactly two parts. The first part _must_ be called `metadata`. Its content type is expected to be `application/json`, the body _must_ be a single JSON object, containing at least the `fileName` and optionally the attachments `description`. The second part _must_ be called `file`, its content type _should_ match the mime type of the file. The body _must_ be the raw content of the file. Note that a `filename` _must_ be indicated in the `Content-Disposition` of this part, although it will be ignored. Instead the `fileName` inside the JSON of the metadata part will be used. |
| [viewAttachment](#viewattachment)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [deleteAttachment](#deleteattachment)                       | Permanently deletes the specified attachment.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [listAttachmentsByMeeting](#listattachmentsbymeeting)       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [addAttachmentToMeeting](#addattachmenttomeeting)           | Adds an attachment with the meeting as its container.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [listAttachmentsByPost](#listattachmentsbypost)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [addAttachmentToPost](#addattachmenttopost)                 | Adds an attachment with the post as its container.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [listAttachmentsByWikiPage](#listattachmentsbywikipage)     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [addAttachmentToWikiPage](#addattachmenttowikipage)         | Adds an attachment with the wiki page as its container.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [listWorkPackageAttachments](#listworkpackageattachments)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [createWorkPackageAttachment](#createworkpackageattachment) | To add an attachment to a work package, a client needs to issue a request of type `multipart/form-data` with exactly two parts. The first part _must_ be called `metadata`. Its content type is expected to be `application/json`, the body _must_ be a single JSON object, containing at least the `fileName` and optionally the attachments `description`. The second part _must_ be called `file`, its content type _should_ match the mime type of the file. The body _must_ be the raw content of the file. Note that a `filename` must be indicated in the `Content-Disposition` of this part, however it will be ignored. Instead the `fileName` inside the JSON of the metadata part will be used.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

## createAttachment

Clients can create attachments without a container first and attach them later on. This is useful if the container does not exist at the time the attachment is uploaded. After the upload, the client can then claim such containerless attachments for any resource eligible (e.g. WorkPackage) on subsequent requests. The upload and the claiming _must_ be done for the same user account. Attachments uploaded by another user cannot be claimed and once claimed for a resource, they cannot be claimed by another. The upload request must be of type `multipart/form-data` with exactly two parts. The first part _must_ be called `metadata`. Its content type is expected to be `application/json`, the body _must_ be a single JSON object, containing at least the `fileName` and optionally the attachments `description`. The second part _must_ be called `file`, its content type _should_ match the mime type of the file. The body _must_ be the raw content of the file. Note that a `filename` _must_ be indicated in the `Content-Disposition` of this part, although it will be ignored. Instead the `fileName` inside the JSON of the metadata part will be used.

- HTTP Method: `POST`
- Endpoint: `/api/v3/attachments`

**Return Type**

`AttachmentModel`

**Example Usage Code Snippet**

```mcp

```

## viewAttachment

- HTTP Method: `GET`
- Endpoint: `/api/v3/attachments/{id}`

**Parameters**

| Name | Type   | Required | Description   |
| :--- | :----- | :------- | :------------ |
| id   | number | ✅       | Attachment id |

**Return Type**

`AttachmentModel`

**Example Usage Code Snippet**

```mcp

```

## deleteAttachment

Permanently deletes the specified attachment.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/attachments/{id}`

**Parameters**

| Name | Type   | Required | Description   |
| :--- | :----- | :------- | :------------ |
| id   | number | ✅       | Attachment id |

**Example Usage Code Snippet**

```mcp

```

## listAttachmentsByMeeting

- HTTP Method: `GET`
- Endpoint: `/api/v3/meetings/{id}/attachments`

**Parameters**

| Name | Type   | Required | Description                                        |
| :--- | :----- | :------- | :------------------------------------------------- |
| id   | number | ✅       | ID of the meeting whose attachments will be listed |

**Return Type**

`AttachmentsModel`

**Example Usage Code Snippet**

```mcp

```

## addAttachmentToMeeting

Adds an attachment with the meeting as its container.

- HTTP Method: `POST`
- Endpoint: `/api/v3/meetings/{id}/attachments`

**Parameters**

| Name | Type   | Required | Description                                 |
| :--- | :----- | :------- | :------------------------------------------ |
| id   | number | ✅       | ID of the meeting to receive the attachment |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## listAttachmentsByPost

- HTTP Method: `GET`
- Endpoint: `/api/v3/posts/{id}/attachments`

**Parameters**

| Name | Type   | Required | Description                                     |
| :--- | :----- | :------- | :---------------------------------------------- |
| id   | number | ✅       | ID of the post whose attachments will be listed |

**Return Type**

`AttachmentsModel`

**Example Usage Code Snippet**

```mcp

```

## addAttachmentToPost

Adds an attachment with the post as its container.

- HTTP Method: `POST`
- Endpoint: `/api/v3/posts/{id}/attachments`

**Parameters**

| Name | Type   | Required | Description                              |
| :--- | :----- | :------- | :--------------------------------------- |
| id   | number | ✅       | ID of the post to receive the attachment |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## listAttachmentsByWikiPage

- HTTP Method: `GET`
- Endpoint: `/api/v3/wiki_pages/{id}/attachments`

**Parameters**

| Name | Type   | Required | Description                                          |
| :--- | :----- | :------- | :--------------------------------------------------- |
| id   | number | ✅       | ID of the wiki page whose attachments will be listed |

**Return Type**

`AttachmentsModel`

**Example Usage Code Snippet**

```mcp

```

## addAttachmentToWikiPage

Adds an attachment with the wiki page as its container.

- HTTP Method: `POST`
- Endpoint: `/api/v3/wiki_pages/{id}/attachments`

**Parameters**

| Name | Type   | Required | Description                                   |
| :--- | :----- | :------- | :-------------------------------------------- |
| id   | number | ✅       | ID of the wiki page to receive the attachment |

**Return Type**

`any`

**Example Usage Code Snippet**

```mcp

```

## listWorkPackageAttachments

- HTTP Method: `GET`
- Endpoint: `/api/v3/work_packages/{id}/attachments`

**Parameters**

| Name | Type   | Required | Description                                             |
| :--- | :----- | :------- | :------------------------------------------------------ |
| id   | number | ✅       | ID of the work package whose attachments will be listed |

**Return Type**

`AttachmentsModel`

**Example Usage Code Snippet**

```mcp

```

## createWorkPackageAttachment

To add an attachment to a work package, a client needs to issue a request of type `multipart/form-data` with exactly two parts. The first part _must_ be called `metadata`. Its content type is expected to be `application/json`, the body _must_ be a single JSON object, containing at least the `fileName` and optionally the attachments `description`. The second part _must_ be called `file`, its content type _should_ match the mime type of the file. The body _must_ be the raw content of the file. Note that a `filename` must be indicated in the `Content-Disposition` of this part, however it will be ignored. Instead the `fileName` inside the JSON of the metadata part will be used.

- HTTP Method: `POST`
- Endpoint: `/api/v3/work_packages/{id}/attachments`

**Parameters**

| Name | Type   | Required | Description                                      |
| :--- | :----- | :------- | :----------------------------------------------- |
| id   | number | ✅       | ID of the work package to receive the attachment |

**Return Type**

`AttachmentModel`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
