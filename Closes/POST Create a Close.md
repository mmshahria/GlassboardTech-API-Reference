
Initiates a request to create a new `closing` for the specified deal. Supply the `key:value` pairs that are required for a `closing` in the request body to execute a `closing` creation operation. Data in the request body should follow the JSON data formatting.

# Parameters

<strong>dealId*<strong> `string`

A unique internal identifier to locate a particular deal on which the closing will perform.

<strong>organizerSignature*<strong> `string`

Organizer's signature in the specified document for this closing. _dataType_ binary-encoded base64 `string`.

<strong>statement<strong>`object`

JSON object descriptor that describes the statement associated with closing.

<strong>subscriptions<strong> `[string]`

JSON array object description that encloses the list of all subscriptions associated with this closing.
