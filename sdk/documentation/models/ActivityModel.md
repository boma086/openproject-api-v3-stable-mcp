# ActivityModel

**Properties**

| Name       | Type                  | Required | Description                                                                                      |
| :--------- | :-------------------- | :------- | :----------------------------------------------------------------------------------------------- |
| \_type     | ActivityModelType     | ❌       |                                                                                                  |
| id         | number                | ❌       | Activity id                                                                                      |
| version    | number                | ❌       | Activity version                                                                                 |
| comment    | Formattable           | ❌       |                                                                                                  |
| details    | Formattable[]         | ❌       |                                                                                                  |
| internal   | boolean               | ❌       | Whether this activity is internal (only visible to users with view_internal_comments permission) |
| createdAt  | string                | ❌       | Time of creation                                                                                 |
| updatedAt  | string                | ❌       | Time of update                                                                                   |
| \_embedded | ActivityModelEmbedded | ❌       |                                                                                                  |
| \_links    | ActivityModelLinks    | ❌       |                                                                                                  |

# ActivityModelType

**Properties**

| Name             | Type   | Required | Description         |
| :--------------- | :----- | :------- | :------------------ |
| ACTIVITY_COMMENT | string | ✅       | "Activity::Comment" |

# ActivityModelEmbedded

**Properties**

| Name        | Type                  | Required | Description                                                                                                                 |
| :---------- | :-------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------------- |
| attachments | \_EmbeddedAttachments | ❌       | Collection of attachments for this activity                                                                                 |
| workPackage | \_EmbeddedWorkPackage | ❌       | The work package this activity belongs to # Conditions Only embedded when the `journable` of the activity is a work package |

# \_EmbeddedAttachments

Collection of attachments for this activity

**Properties**

| Name       | Type                | Required | Description                                               |
| :--------- | :------------------ | :------- | :-------------------------------------------------------- |
| \_type     | AttachmentsType     | ✅       |                                                           |
| total      | number              | ✅       | The total amount of elements available in the collection. |
| count      | number              | ✅       | Actual amount of elements in this response.               |
| \_links    | AttachmentsLinks    | ✅       |                                                           |
| \_embedded | AttachmentsEmbedded | ✅       |                                                           |

# AttachmentsType

**Properties**

| Name       | Type   | Required | Description  |
| :--------- | :----- | :------- | :----------- |
| COLLECTION | string | ✅       | "Collection" |

# AttachmentsLinks

**Properties**

| Name | Type         | Required | Description                                                    |
| :--- | :----------- | :------- | :------------------------------------------------------------- |
| self | \_LinksSelf2 | ✅       | The attachments collection **Resource**: AttachmentsCollection |

# \_LinksSelf2

The attachments collection **Resource**: AttachmentsCollection

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

# AttachmentsEmbedded

**Properties**

| Name     | Type                  | Required | Description |
| :------- | :-------------------- | :------- | :---------- |
| elements | \_EmbeddedElements1[] | ❌       |             |

# \_EmbeddedElements1

Collection of Attachments

**Properties**

| Name        | Type                 | Required | Description                                     |
| :---------- | :------------------- | :------- | :---------------------------------------------- |
| title       | string               | ✅       | The name of the file                            |
| fileName    | string               | ✅       | The name of the uploaded file                   |
| description | ElementsDescription1 | ✅       | A user provided description of the file         |
| contentType | string               | ✅       | The files MIME-Type as determined by the server |
| digest      | string               | ✅       | A checksum for the files content                |
| createdAt   | string               | ✅       | Time of creation                                |
| id          | number               | ❌       | Attachment's id                                 |
| fileSize    | number               | ❌       | The size of the uploaded file in Bytes          |
| \_links     | ElementsLinks1       | ❌       |                                                 |

# ElementsDescription1

A user provided description of the file

**Properties**

| Name   | Type               | Required | Description                                        |
| :----- | :----------------- | :------- | :------------------------------------------------- |
| format | DescriptionFormat1 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string             | ❌       | The raw text, as entered by the user               |
| html   | string             | ❌       | The text converted to HTML according to the format |

# DescriptionFormat1

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# ElementsLinks1

**Properties**

