# StorageWriteModel

**Properties**

| Name                | Type                   | Required | Description                                                                                                                                                                                                                                                                                                  |
| :------------------ | :--------------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string                 | ❌       | Storage name, if not provided, falls back to a default.                                                                                                                                                                                                                                                      |
| storageAudience     | string                 | ❌       | The audience that the storage expects in tokens for requests to it, usually the storage's client ID at the identity provider. This is only required for authentication through single-sign-on and so far only supported for provider type Nextcloud.                                                         |
| applicationPassword | string                 | ❌       | The application password to use for the Nextcloud storage. Ignored if the provider type is not Nextcloud. If a string is provided, the password is set and automatic management is enabled for the storage. If null is provided, the password is unset and automatic management is disabled for the storage. |
| \_links             | StorageWriteModelLinks | ❌       |                                                                                                                                                                                                                                                                                                              |

# StorageWriteModelLinks

**Properties**

| Name                 | Type                         | Required | Description                                                                                                                                                                                                                                                            |
| :------------------- | :--------------------------- | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| origin               | \_LinksOrigin2               | ✅       | The storage's host URL. **Resource**: N/A                                                                                                                                                                                                                              |
| type                 | \_LinksType4                 | ✅       | The urn of the storage type. Currently Nextcloud and OneDrive storages are supported. - urn:openproject-org:api:v3:storages:Nextcloud - urn:openproject-org:api:v3:storages:OneDrive **Resource**: N/A                                                                 |
| authenticationMethod | \_LinksAuthenticationMethod2 | ❌       | The urn of the authentication method. Currently only Nextcloud storages support this setting. - urn:openproject-org:api:v3:storages:authenticationMethod:TwoWayOAuth2 (default) - urn:openproject-org:api:v3:storages:authenticationMethod:OAuth2SSO **Resource**: N/A |

# \_LinksOrigin2

The storage's host URL. **Resource**: N/A

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

# \_LinksType4

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

# \_LinksAuthenticationMethod2

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

<!-- This file was generated by liblab | https://liblab.com/ -->
