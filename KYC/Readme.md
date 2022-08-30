Background and Monitored Lists checks for KYC. Know Your Customer - A standard due diligence process used to assess and monitor customer risk and verify a customer’s identity. Typically referenced in conjunction with AML (Anti-Money Laundering, definition above) as “KYC/AML”.

KYC resource currently supports two types of validation check :

1. Data to Check
2. Profile to Check

It's important to note that each validation check requires valid data from user.

> Know your customer (KYC) is an investment industry standard that aims to assist investment advisors understand more about their customers' financial backgrounds, investing expertise, and risk tolerance.

# KYC RESPONSE MODEL

</strong> Kyc </strong> `object`

JSON object descriptor for the response body of `/kyc` endpoint.

   * <strong>id</strong> `string` <br> A unique identifier for the KYC object.
   * <strong>tenantId</strong> string <br> A unique identifier used for API authentication and authorization. Can be useful for this API's end users.
   * <strong>createdAt</strong> `date-time` <br>  Describes the date & time at which the KYC check request was created. Data formatted as `1970-01-01T00:00:00.000Z`
   * <strong>updatedAt</strong> `date-time` <br> Describes the date & time at which the KYC check request was last updated. Data formatted as `1970-01-01T00:00:00.000Z`
   * <strong>status*</strong> `enum` <br> Current status for the request of KYC check. Valid statuses are `IN_PROGRESS┃COMPLETE┃EXCEPTION`. 
   * <strong>resultDetail</strong> `object` <br> JSON object descriptor that encloses the results of KYC check.
     * <strong>adverseMedia</strong> `enum` <br> An adverse media check or adverse media screening is a broad-based media and press search of a candidate's background via global electronic media sources. Valid statuses from adverse media check are `IN_PROGRESS┃COMPLETE┃EXCEPTION`
     * <strong>monitoredLists</strong> `enum` <br> Valid result statuses are `IN_PROGRESS┃COMPLETE┃EXCEPTION`
     * <strong>politicallyExposedPerson</strong> `enum` <br> Check if politically exposed person. Valid result statuses are `IN_PROGRESS┃COMPLETE┃EXCEPTION`. 
     * <strong>sanction</strong> `enum` <br> Checks the sanction background of the individual. Valid result status are `IN_PROGRESS┃COMPLETE┃EXCEPTION`. 

   * <strong>providerMeta*</strong> `object` <br> JSON object descriptor that encloses important validation check results from 3rd party KYC validators.
   * <strong>applicantId</strong> `string` <br> A unique identifier for the applicant of KYC check.
   * <strong>checkId</strong> `string` <br> The unique identifier records the type of check done on a particular profile.
   * <strong>reason</strong> `string` <br> Additional KYC check reason.
   * <strong>result</strong> `string` <br> Result of the KYC check.
   * <strong>profileId</strong> `string` <br> A unique identifier of the profile on which the KYC was run.
   * <strong>ownerId</strong> `string` <br> The unique identifier of the user who owns this object.
   * <strong>overrideComment</strong> `string` <br> Overridden comment,if any.
   * <strong>migratedToId</strong> `string` <br> New Id to which the individual has been migrated.