| Name             | Type                     | Required | Description                                                                                                                             |
| :--------------- | :----------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| self             | \_LinksSelf3             | ✅       | This attachment **Resource**: Attachment                                                                                                |
| container        | \_LinksContainer1        | ✅       | The object (e.g. WorkPackage) housing the attachment **Resource**: Anything                                                             |
| author           | \_LinksAuthor1           | ✅       | The user who uploaded the attachment **Resource**: User                                                                                 |
| downloadLocation | \_LinksDownloadLocation1 | ✅       | Direct download link to the attachment **Resource**: -                                                                                  |
| delete           | \_LinksDelete1           | ❌       | Deletes this attachment # Conditions **Permission**: edit on attachment container or being the author for attachments without container |

# \_LinksSelf3

This attachment **Resource**: Attachment

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

# \_LinksContainer1

The object (e.g. WorkPackage) housing the attachment **Resource**: Anything

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

# \_LinksAuthor1

The user who uploaded the attachment **Resource**: User

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

# \_LinksDownloadLocation1

Direct download link to the attachment **Resource**: -

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

# \_LinksDelete1

Deletes this attachment # Conditions **Permission**: edit on attachment container or being the author for attachments without container

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

# \_EmbeddedWorkPackage

The work package this activity belongs to # Conditions Only embedded when the `journable` of the activity is a work package

**Properties**

| Name                  | Type                   | Required | Description                                                                                                                                                                                        |
| :-------------------- | :--------------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| subject               | string                 | ✅       | Work package subject                                                                                                                                                                               |
| \_links               | WorkPackageLinks       | ✅       |                                                                                                                                                                                                    |
| id                    | number                 | ❌       | Work package id                                                                                                                                                                                    |
| lockVersion           | number                 | ❌       | The version of the item as used for optimistic locking                                                                                                                                             |
| \_type                | WorkPackageType        | ❌       |                                                                                                                                                                                                    |
| description           | WorkPackageDescription | ❌       | The work package description                                                                                                                                                                       |
| scheduleManually      | boolean                | ❌       | Uses manual scheduling mode when true (default). Uses automatic scheduling mode when false. Can be automatic only when predecessors or children are present.                                       |
| readonly              | boolean                | ❌       | If true, the work package is in a readonly status so with the exception of the status, no other property can be altered.                                                                           |
| startDate             | string                 | ❌       | Scheduled beginning of a work package                                                                                                                                                              |
| dueDate               | string                 | ❌       | Scheduled end of a work package                                                                                                                                                                    |
| date                  | string                 | ❌       | Date on which a milestone is achieved                                                                                                                                                              |
| derivedStartDate      | string                 | ❌       | Similar to start date but is not set by a client but rather deduced by the work packages' descendants. If manual scheduleManually is active, the two dates can deviate.                            |
| derivedDueDate        | string                 | ❌       | Similar to due date but is not set by a client but rather deduced by the work packages' descendants. If manual scheduleManually is active, the two dates can deviate.                              |
| duration              | string                 | ❌       | **(NOT IMPLEMENTED)** The amount of time in hours the work package needs to be completed. Not available for milestone type of work packages.                                                       |
| estimatedTime         | string                 | ❌       | Time a work package likely needs to be completed excluding its descendants                                                                                                                         |
| derivedEstimatedTime  | string                 | ❌       | Time a work package likely needs to be completed including its descendants                                                                                                                         |
| ignoreNonWorkingDays  | boolean                | ❌       | **(NOT IMPLEMENTED)** When scheduling, whether or not to ignore the non working days being defined. A work package with the flag set to true will be allowed to be scheduled to a non working day. |
| spentTime             | string                 | ❌       | The time booked for this work package by users working on it # Conditions **Permission** view time entries                                                                                         |
| percentageDone        | number                 | ❌       | Amount of total completion for a work package                                                                                                                                                      |
| derivedPercentageDone | number                 | ❌       | Amount of total completion for a work package derived from itself and its descendant work packages                                                                                                 |
| createdAt             | string                 | ❌       | Time of creation. Can be writable by admins with the `apiv3_write_readonly_attributes` setting enabled.                                                                                            |
| updatedAt             | string                 | ❌       | Time of the most recent change to the work package.                                                                                                                                                |

# WorkPackageLinks

**Properties**

