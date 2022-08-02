Use the Create a Reverse ACH Transfer endpoint to add a reverse transfer to the queue for processing, if the following conditions are met:


* The Subscription must be in a funded state, either from an on or off-platform transaction.
* The Entity of the Deal for the Subscription must have an active bank account, with the funds available for the refund.
* The Subscription must not have been refunded before. Only One (1) refund is allowed per Subscription.
* All On-Platform Transactions for the Subscription must be Settled (In a 'SENT' state).
  
Supply the unique path parameters `subscriptionId` in the correct canonical path to add a reverse transfer to the queue for processing.

The following properties must be supplied if the Subscription was funded with an off-platform method, or with multiple incoming ACH transactions:

`routing`,`account`,`typeOfAccount`,`nameOnAccount`.


The `ownerId` of the Deal or Subscription must match the `userId` of the current API user.


# Parameters

<strong>routing<strong> `string`

The routing transit number associated with the bank account.

<strong>account<strong> `string`

Account number associated with the bank account for this reverse ACH transfer. 

<strong>typeOfAccount<strong> `enum`

Type of the bank account. Allowed `enum` values are `CHECKING┃SAVINGS`.

<strong>nameOnAccount<strong> `string`

The name of the person or business on the bank account.

<strong>amount<strong> `number`

The amount that will be refunded.If omitted, will attempt a refund the whole subscription amount. Constraints `Min 0.01┃ multiple of 0.01`