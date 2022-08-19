Replace existing asset records to the current user's data source based on the input parameters `key:value` pair that are supplied in the JSON format. Supply the unique `assetId` in the path parameter to execute an update operation to a specific asset resource for the current user.

# Parameters

<strong> name* </strong> `string` 

The Name of the Asset.A valid value must be 2 to 1024 characters.

<strong>description</strong> `string` <br>

The Description of the Asset.

<strong>unitCount</strong> `number`

The number of units on the asset.Constraints `Min 1`. Default value 1.

<strong>allocationAmount<strong> `number`

The amount of funds from the SPV allocated to the asset.Default value 0.

<strong>sector</strong> `string`

The market Sector associated with this asset.

<strong>size<strong> `string` <br>

String value to store the size of the asset.

<strong>category</strong> `string` <br>

The Category for the Asset.

<strong>advisors</strong> `string` <br>

The Advisors on the Asset.

<strong>assetUrl</strong> `string` <br>
The URL for the Asset.The assetUrl is auto-generated when you upload an asset file.
Pattern `[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)?`


<strong>appraisedValue<strong> `number`

The appraised value of an asset refers to the current assessed value by a professional appraiser. Constraints `Min 0┃ multiple of 0.01.`

<strong>fractionalOwnershipAmount</strong> `number`

The amount of Fractional Ownership for the Asset. Constraints `Min 0┃ multiple of 0.01.`


<strong>funding</strong> `object` 

JSON object descriptor that encloses the Funding object associated with this asset.

  * <strong>round<strong> `number` <br> The funding round.The funding round refers to the rounds of funding that startups go through to raise capital. The number representation of  pre-seed, seed, series A, B, C, etc.

  * <strong>targetRaiseAmount</strong> `number` <br> The estimated amount that the organizer is willing to raise. Constraints `multiple of 0.01`.
 
  * <strong>securityType</strong> `string` The type of the security.

  * <strong>preValuation</strong> `number` <br> The Pre valuation amount. Constraints `multiple of 0.01.` It is the process of valuing a company or asset prior to making an investment or obtaining finance.

  * <strong>noOfShare</strong> `number` <br> The number of shares in the funding round.

  * <strong>sharePrice</strong> `number` <br> The price of the shares in the funding round.Constraints `multiple of 0.01`.

<strong>revenueHistory</strong> `[string]`

Array Object descriptor that encloses the Historical Revenue associated with this asset.


<strong>costsHistory</strong> `[string]`

Array Object descriptor that encloses the Historical costs associated with this asset.

<strong>pitchDoc</strong> `string`

The pitch document storage path `string`.
> The visual document that tells investors what they need to know about the assets, business plan, products or services, fundraising needs, and key metrics like valuation, target market, and financial goals.

<strong>videoURL</strong> `string` <br>
The video storage path url associated the asset.

Constraints `2 to 1024 chars`.Allowed `string` character Pattern `[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)?`


<strong>logo</strong> `string`

The logo image path or storage path `string` for the asset.

> A logo is a graphic mark, emblem, or symbol that facilitates and promotes public identification and recognition of a corresponding asset. It may have an abstract or figurative design, or it may include the name it symbolizes as a wordmark.

<strong>banner<strong> `string`

The asset banner image storage path `string`. 

> Banner often contains visual advertising materials.

<strong>contact</strong> `object`

JSON object descriptor that encloses contact details associated with the asset.
  
  * <strong> name </strong> `string` <br> Full name of the contact person.

  * <strong>email</strong> `string` <br> A valid email address.

  * <strong>phone</strong> `string` <br> Phone number.

<strong>id</strong> `string`

The unique internal identifier to locate this asset.

<strong>ownerId*</strong> `string`

The unique identifier of the user who owns this object.

<strong>tenantId*</strong> `string`

A unique identifier used for API authentication and authorization.

<strong>dealId*</strong> `string`

A unique identifier of a deal. It references the interrelation between a asset and a deal.

<strong>type*</strong> `enum`

Type of the asset.Predefined `enum` values are `COMPANY┃REAL_ESTATE┃CRYPTOCURRENCY┃ARTWORK`.

