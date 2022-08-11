Retrieves the real-time bank account balance,for a valid identifier.Supply the unique `entityId` in the path parameter, and this endpoint will respond to the corresponding bank account balacne based on the authentication that was used to make the request.

# Parameters

<strong>balance<strong> `number`

The total amount of money that is currently in the account, including any pending transactions.

> Account balance is made up of all posted credit and debit transactions.

<strong>availableBalance<strong> `number`
The amount of funds available to be withdrawn from the account, as determined by the financial institution.

> Available balance is the current balance minus any holds or debits that haven’t yet been posted to the account. The two balances are likely the same if there are no holds or pending transactions.