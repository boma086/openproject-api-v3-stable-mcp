# MembershipFormModel

**Properties**

| Name       | Type                        | Required | Description |
| :--------- | :-------------------------- | :------- | :---------- |
| \_type     | MembershipFormModelType     | ✅       |             |
| \_embedded | MembershipFormModelEmbedded | ✅       |             |
| \_links    | MembershipFormModelLinks    | ✅       |             |

# MembershipFormModelType

**Properties**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| FORM | string | ✅       | "Form"      |

# MembershipFormModelEmbedded

**Properties**

| Name            | Type                  | Required | Description |
| :-------------- | :-------------------- | :------- | :---------- |
| payload         | MembershipWriteModel  | ✅       |             |
| schema          | MembershipSchemaModel | ✅       |             |
| validationError | ValidationError       | ✅       |             |

# ValidationError

**Properties**

| Name      | Type          | Required | Description |
| :-------- | :------------ | :------- | :---------- |
| base      | ErrorResponse | ❌       |             |
| principal | ErrorResponse | ❌       |             |
| roles     | ErrorResponse | ❌       |             |

# MembershipFormModelLinks

**Properties**

| Name     | Type               | Required | Description                                                                                                |
| :------- | :----------------- | :------- | :--------------------------------------------------------------------------------------------------------- |
| self     | \_LinksSelf44      | ✅       | This form request. **Resource**: Form                                                                      |
| validate | \_LinksValidate1[] | ✅       |                                                                                                            |
| commit   | Commit             | ✅       | The endpoint to create the membership with the same payload, as sent to the form. **Resource**: Membership |

# \_LinksSelf44

This form request. **Resource**: Form

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

# \_LinksValidate1

The endpoint to validate the membership payload.

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

# Commit

The endpoint to create the membership with the same payload, as sent to the form. **Resource**: Membership

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
