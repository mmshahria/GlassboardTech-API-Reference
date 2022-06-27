Retrieves the list of transactions details of a bank account for a valid identifier. In the request, supply the unique `bankAccountId`, and this endpoint will return the associated bank account's transactions list. Data returned as JSON _array_ object.

> Transactions list represents the details of any money that moves in or out of a specified bank account.

<strong>amount</strong> `number`

An amount that is moving in or out of the bank account. In a transaction, the amount cannot be less than _0.01_.

<strong>date</strong> `date`

The date of a specific transaction that occurred . Data formatted as _YYYY-MM-DD_.

<strong>desc</strong> `string`

Description or reference of a specific transaction if specified at the time of creating a transaction.

<strong>book_id</strong> `string┃null`

A unique identifier `book-id` refers to the object that contains the details of fund transfer between two accounts of the same bank in Payments. Returned value can be `null` if it's not a book transfer.

<strong>type</strong> `enum┃null`

The nature of the transaction. _Data-type_ `enum` consists of predefined banking transaction type values (`charge | deposit | hold | hold_release | interest | reversal | withdrawal`).

For _incoming ACH transaction_ type will be `deposit` and for _outgoing ACH transaction_ type will be `withdrawal`


<strong> summary</strong> `string`

Summary description of the transaction.

<strong>balance</strong> `string`

Balance in a transaction details is the remaining total amount of money after being credited or debited based on the type of transaction in the specified bank account.

<strong>id</strong> `string`

A unique identifier for the transaction. Can be useful to retrieve this particular transaction.

<strong>ach_id</strong> `string┃null`

A unique identifier for ACH transaction details. This can be useful to retrieve associated ACH transaction details. The value can be `null` if it's not an ACH transaction. 

> ACH (Automated Clearing House) is a network used for electronically transfer money between bank accounts across the United States.

<strong>wire_id</strong> `string┃null`

A unique identifier for wire transaction details. This can be useful to retrieve associated wire transaction details. The value can be `null` if it's not wire transaction. 

> A wire transfer can be made from one bank account to another bank account, or through a transfer of cash at a cash office.


<strong>wire</strong> `string┃null`

For wire transactions, the Fedwire description, if any. Otherwise the value is `null`.

<strong>fingerprint</strong> `string`

Uniquely identifies a specific transaction. This should be unique for each transaction.