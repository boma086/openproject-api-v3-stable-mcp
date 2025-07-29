# WorkPackageModel

**Properties**

| Name                  | Type                        | Required | Description                                                                                                                                                                                        |
| :-------------------- | :-------------------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| subject               | string                      | ✅       | Work package subject                                                                                                                                                                               |
| \_links               | WorkPackageModelLinks       | ✅       |                                                                                                                                                                                                    |
| id                    | number                      | ❌       | Work package id                                                                                                                                                                                    |
| lockVersion           | number                      | ❌       | The version of the item as used for optimistic locking                                                                                                                                             |
| \_type                | WorkPackageModelType        | ❌       |                                                                                                                                                                                                    |
| description           | WorkPackageModelDescription | ❌       | The work package description                                                                                                                                                                       |
| scheduleManually      | boolean                     | ❌       | Uses manual scheduling mode when true (default). Uses automatic scheduling mode when false. Can be automatic only when predecessors or children are present.                                       |
| readonly              | boolean                     | ❌       | If true, the work package is in a readonly status so with the exception of the status, no other property can be altered.                                                                           |
| startDate             | string                      | ❌       | Scheduled beginning of a work package                                                                                                                                                              |
| dueDate               | string                      | ❌       | Scheduled end of a work package                                                                                                                                                                    |
| date                  | string                      | ❌       | Date on which a milestone is achieved                                                                                                                                                              |
| derivedStartDate      | string                      | ❌       | Similar to start date but is not set by a client but rather deduced by the work packages' descendants. If manual scheduleManually is active, the two dates can deviate.                            |
| derivedDueDate        | string                      | ❌       | Similar to due date but is not set by a client but rather deduced by the work packages' descendants. If manual scheduleManually is active, the two dates can deviate.                              |
| duration              | string                      | ❌       | **(NOT IMPLEMENTED)** The amount of time in hours the work package needs to be completed. Not available for milestone type of work packages.                                                       |
| estimatedTime         | string                      | ❌       | Time a work package likely needs to be completed excluding its descendants                                                                                                                         |
| derivedEstimatedTime  | string                      | ❌       | Time a work package likely needs to be completed including its descendants                                                                                                                         |
| ignoreNonWorkingDays  | boolean                     | ❌       | **(NOT IMPLEMENTED)** When scheduling, whether or not to ignore the non working days being defined. A work package with the flag set to true will be allowed to be scheduled to a non working day. |
| spentTime             | string                      | ❌       | The time booked for this work package by users working on it # Conditions **Permission** view time entries                                                                                         |
| percentageDone        | number                      | ❌       | Amount of total completion for a work package                                                                                                                                                      |
| derivedPercentageDone | number                      | ❌       | Amount of total completion for a work package derived from itself and its descendant work packages                                                                                                 |
| createdAt             | string                      | ❌       | Time of creation. Can be writable by admins with the `apiv3_write_readonly_attributes` setting enabled.                                                                                            |
| updatedAt             | string                      | ❌       | Time of the most recent change to the work package.                                                                                                                                                |

# WorkPackageModelLinks

**Properties**

