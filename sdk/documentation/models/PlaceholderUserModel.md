# PlaceholderUserModel

**Properties**

| Name      | Type                      | Required | Description                                                                                                                  |
| :-------- | :------------------------ | :------- | :--------------------------------------------------------------------------------------------------------------------------- |
| \_type    | PlaceholderUserModelType  | ✅       |                                                                                                                              |
| id        | number                    | ✅       | The principal's unique identifier.                                                                                           |
| name      | string                    | ✅       | The principal's display name, layout depends on instance settings.                                                           |
| \_links   | PlaceholderUserModelLinks | ✅       |                                                                                                                              |
| createdAt | string                    | ❌       | Time of creation                                                                                                             |
| updatedAt | string                    | ❌       | Time of the most recent change to the principal                                                                              |
| status    | string                    | ❌       | The current activation status of the placeholder user. # Conditions - User has `manage_placeholder_user` permission globally |

# PlaceholderUserModelType

**Properties**

| Name             | Type   | Required | Description       |
| :--------------- | :----- | :------- | :---------------- |
| PLACEHOLDER_USER | string | ✅       | "PlaceholderUser" |

# PlaceholderUserModelLinks

**Properties**

| Name              | Type                      | Required | Description                                                                                                     |
| :---------------- | :------------------------ | :------- | :-------------------------------------------------------------------------------------------------------------- |
| showUser          | \_LinksShowUser2          | ✅       | A relative path to show the placeholder user in the web application.                                            |
| delete            | \_LinksDelete12           | ❌       | An href to delete the placeholder user. # Conditions: - `manage_placeholder_user`                               |
| updateImmediately | \_LinksUpdateImmediately9 | ❌       | An href to update the placeholder user. # Conditions: - `manage_placeholder_user` **Resource**: PlaceholderUser |

# \_LinksShowUser2

A relative path to show the placeholder user in the web application.

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

# \_LinksDelete12

An href to delete the placeholder user. # Conditions: - `manage_placeholder_user`

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

# \_LinksUpdateImmediately9

An href to update the placeholder user. # Conditions: - `manage_placeholder_user` **Resource**: PlaceholderUser

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
