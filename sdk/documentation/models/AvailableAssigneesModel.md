# AvailableAssigneesModel

**Properties**

| Name       | Type                            | Required | Description                                               |
| :--------- | :------------------------------ | :------- | :-------------------------------------------------------- |
| \_type     | AvailableAssigneesModelType     | ✅       |                                                           |
| total      | number                          | ✅       | The total amount of elements available in the collection. |
| count      | number                          | ✅       | Actual amount of elements in this response.               |
| \_links    | AvailableAssigneesModelLinks    | ✅       |                                                           |
| \_embedded | AvailableAssigneesModelEmbedded | ✅       |                                                           |

# AvailableAssigneesModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# AvailableAssigneesModelLinks

**Properties**

| Name | Type          | Required | Description                                                                   |
| :--- | :------------ | :------- | :---------------------------------------------------------------------------- |
| self | \_LinksSelf58 | ✅       | The available assignees collection **Resource**: AvailableAssigneesCollection |

# \_LinksSelf58

The available assignees collection **Resource**: AvailableAssigneesCollection

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

# AvailableAssigneesModelEmbedded

**Properties**

| Name     | Type                  | Required | Description |
| :------- | :-------------------- | :------- | :---------- |
| elements | \_EmbeddedElements7[] | ❌       |             |

# \_EmbeddedElements7

Collection of Users

**Properties**

| Name        | Type           | Required | Description                                                                                                                                                        |
| :---------- | :------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_type      | ElementsType3  | ✅       |                                                                                                                                                                    |
| id          | number         | ✅       | The principal's unique identifier.                                                                                                                                 |
| name        | string         | ✅       | The principal's display name, layout depends on instance settings.                                                                                                 |
| \_links     | ElementsLinks5 | ✅       |                                                                                                                                                                    |
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

# ElementsType3

**Properties**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| USER | string | ✅       | "User"      |

# ElementsLinks5

**Properties**

| Name              | Type                       | Required | Description                                                                                                                                                                          |
| :---------------- | :------------------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| showUser          | \_LinksShowUser3           | ❌       | A relative path to show the user in the web application. # Condition - User is not a new record - User is not `locked`                                                               |
| updateImmediately | \_LinksUpdateImmediately12 | ❌       | A link to update the user resource. # Conditions - `admin`                                                                                                                           |
| lock              | \_LinksLock2               | ❌       | Restrict the user from logging in and performing any actions. # Conditions - User is not locked - `admin`                                                                            |
| unlock            | \_LinksUnlock2             | ❌       | Allow a locked user to login and act again. # Conditions - User is not locked - `admin`                                                                                              |
| delete            | \_LinksDelete14            | ❌       | Permanently remove a user from the instance # Conditions either: - `admin` - Setting `users_deletable_by_admin` is set or: - User is self - Setting `users_deletable_by_self` is set |
| authSource        | \_LinksAuthSource2         | ❌       | Permanently remove a user from the instance # Conditions - LDAP authentication configured - `admin`                                                                                  |

# \_LinksShowUser3

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

# \_LinksUpdateImmediately12

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

# \_LinksLock2

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

# \_LinksUnlock2

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

# \_LinksDelete14

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

# \_LinksAuthSource2

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
