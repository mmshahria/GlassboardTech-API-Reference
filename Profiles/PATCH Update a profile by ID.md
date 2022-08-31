Partially modify existing Profile records based on the supplied `key:value` pairs in the JSON format. Supply the unique `profileId` in the path parameter to execute a partial update operation to a specific profile for the current user.

> PATCH is a method of modifying resources where the client sends partial data that is to be updated without modifying the entire data.

# Parameters

<strong> profileType</strong> `enum`

Type of a profile in the organization specified at the time of creating this profile. Predefined `enum` values are  `ORGANIZER┃INVESTOR┃FOUNDER┃INDIVIDUAL`. The variable must be equal to one of the values that have been predefined for it. This can be useful to manage a user's roles in the platform and its access to data.

<strong> displayName </strong> `string`

Preferred display name specified by the authorized profile owner, if any.

<strong>managerId<strong> `string`
Unique ID of the Manager for Deals created by this Profile.

<strong>masterEntityId<strong> `string`
Unique ID of the Master Entity for Deals created by this profile.

<strong> taxDetails </strong> `object`

JSON object descriptor that encloses tax related information for this profile.

  * <strong> registrationType*</strong> `enum` </br> The Type of Tax Registration for this profile.Tax registration type applies to a person or an organization. Predefined `enum` values are `ENTITY┃TRUST┃JOINT┃401K┃IRA┃INDIVIDUAL`. 

  * <strong> taxIdentification*</strong> `object` </br> JSON object descriptor that encloses tax documents identification details.
    * <strong> type</strong> `enum` </br> Type of legal tax document. Predefined `enum` values are `ssn┃giin┃itin┃ftin┃ein`.Allowed `enum` values are `ssn┃itin┃ftin`,If the <strong>registrationType*<strong>  is `INDIVIDUAL` . The variable must be equal to one of the values that have been predefined for it.
    * <strong> value</strong> `string` </br> Tax document identification number for this profile.

<strong> firstName</strong> `string` 

First name of the profile owner if it's an individual profile.

<strong> lastName</strong> `string` 

Last name of the profile owner if it's an individual profile.

<strong> dateOfBirth</strong> `string`

The date of birth of the registered individual associated with this Profile.

<strong> phone</strong> `string`

The contact Phone number associated with this profile.

<strong> email</strong> `email`

The email address associated with this profile. Pattern `^\S+@\S+$`.

<strong> brokerageAccount </strong> `object`

JSON object descriptor that encloses brokerage account details associated with this profile.

  * <strong> brokerName *</strong> `string` </br> Full name of the broker.Constraints Max 128 chars.
  * <strong> dtcNumber *</strong> `string` </br> Depository Trust Company Number.Constraints Max 4 chars.
    > dtcNumber helps facilitate transactions between financial institutions.
  * <strong> accountNumber *</strong> `string` </br> Brokerage account number.Constraints Max 64 chars.

<strong> isRIA</strong> `boolean`


<strong> isERA <strong> `boolean`

Has the value true if the Profile is an entity holds ERA (Exempt Reporting Adviser) status otherwise the value is false.

<strong> isSingleMemberLLC</strong> `boolean`

Has the value _true_, if it's an entity profile representing an LLC company and if the company consists of only one member, or the value _false_ if the company has more than one member.

<strong> isUSBased</strong> `boolean`

Has the value _true_ if the entity is based in the US, or the value false if it not based in the US.

<strong> address </strong> `object`

JSON object descriptor that encloses physical address of the Entity or Individual associated with this profile.

  * <strong> address1* </strong> `string` </br> Address line 1.
  * <strong> address2 </strong> `string` </br> Address line 2.
  * <strong> city* </strong> `string` </br> The city name.
  * <strong> state </strong> `string` </br> The state name.
  * <strong> postalCode* </strong> `string` </br> The postal code.
  * <strong> country* </strong> `string` </br> The country name.

<strong> foreignAddress </strong> `object`

