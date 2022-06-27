Returns the details of a banking beneficiary for a valid identifier.In the request supply the unique `id` and this endpoint will return the corresponding banking beneficiary details.Data returned as JSON object.

>A beneficiary is the person you're sending money to - also known as a recipient. A beneficiary can be a person, or a business entity. A beneficiary bank is the bank which holds the account you're sending money to.

# Attributes

<strong> id </strong> `string`

A unique identifier of the banking beneficiary.

<strong> ownerId* </strong> `string`

A unique identifier of the owner that the bank account is associated with.

<strong> tenantId* </strong> `string`

A unique identifier used for API authentication and authorization. Can be useful for this API's end users.

<strong> name </strong> `string`

The name of the banking beneficiary.

<strong> phone </strong> `string`

The phone number of the banking beneficiary.

<strong> email </strong> `string`

The Email address of the beneficiary.

<strong> serviceObjectId </strong> `string`



<strong> createdAt </strong> `date-time`

Describes the date & time at which the banking beneficiary was created. Data formatted as `1970-01-01T00:00:00.000Z`

<strong> updatedAt </strong> `date-time`

Describes the date & time at which the banking beneficiary was last updated. Data formatted as `1970-01-01T00:00:00.000Z`.

providerMeta `object` 



<strong>isDeleted</strong> `boolean`

Has the value _true_ if a specified banking beneficiary is deleted otherwise the value _false_.