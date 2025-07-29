# StorageReadModel

**Properties**

| Name                   | Type                     | Required | Description                                                                                                                                                                                                                                          |
| :--------------------- | :----------------------- | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id                     | number                   | ✅       | Storage id                                                                                                                                                                                                                                           |
| \_type                 | StorageReadModelType     | ✅       |                                                                                                                                                                                                                                                      |
| name                   | string                   | ✅       | Storage name                                                                                                                                                                                                                                         |
| \_links                | StorageReadModelLinks    | ✅       |                                                                                                                                                                                                                                                      |
| storageAudience        | string                   | ❌       | The audience that the storage expects in tokens for requests to it, usually the storage's client ID at the identity provider. This is only required for authentication through single-sign-on and so far only supported for provider type Nextcloud. |
| tenantId               | string                   | ❌       | The tenant id of a file storage of type OneDrive/SharePoint. Ignored if the provider type is not OneDrive/SharePoint.                                                                                                                                |
| driveId                | string                   | ❌       | The drive id of a file storage of type OneDrive/SharePoint. Ignored if the provider type is not OneDrive/SharePoint.                                                                                                                                 |
| hasApplicationPassword | boolean                  | ❌       | Whether the storage has the application password to use for the Nextcloud storage. Ignored if the provider type is not Nextcloud.                                                                                                                    |
| createdAt              | string                   | ❌       | Time of creation                                                                                                                                                                                                                                     |
| updatedAt              | string                   | ❌       | Time of the most recent change to the storage                                                                                                                                                                                                        |
| configured             | boolean                  | ❌       | Indication, if the storage is fully configured                                                                                                                                                                                                       |
| \_embedded             | StorageReadModelEmbedded | ❌       |                                                                                                                                                                                                                                                      |

# StorageReadModelType

**Properties**

| Name    | Type   | Required | Description |
| :------ | :----- | :------- | :---------- |
| STORAGE | string | ✅       | "Storage"   |

# StorageReadModelLinks

**Properties**

| Name                   | Type                         | Required | Description                                                                                                                                                                                                                                                               |
| :--------------------- | :--------------------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| self                   | \_LinksSelf24                | ✅       | This storage resource. Contains the user defined storage name as title. **Resource**: Storage                                                                                                                                                                             |
| type                   | \_LinksType2                 | ✅       | The urn of the storage type. Currently Nextcloud and OneDrive storages are supported. - urn:openproject-org:api:v3:storages:Nextcloud - urn:openproject-org:api:v3:storages:OneDrive **Resource**: N/A                                                                    |
| open                   | \_LinksOpen1                 | ✅       | URI of the file storage location, from where the user usually starts browsing files. **Resource**: N/A                                                                                                                                                                    |
| authorizationState     | AuthorizationState           | ✅       | The urn of the storage connection state. Can be one of: - urn:openproject-org:api:v3:storages:authorization:Connected - urn:openproject-org:api:v3:storages:authorization:FailedAuthorization - urn:openproject-org:api:v3:storages:authorization:Error **Resource**: N/A |
| authenticationMethod   | \_LinksAuthenticationMethod1 | ❌       | The urn of the authentication method. Currently only Nextcloud storages support this setting. - urn:openproject-org:api:v3:storages:authenticationMethod:TwoWayOAuth2 (default) - urn:openproject-org:api:v3:storages:authenticationMethod:OAuth2SSO **Resource**: N/A    |
| origin                 | \_LinksOrigin1               | ❌       | Web URI of the storage instance. This link is ignored, if the storage is hosted in a cloud and has no own URL, like file storages of type OneDrive/SharePoint. **Resource**: N/A                                                                                          |
| authorize              | Authorize                    | ❌       | The link to the starting point of the authorization cycle for a configured storage provider. # Conditions `authorizationState` is: - urn:openproject-org:api:v3:storages:authorization:FailedAuthorization **Resource**: N/A                                              |
| oauthApplication       | OauthApplication             | ❌       | The OAuth 2 provider application linked to the storage. # Conditions - User has role `admin` **Resource**: OAuthApplication                                                                                                                                               |
| oauthClientCredentials | OauthClientCredentials       | ❌       | The OAuth 2 credentials resource linked to the storage. # Conditions - User has role `admin` **Resource**: OAuthClientCredentials                                                                                                                                         |

# \_LinksSelf24

This storage resource. Contains the user defined storage name as title. **Resource**: Storage

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

# \_LinksType2

The urn of the storage type. Currently Nextcloud and OneDrive storages are supported. - urn:openproject-org:api:v3:storages:Nextcloud - urn:openproject-org:api:v3:storages:OneDrive **Resource**: N/A

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

# \_LinksOpen1

URI of the file storage location, from where the user usually starts browsing files. **Resource**: N/A

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

# AuthorizationState

The urn of the storage connection state. Can be one of: - urn:openproject-org:api:v3:storages:authorization:Connected - urn:openproject-org:api:v3:storages:authorization:FailedAuthorization - urn:openproject-org:api:v3:storages:authorization:Error **Resource**: N/A

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

# \_LinksAuthenticationMethod1

The urn of the authentication method. Currently only Nextcloud storages support this setting. - urn:openproject-org:api:v3:storages:authenticationMethod:TwoWayOAuth2 (default) - urn:openproject-org:api:v3:storages:authenticationMethod:OAuth2SSO **Resource**: N/A

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

# \_LinksOrigin1

Web URI of the storage instance. This link is ignored, if the storage is hosted in a cloud and has no own URL, like file storages of type OneDrive/SharePoint. **Resource**: N/A

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

# Authorize

The link to the starting point of the authorization cycle for a configured storage provider. # Conditions `authorizationState` is: - urn:openproject-org:api:v3:storages:authorization:FailedAuthorization **Resource**: N/A

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

# OauthApplication

The OAuth 2 provider application linked to the storage. # Conditions - User has role `admin` **Resource**: OAuthApplication

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

# OauthClientCredentials

The OAuth 2 credentials resource linked to the storage. # Conditions - User has role `admin` **Resource**: OAuthClientCredentials

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

# StorageReadModelEmbedded

**Properties**

| Name                   | Type                            | Required | Description |
| :--------------------- | :------------------------------ | :------- | :---------- |
| oauthApplication       | OAuthApplicationReadModel       | ❌       |             |
| oauthClientCredentials | OAuthClientCredentialsReadModel | ❌       |             |

<!-- This file was generated by liblab | https://liblab.com/ -->