JSON object descriptor that encloses the foreign address of the Entity or Individual associated with this profile if the profile is outside the territory of the US.

  * <strong> address1* </strong> `string` </br> Foreign Address line 1. Constraints 2 to 1024 chars.
  * <strong> address2 </strong> `string` </br> Foreign Address line 2.Constraints 2 to 1024 chars.
  * <strong> city* </strong> `string` </br> Foreign city name.Constraints 2 to 1024 chars.
  * <strong> state </strong> `string` </br> Foreign state name.Constraints 2 to 1024 chars.
  * <strong> postalCode* </strong> `string` </br> Foreign postal code.Constraints 2 to 1024 chars.
  * <strong> country* </strong> `string` </br> Foreign country name.Constraints 2 to 1024 chars.

<strong> deliveryAddress </strong> `object`

JSON object descriptor that encloses the delivery address associated with this profile.

  * <strong> address1* </strong> `string` </br> Delivery Address line 1.Constraints 2 to 1024 chars.
  * <strong> address2 </strong> `string` </br> Delivery Address line 2.Constraints 2 to 1024 chars.
  * <strong> city* </strong> `string` </br> Delivery city name.Constraints 2 to 1024 chars.
  * <strong> state </strong> `string` </br> Deliver state name.Constraints 2 to 1024 chars.
  * <strong> postalCode* </strong> `string` </br> Delivery postal code.Constraints 2 to 1024 chars.
  * <strong> country* </strong> `string` </br> Delivery country name.Constraints 2 to 1024 chars.

<strong> primarySignatory </strong> `object`

JSON object descriptor that encloses primary signatory (Individual Entity or Person) details for this profile.

  * <strong> id</strong> `string` <br> A unique identifier for the Primary signatory.
  * <strong> ownerId</strong> `string` <br> A unique owner identifier for this primary signatory. 
  * <strong> name</strong> `string` </br> Full name of the primary signatory (Individual Entity or Person).Constraints `2 to 1024 chars`.
  * <strong> type</strong> `string` </br> Type of the primary signatory.Constraints `2 to 1024 chars`.
  * <strong> title</strong> `string` </br> The title of the signer.In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.Constraints `2 to 1024 chars`.
  * <strong> isUSBased</strong> `boolean` <br> Has the value _true_ if the signatory resides in the US, or the value _false_ if the signatory resides outside of the US territory.
  * <strong> address</strong> `object` <br> JSON object descriptor that encloses physical address details of the primary signatory.
  
    * <strong> address1* </strong> `string` </br> Address line 1.Constraints `2 to 1024 chars`.
    * <strong> address2 </strong> `string` </br> Address line 2.Constraints `2 to 1024 chars`.
    * <strong> city* </strong> `string` </br> The city name.Constraints `2 to 1024 chars`.
    * <strong> state </strong> `string` </br> The state name.Constraints `2 to 1024 chars`.
    * <strong> postalCode* </strong> `string` </br> The postal code.Constraints `2 to 1024 chars`.
    * <strong> country* </strong> `string` </br> The country name.Constraints `2 to 1024 chars`.
  
  * <strong> phone</strong> `string` <br> Phone number associated with the primary signatory.
  * <strong> email</strong> `string` <br> Email address associated with the primary signatory.
  * <strong> taxDetails</strong> `object` <br> JSON object descriptor that encloses tax document details of the primary signatory.
    * <strong> type*</strong> `enum`  <br> Type of legal tax document. Predefined `enum` values are `ssn┃itin┃ftin`.
    * <strong> value*</strong> `string` <br> Unique identification number for the tax document.

  * <strong> dateOfBirth</strong> `string` <br> Date of birth of the primary signatory.
  * <strong> stateOfFormation</strong> `string` <br> State of formation if the primary signatory is an individual Entity.
  * <strong> countryOfFormation</strong> `string` <br> The country of formation if the primary signatory is an individual Entity.
  * <strong> taxIdType</strong> `string` <br> Type of the tax identification.
  * <strong> taxId</strong> `string` <br> Unique tax identification number.


<strong> additionalSignatories</strong> `[object]`

