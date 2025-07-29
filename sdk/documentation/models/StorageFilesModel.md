# StorageFilesModel

**Properties**

| Name      | Type                    | Required | Description                                                                                      |
| :-------- | :---------------------- | :------- | :----------------------------------------------------------------------------------------------- |
| \_type    | StorageFilesModelType   | ✅       |                                                                                                  |
| files     | StorageFileModel[]      | ✅       | List of files provided by the selected storage.                                                  |
| parent    | StorageFilesModelParent | ✅       | File of the currently selected parent directory.                                                 |
| ancestors | StorageFileModel[]      | ✅       | List of ancestors of the parent directory. Can be empty, if parent directory was root directory. |
| \_links   | StorageFilesModelLinks  | ✅       |                                                                                                  |

# StorageFilesModelType

**Properties**

| Name          | Type   | Required | Description    |
| :------------ | :----- | :------- | :------------- |
| STORAGE_FILES | string | ✅       | "StorageFiles" |

# StorageFilesModelParent

File of the currently selected parent directory.

**Properties**

| Name               | Type        | Required | Description                                                                                                                                                                    |
| :----------------- | :---------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id                 | string      | ✅       | Linked file's id on the origin                                                                                                                                                 |
| name               | string      | ✅       | Linked file's name on the origin                                                                                                                                               |
| \_type             | ParentType  | ✅       |                                                                                                                                                                                |
| location           | string      | ✅       | Location identification for file in storage                                                                                                                                    |
| \_links            | ParentLinks | ✅       |                                                                                                                                                                                |
| mimeType           | string      | ❌       | MIME type of the linked file. To link a folder entity, the custom MIME type `application/x-op-directory` MUST be provided. Otherwise it defaults back to an unknown MIME type. |
| size               | number      | ❌       | file size on origin in bytes                                                                                                                                                   |
| createdAt          | string      | ❌       | Timestamp of the creation datetime of the file on the origin                                                                                                                   |
| lastModifiedAt     | string      | ❌       | Timestamp of the datetime of the last modification of the file on the origin                                                                                                   |
| createdByName      | string      | ❌       | Display name of the author that created the file on the origin                                                                                                                 |
| lastModifiedByName | string      | ❌       | Display name of the author that modified the file on the origin last                                                                                                           |

# ParentType

**Properties**

| Name         | Type   | Required | Description   |
| :----------- | :----- | :------- | :------------ |
| STORAGE_FILE | string | ✅       | "StorageFile" |

# ParentLinks

**Properties**

| Name | Type          | Required | Description                                                                                  |
| :--- | :------------ | :------- | :------------------------------------------------------------------------------------------- |
| self | \_LinksSelf31 | ✅       | Not provided **Resource**: urn:openproject-org:api:v3:storages:storage_file:no_link_provided |

# \_LinksSelf31

Not provided **Resource**: urn:openproject-org:api:v3:storages:storage_file:no_link_provided

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

# StorageFilesModelLinks

**Properties**

| Name | Type          | Required | Description                                                                                  |
| :--- | :------------ | :------- | :------------------------------------------------------------------------------------------- |
| self | \_LinksSelf32 | ✅       | Not provided **Resource**: urn:openproject-org:api:v3:storages:storage_file:no_link_provided |

# \_LinksSelf32

Not provided **Resource**: urn:openproject-org:api:v3:storages:storage_file:no_link_provided

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
