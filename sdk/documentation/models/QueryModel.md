# QueryModel

**Properties**

| Name              | Type                             | Required | Description                                                                                               |
| :---------------- | :------------------------------- | :------- | :-------------------------------------------------------------------------------------------------------- |
| createdAt         | string                           | ✅       | Time of creation                                                                                          |
| updatedAt         | string                           | ✅       | Time of the most recent change to the query                                                               |
| id                | number                           | ❌       | Query id                                                                                                  |
| name              | string                           | ❌       | Query name                                                                                                |
| filters           | QueryFilterInstanceSchemaModel[] | ❌       | A set of QueryFilters which will be applied to the work packages to determine the resulting work packages |
| sums              | boolean                          | ❌       | Should sums (of supported properties) be shown?                                                           |
| timelineVisible   | boolean                          | ❌       | Should the timeline mode be shown?                                                                        |
| timelineLabels    | string[]                         | ❌       | Which labels are shown in the timeline, empty when default                                                |
| timelineZoomLevel | string                           | ❌       | Which zoom level should the timeline be rendered in?                                                      |
| timestamps        | any[]                            | ❌       | Timestamps to filter by when showing changed attributes on work packages.                                 |
| highlightingMode  | string                           | ❌       | Which highlighting mode should the table have?                                                            |
| showHierarchies   | boolean                          | ❌       | Should the hierarchy mode be enabled?                                                                     |
| hidden            | boolean                          | ❌       | Should the query be hidden from the query list?                                                           |
| public            | boolean                          | ❌       | Can users besides the owner see the query?                                                                |
| starred           | boolean                          | ❌       | Should the query be highlighted to the user?                                                              |
| \_links           | QueryModelLinks                  | ❌       |                                                                                                           |

# QueryModelLinks

**Properties**

| Name              | Type                       | Required | Description                                                                                                                                                                                 |
| :---------------- | :------------------------- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| star              | Star                       | ❌       | Elevates the query to the status of 'starred' # Conditions **Permission**: save queries for own queries, manage public queries for public queries; Only present if query is not yet starred |
| unstar            | Unstar                     | ❌       | Removes the 'starred' status # Conditions **Permission**: save queries for own queries, manage public queries for public queries; Only present if query is starred                          |
| update            | \_LinksUpdate8             | ❌       | Use the Form based process to verify the query before persisting # Conditions **Permission**: view work packages                                                                            |
| updateImmediately | \_LinksUpdateImmediately11 | ❌       | Persist the query without using a Form based process for guidance # Conditions **Permission**: save queries for own queries, manage public queries for public queries;                      |

# Star

Elevates the query to the status of 'starred' # Conditions **Permission**: save queries for own queries, manage public queries for public queries; Only present if query is not yet starred

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

# Unstar

Removes the 'starred' status # Conditions **Permission**: save queries for own queries, manage public queries for public queries; Only present if query is starred

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

# \_LinksUpdate8

Use the Form based process to verify the query before persisting # Conditions **Permission**: view work packages

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

# \_LinksUpdateImmediately11

Persist the query without using a Form based process for guidance # Conditions **Permission**: save queries for own queries, manage public queries for public queries;

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
