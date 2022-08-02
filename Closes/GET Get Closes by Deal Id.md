Retrieves the details of existing closes associated with a deal for a valid identifier. Supply the unique `dealId` in the path parameter, and this endpoint will return the corresponding closes details. Data returned as JSON _array_ object.

# Attributes

<strong>data<strong> `object`
JSON object descriptor that encloses the list of closes served from the database.

<strong>page </strong> `number`

The total number of pages returned for the API call. This can be used as a query string parameter.

<strong>perPage </strong> `number`

The total count of the list of closes returned per page. This attribute can be used as a query string parameter to specify the number of closes the API call shall return.

<strong>totalCount </strong> `number`

The total count of the closes lists the API call returned.
