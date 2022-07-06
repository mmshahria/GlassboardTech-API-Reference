
Retrieves the list of deals for the current user. This endpoint returns data based on the authorized access level of the current user.

# Attributes

<strong> data </strong> `[object]`

Simple descriptor for the JSON _array_ object. It encloses the list of deals.

* <strong> profileId* </strong> `string`

A unique identifier assigned by the system while creating a **organizer** profile as an individual or an entity.


* <strong> minInvestmentAmount* </strong> `number`

A minimum investment amount (in the currency predefined) in a deal that restricts investors from investing below this amount.

* <strong> previouslyRaisedAmount </strong> `number`

The total amount (in the currency predefined) raised previously for the deal or the portfolio company.  Minimum required value is 0 while used as parameter.

* <strong> totalPurchaseAmount </strong> `number`

Use case undefined.

* <strong> organizerCarryPercentage </strong> `number`

Carry Percentage means the rate of return percentage above the initial investment after one year that needs to be paid to a deal **organizer**. It is in the deal **organizer's** discretion as to whether the Carry Percentage will be lower, and such determination may be made up until the date of the Initial Closing. The Carry Percentage equals the sum of organizer Carry Percentage and Additional Carry Percentage. 

_Data-type_ `number` is used for any numeric type, either integers or floating point numbers. A valid _value-range_ is 0 to 100.

* <strong> additionalCarryRecipients </strong> `[object]`
Additional carry recipients details. Data returned as JSON _array_ object. 
    * <strong> individual </strong> `object`</br> Additional carry recipients can either be any _individual_ or any other organizer.  
        * <strong> id </strong> `string` </br> A unique identifier for additional carry recipent specified by a deal organizer for this deal.
        * <strong> ownerId </strong> `string` </br> A unique identifier for the owner id.
        * <strong> name </strong> `string` </br> Full name of the additional carry recipient specified by a deal **organizer**. A valid value must be 2 to 1024 characters.
        * <strong> type </strong> `string` </br> Type of the additional carry recipient. Can be of two types individual or entity.
        * <strong> title </strong> `string` </br> Use case 
        * <strong> isUSBased </strong> `boolean` </br> Has the value _true_ if the carry recipient is based on U.S. or the value _false_ if the recipient is based on other countries.
        *   <strong> address </strong> `object` </br> Additional carry recipient's address. Data Returned as JSON object.
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

    *   <strong> stateOfFormation </strong> `string` </br> The State in Which the deal was formed.
    *   <strong> countryOfFormation </strong> `string` </br> The State in Which the deal was formed.
    *   <strong> taxIdType </strong> `string` </br> Can be useful for defining the type of tax identification document. 
    *   <strong> taxId</strong> `string` Can be useful to keep records of tax identification specified by a deal **organizer** for an additional carry recipient.


    *   <strong> carryPercentage </strong> `number` </br> Additional carry percentage specified by a deal _organizer_. 

_Data-type_ `number` is used for any numeric type, either integers or floating point numbers. Minimum valid _value-range_ is 0 to 100.


* <strong> name* </strong> `string`
A specified deal's _name_ often useful for displaying to <strong>investors</strong> or end users.


* <strong> description </strong> `string`
The description of the deal.HTML format is supported.

* <strong> targetRaiseAmount* </strong> `number`

A target amount (in the currency predefined) is specified by an <strong> organizer </strong> for a deal to raise investment. _Data-type_ `number` is used for any numeric type, either integers or floating point numbers. Minimum valid value is 0 while used as parameter for creating a deal.

* <strong>disabled </strong> `boolean`

Has the value _true_ if a deal exists for raising investment or the value _false_ if a deal is closed. 

* <strong> estimatedCloseDate </strong> `date-time`

An expected close date and time specified by an **organizer** for this deal.

* <strong> marketing </strong> `object`
A Set of `key-value` pairs that is assigned to this JSON _object_ contains all the information related to marketing. This can be useful for storing additional information in a structured format.
      
   * <strong>logo</strong> `string`
  >A logo is a graphic mark, emblem, or symbol that facilitates and promotes public identification and recognition of a corresponding deal's business entity. It may have an abstract or figurative design, or it may include the name it symbolizes as a wordmark.
   * <strong>tagline</strong> `string`
  >A tagline is a catchphrase or memorable statement associated with the corresponding deal's business entity.


* <strong> portfolioCompanyName </strong> `string`

A specified portfolio company name for a deal assigned by an **organizer**. Portfolio company often refers to the company for which a deal _organizer_ raising the investments and in which investors invest their money. A valid value must be 2 to 1024 characters.

