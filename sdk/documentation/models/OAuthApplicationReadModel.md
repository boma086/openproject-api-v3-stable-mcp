# OAuthApplicationReadModel

**Properties**

| Name         | Type                           | Required | Description                                                                         |
| :----------- | :----------------------------- | :------- | :---------------------------------------------------------------------------------- |
| id           | number                         | ✅       |                                                                                     |
| \_type       | OAuthApplicationReadModelType  | ✅       |                                                                                     |
| name         | string                         | ✅       | The name of the OAuth 2 application                                                 |
| clientId     | string                         | ✅       | OAuth 2 client id                                                                   |
| confidential | boolean                        | ✅       | true, if OAuth 2 credentials are confidential, false, if no secret is stored        |
| clientSecret | string                         | ❌       | OAuth 2 client secret. This is only returned when creating a new OAuth application. |
| createdAt    | string                         | ❌       | The time the OAuth 2 Application was created at                                     |
| updatedAt    | string                         | ❌       | The time the OAuth 2 Application was last updated                                   |
| scopes       | string[]                       | ❌       | An array of the scopes of the OAuth 2 Application                                   |
| \_links      | OAuthApplicationReadModelLinks | ❌       |                                                                                     |

# OAuthApplicationReadModelType

**Properties**

| Name               | Type   | Required | Description        |
| :----------------- | :----- | :------- | :----------------- |
| O_AUTH_APPLICATION | string | ✅       | "OAuthApplication" |

# OAuthApplicationReadModelLinks

**Properties**

| Name        | Type                | Required | Description                                                                                                                                                                       |
| :---------- | :------------------ | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| self        | \_LinksSelf22       | ✅       | This OAuth application **Resource**: OAuthApplication                                                                                                                             |
| owner       | Owner               | ✅       | The user that created the OAuth application. **Resource**: User                                                                                                                   |
| redirectUri | RedirectUri[]       | ✅       |                                                                                                                                                                                   |
| integration | \_LinksIntegration1 | ❌       | The resource that integrates this OAuth application into itself. Currently, only `Storage` resources are able to create and maintain own OAuth application. **Resource**: Storage |

# \_LinksSelf22

This OAuth application **Resource**: OAuthApplication

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

# Owner

The user that created the OAuth application. **Resource**: User

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

# RedirectUri

A redirect URI of the OAuth application **Resource**: N/A

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

# \_LinksIntegration1

The resource that integrates this OAuth application into itself. Currently, only `Storage` resources are able to create and maintain own OAuth application. **Resource**: Storage

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
