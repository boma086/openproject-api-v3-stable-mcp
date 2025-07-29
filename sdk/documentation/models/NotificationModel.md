# NotificationModel

**Properties**

| Name       | Type                      | Required | Description                                                              |
| :--------- | :------------------------ | :------- | :----------------------------------------------------------------------- |
| \_type     | NotificationModelType     | ❌       |                                                                          |
| id         | number                    | ❌       | Notification id                                                          |
| reason     | Reason                    | ❌       | The reason for the notification                                          |
| readIan    | boolean                   | ❌       | Whether the notification is marked as read                               |
| details    | ValuesPropertyModel[]     | ❌       | A list of objects including detailed information about the notification. |
| createdAt  | string                    | ❌       | The time the notification was created at                                 |
| updatedAt  | string                    | ❌       | The time the notification was last updated                               |
| \_embedded | NotificationModelEmbedded | ❌       |                                                                          |
| \_links    | NotificationModelLinks    | ❌       |                                                                          |

# NotificationModelType

**Properties**

| Name         | Type   | Required | Description    |
| :----------- | :----- | :------- | :------------- |
| NOTIFICATION | string | ✅       | "Notification" |

# Reason

The reason for the notification

**Properties**

| Name        | Type   | Required | Description   |
| :---------- | :----- | :------- | :------------ |
| ASSIGNED    | string | ✅       | "assigned"    |
| COMMENTED   | string | ✅       | "commented"   |
| CREATED     | string | ✅       | "created"     |
| DATE_ALERT  | string | ✅       | "dateAlert"   |
| MENTIONED   | string | ✅       | "mentioned"   |
| PRIORITIZED | string | ✅       | "prioritized" |
| PROCESSED   | string | ✅       | "processed"   |
| RESPONSIBLE | string | ✅       | "responsible" |
| SUBSCRIBED  | string | ✅       | "subscribed"  |
| SCHEDULED   | string | ✅       | "scheduled"   |
| WATCHED     | string | ✅       | "watched"     |

# NotificationModelEmbedded

**Properties**

| Name     | Type             | Required | Description |
| :------- | :--------------- | :------- | :---------- |
| project  | ProjectModel     | ✅       |             |
| resource | WorkPackageModel | ✅       |             |
| actor    | UserModel        | ❌       |             |
| activity | ActivityModel    | ❌       |             |

# NotificationModelLinks

**Properties**

| Name      | Type             | Required | Description                                                                                                                                                          |
| :-------- | :--------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| self      | \_LinksSelf48    | ✅       | This notification **Resource**: Notification                                                                                                                         |
| project   | \_LinksProject12 | ✅       | The project the notification originated in **Resource**: Project                                                                                                     |
| actor     | Actor            | ✅       | The user that caused the notification. This might be null in case no user triggered the notification. **Resource**: User                                             |
| resource  | Resource         | ✅       | The linked resource of the notification, if any. **Resource**: Polymorphic                                                                                           |
| activity  | \_LinksActivity1 | ✅       | The journal activity, if the notification originated from a journal entry. This might be null in case no activity triggered the notification. **Resource**: Activity |
| details   | \_LinksDetails[] | ✅       |                                                                                                                                                                      |
| readIan   | ReadIan          | ❌       | Request to mark the notification as read. Only available if the notification is currently unread.                                                                    |
| unreadIan | UnreadIan        | ❌       | Request to mark the notification as unread. Only available if the notification is currently read.                                                                    |

# \_LinksSelf48

This notification **Resource**: Notification

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

# \_LinksProject12

The project the notification originated in **Resource**: Project

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

# Actor

The user that caused the notification. This might be null in case no user triggered the notification. **Resource**: User

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

# Resource

The linked resource of the notification, if any. **Resource**: Polymorphic

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

# \_LinksActivity1

The journal activity, if the notification originated from a journal entry. This might be null in case no activity triggered the notification. **Resource**: Activity

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

# \_LinksDetails

A list of objects including detailed information about the notification. The contents of and type of this can vary widely between different notification reasons. **Resource**: Polymorphic (e.g. Values::Property)

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

# ReadIan

Request to mark the notification as read. Only available if the notification is currently unread.

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

# UnreadIan

Request to mark the notification as unread. Only available if the notification is currently read.

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