JSON array object descriptor that encloses additional signatories (Individual Entity or Person) for this profile.

  * <strong> id</strong> `string` <br> A unique identifier for the additional signatories (Individual Entity or Person).
  * <strong> ownerId</strong> `string` <br> A unique identifier of the owner for this additional signatory. 
  * <strong> name</strong> `string` </br> Full name of the additional signatory (Individual Entity or Person).Constraints `2 to 1024 chars`.
  * <strong> type</strong> `string` </br> Type of the additional signatory.Constraints `2 to 1024 chars`.
  * <strong> title</strong> `string` </br> The title of the signer.Constraints `2 to 1024 chars`.In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.
  * <strong> isUSBased</strong> `boolean` <br> Has the value _true_ if the signatory resides in the US, or the value _false_ if the signatory resides outside of the US territory.
  * <strong> address</strong> `object` <br> JSON object descriptor that encloses physical address details of the additional signatory.
  
    * <strong> address1* </strong> `string` </br> Address line 1.Constraints `2 to 1024 chars`.
    * <strong> address2 </strong> `string` </br> Address line 2.Constraints `2 to 1024 chars`.
    * <strong> city* </strong> `string` </br> The city name.Constraints `2 to 1024 chars`.
    * <strong> state </strong> `string` </br> The state name.Constraints `2 to 1024 chars`.
    * <strong> postalCode* </strong> `string` </br> The postal code.Constraints `2 to 1024 chars`.
    * <strong> country* </strong> `string` </br> The country name.Constraints `2 to 1024 chars`.
  
  * <strong> phone</strong> `string` <br> Phone number associated with the additional signatory.
  * <strong> email</strong> `string` <br> Email address associated with the additional signatory.
  * <strong> taxDetails</strong> `object` <br> JSON object descriptor that encloses tax document details of the additional signatory.
    * <strong> type*</strong> `enum`  <br> Type of legal tax document. Predefined `enum` values are `ssn┃itin┃ftin`.
    * <strong> value*</strong> `string` <br> Unique identification number for the tax document.

  * <strong> dateOfBirth</strong> `string` <br> Date of birth of the additional signatory.
  * <strong> stateOfFormation</strong> `string` <br> State of formation if the additional signatory is an individual Entity.
  * <strong> countryOfFormation</strong> `string` <br> Country of formation if the additional signatory is an individual Entity.
  * <strong> taxIdType</strong> `string` <br> Type of the tax identification.
  * <strong> taxId</strong> `string` <br> Unique tax identification number.

<strong> beneficialOwner</strong> `object`

JSON object descriptor that encloses the details of beneficial owner (Individual Entity or Person) for this profile.

> Individuals or natural people who ultimately owns this profile.

  * <strong> id</strong> `string` <br> A unique identifier of the beneficial owner.
  * <strong> ownerId</strong> `string` <br> A unique identifier of the owner for this beneficial owner. 
  * <strong> name</strong> `string` </br> Full name of the beneficial owner. 
  * <strong> type</strong> `string` </br> Type of the beneficial owner.
  * <strong> title</strong> `string` </br> The title of the signer.In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.
  * <strong> isUSBased</strong> `boolean` <br> Has the value _true_ if the beneficial owner resides in the US, or the value _false_ if the beneficial owner resides outside of the US territory.
  * <strong> address</strong> `object` <br> JSON object descriptor that encloses physical address details of the beneficial owner.
  
    * <strong> address1* </strong> `string` </br> Address line 1.
    * <strong> address2 </strong> `string` </br> Address line 2.
    * <strong> city* </strong> `string` </br> The city name.
    * <strong> state </strong> `string` </br> The state name.
    * <strong> postalCode* </strong> `string` </br> The postal code.
    * <strong> country* </strong> `string` </br> The country name.
  
  * <strong> phone</strong> `string` <br> Phone number associated with the beneficial owner.
  * <strong> email</strong> `string` <br> Email address associated with the beneficial owner.
  * <strong> taxDetails</strong> `object` <br> JSON object descriptor that encloses tax document details of the additional signatory.
    * <strong> type*</strong> `enum`  <br> Type of legal tax document. Predefined `enum` values are `ssn┃itin┃ftin`.
    * <strong> value*</strong> `string` <br> Unique identification number for the tax document.

  * <strong> dateOfBirth</strong> `string` <br> Date of birth of the additional signatory.
  * <strong> stateOfFormation</strong> `string` <br> State of formation if the beneficial owner is an Entity.
  * <strong> countryOfFormation</strong> `string` <br> Country of formation if the beneficial owner is an Entity.
  * <strong> taxIdType</strong> `string` <br> Type of the tax identification.
  * <strong> taxId</strong> `string` <br> Unique tax identification number.


