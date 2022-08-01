Retrieves the list of transactions details of a bank account for a valid identifier. In the path parameter, supply the unique `bankAccountId`, and this endpoint will return the associated bank account's transactions list. Data returned as JSON _array_ object.


# Attributes

<strong>amount</strong> `number`

Transaction amount that is moving in or out of the bank account.Note that transactions with type `hold` have an amount, but they do not change the balance.Constraints `Min 0.01┃ multiple of 0.01`.

<strong>date</strong> `date`

The date of a specific transaction that occurred .Data formatted as _YYYY-MM-DD_.

<strong>desc</strong> `string`

Description or reference of a specific transaction if specified at the time of creating a transaction.

<strong>book_id</strong> `string┃null`

The unique identifier of the Booking Transfer that originated in this transaction.Returned value can be `null` if it's not a book transfer.

> A unique identifier `book-id` refers to the object that contains the details of fund transfer between two accounts of the same bank in Payments. 

<strong>type</strong> `enum┃null`

The nature of the transaction. _Data-type_ `enum` consists of predefined banking transaction type values `charge | deposit | hold | hold_release | interest | reversal | withdrawal` or `null`.For _incoming ACH transaction_ type will be `deposit` and for _outgoing ACH transaction_ type will be `withdrawal`.

<strong> summary</strong> `string`

Summary description of the transaction.

<strong>balance</strong> `string`

Account balance immediately after transaction. Transactions of type `hold` do not affect the balance.Constraints `Min 1 chars`.

> Account Balance in a transaction details is the remaining total amount of money after being credited or debited based on the type of transaction in the specified bank account.

<strong>id</strong> `string`

A unique identifier for this transaction.

<strong>ach_id</strong> `string┃null`

A unique identifier of the ACH transaction.The value can be `null` if it's not an ACH transaction. 

> ACH (Automated Clearing House) is a network used for electronically transfer money between bank accounts across the United States.

<strong>wire_id</strong> `string┃null`

A unique identifier of the wire transaction. The value can be `null` if it's not wire transaction. 

> A wire transfer can be made from one bank account to another bank account, or through a transfer of cash at a cash office.

<strong>wire</strong> `string┃null`

For wire transactions, the Fedwire description, if any. Otherwise the value is `null`.

<strong>fingerprint</strong> `string`

A unique fingerprint for this transaction.