Initiates a request to create an ACH transaction. Supply the `key:value` pairs that are required for an ACH transaction in the request body. Data in the request body should follow the JSON data formatting.

# Parameters

<strong>amount*<strong> `number`

Transaction amount that is moving in or out of the bank account.Constraints `Min 0.01┃ multiple of 0.01`.

<strong>routing*<strong> `string`

The routing transit number for a linked bank account for this ACH transaction.

<strong>account*<strong> `string`

Account number for a linked bank account for this ACH transaction. 
> An account number is a unique code assigned to the account owner for identifying a specific bank account holder.

<strong>typeOfAccount*<strong> `enum`

Type of bank account for this ACH transaction.Allowed enum values are `CHECKING┃SAVINGS`.

<strong>accountId*<strong> `string`

Unique bank account identifier for this ACH transaction.

<strong>subAccountId*<strong> `string`

Unique Sub bank account identifier,if any.

<strong>direction*<strong> `enum`

Specifies whether the recipient account is to be credited or debited.Allowed enum values are `CREDIT┃DEBIT`.

<strong>nameOnAccount<strong> `string`

The full name of the person or business on the bank account.