| Name              | Type                      | Required | Description                                                                                                                                                                                                          |
| :---------------- | :------------------------ | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| self              | \_LinksSelf4              | ✅       | This work package **Resource**: WorkPackage                                                                                                                                                                          |
| schema            | \_LinksSchema1            | ✅       | The schema of this work package **Resource**: Schema                                                                                                                                                                 |
| ancestors         | \_LinksAncestors1[]       | ✅       |                                                                                                                                                                                                                      |
| attachments       | \_LinksAttachments1       | ✅       | The files attached to this work package **Resource**: Collection # Conditions - **Setting**: deactivate_work_package_attachments set to false in related project                                                     |
| author            | \_LinksAuthor2            | ✅       | The person that created the work package **Resource**: User                                                                                                                                                          |
| children          | \_LinksChildren1[]        | ✅       |                                                                                                                                                                                                                      |
| priority          | \_LinksPriority1          | ✅       | The priority of the work package **Resource**: Priority                                                                                                                                                              |
| project           | \_LinksProject1           | ✅       | The project to which the work package belongs **Resource**: Project                                                                                                                                                  |
| status            | \_LinksStatus1            | ✅       | The current status of the work package **Resource**: Status                                                                                                                                                          |
| type              | \_LinksType1              | ✅       | The type of the work package **Resource**: Type                                                                                                                                                                      |
| addComment        | \_LinksAddComment1        | ❌       | Post comment to WP # Conditions **Permission**: add work package notes                                                                                                                                               |
| addRelation       | \_LinksAddRelation1       | ❌       | Adds a relation to this work package. # Conditions **Permission**: manage wp relations                                                                                                                               |
| addWatcher        | \_LinksAddWatcher1        | ❌       | Add any user to WP watchers # Conditions **Permission**: add watcher                                                                                                                                                 |
| customActions     | \_LinksCustomActions1[]   | ❌       |                                                                                                                                                                                                                      |
| previewMarkup     | \_LinksPreviewMarkup1     | ❌       | Post markup (in markdown) here to receive an HTML-rendered response                                                                                                                                                  |
| removeWatcher     | \_LinksRemoveWatcher1     | ❌       | Remove any user from WP watchers # Conditions **Permission**: delete watcher                                                                                                                                         |
| delete            | \_LinksDelete2            | ❌       | Delete this work package # Conditions **Permission**: delete_work_packages                                                                                                                                           |
| logTime           | \_LinksLogTime1           | ❌       | Create time entries on the work package # Conditions **Permission**: log_time or log_own_time                                                                                                                        |
| move              | \_LinksMove1              | ❌       | Link to page for moving this work package # Conditions **Permission**: move_work_packages                                                                                                                            |
| copy              | \_LinksCopy1              | ❌       | Link to page for copying this work package # Conditions **Permission**: add_work_packages                                                                                                                            |
| unwatch           | \_LinksUnwatch1           | ❌       | Remove current user from WP watchers # Conditions logged in; watching                                                                                                                                                |
| update            | \_LinksUpdate1            | ❌       | Form endpoint that aids in preparing and performing edits on a work package # Conditions **Permission**: edit work package                                                                                           |
| updateImmediately | \_LinksUpdateImmediately1 | ❌       | Directly perform edits on a work package # Conditions **Permission**: edit work package                                                                                                                              |
| watch             | \_LinksWatch1             | ❌       | Add current user to WP watchers # Conditions logged in; not watching                                                                                                                                                 |
| addAttachment     | \_LinksAddAttachment1     | ❌       | Attach a file to the work package # Conditions - **Permission**: edit work package                                                                                                                                   |
| prepareAttachment | \_LinksPrepareAttachment1 | ❌       | Attach a file to the work package # Conditions - **Setting**: direct uploads enabled                                                                                                                                 |
| assignee          | \_LinksAssignee1          | ❌       | The person that is intended to work on the work package **Resource**: User                                                                                                                                           |
| availableWatchers | \_LinksAvailableWatchers1 | ❌       | All users that can be added to the work package as watchers. **Resource**: User # Conditions **Permission** add work package watchers                                                                                |
| budget            | \_LinksBudget1            | ❌       | The budget this work package is associated to **Resource**: Budget # Conditions **Permission** view cost objects                                                                                                     |
| category          | \_LinksCategory1          | ❌       | The category of the work package **Resource**: Category                                                                                                                                                              |
| addFileLink       | \_LinksAddFileLink1       | ❌       | Add a file link to the work package # Conditions **Permission**: manage_file_links                                                                                                                                   |
| fileLinks         | \_LinksFileLinks1         | ❌       | Gets the file link collection of this work package # Conditions **Permission**: view_file_links                                                                                                                      |
| parent            | \_LinksParent1            | ❌       | Parent work package **Resource**: WorkPackage                                                                                                                                                                        |
| responsible       | \_LinksResponsible1       | ❌       | The person that is responsible for the overall outcome **Resource**: User                                                                                                                                            |
| relations         | \_LinksRelations2         | ❌       | Relations this work package is involved in **Resource**: Relation # Conditions **Permission** view work packages                                                                                                     |
| revisions         | \_LinksRevisions1         | ❌       | Revisions that are referencing the work package **Resource**: Revision # Conditions **Permission** view changesets                                                                                                   |
| timeEntries       | \_LinksTimeEntries2       | ❌       | All time entries logged on the work package. Please note that this is a link to an HTML resource for now and as such, the link is subject to change. **Resource**: N/A # Conditions **Permission** view time entries |
| version           | \_LinksVersion1           | ❌       | The version associated to the work package **Resource**: Version                                                                                                                                                     |
| watchers          | \_LinksWatchers1          | ❌       | All users that are currently watching this work package **Resource**: Collection # Conditions **Permission** view work package watchers                                                                              |

