# HelpTextModel

**Properties**

| Name      | Type               | Required | Description                                 |
| :-------- | :----------------- | :------- | :------------------------------------------ |
| \_type    | HelpTextModelType  | ✅       |                                             |
| id        | number             | ✅       |                                             |
| attribute | string             | ✅       | The attribute the help text is assigned to. |
| scope     | HelpTextModelScope | ✅       |                                             |
| helpText  | Formattable        | ✅       |                                             |
| \_links   | HelpTextModelLinks | ✅       |                                             |

# HelpTextModelType

**Properties**

| Name      | Type   | Required | Description |
| :-------- | :----- | :------- | :---------- |
| HELP_TEXT | string | ✅       | "HelpText"  |

# HelpTextModelScope

**Properties**

| Name         | Type   | Required | Description   |
| :----------- | :----- | :------- | :------------ |
| WORK_PACKAGE | string | ✅       | "WorkPackage" |
| PROJECT      | string | ✅       | "Project"     |

# HelpTextModelLinks

**Properties**

| Name          | Type                  | Required | Description                                                                     |
| :------------ | :-------------------- | :------- | :------------------------------------------------------------------------------ |
| self          | \_LinksSelf37         | ✅       | This help text resource. **Resource**: HelpText                                 |
| editText      | EditText              | ✅       | Edit the help text entry. **Resource**: text/html                               |
| attachments   | \_LinksAttachments6   | ✅       | The attachment collection of this help text. **Resource**: AttachmentCollection |
| addAttachment | \_LinksAddAttachment5 | ✅       | Add an attachment to the help text.                                             |

# \_LinksSelf37

This help text resource. **Resource**: HelpText

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

# EditText

Edit the help text entry. **Resource**: text/html

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

# \_LinksAttachments6

The attachment collection of this help text. **Resource**: AttachmentCollection

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

# \_LinksAddAttachment5

Add an attachment to the help text.

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