| Name              | Type                      | Required | Description                                                                                                                                                                                                          |
| :---------------- | :------------------------ | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| self              | \_LinksSelf25             | ✅       | This work package **Resource**: WorkPackage                                                                                                                                                                          |
| schema            | \_LinksSchema2            | ✅       | The schema of this work package **Resource**: Schema                                                                                                                                                                 |
| ancestors         | \_LinksAncestors2[]       | ✅       |                                                                                                                                                                                                                      |
| attachments       | \_LinksAttachments4       | ✅       | The files attached to this work package **Resource**: Collection # Conditions - **Setting**: deactivate_work_package_attachments set to false in related project                                                     |
| author            | \_LinksAuthor5            | ✅       | The person that created the work package **Resource**: User                                                                                                                                                          |
| children          | \_LinksChildren3[]        | ✅       |                                                                                                                                                                                                                      |
| priority          | \_LinksPriority2          | ✅       | The priority of the work package **Resource**: Priority                                                                                                                                                              |
| project           | \_LinksProject5           | ✅       | The project to which the work package belongs **Resource**: Project                                                                                                                                                  |
| status            | \_LinksStatus2            | ✅       | The current status of the work package **Resource**: Status                                                                                                                                                          |
| type              | \_LinksType3              | ✅       | The type of the work package **Resource**: Type                                                                                                                                                                      |
| addComment        | \_LinksAddComment2        | ❌       | Post comment to WP # Conditions **Permission**: add work package notes                                                                                                                                               |
| addRelation       | \_LinksAddRelation2       | ❌       | Adds a relation to this work package. # Conditions **Permission**: manage wp relations                                                                                                                               |
| addWatcher        | \_LinksAddWatcher2        | ❌       | Add any user to WP watchers # Conditions **Permission**: add watcher                                                                                                                                                 |
| customActions     | \_LinksCustomActions2[]   | ❌       |                                                                                                                                                                                                                      |
| previewMarkup     | \_LinksPreviewMarkup2     | ❌       | Post markup (in markdown) here to receive an HTML-rendered response                                                                                                                                                  |
| removeWatcher     | \_LinksRemoveWatcher2     | ❌       | Remove any user from WP watchers # Conditions **Permission**: delete watcher                                                                                                                                         |
| delete            | \_LinksDelete5            | ❌       | Delete this work package # Conditions **Permission**: delete_work_packages                                                                                                                                           |
| logTime           | \_LinksLogTime2           | ❌       | Create time entries on the work package # Conditions **Permission**: log_time or log_own_time                                                                                                                        |
| move              | \_LinksMove2              | ❌       | Link to page for moving this work package # Conditions **Permission**: move_work_packages                                                                                                                            |
| copy              | \_LinksCopy2              | ❌       | Link to page for copying this work package # Conditions **Permission**: add_work_packages                                                                                                                            |
| unwatch           | \_LinksUnwatch2           | ❌       | Remove current user from WP watchers # Conditions logged in; watching                                                                                                                                                |
| update            | \_LinksUpdate3            | ❌       | Form endpoint that aids in preparing and performing edits on a work package # Conditions **Permission**: edit work package                                                                                           |
| updateImmediately | \_LinksUpdateImmediately2 | ❌       | Directly perform edits on a work package # Conditions **Permission**: edit work package                                                                                                                              |
| watch             | \_LinksWatch2             | ❌       | Add current user to WP watchers # Conditions logged in; not watching                                                                                                                                                 |
| addAttachment     | \_LinksAddAttachment3     | ❌       | Attach a file to the work package # Conditions - **Permission**: edit work package                                                                                                                                   |
| prepareAttachment | \_LinksPrepareAttachment2 | ❌       | Attach a file to the work package # Conditions - **Setting**: direct uploads enabled                                                                                                                                 |
| assignee          | \_LinksAssignee2          | ❌       | The person that is intended to work on the work package **Resource**: User                                                                                                                                           |
| availableWatchers | \_LinksAvailableWatchers2 | ❌       | All users that can be added to the work package as watchers. **Resource**: User # Conditions **Permission** add work package watchers                                                                                |
| budget            | \_LinksBudget2            | ❌       | The budget this work package is associated to **Resource**: Budget # Conditions **Permission** view cost objects                                                                                                     |
| category          | \_LinksCategory2          | ❌       | The category of the work package **Resource**: Category                                                                                                                                                              |
| addFileLink       | \_LinksAddFileLink2       | ❌       | Add a file link to the work package # Conditions **Permission**: manage_file_links                                                                                                                                   |
| fileLinks         | \_LinksFileLinks2         | ❌       | Gets the file link collection of this work package # Conditions **Permission**: view_file_links                                                                                                                      |
| parent            | \_LinksParent3            | ❌       | Parent work package **Resource**: WorkPackage                                                                                                                                                                        |
| responsible       | \_LinksResponsible2       | ❌       | The person that is responsible for the overall outcome **Resource**: User                                                                                                                                            |
| relations         | \_LinksRelations3         | ❌       | Relations this work package is involved in **Resource**: Relation # Conditions **Permission** view work packages                                                                                                     |
| revisions         | \_LinksRevisions2         | ❌       | Revisions that are referencing the work package **Resource**: Revision # Conditions **Permission** view changesets                                                                                                   |
| timeEntries       | \_LinksTimeEntries3       | ❌       | All time entries logged on the work package. Please note that this is a link to an HTML resource for now and as such, the link is subject to change. **Resource**: N/A # Conditions **Permission** view time entries |
| version           | \_LinksVersion2           | ❌       | The version associated to the work package **Resource**: Version                                                                                                                                                     |
| watchers          | \_LinksWatchers2          | ❌       | All users that are currently watching this work package **Resource**: Collection # Conditions **Permission** view work package watchers                                                                              |

