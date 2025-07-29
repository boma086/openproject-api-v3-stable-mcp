# RevisionModel

**Properties**

| Name                | Type               | Required | Description                                                                                                                                            |
| :------------------ | :----------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| identifier          | string             | ✅       | The raw SCM identifier of the revision (e.g. full SHA hash)                                                                                            |
| formattedIdentifier | string             | ✅       | The SCM identifier of the revision, formatted (e.g. shortened unambiguous SHA hash). May be identical to identifier in many cases                      |
| authorName          | string             | ✅       | The name of the author that committed this revision. Note that this name is retrieved from the repository and does not identify a user in OpenProject. |
| message             | Message            | ✅       | The commit message of the revision                                                                                                                     |
| createdAt           | string             | ✅       | The time this revision was committed to the repository                                                                                                 |
| id                  | number             | ❌       | Revision's id, assigned by OpenProject                                                                                                                 |
| \_links             | RevisionModelLinks | ❌       |                                                                                                                                                        |

# Message

The commit message of the revision

**Properties**

| Name   | Type          | Required | Description                                        |
| :----- | :------------ | :------- | :------------------------------------------------- |
| format | MessageFormat | ✅       | Indicates the formatting language of the raw text  |
| raw    | string        | ❌       | The raw text, as entered by the user               |
| html   | string        | ❌       | The text converted to HTML according to the format |

# MessageFormat

Indicates the formatting language of the raw text

**Properties**

| Name     | Type   | Required | Description |
| :------- | :----- | :------- | :---------- |
| PLAIN    | string | ✅       | "plain"     |
| MARKDOWN | string | ✅       | "markdown"  |
| CUSTOM   | string | ✅       | "custom"    |

# RevisionModelLinks

**Properties**

| Name         | Type             | Required | Description                                                                                                 |
| :----------- | :--------------- | :------- | :---------------------------------------------------------------------------------------------------------- |
| self         | \_LinksSelf69    | ✅       | This revision **Resource**: Revision                                                                        |
| project      | \_LinksProject15 | ✅       | The project to which the revision belongs **Resource**: Project                                             |
| showRevision | ShowRevision     | ✅       | A URL to the repository view (outside APIv3) showing this revision **Resource**: -                          |
| author       | \_LinksAuthor8   | ❌       | The user that added this revision, if the authorName was mapped to a user in OpenProject **Resource**: User |

# \_LinksSelf69

This revision **Resource**: Revision

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

# \_LinksProject15

The project to which the revision belongs **Resource**: Project

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

# ShowRevision

A URL to the repository view (outside APIv3) showing this revision **Resource**: -

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

# \_LinksAuthor8

The user that added this revision, if the authorName was mapped to a user in OpenProject **Resource**: User

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
