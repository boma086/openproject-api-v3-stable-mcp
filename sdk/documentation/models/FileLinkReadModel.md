# FileLinkReadModel

**Properties**

| Name       | Type                      | Required | Description                                     |
| :--------- | :------------------------ | :------- | :---------------------------------------------- |
| id         | number                    | ❌       | File link id                                    |
| \_type     | FileLinkReadModelType     | ❌       |                                                 |
| createdAt  | string                    | ❌       | Time of creation                                |
| updatedAt  | string                    | ❌       | Time of the most recent change to the file link |
| originData | FileLinkOriginDataModel   | ❌       |                                                 |
| \_embedded | FileLinkReadModelEmbedded | ❌       |                                                 |
| \_links    | FileLinkReadModelLinks    | ❌       |                                                 |

# FileLinkReadModelType

**Properties**

| Name      | Type   | Required | Description |
| :-------- | :----- | :------- | :---------- |
| FILE_LINK | string | ✅       | "FileLink"  |

# FileLinkReadModelEmbedded

**Properties**

| Name      | Type             | Required | Description |
| :-------- | :--------------- | :------- | :---------- |
| storage   | StorageReadModel | ✅       |             |
| container | WorkPackageModel | ✅       |             |

# FileLinkReadModelLinks

**Properties**

| Name                     | Type                     | Required | Description                                                                                                                                                                                                                                                                                                                    |
| :----------------------- | :----------------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| self                     | \_LinksSelf26            | ❌       | This file link. **Resource**: FileLink                                                                                                                                                                                                                                                                                         |
| storage                  | \_LinksStorage1          | ❌       | The storage resource of the linked file. **Resource**: Storage                                                                                                                                                                                                                                                                 |
| container                | \_LinksContainer4        | ❌       | The container the origin file is linked to. Can be one of the following **Resources**: - WorkPackage                                                                                                                                                                                                                           |
| creator                  | \_LinksCreator1          | ❌       | The creator of the file link. **Resource**: User                                                                                                                                                                                                                                                                               |
| delete                   | \_LinksDelete6           | ❌       | The uri to delete the file link. **Resource**: N/A                                                                                                                                                                                                                                                                             |
| status                   | \_LinksStatus3           | ❌       | The urn of the user specific file link status on its storage. Can be one of: - urn:openproject-org:api:v3:file-links:permission:ViewAllowed - urn:openproject-org:api:v3:file-links:permission:ViewNotAllowed - urn:openproject-org:api:v3:file-links:NotFound - urn:openproject-org:api:v3:file-links:Error **Resource**: N/A |
| originOpen               | OriginOpen               | ❌       | The uri to open the origin file on the origin itself. **Resource**: N/A                                                                                                                                                                                                                                                        |
| staticOriginOpen         | StaticOriginOpen         | ❌       | A static uri to open the origin file on the storage. Responds with a redirect. **Resource**: N/A                                                                                                                                                                                                                               |
| originOpenLocation       | OriginOpenLocation       | ❌       | The uri to open the location of origin file on the origin itself. **Resource**: N/A                                                                                                                                                                                                                                            |
| staticOriginOpenLocation | StaticOriginOpenLocation | ❌       | A static uri to open the location of the origin file on the storage. Responds with a redirect. **Resource**: N/A                                                                                                                                                                                                               |
| staticOriginDownload     | StaticOriginDownload     | ❌       | A static uri to generate a new download URL from the storage. Responds with a redirect. **Resource**: N/A                                                                                                                                                                                                                      |

# \_LinksSelf26

This file link. **Resource**: FileLink

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

# \_LinksStorage1

The storage resource of the linked file. **Resource**: Storage

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

# \_LinksContainer4

The container the origin file is linked to. Can be one of the following **Resources**: - WorkPackage

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

# \_LinksCreator1

The creator of the file link. **Resource**: User

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

# \_LinksDelete6

The uri to delete the file link. **Resource**: N/A

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

# \_LinksStatus3

The urn of the user specific file link status on its storage. Can be one of: - urn:openproject-org:api:v3:file-links:permission:ViewAllowed - urn:openproject-org:api:v3:file-links:permission:ViewNotAllowed - urn:openproject-org:api:v3:file-links:NotFound - urn:openproject-org:api:v3:file-links:Error **Resource**: N/A

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

# OriginOpen

The uri to open the origin file on the origin itself. **Resource**: N/A

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

# StaticOriginOpen

A static uri to open the origin file on the storage. Responds with a redirect. **Resource**: N/A

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

# OriginOpenLocation

The uri to open the location of origin file on the origin itself. **Resource**: N/A

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

# StaticOriginOpenLocation

A static uri to open the location of the origin file on the storage. Responds with a redirect. **Resource**: N/A

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

# StaticOriginDownload

A static uri to generate a new download URL from the storage. Responds with a redirect. **Resource**: N/A

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
