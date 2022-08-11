Initiates a request to create an entity based on the input parameters `key:value` pair that are supplied in the request body.Data in the request body should follow the JSON data formatting.

# Parameters

<strong>name*<strong> `string`

Legal Name of the Entity. A valid value must be 2 to 1024 characters.

<strong>entityType*<strong> `enum`

The Type of Entity. Allowed `enum` values are `LIMITED_LIABILITY_COMPANY┃LIMITED_PARTNERSHIP┃C_CORPORATION┃CORPORATION`.The variable must be equal to one of the values that have been predefined for it.

<strong>regulationType<strong> `enum`

The Regulation Type for the Entity. Allowed enum values are `REGULATION_D┃REGULATION_S┃REGULATION_D_S`.The variable must be equal to one of the values that have been predefined for it.

<strong>regDExemption<strong> `enum┃null`

The Regulation D Exemption. Allowed `enum` values are  `b┃c`.

<strong>ein<strong> `string┃null`

The EIN number for the Entity. Pattern `^(0[1-9]|[1-9]\d)-\d{7}$`.

<strong>arbitration<strong> `object`

JSON object descriptor that encloses a set of `key:value` pairs representing arbitration location information.
> Arbitration is a mechanism whereby a disagreement is submitted, by consent of the parties, to one or more arbitrators who render a legally enforceable ruling.
* <strong>city<strong> `string`
Arbitration City name.
* <strong>state<strong> `string`
Arbitration State name.
* <strong>country<strong> `string`
Arbitration Country name.

<strong>registeredAgent<strong> `string┃null`

Registered Agent associated with this entity.The value can be `null` if there is no registered agent for this entity. 

<strong>assetComposition<strong> `string┃null`

Asset Composition.The value can be `null` if there is no Asset Composition for this entity. 

<strong>bankAccount<strong> `object`

JSON object descriptor that encloses a set of `key:value` pairs are representing bank account information associated with this entity.
 
* <strong>bankContact<strong> `object` 
JSON object descriptor that encloses a set of `key:value` pairs representing bank contact details. 
   * <strong>name<strong> `string` </br>
    Bank Contact Name(person).
   * <strong>phone<strong> `string` </br>
    Bank Contact Phone number.
   * <strong>email<strong> `email` </br>
    Bank Contact Email address.

<strong>minInvestmentAmount*<strong> `number`

Minimum investment amount required to participate in the deal. Constraints `Min 0┃Max 6000000`.

<strong>fundType<strong> `enum`

Fund Type for this entity. Allowed `enum` values are `STANDARD_SPV┃SPV_FUND┃VENTURE_FUND`.The variable must be equal to one of the values that have been predefined for it.

<strong>legalFormat<strong> `enum`

Legal Format for this entity. Allowed `enum` values are `SERIES┃STANDALONE`.The variable must be equal to one of the values that have been predefined for it.

<strong>managementFee<strong> `object`

JSON object descriptor that encloses the  information for management fee deduction.

* <strong>type<strong> `enum` </br>
Management Fee Type. Allowed enum values are  `percent┃flat`.The variable must be equal to one of the values that have been predefined for it.
* <strong>amount<strong> `number` </br>
Management Fee Amount.Constraints `multiple of 0.01`.
* <strong>duration<strong> `number` </br>
Management Fee Duration.
* <strong>frequency<strong> `enum` </br>
Management Fee Frequency. Allowed enum values are  `Annual┃Once`.The variable must be equal to one of the values that have been predefined for it.
* <strong>feesPaymentMethod<strong> `string` </br>
Management Fees Payment Method.

<strong>expenseReserve<strong>`object`

JSON object descriptor that encloses a set of `key:value` pairs representing Expense Reserve information.

* <strong>amount<strong> `number`
Expense Reserve Amount. Constraints `multiple of 0.01`.
* <strong>type<strong> `enum`
Expense Reserve Type. Allowed enum values are `Flat Fee┃Percent`.The variable must be equal to one of the values that have been predefined for it.
* <strong>calculationMethod<strong> `enum`
Fee calculation method. Allowed `enum` values are `minus┃plus`.The variable must be equal to one of the values that have been predefined for it.

<strong>countryOfFormation<strong> `string`

The Country the Entity was formed in.Constraints `2 to 1024 chars`.

<strong>stateOfFormation<strong> `string┃null`

The State the Entity was formed in.A valid value must be 2 to 1024 characters or the value can be `null`.

<strong>legalIncOrder<strong> `object`

JSON object descriptor that encloses the Legal Inc Order Details associated with the entity.
* <strong>status<strong> `string` </br>Order Status.
* <strong>statusDescription<strong> `string`</br>Status Description.
* <strong>ein<strong> `string` </br> EIN number.EIN Pattern `^(0[1-9]|[1-9]\d)-\d{7}$`.
* <strong>orderId<strong> `number` </br>Order ID.
* <strong>orderPlacedDate<strong> `date-time` </br>The date & time at which Order Placed On.
* <strong>orderFulfilledDate<strong> `date-time` </br> The date & time at whichOrder Fulfilled On.

<strong>tenantId<strong> `string`

A unique identifier used for API authentication and authorization.
>Tenant refers to the end user of this API and It's required for identity and access management.

<strong>dealId<strong> `string`

The unique deal identifier associated this entity.

<strong>entityDocuments<strong> `object`

JSON object descriptor that encloses the legal documents associated with this entity.

* <strong>operatingAgreement<strong> `string` </br> Operating Agreement document.
* <strong>privatePlacementMemorandum<strong> `string` </br> Private PlacementMemorandum document.
* <strong>subscriptionAgreement<strong> `string` </br> Subscription Agreement document.
* <strong>einLetter<strong> `string` </br> EIN letter document.

<strong>files<strong> `[string]`

Array Object descriptor that encloses the list of URLs or legal documents or file paths referencing the files associated with this entity, meant to be displayable to the investors.

<strong>createdAt<strong> `date-time`

The date & time at which the entity was created.

<strong>updatedAt<strong> `date-time`

The date & time at which the entity was last updated.

<strong>deletedAt<strong> `date-time`

The date & time at which the entity was deleted.

<strong>isDeleted<strong> `boolean`

Has the value _true_ if this particular entity is deleted; otherwise, the value _false_.

<strong>managerId<strong> `string┃null`

The unique manager identifier for this entity.

<strong>masterEntityId<strong> `string┃null`

The unique master entity identifier for this entity.

<strong>ownerId<strong> `string`

A unique identifier of the owner for this deal. 

<strong>additionalProperties<strong> `object`

JSON object descriptor that encloses a set of `key:value` pairs representing additional properties for this entity. The enclosed data body must be in JSON format.

<strong>registrationNumber<strong> `string`

The legal entity's registration number.

<strong>formationDate<strong> `date-time`

The legal entity's official formation date.