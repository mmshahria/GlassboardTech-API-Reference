Retrieves the bank account information for a valid identifier. Supply the unique `entityId` in the path parameter, and this endpoint will respond to the corresponding bank account details based on the authentication that was used to make the request.


# Attributes

<strong>id<strong> `string`

The unique internal identifier to locate this bank account.

<strong>counterpartyId<strong> `string`

Counter party identifier for banking provider.

<strong>providerMeta<strong> `object`

JSON Object descriptor that encloses the provider meta details.

<strong>bankName<strong> `string`

Name of the bank associated with the <strong>routingNumber</strong> for this bank account.

<strong>accountNumber<strong> `string`

Bank account number associated with this bank account.

<strong>routingNumber<strong> `string`

The routing transit number associated with this bank account.

<strong>accountName<strong> `string`

The name of the person or business that owns the bank account.The name of the person who holds the bank account.

<strong>isDefaultForDistributions<strong> `boolean`

Has the value _true_ if this bank account is default for distributions, or the value _false_ if it's not.

> Default Distribution means payment in a lump sum distribution.

<any-key>: any

Place holder for <any-key>