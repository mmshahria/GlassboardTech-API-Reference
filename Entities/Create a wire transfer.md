Initiates a request to create an  Outgoing Wire Transaction. Supply the unique `accountId` in the path parameter to execute an Outgoing Wire Transaction create operation. Data in the request body should follow the JSON data formatting.

> The Outgoing Wire Transfer transaction is used to transfer funds from managed accounts to an external bank account.

# Parameter

<strong>amount*<strong> `number`


Constraints: Min 0.01
<strong>beneficiaryId*<strong> `string`


Constraints: Min 1 chars
<strong>instructions*<strong> `string`


Constraints: Min 1 chars
<strong>scheduledForDate<strong> `date`

