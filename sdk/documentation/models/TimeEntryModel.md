# TimeEntryModel

**Properties**

| Name      | Type                | Required | Description                                                                                                                                                                                                                                                                                              |
| :-------- | :------------------ | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id        | number              | ❌       | The id of the time entry                                                                                                                                                                                                                                                                                 |
| comment   | string              | ❌       | A comment to the time entry                                                                                                                                                                                                                                                                              |
| spentOn   | string              | ❌       | The date the expenditure is booked for                                                                                                                                                                                                                                                                   |
| hours     | string              | ❌       | The time quantifying the expenditure                                                                                                                                                                                                                                                                     |
| ongoing   | boolean             | ❌       | Whether the time entry is actively tracking time                                                                                                                                                                                                                                                         |
| createdAt | string              | ❌       | The time the time entry was created                                                                                                                                                                                                                                                                      |
| startTime | string              | ❌       | The time the time entry was started, or null if the time entry does not have a start time. The time is returned as UTC time, if presented to the user it should be converted to the user's timezone. This field is only available if the global `allow_tracking_start_and_end_times` setting is enabled. |
| endTime   | string              | ❌       | The time the time entry was ended, or null if the time entry does not have a start time. The time is returned as UTC time, if presented to the user it should be converted to the user's timezone. This field is only available if the global `allow_tracking_start_and_end_times` setting is enabled.   |
| updatedAt | string              | ❌       | The time the time entry was last updated                                                                                                                                                                                                                                                                 |
| \_links   | TimeEntryModelLinks | ❌       |                                                                                                                                                                                                                                                                                                          |

# TimeEntryModelLinks

**Properties**

| Name              | Type                       | Required | Description                                                                                                                                                                                |
| :---------------- | :------------------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| self              | \_LinksSelf72              | ✅       | This time entry **Resource**: TimeEntry                                                                                                                                                    |
| project           | \_LinksProject16           | ✅       | The project the time entry is bundled in. The project might be different from the work package's project once the workPackage is moved. **Resource**: Project                              |
| user              | \_LinksUser3               | ✅       | The user the time entry tracks expenditures for **Resource**: User                                                                                                                         |
| activity          | \_LinksActivity2           | ✅       | The time entry activity the time entry is categorized as **Resource**: TimeEntriesActivity                                                                                                 |
| updateImmediately | \_LinksUpdateImmediately17 | ❌       | Directly perform edits on this time entry # Conditions **Permission**: 'edit time entries' or 'edit own time entries' if the time entry belongs to the user                                |
| update            | \_LinksUpdate11            | ❌       | Form endpoint that aids in preparing and performing edits on a TimeEntry # Conditions **Permission**: 'edit time entries' or 'edit own time entries' if the time entry belongs to the user |
| delete            | \_LinksDelete17            | ❌       | Delete this time entry # Conditions **Permission**: 'edit time entries' or 'edit own time entries' if the time entry belongs to the user                                                   |
| schema            | \_LinksSchema5             | ❌       | The time entry schema **Resource**: Schema                                                                                                                                                 |
| workPackage       | \_LinksWorkPackage3        | ❌       | The work package the time entry is created on **Resource**: WorkPackage                                                                                                                    |

# \_LinksSelf72

This time entry **Resource**: TimeEntry

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

# \_LinksProject16

The project the time entry is bundled in. The project might be different from the work package's project once the workPackage is moved. **Resource**: Project

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

# \_LinksUser3

The user the time entry tracks expenditures for **Resource**: User

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

# \_LinksActivity2

The time entry activity the time entry is categorized as **Resource**: TimeEntriesActivity

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

# \_LinksUpdateImmediately17

Directly perform edits on this time entry # Conditions **Permission**: 'edit time entries' or 'edit own time entries' if the time entry belongs to the user

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

# \_LinksUpdate11

Form endpoint that aids in preparing and performing edits on a TimeEntry # Conditions **Permission**: 'edit time entries' or 'edit own time entries' if the time entry belongs to the user

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

# \_LinksDelete17

Delete this time entry # Conditions **Permission**: 'edit time entries' or 'edit own time entries' if the time entry belongs to the user

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

# \_LinksSchema5

The time entry schema **Resource**: Schema

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

# \_LinksWorkPackage3

The work package the time entry is created on **Resource**: WorkPackage

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
