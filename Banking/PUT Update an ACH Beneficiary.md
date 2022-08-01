Update existing ACH beneficiary records to the current user's data source based on the input parameters `key:value` pair that are supplied in the JSON format. Supply the unique `beneficiaryId` in the path parameter to execute an update operation to a specific ACH beneficiary resource for the current user.

# Parameters

<strong>name<strong> `string`

The name chosen by the user for this beneficiary.

<strong>email<strong> `string`

Email address associated with the beneficiary.

<strong>phone<strong> `string`

Phone number associated with the beneficiary.

<strong>nameOnAccount*<strong> `string`

The full name of the person or business associated with the bank account.

<strong>accountNumber*<strong> `string`

Account number for a linked bank account for this beneficiary. 

> An account number is a unique code assigned to the account owner for identifying a specific bank account holder.

<strong>routingNumber*<strong> `string`

The routing transit number for the bank account.The routing transit number for a linked bank account for this ACH transaction.

<strong>accountType*<strong> `string`

Type of bank account for this beneficiary.