<strong>subType</strong> `string`

Classification tier of an asset.

<strong>primaryContact</strong> `object`

JSON object descriptor that encloses primary contact details associated with the asset.

<strong>companyMarketSector</strong> `enum` 

The market sector of the company if the asset type is company. Predefined `enum` values for the market sectors are `COMMUNICATION_SERVICES┃CONSUMER_DISCRETIONARY┃CONSUMER_STAPLES┃ENERGY┃FINANCIALS┃HEALTHCARE┃INDUSTRIALS┃INFORMATION_TECHNOLOGY┃MATERIALS┃REAL_ESTATE┃UTILITIES`

<strong> details </strong> `[object]`

JSON array object descriptor that encloses details object reference associated with the asset. Each array index consists of a disparate object for specific details.

<strong> properties </strong> `[object]`

JSON array object descriptor that encloses properties object reference associated with the asset. Each array index consists of a disparate object for specific property details.

<strong>videoUrl</strong> `string` <br>
The video storage path url associated with the asset. Allowed `string` character Pattern `[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)?`

<strong>artist</strong> `object`

JSON object descriptor that encloses details of artist if the asset somehow relates to art that  include graphics, 3D models, sound effects, music, vehicles, head-up displays (HUDs), icons, etc.

* <strong>name<strong> `string` <br> Full name of the artist.
* <strong>location<strong> `string` <br> Location of the artist.
* <strong>images<strong> `[string]` <br>JSON array object descriptor that encloses the images. Each array index consists of storage `string` path to the image file.

<strong>team</strong> `[object]`

JSON  array object descriptor that encloses the team member details associated with the asset.

  * <strong>name</strong> `string` <br> Full name of the team member.
  * <strong>role</strong> `string` <br> Professional role in the team.
  * <strong>linkedInUrl</strong> `string` <br> LinkedIn profile url of team member.
  * <strong>email</strong> `string` <br> The email address of the team member.
  * <strong>phone</strong> `string` <br> The phone number of the team member.
  * <strong>image</strong> `string` <br> Profile image path url if any. Path `string` of the image.

<strong>invitedOrganizers</strong> `[string]`

JSON array object descriptor that encloses the details of invited organizers associated with the asset.

<strong>files</strong> `[string]`

JSON array object descriptor that encloses asset files storage `string` paths. Each array index consists of a `string` path to a specific file.

<strong>assetDocuments<strong> `object` 

JSON object descriptor that contains the asset documents.

* <strong>founderDocuments<strong> `[string]` </br> Array Object descriptor that encloses the list of founder legal documents or files associated with the asset.


<strong>images</strong> `[string]`

JSON array object descriptor that contains asset related images. Each array index consists of storage `string` path to the image file.

<strong>video</strong> `string`
The video storage path URL associated with the asset often contains advertising materials, if any. Allowed `string` character pattern `[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)?`.

<strong>isPublic</strong> `boolean`

Has the value _true_ if this asset is public, or the value _false_ if it is not.

<strong>founderIds</strong> `[string]` 

JSON object descriptor that encloses array list of founder's unique identifier if the asset consists of disparate founder. Each _array_ index consists of a unique identifier of a founder.

<strong>founderProfileId</strong> `string`

The ProfileId of the Founder of the asset.

<strong>foundersAssessment</strong> `object`

JSON object descriptor that encloses the founder assessment questions.

<strong>createdAt</strong> `date-time` 

Describes the date & time at which the asset was created. Data formatted as `1970-01-01T00:00:00.000Z.`.

<strong>updatedAt</strong> `date-time`

Describes the date & time at which the asset was last updated. Data formatted as `1970-01-01T00:00:00.000Z.`.

<strong>deletedAt</strong> `date-time`

Describes the date & time at which the asset was deleted. Data formatted as `1970-01-01T00:00:00.000Z.`.

<strong>isDeleted</strong> `boolean` 

Has the value _true_ if the asset is in the deleted status or the value _false_ if it's not in the deleted status.

<strong>assetTypeId<strong> `string` <br> The Unique asset type identification.

<strong>additionalProperties</strong> `object`

JSON object descriptor that encloses additional properties related to the asset.

