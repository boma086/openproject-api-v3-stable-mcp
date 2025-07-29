# WorkPackageFormModel

The work package creation form. This object is returned, whenever a work package form endpoint is called. It contains an allowed payload definition, the full schema and any validation errors on the current request body.

**Properties**

| Name       | Type                         | Required | Description |
| :--------- | :--------------------------- | :------- | :---------- |
| \_type     | WorkPackageFormModelType     | ❌       |             |
| \_embedded | WorkPackageFormModelEmbedded | ❌       |             |
| \_links    | WorkPackageFormModelLinks    | ❌       |             |

# WorkPackageFormModelType

**Properties**

| Name | Type   | Required | Description |
| :--- | :----- | :------- | :---------- |
| FORM | string | ✅       | "Form"      |

# WorkPackageFormModelEmbedded

**Properties**

| Name             | Type                   | Required | Description                                                                                                                                                                                      |
| :--------------- | :--------------------- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| payload          | WorkPackageWriteModel  | ❌       | This model is used for creating and updating work packages. It can also be used for validation against the work package form endpoints.                                                          |
| schema           | WorkPackageSchemaModel | ❌       | A schema for a work package. This schema defines the attributes of a work package. TODO: Incomplete, needs to be updated with the real behaviour of schemas (when does which attribute appear?). |
| validationErrors | any                    | ❌       | All validation errors, where the key is the faulty property. The object is empty, if the request body is valid.                                                                                  |

# WorkPackageFormModelLinks

**Properties**

| Name          | Type                  | Required | Description                                                                                 |
| :------------ | :-------------------- | :------- | :------------------------------------------------------------------------------------------ |
| self          | \_LinksSelf57         | ❌       | This form endpoint **Resource** : Form                                                      |
| validate      | \_LinksValidate2      | ❌       | The endpoint for validating the request bodies. Often referring to this very form endpoint. |
| previewMarkup | \_LinksPreviewMarkup3 | ❌       | Renders a markup preview for the work package form.                                         |
| customFields  | CustomFields          | ❌       | Link to the HTML page for the custom field definitions.                                     |
| configureForm | ConfigureForm         | ❌       | Link to the HTML page for the form configuration.                                           |

# \_LinksSelf57

This form endpoint **Resource** : Form

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

# \_LinksValidate2

The endpoint for validating the request bodies. Often referring to this very form endpoint.

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

# \_LinksPreviewMarkup3

Renders a markup preview for the work package form.

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

# CustomFields

Link to the HTML page for the custom field definitions.

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

# ConfigureForm

Link to the HTML page for the form configuration.

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
