Retrieves the details of a specified subscription for a valid identifier. Supply the unique `subscriptionId`, and this endpoint will respond to the corresponding subscription details for the current user.

# Attributes

<strong>tenantId<strong> `string`
A unique identifier used for API authentication and authorization.

> Tenant refers to the end user of this API and It's required for identity and access management.

<strong>dealId<strong> `string`

A unique identifier of a particular deal for this subscription.It refers to a particular deal to which a subscriber is making a investment.

<strong>name*<strong> `string`

The Name of the particular deal for this subscription.Constraints `2 to 1024 chars`.

<strong>email*<strong> `string`

The contact email address of the subscriber.Pattern `^\S+@\S+$`.

<strong>phone<strong> `string`
The contact phone number of the subscriber.

<strong>type<strong>  `enum`

Category of subscriber.`type` applies to a person or an organization. Predefined `enum` values are `INDIVIDUAL┃ENTITY┃TRUST┃JOINT`. 

<strong>status*<strong> `enum`

Accreditation Status for this subscription._Data-type_ `enum` consists of predefined status values `INVITED┃PENDING┃COMMITTED┃COMPLETED┃CLOSED┃CANCELLED┃TRANSFERRED┃REFUNDED┃FUNDING SENT┃FUNDS_IN_TRANSIT-MANUAL`.The variable must be equal to one of the values that have been predefined for it while updating the subscription _status_.

<strong>amount<strong> `number`

The amount Investor/subscriber intends to invest in a deal.Constraints `Min 0`.

<strong>reconciledAmount<strong> `number`

Amount actually received for this subscription. Constraints `Min 0┃Max 6000000`.

<strong>ownershipPercentageAtClose<strong> `number`

Ownership Percentage At the time of Close.Constraints `Min 0`.

> A close can represent the close of the entire deal or just a subset of investments (i.e. a tranche).

<strong>ownershipPercentageAtDistribution<strong> `number`

Ownership Percentage At the time of Distribution.Constraints `Min 0`.

> `Distribution` means the transfer of money or property by the Fund/Deal to one or more Members with respect
to their Interests, without separate consideration

<strong>transactionId<strong> `string`

Unique transaction identifier generated from the electronic transfer of fund for this subscription.

<strong>transactionIds<strong> `[string]`

JSON object descriptor that encloses an array list of transaction's unique identifiers if the subscription consists of disparate subscribers. Each _array_ index consists of a disparate transaction identifier.

<strong>bankTransactionIds<strong> `[string]`

JSON object descriptor that encloses an array list of bank transaction's unique identifiers if the subscription consists of disparate subscribers. Each _array_ index consists of a disparate bank transaction identifier.

<strong>reverseTransactionId<strong> `string`

Unique reverse transaction identifier for this subscription.

<strong>distributionTransactionIds<strong> `[string]`

JSON object descriptor that encloses an array list of distribution transaction's unique identifiers if the subscription consists of disparate subscribers. Each _array_ index consists of a distributed transaction identifier.

<strong>isDocsSigned<strong> `boolean`

Has the value _true_ if the subscription documents are signed by the subscriber or the value _false_ if it's not.

<strong>isAmountMatched<strong> `boolean`

Has the value _true_ if the subscription `amount` matched or the value _false_ if it's not.

<strong>isKycAmlPassed<strong> `boolean`

Has the value _true_ if the subscriber passed the KycAml or the value _false_ if it's not.

<strong>signers<strong> `[objcet]`

JSON _array_ object descriptor that encloses the list of signers for this subscription.

<strong>bankAccount<strong> `object`

JSON object descriptor that encloses the details of bank account for this subscription.

<strong>fundingInfo<strong> `object`

JSON object descriptor that encloses the inforamtion on where the money used to fund the subscription was sourced from.

* <strong>bankName<strong> `string` </br> The name of the bank from which the subscriber's subscription payment is being sent.
* <strong>isCustomerOfBank<strong> `boolean` </br> Has the value true if the subscriber is a customer of the bank, or is the value _false_ if it's not.
* <strong>isFATFBank<strong> `boolean` </br> Has the value true if the bank is located in the United States or another country that is a member of the Financial Action Task Force (FATF) on Money Laundering, or is the value  _false_ if it's not.
  

<strong>accountTransaction<strong> `object`

JSON object descriptor that encloses the details of account transaction for this subscription.

<strong>documents<strong> `object`

JSON object descriptor that contatins the legal documents for this subscription.

* <strong>capitalAccountStatement<strong> `string` </br> Subscription Document.
* <strong>historicalCapitalAccountStatements<strong> `string` </br> Subscription Document.
* <strong>signerOneOASigPage<strong> `string` </br> Subscription Document.
* <strong>signerTwoOASigPage<strong> `string` </br> Subscription Document.
* <strong>investorSASigPage<strong> `string` </br> Subscription Document.
* <strong>signerOneTaxDoc<strong> `string` </br> Subscription Document.
* <strong>signerTwoTaxDoc<strong> `string` </br> Subscription Document.
* <strong>mergedSignerOneOA<strong> `string` </br> Subscription Document.
* <strong>mergedSignerTwoOA<strong> `string` </br> Subscription Document.
* <strong>mergedInvestorSA<strong> `string` </br> Subscription Document.
* <strong>mergedCounterSignedOA<strong> `string` </br> Subscription Document.
* <strong>mergedCounterSignedSA<strong> `string` </br> Subscription Document.
* <strong>taxes<strong> `[object]` </br> 
JSON object descriptor that encloses tax-related information. Each _array_ index consists of `year` and a unique file identifier of taxes.
  * <strong>year<strong> `number` </br> Subscription's taxable year.
  * <strong>fileId<strong> `string` </br> A unique identifier of the legal document or file associated with the tax.

