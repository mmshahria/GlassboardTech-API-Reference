Initiates a request to create a new ACH banking beneficiary for the given account belonging to the authenticated user. Supply the `key:value` pairs that are required for an ACH banking beneficiary in the request body to execute an ACH banking beneficiary create operation. Data in the request body should follow the JSON data formatting.

# Parameters

<strong>name<strong> `string`

The name chosen by the user for this beneficiary.

<strong>email<strong> `string`

Email address associated with the beneficiary.

<strong>phone<strong> `string`

Phone number associated with the beneficiary.

<strong>nameOnAccount*<strong> `string`

The full name of the person or business on the bank account.

<strong>accountNumber*<strong> `string`

Account number for a linked bank account for this beneficiary. 
> An account number is a unique code assigned to the account owner for identifying a specific bank account holder.

<strong>routingNumber*<strong> `string`

The routing transit number for the bank account.

<strong>accountType*<strong> `string`

Type of bank account for this beneficiary.