# \_LinksSelf4

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

# \_LinksSchema1

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

# \_LinksAncestors1

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

# \_LinksAttachments1

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

# \_LinksAuthor2

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

# \_LinksChildren1

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

# \_LinksPriority1

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

# \_LinksProject1

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

# \_LinksStatus1

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

# \_LinksType1

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

# \_LinksAddComment1

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

# \_LinksAddRelation1

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

# \_LinksAddWatcher1

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

# \_LinksCustomActions1

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

# \_LinksPreviewMarkup1

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

# \_LinksRemoveWatcher1

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

# \_LinksDelete2

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

# \_LinksLogTime1

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

# \_LinksMove1

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

# \_LinksCopy1

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

# \_LinksUnwatch1

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

# \_LinksUpdate1

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

# \_LinksUpdateImmediately1

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

# \_LinksWatch1

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

# \_LinksAddAttachment1

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

# \_LinksPrepareAttachment1

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

# \_LinksAssignee1

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

# \_LinksAvailableWatchers1

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

# \_LinksBudget1

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

# \_LinksCategory1

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

# \_LinksAddFileLink1

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

# \_LinksFileLinks1

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

# \_LinksParent1

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

# \_LinksResponsible1

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

# \_LinksRelations2

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

# \_LinksRevisions1

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

# \_LinksTimeEntries2

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

# \_LinksVersion1

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

# \_LinksWatchers1

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

# WorkPackageType

**Properties**

| Name         | Type   | Required | Description   |
| :----------- | :----- | :------- | :------------ |
| WORK_PACKAGE | string | ✅       | "WorkPackage" |

# WorkPackageDescription

The work package description

**Properties**

| Name   | Type               | Required | Description                                        |
| :----- | :----------------- | :------- | :------------------------------------------------- |
| format | DescriptionFormat2 | ✅       | Indicates the formatting language of the raw text  |
| raw    | string             | ❌       | The raw text, as entered by the user               |
| html   | string             | ❌       | The text converted to HTML according to the format |

# DescriptionFormat2

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# ActivityModelLinks

**Properties**

| Name          | Type                  | Required | Description                                                                                                                                |
| :------------ | :-------------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------- |
| self          | \_LinksSelf5          | ❌       | This activity **Resource**: Activity                                                                                                       |
| workPackage   | \_LinksWorkPackage1   | ❌       | The work package this activity belongs to **Resource**: WorkPackage                                                                        |
| user          | \_LinksUser2          | ❌       | The user who created this activity **Resource**: Principal                                                                                 |
| update        | \_LinksUpdate2        | ❌       | Update this activity                                                                                                                       |
| attachments   | \_LinksAttachments2   | ❌       | The attachment collection of this activity **Resource**: Attachments                                                                       |
| addAttachment | \_LinksAddAttachment2 | ❌       | Attach a file to the activity # Conditions **Permissions**: - `add_work_package_comments` - for internal comments: `add_internal_comments` |

# \_LinksSelf5

This activity **Resource**: Activity

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

# \_LinksWorkPackage1

The work package this activity belongs to **Resource**: WorkPackage

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

# \_LinksUser2

The user who created this activity **Resource**: Principal

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

# \_LinksUpdate2

Update this activity

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

# \_LinksAttachments2

The attachment collection of this activity **Resource**: Attachments

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

# \_LinksAddAttachment2

Attach a file to the activity # Conditions **Permissions**: - `add_work_package_comments` - for internal comments: `add_internal_comments`

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
