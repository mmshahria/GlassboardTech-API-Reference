Update existing profile records to the current user's (API end user) data source using the input parameters `key:value` pairs that are supplied in the request body. Supply the unique path parameter `profileId` in the canonical path to execute an update operation to a specific profile resource.

# Parameters

<strong> id</strong> `string`

A unique identifier assigned by the system while creating a user profile as an individual or an entity.

<strong> jointType</strong> `enum` 

The type of the joint profile. There is a significant legal distinction and rights to supervisorship between the account holders in some jurisdictions. Predefined `enum` values are
`JOINT_TENANTS_WITH_RIGHTS_OF_SURVIVORSHIP┃TENANTS_IN_COMMON┃COMMUNITY_PROPERTY┃TENANTS_BY_ENTIRETY`.

<strong> firstName</strong> `string` 

First name of the profile owner if it's an individual profile.

<strong> lastName</strong> `string` 

Last name of the profile owner if it's an individual profile 

<strong> address </strong> `object`

JSON object descriptor that encloses physical address of the Entity or Individual associated with this profile.

  * <strong> address1* </strong> `string` </br> Address line 1.
  * <strong> address2 </strong> `string` </br> Address line 2.
  * <strong> city* </strong> `string` </br> The city name.
  * <strong> state </strong> `string` </br> The state name.
  * <strong> postalCode* </strong> `string` </br> The postal code.
  * <strong> country* </strong> `string` </br> The country name.

<strong> deliveryAddress </strong> `object`

JSON object descriptor that encloses the delivery address associated with this profile.

  * <strong> address1* </strong> `string` </br> Address line 1.
  * <strong> address2 </strong> `string` </br> Address line 2.
  * <strong> city* </strong> `string` </br> The city name.
  * <strong> state </strong> `string` </br> The state name.
  * <strong> postalCode* </strong> `string` </br> The postal code.
  * <strong> country* </strong> `string` </br> The country name.

<strong> foreignAddress </strong> `object`

JSON object descriptor that encloses the foreign address associated with this profile if the profile is outside the territory of US.

  * <strong> address1* </strong> `string` </br> Address line 1.
  * <strong> address2 </strong> `string` </br> Address line 2.
  * <strong> city* </strong> `string` </br> The city name.
  * <strong> state </strong> `string` </br> The state name.
  * <strong> postalCode* </strong> `string` </br> The postal code.
  * <strong> country* </strong> `string` </br> The country name.

<strong> phone</strong> `string`

The contact Phone number associated with this profile.

<strong> dateOfBirth</strong> `string`

The date of birth of the registered individual associated with this Profile.

<strong> dateOfFormation</strong> `string`

Date of formation refers to the date on which the Entity (If Entity Profile) has been officially registered.

<strong> email</strong> `email`

The email address associated with this profile. Pattern `^\S+@\S+$`

<strong> taxDetails </strong> `object`

JSON object descriptor that encloses tax related information for this profile.

  * <strong> registrationType*</strong> `enum` </br> Tax registration type applies to a person or an organization. Predefined `enum` values are `ENTITY┃TRUST┃JOINT┃401K┃IRA┃INDIVIDUAL`. 

  * <strong> taxIdentification*</strong> `object` </br> JSON object descriptor that encloses tax documents identification details.
    * <strong> type</strong> `enum` </br> Type of legal tax document. Predefined `enum` values are `ssn┃giin┃itin┃ftin┃ein`.Allowed `enum` values are `ssn┃itin┃ftin`,If the <strong>registrationType*<strong>  is `INDIVIDUAL` . The variable must be equal to one of the values that have been predefined for it.
    * <strong> value</strong> `string` </br> Tax document identification number.

<strong> title</strong> `string`
The Title of the Individual associated with this profile, If individual profile.

> In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.

<strong> isUSBased</strong> `boolean`

Has the value _true_ if the profile or the entity is based in US, or the value false if not based in US.

<strong> isRIA</strong> `boolean`

<strong> isERAboolean <strong> `boolean`

<strong> ERAStatus</strong> `string`

<strong> primaryContact</strong> `object`

JSON object descriptor that encloses primary contact details for this profile.

<strong> isSingleMemberLLC</strong> `boolean`

Has the value _true_, if it's an entity profile representing an LLC company and if the company consists of only one member, or the value _false_ if the company has more than one member.

<strong> primarySignatory </strong> `object`

