
Returns the details of a linked bank account for a valid identifier.In the request supply the unique `accountId` and this endpoint will return the corresponding bank account details.

# Attributes

<strong> id </strong> `string`

A unique identifier of the account that the bank account is associated with.

<strong> ownerId </strong> `string`

A unique identifier of the owner that the bank account is associated with.


<strong> status </strong> `string`

Describes the bank accounts’s current status. 

For bank accounts, possible values are `DRAFT┃IN-PROVISIONING┃OPEN┃IN CLOSING┃CLOSED`.

<strong> tenantId </strong> `string`

A unique identifier used for API authentication and authorization. Can be useful for this API's end users.

<strong> createdAt </strong> `date-time`

Describes the date & time at which the bank account was created. Data formatted as `1970-01-01T00:00:00.000Z`

<strong> updatedAt </strong> `date-time`

Describes the date & time at which the bank account was last updated. Data formatted as `1970-01-01T00:00:00.000Z`.

<strong> accountNumber </strong> `string`

An account number is a unique code assigned to the account owner for identifying a specific bank account holder.

<strong> routingNumber </strong>r `string`

The routing transit number for the bank account.

<strong> accountName </strong> `string`

The name of the person or business that owns the bank account.

<strong> bankName </strong> `string`

Name of the bank associated with the <strong>routingNumber</strong>

<strong> bankAddress </strong> `string`

Returns the bankAddress of the specified bank.

<strong>bankContact </storng> `object` 

Returns the bankContact details. Data returned as JSON object.

*   <strong> name </strong> `string`</br> The name of the person or business that owns the bank account.
*   <strong> phone </strong> `string`</br> The phone number of the person or business that owns the bank account.
*   <strong> email </strong> `string`</br> The email address of the person or business that owns the bank account.

<strong> swiftCode </strong> `string`

SWIFT code for the specified bank account. A SWIFT code identifies the country, bank and branch to which an account is registered.

<strong> tenantIdForFees </strong> `string`

Use case Undefined.

<strong>tenantIdForBlueSky </strong> `string`

Use case Undefined.

`any-key`: `any value`

Placeholder for set of `key:value` pair.