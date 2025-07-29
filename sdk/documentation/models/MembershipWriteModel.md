# MembershipWriteModel

**Properties**

| Name    | Type                      | Required | Description |
| :------ | :------------------------ | :------- | :---------- |
| \_links | MembershipWriteModelLinks | ✅       |             |
| \_meta  | \_Meta                    | ❌       |             |

# MembershipWriteModelLinks

**Properties**

| Name      | Type              | Required | Description                                                                                                                                 |
| :-------- | :---------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| principal | \_LinksPrincipal2 | ❌       | The principal that is to get a membership. **Resource**: Principal                                                                          |
| roles     | \_LinksRoles2[]   | ❌       |                                                                                                                                             |
| project   | \_LinksProject9   | ❌       | The project that is to get a membership. If no project is given, the principal's membership is supposed to be global. **Resource**: Project |

# \_LinksPrincipal2

The principal that is to get a membership. **Resource**: Principal

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

# \_LinksRoles2

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

# \_LinksProject9

The project that is to get a membership. If no project is given, the principal's membership is supposed to be global. **Resource**: Project

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

# \_Meta

**Properties**

| Name                | Type                | Required | Description                                                                        |
| :------------------ | :------------------ | :------- | :--------------------------------------------------------------------------------- |
| notificationMessage | NotificationMessage | ❌       | A customised notification message, which will overwrite the standard notification. |
| sendNotification    | boolean             | ❌       | Set to false, if no notification should get sent.                                  |

# NotificationMessage

A customised notification message, which will overwrite the standard notification.

**Properties**

| Name   | Type                      | Required | Description                                        |
| :----- | :------------------------ | :------- | :------------------------------------------------- |
| format | NotificationMessageFormat | ✅       | Indicates the formatting language of the raw text  |
| raw    | string                    | ❌       | The raw text, as entered by the user               |
| html   | string                    | ❌       | The text converted to HTML according to the format |

# NotificationMessageFormat

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

<!-- This file was generated by liblab | https://liblab.com/ -->
