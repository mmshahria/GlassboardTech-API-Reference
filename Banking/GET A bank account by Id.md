Returns the details of a linked bank account for a valid identifier.Supply the unique `accountId` in the path parameter and this endpoint will return the corresponding bank account details.

# Attributes

<strong> id </strong> `string`

The internal identifier to locate the bank account.

<strong> ownerId </strong> `string`

The unique identifier of the user who owns this object.

<strong> status </strong> `string`

Describes the bank accounts’ current status. Allowed values are `DRAFT┃IN-PROVISIONING┃OPEN┃IN CLOSING┃CLOSED`.

<strong> tenantId </strong> `string`

A unique identifier used for API authentication and authorization.

>Tenant refers to the end user of this API and It's required for identity and access management.

<strong> createdAt </strong> `date-time`

Describes the date & time at which the bank account was created. Data formatted as `1970-01-01T00:00:00.000Z`.

<strong> updatedAt </strong> `date-time`

Describes the date & time at which the bank account was last updated. Data formatted as `1970-01-01T00:00:00.000Z`.

<strong> accountNumber </strong> `string`

Bank account number associated with this bank account.

<strong> routingNumber </strong>r `string`

The routing transit number associated with this bank account.

<strong> accountName </strong> `string`

The name of the natural person or business that owns the bank account.

<strong> bankName </strong> `string`

Name of the bank associated with the <strong>routingNumber</strong> for this bank account.

<strong> bankAddress </strong> `string`

The physical address of the bank. 

<strong>bankContact </storng> `object` 

JSON object descriptor that encloses a set of `key:value` pairs representing bank contact details. 

*   <strong> name </strong> `string`</br> Bank Contact Name(person).
*   <strong> phone </strong> `string`</br> Bank Contact Phone number.
*   <strong> email </strong> `string`</br> Bank Contact Email address.

<strong> swiftCode </strong> `string`

SWIFT code for the specified bank account. A SWIFT code identifies the country, bank and branch to which an account is registered.

<strong> tenantIdForFees </strong> `string`



<strong>tenantIdForBlueSky </strong> `string`



`any-key`: `any value`

Placeholder for set of `key:value` pair.