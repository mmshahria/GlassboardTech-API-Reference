Get an Investment Fund Legal Document for a specific Entity,of the document type that you specify.Supply the unique path parameters `entityId` and `documentType` in the correct canonical path to retrieve Investment Fund Legal Document for the specified subscription.

# Attributes

<strong>id<strong> `string`

The unique internal identifier to locate this legal document.

<strong>ownerId<strong> `string`

The unique owner identifier for this document.

<strong>tenantId<strong> `string`

A unique identifier used for API authentication and authorization.

<strong>name<strong> `string`

The name of the document. Constraints `2 to 1024 chars`.

<strong>size<strong> `string`

The size in bytes of the file object.The size of the document's content in bytes. 

<strong>type<strong> `string`

The type of the document.

<strong>key<strong> `string`



<strong>thumbnail<strong> `string`

A short-lived link to the document's thumbnail, if available.A thumbnail for the file, if available. 

<strong>lastModified<strong> `string`

The last time the document was modified.

<strong>createdAt<strong> `date-time`

The time at which the document was created.

<strong>updatedAt<strong> `date-time`

The time at which the document was updated.

<strong>deletedAt<strong> `date-time`

The time at which the document was deleted.

<strong>isDeleted<strong> `boolean`

Has the value _true_ if this particular document is deleted; otherwise, the value _false_.

<strong>generating<strong> `boolean`



<strong>isPublic<strong> `boolean`

Has the value _true_ if this particular document is Public; otherwise, the value _false_.

<strong>additionalProperties<strong> `object`

JSON object descriptor that encloses a set of `key:value` pairs representing additional properties for this document.This can be useful for storing additional information in a structured format.The enclosed data body must be in JSON format.