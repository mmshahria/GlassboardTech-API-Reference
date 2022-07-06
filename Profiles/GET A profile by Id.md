Retrieves the details of an existing profile for a valid identifier. Supply the unique `id` either from a profile creation request or the profile list to retrieve specified profile's information.

# Attributes

<strong> id</strong> `string`

A unique identifier used to locate a certain user's profile.

<strong> tenantId</strong> `string`

A unique identifier of the tenant to which the profile belongs.

> Tenant refers to the end user of this API and It's required for identity and access management.

<strong> profileType</strong> `enum`

Type of a profile in the organization specified at the time of creating this profile. Predefined `enum` values are  `ORGANIZER┃INVESTOR┃FOUNDER┃INDIVIDUAL`. The variable must be equal to one of the values that have been predefined for it. This can be useful to manage a user's roles in the platform and its access to data.

<strong> stateOfFormation</strong> `string`

If the profile is representing an entity, such as a firm or company, then the state in which it was registered will be included here.

<strong> countryOfFormation</strong> `string`

If the profile is representing an entity, such as a firm or company, then the country in which it was registered will be included here.

<strong> displayName </strong> `string`

Preferred display name specified by the authorized profile owner, if any.

<strong> name</strong> `string` 

 Full name of this profile.

<strong> jointAccountName</strong> `string` 

 The name of the joint account if it's a `jointType` account.
 
 > A joint account is a type of account in which more than one owner has access to the resource inside the account depending upon the `jointType`.

<strong> typeOfEntity</strong> `enum`

_Data-type_ `enum` 

Consists of predefined legal business entity type `LIMITED_LIABILITY_COMPANY┃LIMITED_PARTNERSHIP┃C_CORPORATION┃S_CORPORATION┃GENERAL_PARTNERSHIP┃501_C_NONPROFIT┃FOREIGN_ENTITY┃INDIVIDUAL┃CORPORATION`. 

The variable must be equal to one of the values that have been predefined for it.

<strong> jointType</strong> `enum` 

 The type of the joint account. There is a significant legal distinction and rights to supervisorship between the account holders in some jurisdictions. Predefined `enum` values are
`JOINT_TENANTS_WITH_RIGHTS_OF_SURVIVORSHIP┃TENANTS_IN_COMMON┃COMMUNITY_PROPERTY┃TENANTS_BY_ENTIRETY`.

<strong> firstName</strong> `string` 

First name of the person if it's an individual profile.

<strong> lastName</strong> `string` 

Last name of the person if it's an individual profile 

<strong> address </strong> `object`

JSON object descriptor that encloses address of the Entity or Individual associated with this profile.

  * <strong> address1* </strong> `string` </br> Address line 1.
  * <strong> address2 </strong> `string` </br> Address line 2.
  * <strong> city* </strong> `string` </br> The city name.
  * <strong> state </strong> `string` </br> The state name.
  * <strong> postalCode* </strong> `string` </br> The postal code.
  * <strong> country* </strong> `string` </br> The country name.

<strong> deliveryAddress </strong> `object`

JSON object descriptor that encloses delivery address associated with this profile.

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

Phone number associated with this profile.

<strong> dateOfBirth</strong> `string`

The date of birth of the registered individual.

<strong> dateOfFormation</strong> `string`

Date of formation refers to the date on which the entity has been officially registered.

<strong> email</strong> `email`

The email address associated with this profile. 

<strong> taxDetails </strong> `object`

JSON object descriptor that encloses tax related information for this profile.

  * <strong> registrationType*</strong> `enum` </br> Tax registration type applies to a person or an organization. Predefined `enum` values are `INDIVIDUAL┃ENTITY┃TRUST┃JOINT`. 

  * <strong> taxIdentification*</strong> `object` </br> JSON object descriptor that encloses tax documents identification details.
    * <strong> type</strong> `enum` </br> Type of legal tax document. Predefined `enum` values are `ssn┃giin┃itin┃ftin┃ein`. The variable must be equal to one of the values that have been predefined for it.
    * <strong> value</strong> `string` </br> Tax document identification number.

<strong> title</strong> `string`

In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.

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

JSON object descriptor that encloses primary signatory details for this profile.

  * <strong> id</strong> `string` <br> A unique identifier.
  * <strong> ownerId</strong> `string` <br> A unique identifier of the owner for this primary signatory. 
  * <strong> name</strong> `string` </br> Full name of the primary signatory. 
  * <strong> type</strong> `string` </br> Type of the primary signatory.
  * <strong> title</strong> `string` </br> In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.
  * <strong> isUSBased</strong> `boolean` <br> Has the value _true_ if the signatory resides in the US, or the value _false_ if the signatory resides outside of the US territory.
  * <strong> address</strong> `object` <br> JSON object descriptor that encloses physical address details of the primary signatory.
  
    * <strong> address1* </strong> `string` </br> Address line 1.
    * <strong> address2 </strong> `string` </br> Address line 2.
    * <strong> city* </strong> `string` </br> The city name.
    * <strong> state </strong> `string` </br> The state name.
    * <strong> postalCode* </strong> `string` </br> The postal code.
    * <strong> country* </strong> `string` </br> The country name.
  
  * <strong> phone</strong> `string` <br> Phone number associated with the primary signatory.
  * <strong> email</strong> `string` <br> Email address associated with the primary signatory.
  * <strong> taxDetails</strong> `object` <br> JSON object descriptor that encloses tax document details of the primary signatory.
    * <strong> type*</strong> `enum`  <br> Type of legal tax document. Predefined `enum` values are `ssn┃itin┃ftin`.
    * <strong> value*</strong> `string` <br> Unique identification number for the tax document.

  * <strong> dateOfBirth</strong> `string` <br> Date of birth of the primary signatory.
  * <strong> stateOfFormation</strong> `string` <br> State of formation if primary signatory is an Entity.
  * <strong> countryOfFormation</strong> `string` <br> Country of formation primary signatory is an Entity.
  * <strong> taxIdType</strong> `string` <br> Type of the tax identification.
  * <strong> taxId</strong> `string` <br> Unique tax identification number.

