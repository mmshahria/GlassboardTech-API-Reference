
Retrieves the list of linked bank accounts for the current user. In the request supply, the values of the query string parameters  `perPage` `page` and this endpoint will return the corresponding list of bank account details.


# Attributes

<strong> data </strong> `[object]`

An array list of bank accounts. Here, the data attribute is used as a simple descriptor for the returned array list object that encloses the list of bank accounts for the current user.

* <strong> id </strong> `string` </br> A unique internal identifier to locate the bank account.

* <strong> status </strong> `string` </br> Current status of the bank account.Allowed values are `DRAFT┃IN-PROVISIONING┃OPEN┃IN CLOSING┃CLOSED`.

* <strong> accountNumber </strong> `string` </br>.Bank account number associated with this bank account.
  > An account number is a unique code assigned to the account owner for identifying a specific bank account holder.

* <strong> routingNumber </strong> `string` </br>The routing transit number associated with this bank account.

* <strong> accountName </strong> `string` </br> The name of the person or business that owns the bank account.

* <strong> bankName </strong> `string` </br> Name of the bank associated with the <strong>routingNumber</strong> for this bank account.

<strong>page </strong> `number`

The total number of pages returned for the API call. This can be used as a query string parameter.

<strong>perPage </strong> `number`

The total count of the list of bank accounts returned per page. This attribute can be used as a query string parameter to specify the number of bank accounts the API call shall return.

<strong>totalCount </strong> `number`

The total count of the bank accounts lists the API call returned.