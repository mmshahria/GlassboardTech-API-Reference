Returns the details of a banking beneficiary for a valid identifier.Supply the unique `id` in the path parameter and this endpoint will return the corresponding banking beneficiary details.

>A beneficiary is a person you're sending money to - also known as a recipient. A beneficiary can be a person or a business entity. A beneficiary bank is a bank which holds the account you're sending money.

# Attributes

<strong> id </strong> `string`

A unique internal identifier of the banking beneficiary.

<strong> ownerId* </strong> `string`

A unique identifier of the owner.

<strong> tenantId* </strong> `string`

A unique identifier used for API authentication and authorization.

>Tenant refers to the end user of this API and It's required for identity and access management.

<strong> name </strong> `string`

The name of the banking beneficiary.

<strong> phone </strong> `string`

The phone number of the banking beneficiary.

<strong> email </strong> `string`

The Email address of the beneficiary.

<strong> serviceObjectId </strong> `string`

Counter party identifier for banking provider

<strong> createdAt </strong> `date-time`

Describes the date & time at which the banking beneficiary was created. Data formatted as `1970-01-01T00:00:00.000Z`

<strong> updatedAt </strong> `date-time`

Describes the date & time at which the banking beneficiary was last updated. Data formatted as `1970-01-01T00:00:00.000Z`.

<strong>isDeleted</strong> `boolean`

Has the value _true_ if the banking beneficiary is deleted; otherwise, the value _false_.