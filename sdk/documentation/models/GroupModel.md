# GroupModel

**Properties**

| Name       | Type               | Required | Description                                                        |
| :--------- | :----------------- | :------- | :----------------------------------------------------------------- |
| \_type     | GroupModelType     | ✅       |                                                                    |
| id         | number             | ✅       | The principal's unique identifier.                                 |
| name       | string             | ✅       | The principal's display name, layout depends on instance settings. |
| \_links    | GroupModelLinks    | ✅       |                                                                    |
| \_embedded | GroupModelEmbedded | ✅       |                                                                    |
| createdAt  | string             | ❌       | Time of creation                                                   |
| updatedAt  | string             | ❌       | Time of the most recent change to the principal                    |

# GroupModelType

**Properties**

| Name  | Type   | Required | Description |
| :---- | :----- | :------- | :---------- |
| GROUP | string | ✅       | "Group"     |

# GroupModelLinks

**Properties**

| Name              | Type                      | Required | Description                                                              |
| :---------------- | :------------------------ | :------- | :----------------------------------------------------------------------- |
| members           | \_LinksMembers1[]         | ❌       |                                                                          |
| delete            | \_LinksDelete8            | ❌       | An href to delete the group. # Conditions: - `admin`                     |
| updateImmediately | \_LinksUpdateImmediately4 | ❌       | An href to update the group. # Conditions: - `admin` **Resource**: Group |

# \_LinksMembers1

A member of the group # Conditions: - user has permission `manage_members` in any project **Resource**: User

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

# \_LinksDelete8

An href to delete the group. # Conditions: - `admin`

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

# \_LinksUpdateImmediately4

An href to update the group. # Conditions: - `admin` **Resource**: Group

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

# GroupModelEmbedded

**Properties**

| Name    | Type  | Required | Description               |
| :------ | :---- | :------- | :------------------------ |
| members | any[] | ❌       | Embedded list of members. |

<!-- This file was generated by liblab | https://liblab.com/ -->
