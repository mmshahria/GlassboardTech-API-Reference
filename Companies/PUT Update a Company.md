Replace an existing company records to the current user's data source based on the input parameters `key:value` pair that are supplied in the JSON format. Supply the unique `companyId` in the path parameter to execute an update operation to a specific company resource for the current user.

# Parameters

<strong>name<strong> `string`
The name of the company.A valid value must be 2 to 1024 characters.

<strong>website<strong> `string`
The website address of the company, if any.A valid value must be 2 to 1024 characters.

<strong>email<strong> `string`
The contact email address of the company.Pattern `^\S+@\S+$A `. A valid value must be 2 to 1024 characters.

<strong>type<strong> `enum`
The registration type of the company in the platform. Expected enum values are `MASTER_ENTITY┃REGISTERED_AGENT┃MANAGER`.

<strong>phone<strong> `string`
The contact phone number of the company.

<strong>stateOfFormation<strong> `string`
Name of the state where the company was Formed.

<strong>address<strong> `object`

JSON object descriptor that encloses the physical address of the company.

* <strong>address1*<strong> `string` <br> Company address Line 1.A valid value must be 2 to 1024 characters.
* <strong>address2</strong> `string` <br> Company address Line 2.A valid value must be 2 to 1024 characters.
* <strong>city*<strong> `string` <br> City name.A valid value must be 2 to 1024 characters.
* <strong>state<strong> `string` <br> State name.A valid value must be 2 to 1024 characters.
* <strong>postalCode*<strong> `string` <br> Postal code of the company.A valid value must be 2 to 1024 characters.
* <strong>country*<strong> `string` <br> Country name.A valid value must be 2 to 1024 characters.

<strong>taxContact<strong> `objcet`

JSON object descriptor that encloses the tax contact details.

* <strong>type<strong> `enum` <br> Tax ID type. Expected predefined values are `ssn┃itin┃ftin`.
* <strong>taxId<strong> `string` <br> Tax document identification number.
* <strong>address1<strong> `string` <br> Tax Contact Address 1.
* <strong>address2<strong> `string` <br> Tax Contact Address 2.
* <strong>city<strong> `string` <br> Tax Contact City name.
* <strong>state<strong> `string` <br> Tax Contact State name.
* <strong>postalCode<strong> `string` <br> Tax Contact Postal Code.
* <strong>country<strong> `string` <br> Tax Contact Country name.

<strong>createdAt<strong> `date-time` <br> The date and time stamp when the company object is created on the platform.

<strong>updatedAt<strong> `date-time` <br> The date and time stamp when the company object was last modified.

<strong>entityType<strong> `enum`

The Entity Type of company. Predefined legal entity types are `LLC┃Corporation┃Non-Profit┃LP┃LLP┃GP┃DBA┃LIMITED_LIABILITY_COMPANY┃LIMITED_PARTNERSHIP`.

<strong>individuals<strong> `[object]`

Array object descriptor that encloses the detailed lists of each individual associated with the company.

<strong>individual<strong> `objcet`

Object descriptor that encloses a single individual's details associated with the company. Such as individual owners of the Single-member LLC or sole proprietary business.

<strong>businesses<strong> `[object]`

Array object descriptor that encloses the detailed list of disparate businesses or fields of business the company has been associated with.

<strong>business<strong> `objcet`

Object descriptor that encloses the field of business the company is associated with.

<strong>ein<strong> `string`

The EIN number of the company.Pattern `^(0[1-9]|[1-9]\d)-\d{7}$`.

<strong>files<strong> `[string]`

Array Object descriptor that encloses the list of legal documents or files associated with the company.

<strong>additionalProperties<strong> `object`

JSON object descriptor that encloses a set of `key:value` pairs representing additional properties for the company.This can be useful for storing additional information in a structured format.  The enclosed data body must be in JSON format.

<strong>formationDate<strong> `date`

Formation Date of the company.

<strong>ownerId<strong> `string`

The unique identifier of the user who owns this object.

<strong>tenantId<strong> `string`

A unique identifier required for authorization.

<strong>seriesPrefix<strong> `string`

Prefix of the series name.Used to denote the prefix used for series naming. If left blank will use `Fund`.

<strong>seriesNumber<strong> `number`

The next number to use in sequence for SPV names. 

<strong>useOrganizerSSNForEINOrders<strong> `boolean`

This will use the organizer's SSN for EIN obtainment. Has the value _true_ if the organizer's SSN will use for EIN obtainment, or the value _false_ if it's not.

<strong>professionalEntity<strong> `boolean`

Used to denote if the entity being created is a 'Professional Company' as defined by the state.Has the value _true_ if it's professional entity, or the value false if it's not. 

<strong>typeOfBusiness<strong> `string`
Type of Business/Purpose (Finance & Insurance).

<strong>typeOfBusinessActivity<strong> `string`
Used to specify the type of business activity the company engages in, as defined by the IRS.

<strong>arbitrationCity<strong> `string`

Arbitration City name.
> Arbitration is a mechanism whereby a disagreement is submitted, by consent of the parties, to one or more arbitrators who render a legally enforceable ruling.

<strong>arbitrationState<strong> `string`

Arbitration State.

<strong>howWillBeBusinessManaged<strong> `enum`

Describe the management strategy that will be used for the business.
Allowed enum values are `Solely by the owner(s) (Member-managed)┃Some, but not all, owners (Manager-managed)┃By the owner(s) and other managers (Manager-managed)┃Solely by the manager(s) (Manager-Managed)`.