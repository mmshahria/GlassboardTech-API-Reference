Retrieves the list of files for the current user. In the request supply, the values of the query string parameters  `perPage` `page` and this endpoint will return the corresponding list of files.

# Attributes

<strong> data </strong> `[object]`

An array list of files. Here, the data attribute is used as a simple descriptor for the returned array list object that encloses the list of files for the current user.

<strong>id<strong> `string`

A unique identifier to locate this file./The unique identifier that represents a file.

<strong>ownerId<strong> `string`

The unique owner identifier for this file.

<strong>tenantId<strong> `string`

A unique identifier used for API authentication and authorization.

<strong>name<strong> `string`

The name of the file. Constraints `2 to 1024 chars`.

<strong>size<strong> `string`

The size in bytes of the file object.The size of the file's content in bytes. 

<strong>type<strong> `string`

The type of the file.

<strong>key<strong> `string`


<strong>thumbnail<strong> `string`

A short-lived link to the file's thumbnail, if available.A thumbnail for the file, if available. 

<strong>lastModified<strong> `string`

The last time the file was modified by anyone.

<strong>createdAt<strong> `date-time`

The time at which the file was created.

<strong>updatedAt<strong> `date-time`

The time at which the file was updated.

<strong>deletedAt<strong> `date-time`

The time at which the file was deleted.

<strong>isDeleted<strong> `boolean`

Has the value _true_ if this particular file is deleted; otherwise, the value _false_.

<strong>generating<strong> `boolean`


<strong>isPublic<strong> `boolean`

Has the value _true_ if this particular file is Public; otherwise, the value _false_.

<strong>additionalProperties<strong> `object`

JSON object descriptor that encloses a set of `key:value` pairs representing additional properties for this file.This can be useful for storing additional information in a structured format.  The enclosed data body must be in JSON format.

<strong>page </strong> `number`

The total number of pages returned for the API call. This can be used as a query string parameter.

<strong>perPage </strong> `number`

The total count of the list of files returned per page. This attribute can be used as a query string parameter to specify the number of files the API call shall return.

<strong>totalCount </strong> `number`

The total count of the files lists the API call returned.