# UserModel

**Properties**

| Name        | Type           | Required | Description                                                                                                                                                        |
| :---------- | :------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_type      | UserModelType  | ✅       |                                                                                                                                                                    |
| id          | number         | ✅       | The principal's unique identifier.                                                                                                                                 |
| name        | string         | ✅       | The principal's display name, layout depends on instance settings.                                                                                                 |
| \_links     | UserModelLinks | ✅       |                                                                                                                                                                    |
| avatar      | string         | ✅       | URL to user's avatar                                                                                                                                               |
| createdAt   | string         | ❌       | Time of creation                                                                                                                                                   |
| updatedAt   | string         | ❌       | Time of the most recent change to the user                                                                                                                         |
| login       | string         | ❌       | The user's login name # Conditions - User is self, or `create_user` or `manage_user` permission globally                                                           |
| firstName   | string         | ❌       | The user's first name # Conditions - User is self, or `create_user` or `manage_user` permission globally                                                           |
| lastName    | string         | ❌       | The user's last name # Conditions - User is self, or `create_user` or `manage_user` permission globally                                                            |
| email       | string         | ❌       | The user's email address # Conditions - E-Mail address not hidden - User is not a new record - User is self, or `create_user` or `manage_user` permission globally |
| admin       | boolean        | ❌       | Flag indicating whether or not the user is an admin # Conditions - `admin`                                                                                         |
| status      | string         | ❌       | The current activation status of the user. # Conditions - User is self, or `create_user` or `manage_user` permission globally                                      |
| language    | string         | ❌       | User's language \| ISO 639-1 format # Conditions - User is self, or `create_user` or `manage_user` permission globally                                             |
| identityUrl | string         | ❌       | User's identity_url for OmniAuth authentication. # Conditions - User is self, or `create_user` or `manage_user` permission globally                                |

# UserModelType

**Properties**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| USER | string | ✅       | "User"      |

# UserModelLinks

**Properties**

| Name              | Type                      | Required | Description                                                                                                                                                                          |
| :---------------- | :------------------------ | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| showUser          | \_LinksShowUser1          | ❌       | A relative path to show the user in the web application. # Condition - User is not a new record - User is not `locked`                                                               |
| updateImmediately | \_LinksUpdateImmediately6 | ❌       | A link to update the user resource. # Conditions - `admin`                                                                                                                           |
| lock              | \_LinksLock1              | ❌       | Restrict the user from logging in and performing any actions. # Conditions - User is not locked - `admin`                                                                            |
| unlock            | \_LinksUnlock1            | ❌       | Allow a locked user to login and act again. # Conditions - User is not locked - `admin`                                                                                              |
| delete            | \_LinksDelete10           | ❌       | Permanently remove a user from the instance # Conditions either: - `admin` - Setting `users_deletable_by_admin` is set or: - User is self - Setting `users_deletable_by_self` is set |
| authSource        | \_LinksAuthSource1        | ❌       | Permanently remove a user from the instance # Conditions - LDAP authentication configured - `admin`                                                                                  |

# \_LinksShowUser1

A relative path to show the user in the web application. # Condition - User is not a new record - User is not `locked`

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

# \_LinksUpdateImmediately6

A link to update the user resource. # Conditions - `admin`

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

# \_LinksLock1

Restrict the user from logging in and performing any actions. # Conditions - User is not locked - `admin`

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

# \_LinksUnlock1

Allow a locked user to login and act again. # Conditions - User is not locked - `admin`

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

# \_LinksDelete10

Permanently remove a user from the instance # Conditions either: - `admin` - Setting `users_deletable_by_admin` is set or: - User is self - Setting `users_deletable_by_self` is set

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

# \_LinksAuthSource1

Permanently remove a user from the instance # Conditions - LDAP authentication configured - `admin`

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