JSON object descriptor that encloses primary signatory (Individual Entity or Person) details for this profile.

  * <strong> id</strong> `string` <br> A unique identifier.
  * <strong> ownerId</strong> `string` <br> A unique identifier of the owner for this primary signatory. 
  * <strong> name</strong> `string` </br> Full name of the primary signatory.Constraints `2 to 1024 chars`.
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
  * <strong> stateOfFormation</strong> `string` <br> State of formation if primary signatory is individual Entity.
  * <strong> countryOfFormation</strong> `string` <br> Country of formation primary signatory is individual Entity.
  * <strong> taxIdType</strong> `string` <br> Type of the tax identification.
  * <strong> taxId</strong> `string` <br> Unique tax identification number.

<strong> additionalSignatories</strong> `[object]`

JSON object descriptor that encloses additional signatories (Individual Entity or Person) for this profile.

  * <strong> id</strong> `string` <br> A unique identifier.
  * <strong> ownerId</strong> `string` <br> A unique identifier of the owner for this additional signatory. 
  * <strong> name</strong> `string` </br> Full name of the additional signatory.Constraints `2 to 1024 chars`.
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

  * <strong> id</strong> `string` <br> A unique identifier.
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
  * <strong> stateOfFormation</strong> `string` <br> State of formation if beneficial owner is an Entity.
  * <strong> countryOfFormation</strong> `string` <br> Country of formation beneficial owner is an Entity.
  * <strong> taxIdType</strong> `string` <br> Type of the tax identification.
  * <strong> taxId</strong> `string` <br> Unique tax identification number.

<strong> investorStatus</strong> `[number]`

Investor Status representation for Document Generation. Numbers in index correspond to checkboxes in documents, in numerical order.

<strong> managerId</strong> `string`

The Default Manager ID for deals associated with this profile.

<strong> masterEntityId</strong> `string`

The Default Master Entity ID for deals associated with this profile.

<strong> ownerId</strong> `string`

The Default Owner ID associated with this profile.

<strong> bankingUser</strong> `object`

External Banking User.

  * <strong> id </strong> `string`
  * <strong> accounts </strong> `[object]` </br> An array object descriptor that encloses the list of accounts for banking user associated with this profile.

<strong> purchaserStatus</strong> `[number]` 

Purchaser Status representation for Qualified purchaser Document Generation. Numbers in index correspond to checkboxes in documents, in numerical order.

<strong> createdAt</strong> `date-time` 

Timestamp for the creation of the profile.

<strong> updatedAt</strong> `date-time`

Timestamp for the last update record.

<strong> isDeleted</strong> `boolean`

Has the value true if the profile is deleted or the value false if it's not deleted.

<strong> brokerageAccount </strong> `object`

JSON object descriptor that encloses brokerage account details associated with this profile.

  * <strong> brokerName *</strong> `string` </br> Full name of the broker.Constraints Max 128 chars.
  * <strong> dtcNumber *</strong> `string` </br> Constraints Max 4 chars.
    > dtcNumber helps facilitate transactions between financial institutions.
  * <strong> accountNumber *</strong> `string` </br> Brokerage account number.Constraints Max 64 chars.

<strong> offPlatformAccounts </strong> `[object]`

  * <strong> routingNumber</strong> `string` </br> Routing number of a specified bank account.Allowed pattern `[012346789][0-9]$`
  * <strong> bankName</strong> `string` </br> Name of a specified bank.
  * <strong> originatorName</strong> `string` </br> Name of the originator (e.g. name of the company or association). 
  > The originator is the company that receives the Direct Debit payments.
  * <strong> accountNumber</strong> `string` </br> Account number of a specified bank account.

<strong> additionalProperties </strong> `object`

JSON object descriptor for additional properties.

  * <strong> formedToInvestInFund</strong> `boolean`
  * <strong> isInvestmentCompany</strong> `boolean`
  * <strong> isExpatriate</strong> `enum`  </br>  Allowed enum values are `permanent┃temporary`.
  * <strong> jurisdiction</strong> `string`
  * <strong> fundDocumentTemplateId</strong> `string` </br>	The Default Fund Document Template ID to use for the Deal.
  * <strong> passportOrId</strong> `string` 
  * <strong> isDisregarded<strong> `boolean` </br> Has the value true if an entity profile is disregarded or a trust profile is under SSN, Otherwise, the value is false.