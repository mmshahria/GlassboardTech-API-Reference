
Retrieves the list of linked bank accounts for the current user. In the request supply values of the query string parameters  `perPage` `page` and this endpoint will return the corresponding list of bank accounts details.


# Attributes

<strong> data </strong> `[object]`

An array list of bank accounts. Here, the data attribute is used as a simple descriptor for the returned array list object that encloses the list of bank accounts for the current user.

* <strong> id </strong> `string` </br> A unique identifier of a linked bank account that is associated with the current user.

* <strong> status </strong> `string` </br> Current status of a linked bank account for the current user.

* <strong> accountNumber </strong> `string` </br> Account number for a linked bank account. 
  > An account number is a unique code assigned to the account owner for identifying a specific bank account holder.

* <strong> routingNumber </strong> `string` </br>The routing transit number for a linked bank account.

* <strong> accountName </strong> `string` </br> The name of the person or business for a linked bank account.

* <strong> bankName </strong> `string` </br> Name of the bank associated with the <strong>routingNumber</strong> for a linked bank account.

<strong>page </strong> `number`

The number of page returned for the API call. This attribute can be used as a query string parameter to specify the number of bank accounts the API call shall return.

<strong>perPage </strong> `number`

The  total count of the list of bank accounts returned per page. This attribute can be used as a query string parameter to specify the number of bank accounts the API call shall return.

<strong>totalCount </strong> `number`

Total count of the bank accounts list the API call returned.