<strong> additionalSignatories</strong> `[object]`

JSON object descriptor that encloses additional signatories for this profile.

  * <strong> id</strong> `string` <br> A unique identifier.
  * <strong> ownerId</strong> `string` <br> A unique identifier of the owner for this additional signatory. 
  * <strong> name</strong> `string` </br> Full name of the additional signatory. 
  * <strong> type</strong> `string` </br> Type of the additional signatory.
  * <strong> title</strong> `string` </br> In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.
  * <strong> isUSBased</strong> `boolean` <br> Has the value _true_ if the signatory resides in the US, or the value _false_ if the signatory resides outside of the US territory.
  * <strong> address</strong> `object` <br> JSON object descriptor that encloses physical address details of the additional signatory.
  
    * <strong> address1* </strong> `string` </br> Address line 1.
    * <strong> address2 </strong> `string` </br> Address line 2.
    * <strong> city* </strong> `string` </br> The city name.
    * <strong> state </strong> `string` </br> The state name.
    * <strong> postalCode* </strong> `string` </br> The postal code.
    * <strong> country* </strong> `string` </br> The country name.
  
  * <strong> phone</strong> `string` <br> Phone number associated with the additional signatory.
  * <strong> email</strong> `string` <br> Email address associated with the additional signatory.
  * <strong> taxDetails</strong> `object` <br> JSON object descriptor that encloses tax document details of the additional signatory.
    * <strong> type*</strong> `enum`  <br> Type of legal tax document. Predefined `enum` values are `ssn┃itin┃ftin`.
    * <strong> value*</strong> `string` <br> Unique identification number for the tax document.

  * <strong> dateOfBirth</strong> `string` <br> Date of birth of the additional signatory.
  * <strong> stateOfFormation</strong> `string` <br> State of formation if additional signatory is an Entity.
  * <strong> countryOfFormation</strong> `string` <br> Country of formation additional signatory is an Entity.
  * <strong> taxIdType</strong> `string` <br> Type of the tax identification.
  * <strong> taxId</strong> `string` <br> Unique tax identification number.

</br>

<strong> beneficialOwner</strong> `object`

JSON object descriptor that encloses the details of beneficial owner for this profile.

> Individuals or natural people who ultimately owns this profile.

  * <strong> id</strong> `string` <br> A unique identifier.
  * <strong> ownerId</strong> `string` <br> A unique identifier of the owner for this beneficial owner. 
  * <strong> name</strong> `string` </br> Full name of the beneficial owner. 
  * <strong> type</strong> `string` </br> Type of the beneficial owner.
  * <strong> title</strong> `string` </br> In some settings, a person's title may consist of one or more words placed before or after their given name. There are a number of ways it might be used, including heredity, official status, or academic or professional certification.
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

<strong> masterEntityId</strong> `string`

<strong> ownerId</strong> `string`

<strong> bankingUser</strong> `object`

External Banking User.

  * <strong> id </strong> `string` </br>
  * <strong> accounts </strong> `[object]` </br> An _array_ list contains a set of `key:value` pairs.

<strong> purchaserStatus</strong> `[number]` An _array_ list of numbers.

<strong> createdAt</strong> `date-time` 

Timestamp for the creation of the profile.

<strong> updatedAt</strong> `date-time`

Timestamp for the last update record.

<strong> isDeleted</strong> `boolean`

Has the value true if the profile is deleted or the value false if it's not deleted.

<strong> brokerageAccount </strong> `object`

JSON object descriptor that encloses brokerage account details.

  * <strong> brokerName *</strong> `string` </br> Constraints Max 128 chars.
  * <strong> dtcNumber *</strong> `string` </br> Constraints Max 4 chars.
    > dtcNumber helps facilitate transactions between financial institutions.
  * <strong> accountNumber *</strong> `string` </br> Constraints Max 64 chars.

<strong> offPlatformAccounts </strong> `[object]`

  * <strong> routingNumber</strong> `string` </br> Routing number of a specified bank account.  Allowed pattern `[012346789][0-9]$`
  * <strong> bankName</strong> `string` </br> Name of a specified bank.
  * <strong> originatorName</strong> `string` </br> 
  * <strong> accountNumber</strong> `string` </br> Account number of a specified bank account.

<strong> additionalProperties </strong> `object`

JSON object descriptor for additional properties.

  * <strong> formedToInvestInFund</strong> `boolean`
  * <strong> isInvestmentCompany</strong> `boolean`
  * <strong> isExpatriate</strong> `enum`  Allowed enum values are `permanent┃temporary`.
  * <strong> jurisdiction</strong> `string`
  * <strong> fundDocumentTemplateId</strong> `string` 
  * <strong> passportOrId</strong> `string`