# \_LinksSelf25

This work package **Resource**: WorkPackage

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

# \_LinksSchema2

The schema of this work package **Resource**: Schema

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

# \_LinksAncestors2

A visible ancestor work package of the current work package. **Resource**: WorkPackage # Conditions **Permission** view work packages

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

# \_LinksAttachments4

The files attached to this work package **Resource**: Collection # Conditions - **Setting**: deactivate_work_package_attachments set to false in related project

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

# \_LinksAuthor5

The person that created the work package **Resource**: User

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

# \_LinksChildren3

A visible child work package of the current work package. **Resource**: WorkPackage # Conditions **Permission** view work packages

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

# \_LinksPriority2

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

# \_LinksProject5

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

# \_LinksStatus2

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

# \_LinksType3

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

# \_LinksAddComment2

Post comment to WP # Conditions **Permission**: add work package notes

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

# \_LinksAddRelation2

Adds a relation to this work package. # Conditions **Permission**: manage wp relations

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

# \_LinksAddWatcher2

Add any user to WP watchers # Conditions **Permission**: add watcher

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

# \_LinksCustomActions2

A predefined action that can be applied to the work package. **Resource**: CustomAction

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

# \_LinksPreviewMarkup2

Post markup (in markdown) here to receive an HTML-rendered response

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

# \_LinksRemoveWatcher2

Remove any user from WP watchers # Conditions **Permission**: delete watcher

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

# \_LinksDelete5

Delete this work package # Conditions **Permission**: delete_work_packages

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

# \_LinksLogTime2

Create time entries on the work package # Conditions **Permission**: log_time or log_own_time

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

# \_LinksMove2

Link to page for moving this work package # Conditions **Permission**: move_work_packages

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

# \_LinksCopy2

Link to page for copying this work package # Conditions **Permission**: add_work_packages

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

# \_LinksUnwatch2

Remove current user from WP watchers # Conditions logged in; watching

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

# \_LinksUpdate3

Form endpoint that aids in preparing and performing edits on a work package # Conditions **Permission**: edit work package

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

# \_LinksUpdateImmediately2

Directly perform edits on a work package # Conditions **Permission**: edit work package

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

# \_LinksWatch2

Add current user to WP watchers # Conditions logged in; not watching

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

# \_LinksAddAttachment3

Attach a file to the work package # Conditions - **Permission**: edit work package

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

# \_LinksPrepareAttachment2

Attach a file to the work package # Conditions - **Setting**: direct uploads enabled

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

# \_LinksAssignee2

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

# \_LinksAvailableWatchers2

All users that can be added to the work package as watchers. **Resource**: User # Conditions **Permission** add work package watchers

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

# \_LinksBudget2

The budget this work package is associated to **Resource**: Budget # Conditions **Permission** view cost objects

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

# \_LinksCategory2

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

# \_LinksAddFileLink2

Add a file link to the work package # Conditions **Permission**: manage_file_links

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

# \_LinksFileLinks2

Gets the file link collection of this work package # Conditions **Permission**: view_file_links

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

# \_LinksParent3

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

# \_LinksResponsible2

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

# \_LinksRelations3

Relations this work package is involved in **Resource**: Relation # Conditions **Permission** view work packages

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

# \_LinksRevisions2

Revisions that are referencing the work package **Resource**: Revision # Conditions **Permission** view changesets

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

# \_LinksTimeEntries3

All time entries logged on the work package. Please note that this is a link to an HTML resource for now and as such, the link is subject to change. **Resource**: N/A # Conditions **Permission** view time entries

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

# \_LinksVersion2

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

# \_LinksWatchers2

All users that are currently watching this work package **Resource**: Collection # Conditions **Permission** view work package watchers

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

# WorkPackageModelType

**Properties**

| Name         | Type   | Required | Description   |
| :----------- | :----- | :------- | :------------ |
| WORK_PACKAGE | string | ✅       | "WorkPackage" |

# WorkPackageModelDescription

The work package description

**Properties**

| Name   | Type               | Required | Description                                        |
| :----- | :----------------- | :------- | :------------------------------------------------- |
| format | DescriptionFormat5 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string             | ❌       | The raw text, as entered by the user               |
| html   | string             | ❌       | The text converted to HTML according to the format |

# DescriptionFormat5

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

<!-- This file was generated by liblab | https://liblab.com/ -->
