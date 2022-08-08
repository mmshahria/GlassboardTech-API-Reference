Retrieves an existing file for a valid identifier. Supply the unique `fileId` in the path parameter, and this endpoint will return the corresponding file.

# Attributes

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