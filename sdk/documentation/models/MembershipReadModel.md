# MembershipReadModel

**Properties**

| Name       | Type                        | Required | Description                               |
| :--------- | :-------------------------- | :------- | :---------------------------------------- |
| \_type     | MembershipReadModelType     | ✅       |                                           |
| id         | number                      | ✅       | The membership's id                       |
| createdAt  | string                      | ✅       | The time the membership was created.      |
| updatedAt  | string                      | ✅       | The time the membership was last updated. |
| \_links    | MembershipReadModelLinks    | ✅       |                                           |
| \_embedded | MembershipReadModelEmbedded | ❌       |                                           |

# MembershipReadModelType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| MEMBERSHIP | string | ✅       | "Membership" |

# MembershipReadModelLinks

**Properties**

| Name              | Type                      | Required | Description                                                                                                   |
| :---------------- | :------------------------ | :------- | :------------------------------------------------------------------------------------------------------------ |
| self              | \_LinksSelf41             | ✅       | This membership. **Resource**: Membership                                                                     |
| schema            | \_LinksSchema3            | ✅       | This membership schema. **Resource**: Schema                                                                  |
| project           | \_LinksProject8           | ✅       | The project the membership is related to. **Resource**: Project                                               |
| principal         | \_LinksPrincipal1         | ✅       | The principal the membership is related to. **Resource**: Principal                                           |
| roles             | \_LinksRoles1[]           | ✅       |                                                                                                               |
| update            | \_LinksUpdate6            | ❌       | The endpoint for updating the membership. # Conditions **Permission**: manage_members                         |
| updateImmediately | \_LinksUpdateImmediately7 | ❌       | The endpoint for updating the membership without form validation. # Conditions **Permission**: manage_members |

# \_LinksSelf41

This membership. **Resource**: Membership

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

# \_LinksSchema3

This membership schema. **Resource**: Schema

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

# \_LinksProject8

The project the membership is related to. **Resource**: Project

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

# \_LinksPrincipal1

The principal the membership is related to. **Resource**: Principal

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

# \_LinksRoles1

A role the principal has. **Resource**: Role

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

# \_LinksUpdate6

The endpoint for updating the membership. # Conditions **Permission**: manage_members

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

# \_LinksUpdateImmediately7

The endpoint for updating the membership without form validation. # Conditions **Permission**: manage_members

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

# MembershipReadModelEmbedded

**Properties**

| Name      | Type                | Required | Description |
| :-------- | :------------------ | :------- | :---------- |
| project   | ProjectModel        | ❌       |             |
| principal | \_EmbeddedPrincipal | ❌       |             |
| roles     | RoleModel[]         | ❌       |             |

# \_EmbeddedPrincipal

<!-- This file was generated by liblab | https://liblab.com/ -->
