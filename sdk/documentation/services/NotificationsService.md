# NotificationsService

A list of all methods in the `NotificationsService` service. Click on the method name to view detailed information about that method.

| Methods                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listNotifications](#listnotifications)           | Returns the collection of available in-app notifications. The notifications returned depend on the provided parameters and also on the requesting user's permissions. Contrary to most collections, this one also links to and embeds schemas for the `details` properties of the notifications returned. This is an optimization. Clients will receive the information necessary to display the various types of details that a notification can carry. |
| [readNotifications](#readnotifications)           | Marks the whole notification collection as read. The collection contains only elements the authenticated user can see, and can be further reduced with filters.                                                                                                                                                                                                                                                                                          |
| [unreadNotifications](#unreadnotifications)       | Marks the whole notification collection as unread. The collection contains only elements the authenticated user can see, and can be further reduced with filters.                                                                                                                                                                                                                                                                                        |
| [viewNotification](#viewnotification)             | Returns the notification identified by the notification id.                                                                                                                                                                                                                                                                                                                                                                                              |
| [viewNotificationDetail](#viewnotificationdetail) | Returns an individual detail of a notification identified by the notification id and the id of the detail.                                                                                                                                                                                                                                                                                                                                               |
| [readNotification](#readnotification)             | Marks the given notification as read.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [unreadNotification](#unreadnotification)         | Marks the given notification as unread.                                                                                                                                                                                                                                                                                                                                                                                                                  |

## listNotifications

Returns the collection of available in-app notifications. The notifications returned depend on the provided parameters and also on the requesting user's permissions. Contrary to most collections, this one also links to and embeds schemas for the `details` properties of the notifications returned. This is an optimization. Clients will receive the information necessary to display the various types of details that a notification can carry.

- HTTP Method: `GET`
- Endpoint: `/api/v3/notifications`

**Parameters**

| Name     | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :------- | :----- | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| offset   | number | ❌       | Page number inside the requested collection.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| pageSize | number | ❌       | Number of elements to display per page.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| sortBy   | string | ❌       | JSON specifying sort criteria. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported sorts are: + id: Sort by primary key + reason: Sort by notification reason + readIAN: Sort by read status                                                                                                                                                                                                                                                                                                                                                                                                                             |
| groupBy  | string | ❌       | string specifying group_by criteria. + reason: Group by notification reason + project: Sort by associated project                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| filters  | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + id: Filter by primary key + project: Filter by the project the notification was created in + readIAN: Filter by read status + reason: Filter by the reason, e.g. 'mentioned' or 'assigned' the notification was created because of + resourceId: Filter by the id of the resource the notification was created for. Ideally used together with the `resourceType` filter. + resourceType: Filter by the type of the resource the notification was created for. Ideally used together with the `resourceId` filter. |

**Return Type**

`NotificationCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## readNotifications

Marks the whole notification collection as read. The collection contains only elements the authenticated user can see, and can be further reduced with filters.

- HTTP Method: `POST`
- Endpoint: `/api/v3/notifications/read_ian`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + id: Filter by primary key + project: Filter by the project the notification was created in + reason: Filter by the reason, e.g. 'mentioned' or 'assigned' the notification was created because of + resourceId: Filter by the id of the resource the notification was created for. Ideally used together with the `resourceType` filter. + resourceType: Filter by the type of the resource the notification was created for. Ideally used together with the `resourceId` filter. |

**Example Usage Code Snippet**

```mcp

```

## unreadNotifications

Marks the whole notification collection as unread. The collection contains only elements the authenticated user can see, and can be further reduced with filters.

- HTTP Method: `POST`
- Endpoint: `/api/v3/notifications/unread_ian`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + id: Filter by primary key + project: Filter by the project the notification was created in + reason: Filter by the reason, e.g. 'mentioned' or 'assigned' the notification was created because of + resourceId: Filter by the id of the resource the notification was created for. Ideally used together with the `resourceType` filter. + resourceType: Filter by the type of the resource the notification was created for. Ideally used together with the `resourceId` filter. |

**Example Usage Code Snippet**

```mcp

```

## viewNotification

Returns the notification identified by the notification id.

- HTTP Method: `GET`
- Endpoint: `/api/v3/notifications/{id}`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | notification id |

**Return Type**

`NotificationModel`

**Example Usage Code Snippet**

```mcp

```

## viewNotificationDetail

Returns an individual detail of a notification identified by the notification id and the id of the detail.

- HTTP Method: `GET`
- Endpoint: `/api/v3/notifications/{notification_id}/details/{id}`

**Parameters**

| Name           | Type   | Required | Description     |
| :------------- | :----- | :------- | :-------------- |
| notificationId | number | ✅       | notification id |
| id             | number | ✅       | detail id       |

**Return Type**

`ValuesPropertyModel`

**Example Usage Code Snippet**

```mcp

```

## readNotification

Marks the given notification as read.

- HTTP Method: `POST`
- Endpoint: `/api/v3/notifications/{id}/read_ian`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | notification id |

**Example Usage Code Snippet**

```mcp

```

## unreadNotification

Marks the given notification as unread.

- HTTP Method: `POST`
- Endpoint: `/api/v3/notifications/{id}/unread_ian`

**Parameters**

| Name | Type   | Required | Description     |
| :--- | :----- | :------- | :-------------- |
| id   | number | ✅       | notification id |

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
