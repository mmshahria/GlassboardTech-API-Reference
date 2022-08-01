Update existing banking beneficiary records to the current user's data source based on the input parameters `key:value` pair that are supplied in the JSON format. Supply the unique `beneficiaryId` in the path parameter to execute an update operation to a specific beneficiary resource for the current user.

# Parameters

<strong>id<strong> `string`

The internal identifier of the banking beneficiary.

<strong>ownerId<strong> `string`

A unique identifier of the owner.

<strong>tenantId<strong> `string`

A unique identifier used for API authentication and authorization.

<strong>serviceObjectId<strong> `string`




<strong>name*<strong> `string`

The name chosen by the user for this beneficiary.

<strong>email<strong> `string`

Email address associated with the beneficiary.

<strong>phone<strong> `string`

Phone number associated with the beneficiary.

<strong>routingNumber*<strong> `string`

The routing transit number for the bank account.

<strong>accountNumber*<strong> `string`

The account number for the beneficiary.

<strong>bankName*<strong> `string`

Name of the bank associated with the <strong>routingNumber</strong>.

<strong>bankAddress*<strong> `object`

JSON object descriptor that encloses the bank address details.

* <strong>street_1<strong> `string` </br> Street address line 1.
* <strong>street_2<strong> `string` </br> Street address line 2.
* <strong>city<strong> `string` </br> The city name.
* <strong>postal_code<strong> `string` </br> The postal code.
* <strong>region<strong> `string` </br> The region in which the bank is located.Constraints `Max 2 chars`.
* <strong>country<strong> `string` </br> The country in which the bank is located.Constraints `Max 2 chars`.

<strong>addressOnAccount*<strong> `object`

JSON object descriptor that encloses the details of address on Account.

* <strong>street_1<strong> `string` </br> Street address line 1.
* <strong>street_2<strong> `string` </br> Street address line 2.
* <strong>city<strong> `string` </br> The city name.
* <strong>postal_code<strong>: `string` </br> The postal code.
* <strong>region<strong> `string` </br> The region in which the bank account is located.Constraints `Max 2 chars`.
* <strong>country<strong> `string` </br> The country in which the bank account is located.Constraints `Max 2 chars`.

<strong>type*<strong> `string`