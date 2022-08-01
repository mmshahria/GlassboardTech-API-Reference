Initiates a request to create an  Outgoing Wire Transaction. Supply the unique `accountId` in the path parameter to execute an Outgoing Wire Transaction create operation. Data in the request body should follow the JSON data formatting.

> The Outgoing Wire Transfer transaction is used to transfer funds from managed accounts to an external bank account.

# Parameters

<strong>direction*<strong> `enum`

 The direction of the transaction from the perspective of the originating account. For Wire transactions, this can only be `CREDIT`.  Allowed enum value is `CREDIT`.

<strong>nameOnAccount*<strong> `string`

The Account Holder's name on the receiving account. Constraints `Min 1 chars`.

<strong>addressOnAccount*<strong> {


<strong>address1*<strong> `string`

Street Name Line 1.Constraints `2 to 1024 chars`.

<strong>address2<strong> `string`

Street Name Line 2. Constraints `Max 1024 chars`.

<strong>city*<strong> `string`

City of Address. Constraints `2 to 1024 chars`.
<strong>region*<strong> `string`

Region or State of Address.Constraints `2 to 1024 chars`.

<strong>postalCode*<strong> `string`

Postal Code: Postal (or ZIP) Code of Address.Constraints `2 to 1024 chars`

<strong>country*<strong> `enum`

Country: ISO 3166-1 Full Country name in ISO-639-1 (EN) Format

<strong>bankAddress*<strong> {


<strong>address1*<strong> `string`

Street Name Line 1.Constraints `2 to 1024 chars`

<strong>address2<strong> `string`

Street Name Line 2. Constraints `Max 1024 chars`.

<strong>city*<strong> `string`

City of Address.Constraints `2 to 1024 chars`.

<strong>region*<strong> `string`

Region or State of Address.Constraints `2 to 1024 chars`

<strong>postalCode*<strong> `string`

Postal (or ZIP) Code of Address.Constraints `2 to 1024 chars`.

<strong>country*<strong> `enum`

ISO 3166-1 Full Country name in ISO-639-1 (EN) Format

<strong>bankName*<strong> `string`

The Name of the receiving Bank. Constraints `Min 3 chars`.
<strong>account*<strong> `string`

The account number of the receiving account.Constraints `Min 1 chars`.

<strong>routing*<strong> `string`

The routing number of the receiving account. Constraints `Min 1 chars`.
<strong>instructions<strong> `string`

Additional instructions for the Wire. Limited to 140 characters. Constraints `Max 140 chars`

<strong>amount*<strong> `number`


