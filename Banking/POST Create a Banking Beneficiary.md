Initiates a request to create a new banking beneficiary for the given account belonging to the authenticated user.Supply the `key:value` pairs that are required for a banking beneficiary in the request body to execute a banking beneficiary create operation.Data in the request body should follow the JSON data formatting.

> A beneficiary is a bank-authorized account that will receive a payment or transfer.Each beneficiary is associated with a particular account, which allows that account to transmit funds to that beneficiary.

# Parameters

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