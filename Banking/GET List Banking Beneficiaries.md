Retrieves the list of Banking Beneficiaries for the current user. In the request supply, the values of the query string parameters  `perPage` `page` and this endpoint will return the corresponding list of Banking Beneficiaries' details.


# Attributes

<strong> data </strong> `[object]`

An array list of Banking Beneficiaries. Here, the data attribute is used as a simple descriptor for the returned array list object that encloses the list of Banking Beneficiaries for the current user.

<strong>id<strong> `string`

The unique internal identifier to locate a particular banking beneficiary.

<strong>ownerId*<strong> `string`

The unique internal owner identifier for this beneficiary.

<strong>tenantId*<strong> `string`

A unique identifier used for API authentication and authorization.

<strong>name<strong> `string`

Full name of the banking beneficiary.

<strong>phone<strong> `string`

The phone number of the banking beneficiary.

<strong>email<strong> `string`

The Email address of the beneficiary.

<strong>serviceObjectId<strong> `string`

Counter party identifier for banking provider

<strong>createdAt<strong> `date-time`

Timestamp for the creation of this banking beneficiary.

<strong>updatedAt<strong> `date-time`

Timestamp for the last update record for this beneficiary.

<strong>isDeleted<strong> `boolean`

Has the value _true_ if this particular banking beneficiary is deleted; otherwise, the value _false_.

<strong>page </strong> `number`

The total number of pages returned for the API call. This can be used as a query string parameter.

<strong>perPage </strong> `number`

The total count of the list of Banking Beneficiaries returned per page. This attribute can be used as a query string parameter to specify the number of Banking Beneficiaries the API call shall return.

<strong>totalCount </strong> `number`

The total count of the Banking Beneficiaries lists the API call returned.