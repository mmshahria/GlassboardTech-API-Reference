
Partially modify an existing deal resource  based on the input parameters `key:value` pair that are supplied in  JSON format. Supply the unique `dealId` from either a deal creation request or the deal lists. Our API will update the specified deal information according to the supplied data. 

> PATCH is a method of modifying resources where the client sends partial data that is to be updated without modifying the entire data.

# Parameters

<strong> profileId* </strong> `string`

A unique identifier assigned by the system while creating a **organizer** profile as an individual or an entity.

<strong> minInvestmentAmount* </strong> `number`

A minimum investment amount (in the currency predefined) in a deal that restricts investors from investing below this amount. Minimum required value is 0 while used as parameter.

<strong> previouslyRaisedAmount </strong> `number`

The total amount (in the currency predefined) raised previously for the deal or the portfolio company.  Minimum required value is 0 while used as parameter.

<strong> totalPurchaseAmount </strong> `number`

Use case undefined.

<strong> organizerCarryPercentage </strong> `number`

Carry Percentage means the rate of return percentage above the initial investment after one year that needs to be paid to a deal **organizer**. It is in the deal **organizer's** discretion as to whether the Carry Percentage will be lower, and such determination may be made up until the date of the Initial Closing. The Carry Percentage equals the sum of organizer Carry Percentage and Additional Carry Percentage. 

_Data-type_ `number` is used for any numeric type, either integers or floating point numbers. A valid _value-range_ is 0 to 100.

<strong> additionalCarryRecipients </strong> `[object]` </br>
Additional carry recipients details. Data returned as JSON _array_ object. 
* <strong> individual </strong> `object`</br> Additional carry recipients can either be any _individual_ or any other organizer.  
    * <strong> id </strong> `string` </br> A unique identifier for additional carry recipient specified by a deal organizer for this deal.
    * <strong> ownerId </strong> `string` </br> A unique identifier for the owner id.
    * <strong> name </strong> `string` </br> Full name of the additional carry recipient specified by a deal **organizer**. A valid value must be 2 to 1024 characters.
    * <strong> type </strong> `string` </br> Type of the additional carry recipient. Can be useful to define the type of carry recipients.
        * <strong> title </strong> `string` </br> Use case undefined.
    * <strong> isUSBased </strong> `boolean` </br> Has the value _true_ if the carry recipient is based on U.S. or the value _false_ if the recipient is based on other countries.
    *   <strong> address </strong> `object` </br> Additional carry recipient's address object.
        * <strong> address1* </strong> `string` </br> Address line 1 (e.g., street, PO Box, or company name).
        * <strong> address2 </strong> `string` </br> Address line 2 (e.g., apartment, suite, unit, or building).
        * <strong> city* </strong> `string` </br> City, district, suburb, town, or village.
            * <strong> state </strong> `string` </br> State, county, province, or region.
        * <strong> postalCode* </strong> `string` </br> ZIP or postal code.
        *  <strong> country* </strong> `string` </br> Can be used for full country name or Two-letter country code.
*   <strong> phone </strong> `string` </br> Additional carry recipients phone number.
*   <strong> email </strong> `string` </br> Additional carry recipients email address.
*   <strong> taxDetails `object` </strong> 
    *   <strong> type* </strong> `enum` </br> Type of tax identification document. _Data-type_ `enum` consists of predefined type values `ssn┃itin┃ftin.`
    *   <strong> value* </strong> `string` </br> Contains Alphanumeric value of the tax document identification.
*   <strong> dateOfBirth </strong> `string` </br> Date of birth of this additional carry recipient. Data must be formatted as _YY-MM-DD_.
*   <strong> stateOfFormation </strong> `string` </br> The state of formation if the carry recipient is an entity.
*   <strong> countryOfFormation </strong> `string` </br> The country of formation if carry recipient is an entity.
*   <strong> taxIdType </strong> `string` </br> Can be useful for defining the type of tax identification document. 
*   <strong> taxId</strong> `string` Can be useful to keep records of tax identification specified by a deal **organizer** for an additional carry recipient.
* <strong> carryPercentage </strong> `number` </br> Additional carry percentage specified by a deal _organizer_. _Data-type_ `number` is used for any numeric type, either integers or floating point numbers. Value can not exceed 20.

 <strong> name* </strong> `string`

A meaningful name for this deal, often useful for displaying to investors.

  <strong> description </strong> `string`
The description for this deal. Supports HTML format.

  <strong> targetRaiseAmount* </strong> `number`

A target amount (in the currency predefined) is specified by an <strong> organizer </strong> for a deal to raise funds. _Data-type_ `number` is used for any numeric type, either integers or floating point numbers. Minimum valid value is 0 while used as parameter.

  <strong>disabled </strong> `boolean`

