# WorkPackagePatchModel

**Properties**

| Name                 | Type                             | Required | Description                                                                                                                                                                                                                                                                                             |
| :------------------- | :------------------------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| lockVersion          | number                           | ✅       | The version of the item as used for optimistic locking                                                                                                                                                                                                                                                  |
| subject              | string                           | ❌       | Work package subject                                                                                                                                                                                                                                                                                    |
| description          | WorkPackagePatchModelDescription | ❌       | The work package description                                                                                                                                                                                                                                                                            |
| scheduleManually     | boolean                          | ❌       | Uses manual scheduling mode when true (default). Uses automatic scheduling mode when false. Can be automatic only when predecessors or children are present.                                                                                                                                            |
| startDate            | string                           | ❌       | Scheduled beginning of a work package                                                                                                                                                                                                                                                                   |
| dueDate              | string                           | ❌       | Scheduled end of a work package                                                                                                                                                                                                                                                                         |
| estimatedTime        | string                           | ❌       | Time a work package likely needs to be completed excluding its descendants                                                                                                                                                                                                                              |
| duration             | string                           | ❌       | The amount of time in hours the work package needs to be completed. This value must be bigger or equal to `P1D`, and any the value will get floored to the nearest day. The duration has no effect, unless either a start date or a due date is set. Not available for milestone type of work packages. |
| ignoreNonWorkingDays | boolean                          | ❌       | When scheduling, whether or not to ignore the non working days being defined. A work package with the flag set to true will be allowed to be scheduled to a non working day.                                                                                                                            |
| \_links              | WorkPackagePatchModelLinks       | ❌       |                                                                                                                                                                                                                                                                                                         |

# WorkPackagePatchModelDescription

The work package description

**Properties**

| Name   | Type               | Required | Description                                        |
| :----- | :----------------- | :------- | :------------------------------------------------- |
| format | DescriptionFormat8 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string             | ❌       | The raw text, as entered by the user               |
| html   | string             | ❌       | The text converted to HTML according to the format |

# DescriptionFormat8

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# WorkPackagePatchModelLinks

**Properties**

| Name        | Type                | Required | Description                                                                |
| :---------- | :------------------ | :------- | :------------------------------------------------------------------------- |
| category    | \_LinksCategory4    | ❌       | The category of the work package **Resource**: Category                    |
| type        | \_LinksType6        | ❌       | The type of the work package **Resource**: Type                            |
| priority    | \_LinksPriority4    | ❌       | The priority of the work package **Resource**: Priority                    |
| project     | \_LinksProject14    | ❌       | The project to which the work package belongs **Resource**: Project        |
| status      | \_LinksStatus7      | ❌       | The current status of the work package **Resource**: Status                |
| responsible | \_LinksResponsible4 | ❌       | The person that is responsible for the overall outcome **Resource**: User  |
| assignee    | \_LinksAssignee4    | ❌       | The person that is intended to work on the work package **Resource**: User |
| version     | \_LinksVersion4     | ❌       | The version associated to the work package **Resource**: Version           |
| parent      | \_LinksParent7      | ❌       | Parent work package **Resource**: WorkPackage                              |

# \_LinksCategory4

The category of the work package **Resource**: Category

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

# \_LinksType6

The type of the work package **Resource**: Type

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

# \_LinksPriority4

The priority of the work package **Resource**: Priority

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

# \_LinksProject14

The project to which the work package belongs **Resource**: Project

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

# \_LinksStatus7

The current status of the work package **Resource**: Status

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

# \_LinksResponsible4

The person that is responsible for the overall outcome **Resource**: User

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

# \_LinksAssignee4

The person that is intended to work on the work package **Resource**: User

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

# \_LinksVersion4

The version associated to the work package **Resource**: Version

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

# \_LinksParent7

Parent work package **Resource**: WorkPackage

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
