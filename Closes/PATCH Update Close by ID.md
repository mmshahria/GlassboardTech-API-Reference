Partially modify existing close records based on the supplied `key:value` pairs in the JSON format. Supply the unique `closeId` in the path parameter to execute a partial update operation to a specific close for the current user.

# Parameters

<strong>id<strong> `string`

A unique internal identifier to locate this close.

<strong>ownerId<strong> `string`

The unique internal owner identifier for this close.

<strong>tenantId<strong> `string`

A unique identifier used for API authentication and authorization.

<strong>organizerSignature<strong> `string`

Organizer's signature in the specified document for this closing. _dataType_ binary-encoded base64 `string`.

<strong>fundManagerSignature<strong> `string`

Fund Managers's signature in the specified document for this closing. _dataType_ binary-encoded base64 `string`.

<strong>files<strong> `[string]`

JSON array Object descriptor that encloses the list of legal documents or files associated with this close.

<strong>dateClosed<strong> `date-time`

The date and time at which a particular deal was closed.

<strong>fundsWiredDate<strong> `date-time`

The Date and time at which the funds were wired.

<strong>readyToCounterSign<strong> `boolean`

Has the value _true_ if the legal documents associated with this close are ready to Countersign;otherwise, the value is _false_.

> A countersignature is an extra signature that is added to a contract or other document that has already been signed.

<strong>fundManagerSigned<strong> `boolean`

Has the value _true_ if the fund manager signed in the specified legal documents for this closing;otherwise, the value is _false_.

<strong>needsApproval<strong> `boolean`

Checks whether this close needs approval. Has the value _true_ if this particular close needs approval; otherwise, the value is _false_.

<strong>blueSky<strong>`object`

JSON Object descriptor that encloses the blue sky information associated with this close.
* <strong>filedDate<strong> `object`
JSON Object descriptor encloses the timestamp at which the blue sky filing was completed.

<strong>purchaseDocsSignedDate<strong> `date-time`

The Date and time at which the purchase docs were signed.

<strong>statement<strong>`object`

JSON object descriptor that describes the statement for this close.

<strong>createdAt<strong> `date-time`

Timestamp for the creation of the close.

<strong>sequence<strong> `number`

Sequence number associated with this close.

<strong>status<strong>`object`

JSON object descriptor that describes the current status for this close.

<strong>updatedAt<strong> `date-time`

Timestamp for the last update record for this close.

<strong>feesPaymentTransferId<strong> `string`

A unique internal fees Payment Transfer identifier for this close.

<strong>blueSkyPaymentTransferId<strong> `string`

A unique internal identifier of the blue Sky Payment Transfer for this close.

<strong>formDFiledDate<strong> `date-time`

The Date and time at which the Form-D filing was completed.

<strong>blueSkyPaidDate<strong> `date-time`

The Date and time at which the blue sky fees were paid.

<strong>blueSkyReceipt<strong> `string`

Blue Sky Receipt Number for this close.

<strong>deletedAt<strong> `date-time`

The date & time at which the close was deleted.

<strong>entityId<strong> `string`

A unique internal identifier of the entity associated with this close.

<strong>dealId<strong> `string`

A unique internal identifier of the deal associated with this close.

<strong>isDeleted<strong> `boolean`

Has the value _true_ if this particular close is deleted; otherwise, the value _false_.

<strong>formDFileNumber<strong> `string`

Form-D File Number associated with this close. Constraints `Max 64 chars`.