Has the value _true_ if a deal exists for raising funds or the value _false_ if a deal is closed. 

 <strong> estimatedCloseDate </strong> `date-time`

An expected close date and time this deal.

 <strong> marketing </strong> `object`

A Set of `key-value` pairs representing marketing related information. This can be useful for storing additional information in a structured format.
      
   * <strong>logo</strong> `string` <br>
  > A logo is a graphic mark, emblem, or symbol that facilitates and promotes public identification and recognition of a corresponding deal's business entity. It may have an abstract or figurative design, or it may include the name it symbolizes as a wordmark.

   * <strong>tagline</strong> `string`
   > A tagline is a catchphrase or memorable statement associated with the corresponding deal's business entity.

 <strong> portfolioCompanyName </strong> `string`

Portfolio company name for this deal.

> Portfolio company often refers to the company for which a deal _organizer_ raising the funds for and in which investors invest their money. A valid value must be 2 to 1024 characters.

 <strong> portfolioCompanyState </strong> `string`

The state address of the portfolio company. A valid value must be 2 to 1024 characters.

 <strong> portfolioCompanyEntity </strong> `enum`

The entity types of the portfolio company. 

Accepted `enum` values are `LIMITED_LIABILITY_COMPANY┃LIMITED_PARTNERSHIP┃C_CORPORATION┃S_CORPORATION ┃ GENERAL_PARTNERSHIP ┃ FOREIGN_ENTITY ┃ CORPORATION`.

The variable must be equal to one of the values that have been predefined for it.


 <strong> securityType </strong> `enum`

The type of the security for this deal. Predefined `enum` security type values are `COMMON_STOCK┃PREFERRED_STOCK┃CONVERTIBLE_PROMISSORY_NOTE┃SAFE┃SAFT┃SAFE-T┃LLC_MEMBERSHIP_UNITS┃LP_MEMBERSHIP_UNITS┃CRYPTOCURENCY┃OTHER`. The variable must be equal to one of the values that have been predefined for it.

> Securities are a way for investors to make money by lending them to companies and governments. By buying a share or a bond, an investor is voting for that company's future growth. Securities inject money into the economy, helping both the investor and the issuer. 

  <strong> isPublic </strong> `boolean`

Has the value _true_ if a deal is visible to public investors for raising funds or the value _false_ if a deal is visible only to the privately invited investors.

  <strong> requireQualifiedPurchaser </strong> `boolean`

Has the value _true_ if a deal organizer is looking for qualified investors in the platform or the value _false_ if it is not required.

 <strong>id </strong> `string`

A unique identifier for a specified deal.

  <strong> ownerId </strong> `string`

A unique identifier of the owner for this deal. 

 <strong> tenantId </strong> `string`

A unique identifier used for API authentication and authorization.

  <strong> entityId </strong> `string`

A unique identifier for an _entity_.

  <strong> assetIds </strong> `[string]`

A list of unique identifiers for assets.

  <strong> files </strong> `[string]`

A list of URLs  or file paths referencing the files attached to this deal by an _organizer_, meant to be displayable to the investors. Values are returned as an _array_ list.

  <strong> organizerFiles </strong> `[string]`

A list of URLs or file paths referencing the files attached to this deal by an _organizer_. Values are returned as an _array_ list.

  <strong> portfolioCompanyContact `object` </strong>

Contact details of the portfolio company. A set of `key:value` pairs representing essential contact details of the portfolio company.

  <strong> status* </strong> `enum`

The current status of the deal. Predefined `enum` values are `DRAFT┃IN-PROVISIONING┃OPEN┃IN CLOSING┃CLOSED.` The variable must be equal to one of the values that have been predefined for it while updating the deal _status_.

  <strong> createdAt </strong> `date-time`

Describes the date & time at which the deal was created. Data must be formatted as `1970-01-01T00:00:00.000Z`

  <strong> updatedAt </strong> `date-time`

Describes the date & time at which the deal was last updated. Must be formatted as `1970-01-01T00:00:00.000Z`.

  <strong> ownersDealUrl </strong> `string`

The deal url reference the owners.

 <strong> deletedAt </strong> `date-time`

Describes the date & time at which the deal was deleted. Must be formatted as `1970-01-01T00:00:00.000Z`


  <strong> isDeleted </strong> `boolean`

Has the value _true_ if a specified deal is deleted by the deal **organizer** or the value _false_ if the deal has other __status__.

  <strong> additionalProperties </strong> `object`

A set of `key:value` pairs representing additional properties for this deal. Enclosed data body must be in JSON format.

  <strong> taxData </strong> `object`

A set of `key:value` pairs representing tax related information.

  <strong> importedSource </strong> `string`

Use case undefined.

  <strong> importedDate</strong> `date-time ┃ null`

Use case undefined.

  <strong> estimatedCloseCount </strong> `number`

The total count of closed investors for a deal by the `organizer`