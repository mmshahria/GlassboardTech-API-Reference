Retrieves an specified company for a valid identifier for the current user. Supply the unique `companyId` and this endpoint will respond with the corresponding asset details for the current user.

<strong>name<strong> `string`
The name of the company.

<strong>website<strong> `string`
The website address of the company, if any.

<strong>email<strong> `string`
The contact email address of the company.

<strong>type<strong> `enum`
The registration type of the company in the platform. Expected enum values are `MASTER_ENTITY┃REGISTERED_AGENT┃MANAGER`.

<strong>entityType<strong> `string`
The legal entity type of the company. Examples are LLC, Sole proprietary. Predefined legal entity types are `LLC┃Corporation┃Non-Profit┃LP┃LLP┃GP┃DBA`.

<strong>phone<strong> `string`
The contact phone number of the company.

<strong>stateOfFormation<strong> `string`
The name of the state refers to the state where the company was registered.

<strong>address<strong> `object`
The contact Address object descriptor of the company.
* <strong>address1*<strong> `string` <br> Company contact address Line 1.

* <strong>address2</strong> `string` <br> Company contact address Line 2.

* <strong>city*<strong> `string` <br> City where the company registered.

* <strong>state<strong> `string` <br> State name where the company registered.

* <strong>postalCode*<strong> `string` <br> Current contact postal code of the company.

* <strong>country*<strong> `string` <br> The contact country name of the company.

<strong>taxContact<strong> `objcet`

The tax contact object descriptor that encloses the  validated tax contact information.

* <strong>type<strong> `enum` <br> The legal of type of the tax registration. Expected predefined values are `ssn┃itin┃ftin`.

* <strong>taxId<strong> `string` <br> The unique tax document identification number.

* <strong>address1<strong> `string` <br> Tax Contact Address 1.

* <strong>address2<strong> `string` <br> Tax Contact Address 2.

* <strong>city<strong> `string` <br> Tax Contact City name.

* <strong>state<strong> `string` <br> Tax Contact State name.

* <strong>postalCode<strong> `string` <br> Tax Contact Postal Code.

* <strong>country<strong> `string` <br> Tax Contact Country name.

<strong>createdAt<strong> `date-time` <br> The date and time stamp when the company information is first introduced in the platform.

<strong>updatedAt<strong> `date-time` <br> The date and time stamp when the company information last modified.

<strong>entityType<strong> `enum`

The Entity Type of company. Allowed: `LLC┃Corporation┃Non-Profit┃LP┃LLP┃GP┃DBA`

<strong>individuals<strong> [object]

Array object descriptor that encloses the detailed lists of each member associated with the company.

<strong>individual<strong> `objcet`

Object descriptor that encloses a single individual's details associated with the company. Such as individual owners of the Single-member LLC or sole proprietary business.

<strong>businesses<strong> `[object]`

Array object descriptor that encloses the detailed list of disparate businesses or fields of business the company has been associated with.

<strong>business<strong> `objcet`

Object descriptor that encloses the field of business the company is associated with.

<strong>ein<strong> `string`

The unique EIN number of the company.

<strong>files<strong> `[string]`

Array Object descriptor that encloses the list of legal documents or files associated with the company.

<strong>additionalProperties<strong> `object`

Object descriptor that encloses additional details of the company.

<strong>id<strong> `string`

The unique identifier of the company.

<strong>ownerId<strong> `string`

The unique owner identifier of the company.

<strong>tenantId<strong> `string`

A unique identifier required for authorization.

<strong>seriesPrefix<strong> `string`

Prefix of the series name.

<strong>seriesNumber<strong> `number`

The number of the series the company has completed for raising money.

<strong>useOrganizerSSNForEINOrders<strong>: `boolean`

This will use the organizer's SSN for EIN obtainment

<strong>legalIncOrder<strong> `object`

Legal Inc Order Details:

* <strong>status<strong> `string`

Order Status

* <strong>statusDescription<strong> `string`
Status Description

* <strong>ein<strong> `string`

EIN Pattern `^(0[1-9]|[1-9]\d)-\d{7}$`

* <strong>orderId<strong> `number`

Order ID

* <strong>orderPlacedDate<strong> `date-time`

Order Placed on

* <strong>orderFulfilledDate<strong> `date-time`
Order Fulfilled on

<strong>professionalEntity<strong> `boolean`

Has the value _true_ if it's professional entity, or the value false if it's not. 

<strong>typeOfBusiness<strong> `string`
Type of Business/Purpose: Type of Business/Purpose (Finance & Insurance)

<strong>typeOfBusinessActivity<strong> `string`
Type of Business Activity: Type of Business Activity (Finance)

<strong>individualOrBusiness<strong>: `enum`
Business/Individual Allowed `enum` values are `Individual┃Business`

<strong>feesAccount<strong> `object`
Object descriptor that encloses the account information for fees deduction.

* <strong>providerMeta<strong> `object` <br> Object descriptor that encloses fees provider's meta details.

  * <strong>typeId<strong> `string` <br> The type of the fees account.

  * <strong>accountStatus<strong> `string` <br> The current status of the fees account.

  * <strong>accountApplicationId<strong> `string` <br> The unique identifier for the account application.

  * <strong>accountId<strong> `string` A unique identifier of the account.

* <strong>createdAt<strong> `date-time` <br> The date and time stamp when the fees account is first introduced in the platform.

* <strong>updatedAt<strong> `date-time` <br> The last date and time stamp when the fees account's information has been modified.

* <strong>bankName<strong> `string` <br> The name of the bank for the fees account. 

* <strong>accountNumber<strong> `string` <br> The bank account number.

* <strong>routingNumber<strong> `string` <br> The routing number associated with the bank account.

* <strong>accountName<strong> `string` <br> The name of the person or entity authorized to have an account in the mentioned bank.

* <strong>bankContact<strong> `object` <br> The contact details of the bank branch.

  * <strong>name<strong> `string` <br> Name of the bank.

  * <strong>phone<strong> `string` <br> Official phone to contact.

  * <strong>email<strong> `string` <br> Email address to contact.

<strong>arbitrationCity<strong> `string`

Arbitration City

<strong>arbitrationState<strong> `string`

Arbitration State

<strong>howWillBeBusinessManaged<strong> `enum`

How Will Be Business Managed?

 How will the business be managed (can have 1-many owners/managers).
 
 Allowed `Solely by the owner(s) (Member-managed)┃Some, but not all, owners (Manager-managed)┃By the owner(s) and other managers (Manager-managed)┃Solely by the manager(s) (Manager-Managed)`