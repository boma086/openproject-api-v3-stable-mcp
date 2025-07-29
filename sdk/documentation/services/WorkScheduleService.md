# WorkScheduleService

A list of all methods in the `WorkScheduleService` service. Click on the method name to view detailed information about that method.

| Methods                                     | Description                                                                                                                                                                                                                                                 |
| :------------------------------------------ | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [listNonWorkingDays](#listnonworkingdays)   | Lists all one-time non working days, such as holidays. It does not lists the non working weekdays, such as each Saturday, Sunday. For listing the weekends, the `/api/v3/days` endpoint should be used. All days from current year are returned by default. |
| [createNonWorkingDay](#createnonworkingday) | **(NOT IMPLEMENTED)** Marks a day as being a non-working day. Note: creating a non-working day will not affect the start and finish dates of work packages but will affect their duration.                                                                  |
| [viewNonWorkingDay](#viewnonworkingday)     | Returns the non-working day information for a given date.                                                                                                                                                                                                   |
| [updateNonWorkingDay](#updatenonworkingday) | **(NOT IMPLEMENTED)** Update the non-working day information for a given date.                                                                                                                                                                              |
| [deleteNonWorkingDay](#deletenonworkingday) | **(NOT IMPLEMENTED)** Removes the non-working day at the given date. Note: deleting a non-working day will not affect the start and finish dates of work packages but will affect their duration.                                                           |
| [listWeekDays](#listweekdays)               | Lists week days with work schedule information.                                                                                                                                                                                                             |
| [updateWeekDays](#updateweekdays)           | **(NOT IMPLEMENTED)** Update multiple week days with work schedule information.                                                                                                                                                                             |
| [viewWeekDay](#viewweekday)                 | View a week day and its attributes.                                                                                                                                                                                                                         |
| [updateWeekDay](#updateweekday)             | **(NOT IMPLEMENTED)** Makes a week day a working or non-working day. Note: changing a week day working attribute will not affect the start and finish dates of work packages but will affect their duration attribute.                                      |
| [listDays](#listdays)                       | Lists days information for a given date interval. All days from the beginning of current month to the end of following month are returned by default.                                                                                                       |
| [viewDay](#viewday)                         | View the day information for a given date.                                                                                                                                                                                                                  |

## listNonWorkingDays

Lists all one-time non working days, such as holidays. It does not lists the non working weekdays, such as each Saturday, Sunday. For listing the weekends, the `/api/v3/days` endpoint should be used. All days from current year are returned by default.

- HTTP Method: `GET`
- Endpoint: `/api/v3/days/non_working`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| :------ | :----- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + date: the inclusive date interval to scope days to look up. When unspecified, default is from the beginning to the end of current year. Example: `{ "date": { "operator": "\<\>d", "values": ["2022-05-02","2022-05-26"] } }` would return days between May 5 and May 26 2022, inclusive. |

**Return Type**

`NonWorkingDayCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## createNonWorkingDay

**(NOT IMPLEMENTED)** Marks a day as being a non-working day. Note: creating a non-working day will not affect the start and finish dates of work packages but will affect their duration.

- HTTP Method: `POST`
- Endpoint: `/api/v3/days/non_working`

**Parameters**

| Name | Type                                                  | Required | Description       |
| :--- | :---------------------------------------------------- | :------- | :---------------- |
| body | [NonWorkingDayModel](../models/NonWorkingDayModel.md) | ❌       | The request body. |

**Return Type**

`NonWorkingDayModel`

**Example Usage Code Snippet**

```mcp

```

## viewNonWorkingDay

Returns the non-working day information for a given date.

- HTTP Method: `GET`
- Endpoint: `/api/v3/days/non_working/{date}`

**Parameters**

| Name | Type   | Required | Description                                                 |
| :--- | :----- | :------- | :---------------------------------------------------------- |
| date | string | ✅       | The date of the non-working day to view in ISO 8601 format. |

**Return Type**

`NonWorkingDayModel`

**Example Usage Code Snippet**

```mcp

```

## updateNonWorkingDay

**(NOT IMPLEMENTED)** Update the non-working day information for a given date.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/days/non_working/{date}`

**Parameters**

| Name | Type                                                  | Required | Description                                                 |
| :--- | :---------------------------------------------------- | :------- | :---------------------------------------------------------- |
| body | [NonWorkingDayModel](../models/NonWorkingDayModel.md) | ❌       | The request body.                                           |
| date | string                                                | ✅       | The date of the non-working day to view in ISO 8601 format. |

**Return Type**

`NonWorkingDayModel`

**Example Usage Code Snippet**

```mcp

```

## deleteNonWorkingDay

**(NOT IMPLEMENTED)** Removes the non-working day at the given date. Note: deleting a non-working day will not affect the start and finish dates of work packages but will affect their duration.

- HTTP Method: `DELETE`
- Endpoint: `/api/v3/days/non_working/{date}`

**Parameters**

| Name | Type   | Required | Description                                                 |
| :--- | :----- | :------- | :---------------------------------------------------------- |
| date | string | ✅       | The date of the non-working day to view in ISO 8601 format. |

**Example Usage Code Snippet**

```mcp

```

## listWeekDays

Lists week days with work schedule information.

- HTTP Method: `GET`
- Endpoint: `/api/v3/days/week`

**Return Type**

`WeekDayCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## updateWeekDays

**(NOT IMPLEMENTED)** Update multiple week days with work schedule information.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/days/week`

**Parameters**

| Name | Type                                                                    | Required | Description       |
| :--- | :---------------------------------------------------------------------- | :------- | :---------------- |
| body | [WeekDayCollectionWriteModel](../models/WeekDayCollectionWriteModel.md) | ❌       | The request body. |

**Return Type**

`WeekDayCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## viewWeekDay

View a week day and its attributes.

- HTTP Method: `GET`
- Endpoint: `/api/v3/days/week/{day}`

**Parameters**

| Name | Type   | Required | Description                                         |
| :--- | :----- | :------- | :-------------------------------------------------- |
| day  | number | ✅       | The week day from 1 to 7. 1 is Monday. 7 is Sunday. |

**Return Type**

`WeekDayModel`

**Example Usage Code Snippet**

```mcp

```

## updateWeekDay

**(NOT IMPLEMENTED)** Makes a week day a working or non-working day. Note: changing a week day working attribute will not affect the start and finish dates of work packages but will affect their duration attribute.

- HTTP Method: `PATCH`
- Endpoint: `/api/v3/days/week/{day}`

**Parameters**

| Name | Type                                                | Required | Description                                         |
| :--- | :-------------------------------------------------- | :------- | :-------------------------------------------------- |
| body | [WeekDayWriteModel](../models/WeekDayWriteModel.md) | ❌       | The request body.                                   |
| day  | number                                              | ✅       | The week day from 1 to 7. 1 is Monday. 7 is Sunday. |

**Return Type**

`WeekDayModel`

**Example Usage Code Snippet**

```mcp

```

## listDays

Lists days information for a given date interval. All days from the beginning of current month to the end of following month are returned by default.

- HTTP Method: `GET`
- Endpoint: `/api/v3/days`

**Parameters**

| Name    | Type   | Required | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| :------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| filters | string | ❌       | JSON specifying filter conditions. Accepts the same format as returned by the [queries](https://www.openproject.org/docs/api/endpoints/queries/) endpoint. Currently supported filters are: + date: the inclusive date interval to scope days to look up. When unspecified, default is from the beginning of current month to the end of following month. Example: `{ "date": { "operator": "\<\>d", "values": ["2022-05-02","2022-05-26"] } }` would return days between May 5 and May 26 2022, inclusive. + working: when `true`, returns only the working days. When `false`, returns only the non-working days (weekend days and non-working days). When unspecified, returns both working and non-working days. Example: `{ "working": { "operator": "=", "values": ["t"] } }` would exclude non-working days from the response. |

**Return Type**

`DayCollectionModel`

**Example Usage Code Snippet**

```mcp

```

## viewDay

View the day information for a given date.

- HTTP Method: `GET`
- Endpoint: `/api/v3/days/{date}`

**Parameters**

| Name | Type   | Required | Description                                                 |
| :--- | :----- | :------- | :---------------------------------------------------------- |
| date | string | ✅       | The date of the non-working day to view in ISO 8601 format. |

**Return Type**

`DayModel`

**Example Usage Code Snippet**

```mcp

```

<!-- This file was generated by liblab | https://liblab.com/ -->
