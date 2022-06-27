Data check to validate the authenticity of supplied data and respond with multiple statuses throughout its lifetime as it progresses through the verification flow. Supply the unique identifying information of an individual in the request body, and our API will respond with the corresponding identity validation results.

> In order to perform `/identity/kyc` validation, the following fields must be configured with valid values.

# Parameters

<strong> Data to KYC Check </strong> `object`

Data to KYC check includes the applicant's name, address, email address, date of birth, and identification Number, etc.

<strong> firstName* </strong> `string`

Specify the first name of the applicant. Valid values 2 to 1024 characters.

<strong>lastName*</strong> `string`

Specify the last name of the applicant. Valid values 2 to 1024 characters.


<strong>address*</strong>

Specify the current address of the applicant.

The following characters will be filtered from all fields `!$%^*=<>`

<strong>street1*</strong> `string`

Specify the street address of applicant.


<strong>street2</strong> `string`

Specify additional street address of the applicant if available.


<strong>city</strong>* `string`

Specify the city, the applicant currently residing in.


<strong>region*</strong> `string`

Specify the regional address of the applicant.

<strong>postalCode*</strong> `string`

The postcode (ZIP code) of the applicant's address. Constraints: 2 to 1024 chars.

For UK postcodes, specify the value in the following format: `SW4 6EH.`
For US postcodes, use ZIP format: `84121`


<strong>country*</strong>: `enum`

Specify the full name of the country, the applicant currently residing in.


<strong>email</strong> `string`

Specify the current email address of the applicant.

<strong>dateOfBirth*</strong> `date`

Specify the date of birth of the applicant.Data formatted as _YY-MM-DD_.

<strong>identificationNumbers*</strong> `[object]`

JSON object descriptor for government-issued numeral or string of numerals used for validating the authenticity of government-issued identity documents.

<strong>type*</strong> `enum`

Specify the valid type of government issued document. Valid `enum` values are `ssn┃social_insurance┃tax_id┃identity_card┃driving_license`

<strong>value*</strong> `string`

Specify the identification number corresponding to the type of document.Type of `ssn` supports both the full SSN or the last 4 digits. If the full SSN is provided then it must be in the format `xxx-xx-xxxx.`

<strong> state </strong> `enum`

Specify the state that issued the document. Valid `enum` values are.
`AR┃DC┃DE┃FL┃GA┃KS┃LA┃MD┃MO┃MS┃NC┃OK┃SC┃TN┃TX┃WV┃AL┃CT┃IA┃IL┃IN┃ME┃MI┃MN┃NE┃NH┃NJ┃NY┃OH┃RI┃VT┃WI┃CA┃CO┃NM┃NV┃UT┃AZ┃ID┃MT┃ND┃OR┃SD┃WA┃WY┃HI┃AK┃KY┃MA┃PA┃VA`

Only required for the `driving_licence` type in United States of America