* <strong> portfolioCompanyState </strong> `string`

A specified state address of the portfolio company for specific deal assigned by a deal **organizer**. Portfolio company often refers to the company for which a deal _organizer_ raising the investments and in which investors invest their money. A valid value must be 2 to 1024 characters.

* <strong> portfolioCompanyEntity </strong> `enum`

Portfolio company entity refers to the different legal entity types of the portfolio company that is specified by a deal **organizer**. 

_Data-type_ `enum` consists of predefined legal business entity type values

`LIMITED_LIABILITY_COMPANY┃LIMITED_PARTNERSHIP┃C_CORPORATION┃S_CORPORATION ┃ GENERAL_PARTNERSHIP ┃ FOREIGN_ENTITY ┃ CORPORATION.` 

The variable must be equal to one of the values that have been predefined for it.


* <strong> securityType </strong> `enum`
Securities are a way for investors to make money by lending them to companies and governments. By buying a share or a bond, an investor is voting for that company's future growth. Securities inject money into the economy, helping both the investor and the issuer. 
_Data-type_ `enum` consists of predefined security type values

`COMMON_STOCK┃PREFERRED_STOCK┃CONVERTIBLE_PROMISSORY_NOTE┃SAFE┃SAFT┃SAFE-T┃LLC_MEMBERSHIP_UNITS┃LP_MEMBERSHIP_UNITS┃CRYPTOCURENCY┃OTHER.` 

The variable must be equal to one of the values that have been predefined for it.

* <strong> isPublic </strong> `boolean`

Has the value _true_ if a deal is visible to public investors for raising investment or the value _false_ if a deal is visible only to the privately invited investors. Can be useful to compare public or private company.


* <strong> requireQualifiedPurchaser </strong> `boolean`

Has the value _true_ if a deal organizer is looking for qualified investors in the platform or the value _false_ if it is not required.

* <strong>id </strong> `string`

A unique identifier for a specified deal.

* <strong> ownerId </strong> `string`

A unique identifier of the owner for a specified deal, and often refers to a deal <strong>organizer</strong>.

* <strong> tenantId </strong> `string`

A unique identifier used for API authentication and authorization. Can be useful for this API's end users.

* <strong> entityId </strong> `string`

A unique identifier for an _entity_.

* <strong> assetIds </strong> `[string]`

A list of unique identifiers for assets. Data returned as an _array_ list.

* <strong> files </strong> `[string]`

A list of URLs  or file paths referencing the files attached to this deal by an _organizer_, meant to be displayable to the investors. Values are returned as an _array_ list.

* <strong> organizerFiles </strong> `[string]`

A list of URLs or file paths referencing the files attached to this deal by an _organizer_. Values are returned as an _array_ list.

* <strong> portfolioCompanyContact </strong> `object` 

Contact details of the portfolio company. Can be useful to store additional contact details of a portfolio company as a set of `key:value` pairs.

* <strong> status* </strong> `enum`

Describes the deal’s current status. 

_Data-type_ `enum` consists of predefined status values `DRAFT┃IN-PROVISIONING┃OPEN┃IN CLOSING┃CLOSED.` The variable must be equal to one of the values that have been predefined for it while updating the deal _status_.


* <strong> createdAt </strong> `date-time`

Describes the date & time at which the deal was created. Data formatted as `1970-01-01T00:00:00.000Z`

* <strong> updatedAt </strong> `date-time`

Describes the date & time at which the deal was last updated. Data formatted as `1970-01-01T00:00:00.000Z`.

* <strong> ownersDealUrl </strong> `string`

Use case undefined.

* <strong> deletedAt </strong> `date-time`

Describes the date & time at which the deal was deleted. Data formatted as `1970-01-01T00:00:00.000Z`


* <strong> isDeleted </strong> `boolean`

Has the value _true_ if a specified deal is deleted by the deal **organizer** or the value _false_ if the deal has other __status__.


* <strong> additionalProperties </strong> `object` <br> A set of `key:value` pairs representing additional properties for this deal. Enclosed data body must be in JSON format.

* <strong> taxData </strong> `object` <br> A set of `key:value` pairs representing tax related information.

* <strong> importedSource </strong> `string` <br> Use case undefined.

* <strong> importedDate</strong> `date-time ┃ null` <br> Use case undefined.

* <strong> estimatedCloseCount </strong> `number` <br> Use case undefined.

<strong>page</strong> `number`

The number of page returned for the API call. This attribute can be used as a query string parameter.

<strong>perPage</strong> `number`

The total count of deals returned per page. This can be specified as a query string parameter.

<strong>totalCount</strong> `number`

Total count of the deals list the API call returned.