<strong>managedAccountDetails<strong> `object`
JSON object descriptor that encloses the Managed Account Details for this profile.

* <strong>accountName<strong> `string` </br>
Account Name. Constraints Max 128 chars.
* <strong>accountNumber<strong> `string` </br>
Account Number. Constraints Max 64 chars.
* <strong>custodianName<strong> `string` </br>
Custodian Name. Constraints Max 128 chars.

<strong>id<strong>: `string`
The unique internal identifier to locate this Profile.

<strong> name</strong> `string` 

Full name of entity,If the profile is representing an entity, such as a firm or company.

<strong> typeOfEntity</strong> `enum`
The Type of Entity If the profile is representing an entity.
_Data-type_ `enum` Consists of predefined legal business entity type `LIMITED_LIABILITY_COMPANY┃LIMITED_PARTNERSHIP┃C_CORPORATION┃S_CORPORATION┃GENERAL_PARTNERSHIP┃501_C_NONPROFIT┃FOREIGN_ENTITY┃INDIVIDUAL┃CORPORATION`. The variable must be equal to one of the values that have been predefined for it.

<strong>dateOfFormation<strong> `date`
The Date of Formation of the Entity.

<strong> stateOfFormation</strong> `string`

If the profile represents an entity, then the state in which it was formed will be included here.

<strong> countryOfFormation</strong> `string`

If the profile represents an entity, then the Country in which it was formed will be included here.


<strong> jointType</strong> `enum` 

The type of the joint profile (If Joint Profile Type). There is a significant legal distinction and rights to supervisorship between the account holders in some jurisdictions. Predefined `enum` values are
`JOINT_TENANTS_WITH_RIGHTS_OF_SURVIVORSHIP┃TENANTS_IN_COMMON┃COMMUNITY_PROPERTY┃TENANTS_BY_ENTIRETY`.


<strong> title</strong> `string`
The Title of the Individual associated with this profile, If individual profile.

> In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.

<strong> ERAStatus</strong> `string`

<strong>tenantId<strong> `string`

A unique identifier used for API authentication and authorization.

<strong> primaryContact</strong> `object`

JSON object descriptor that encloses primary contact details for this profile.

<strong> investorStatus</strong> `[number]`

Investor Status representation for Document Generation. Numbers in index correspond to checkboxes in documents, in numerical order.

<strong> ownerId</strong> `string`

The Default Owner ID associated with this profile.

<strong> bankingUser</strong> `object`

External Banking User. This is used for storing external bank accounts for organizers.

  * <strong> id </strong> `string`
  * <strong> accounts </strong> `[object]` </br> An array object descriptor that encloses the list of accounts for banking user associated with this profile.

<strong> purchaserStatus</strong> `[number]`

<strong> createdAt</strong> `date-time` 

Timestamp for the creation of the profile.

<strong> updatedAt</strong> `date-time`

Timestamp for the last update record.

<strong> isDeleted</strong> `boolean`

Has the value true if the profile is deleted or the value false if it's not deleted.

<strong> additionalProperties </strong> `object`

JSON object descriptor for additional properties.

  * <strong> formedToInvestInFund</strong> `boolean` </br> Has the value true if this profile specifically created to invest in a certain fund, otherwise the value is flase.
  * <strong> isInvestmentCompany</strong> `boolean`
  * <strong> isExpatriate</strong> `enum`  </br>  Allowed enum values are `permanent┃temporary`.
  * <strong> jurisdiction</strong> `string` </br> Used in the subscription agreement for arbitration location.
  * <strong> fundDocumentTemplateId</strong> `string` </br>	The Default Fund Document Template ID to use for the Deal.
  * <strong> passportOrId</strong> `string` 
  * <strong> isDisregarded<strong> `boolean` </br> Has the value true if the profile is a disregarded entity or trust, otherwise the value is false.