<strong>files<strong> `[string]`

Array Object descriptor that encloses the list of legal documents or files associated with the subscription.

<strong>closeDoc<strong> `string`

File ID of the compiled documents for a Closed Subscription.

<strong>createdAt<strong> `date-time`

The date and time stamp when the subscription was Created.

<strong>updatedAt<strong> `date-time`

The date and time stamp when the subscription information was last modified.

<strong>signature<strong> `string`

Subscriber's signature in the legal document for the subscription.

<strong>deletedAt<strong> `date-time`

The date & time at which the subscription was deleted.

<strong>isDeleted<strong> `boolean`

Has the value true if the subscription is deleted or the value false if it's not deleted.

<strong>acquisitionMethod<strong> `enum`

Subscriber acquisition Method for this subscirption.Predefined `enum` values are `DIRECT_LINK┃INVITATION`.

<strong>ownerId<strong> `string`

The unique identifier of the user who owns this object.

<strong>profileId<strong> `string`

A unique identifier of the subscriber profile.

<strong>sideLetter<strong> `object`

JSON object descriptor that encloses the Side Letter Properties that overrides the Deal settings for this subscription. Can override the Carry and Management Fee.

* <strong>managementFee<strong> `object` </br>
Object descriptor that encloses the Side Letter Management Fee that overrides the fee settings on the deal for this subscription. 
  * <strong>amount<strong> `number` </br> The amount of the management fee.
  * <strong>duration<strong> `number` </br> Duration of Management Fee.
  * <strong>frequency<strong> `string` </br> Periodicity of Management Fee.
  * <strong>percent<strong> `number` </br>
  * <strong>type<strong> `string` </br> Type of management fee.
  * <strong>feesPaymentMethod<strong> `string` </br> Management fees payment method.
  * <strong>isRecurring<strong> `boolean` </br> Checks whether the Management Fee for the deal is assessed annually.
* <strong>organizerCarryPercentage<strong> `object` </br>
  JSON object descriptor that encloses the organizer Carry Percentage related information.
  > Carry Percentage means the rate of return percentage above the initial investment after one year that needs to be paid to a deal **organizer**. It is in the deal **organizer's** discretion as to whether the Carry Percentage will be lower, and such determination may be made up until the date of the Initial Closing.
  * <strong>type<strong>: `enum` </br>
Type of Organizer Carry percentage. Predefined `enum` values are  `percent┃flat`.
  * <strong>amount<strong>: `number` </br>
The amount of Organizer Carry percentage. Constraints `multiple of 0.01`
  * <strong>tiers<strong>: `[object]` </br>
JSON _array_ object descriptor that encloses classification tier of Organizer carry percentage.
    * <strong>breakpoint<strong> `number` </br>
Carry Percentage Breakpoint.
    * <strong>amount<strong> `number` </br>
Carry Percentage Amount. Constraints `Min 0┃Max 100┃ multiple of 0.001`


<strong>additionalProperties<strong> `object`

JSON object descriptor that encloses a set of `key:value` pairs representing additional properties for this file.This can be useful for storing additional information in a structured format.  The enclosed data body must be in JSON format.

<strong>additionalFiles<strong> `[string]`

Array Object descriptor that encloses the list of additional legal documents or files associated with the subscription.

<strong>k1File<strong> `string`

Tax file issued annually by Internal Revenue Service (IRS) for this subscription. 


<strong>is40OrMoreTotalAssets<strong> `boolean`

Has the value _true_, if it's an entity profile and if the company has a total-debt-to-total-assets ratio of 0.4, 40% of its assets are financed by creditors, and 60% are financed by owners' (shareholders') equity, or the value _false_ if the company has a different total-debt-to-total-assets ratio.

<strong>isAffiliate<strong> `boolean`

Has the value _true_ if the subscription has an affiliate, or the value _false_ if it's not.

> Affiliate means any person, directly or indirectly, through one or more intermediaries, that controls, is controlled by, or is under common control with another person.

<strong>closeId<strong> `string`

The Unique internal identifier of the related Close Object for this subscription.

> A close can represent the close of the entire deal or just a subset of investments (i.e. a tranche).

<strong>capitalCallApproveType<strong> `enum`

The type of capital call approval.Allowed `enum` values are `PRE-APPROVAL┃MANUAL_APPROVAL┃MANUAL_PAYMENT`.The variable must be equal to one of the values that have been predefined for it while selecting the capital call approval type.

> A capital call is the process by which a fund/deal manager asks the fund/deal investors/subscribers to contribute their pro rata portion of their fund commitments.