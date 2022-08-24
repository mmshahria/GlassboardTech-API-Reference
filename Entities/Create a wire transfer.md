Initiates a request to create an  Outgoing Wire Transaction. Supply the unique `accountId` in the path parameter to execute an Outgoing Wire Transaction create operation. Data in the request body should follow the JSON data formatting.

# Parameter

<strong>amount*<strong> `number`

A positive integer representing how much to transfer.Constraints `Min 0.01`.

<strong>beneficiaryId*<strong> `string`

The unique beneficiary identifier for this wire transfer.Constraints `Min 1 chars`

<strong>instructions*<strong> `string`

Additional instructions for the Wire transaction.Constraints `Min 1 chars`.

<strong>scheduledForDate<strong> `date`

Scheduled Transaction date for this wire transfer.