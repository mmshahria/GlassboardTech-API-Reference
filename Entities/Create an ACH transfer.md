Use the Create an ACH Transfer endpoint to place the transfer into the queue for processing.Supply the unique path parameters `entityId` in the correct canonical path to place the transfer into the queue for processing.

> ACH transfers are electronic, bank-to-bank money transfers processed through the Automated Clearing House (ACH) Network.

# Parameter

<strong>amount*<strong> `number`

A positive integer representing how much to transfer.Constraints `Min 0.01`.

<strong>beneficiaryId*<strong> `string`

The unique beneficiary identifier for this wire transfer.Constraints `Min 1 chars`.