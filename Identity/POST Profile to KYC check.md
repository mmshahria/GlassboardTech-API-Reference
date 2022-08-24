Profile identity check to validate the authenticity using supplied `profileId` and respond with multiple statuses throughout its lifetime as it progresses through the verification flow. Supply the `profileId` of an existing profile in the request body and our API will respond with the corresponding identity validation results.


# Parameters

<strong> Profile to KYC Check </strong> `object`

<strong>profileId*</strong> `string`

Specify the unique identifier of an existing profile on which the check will run.