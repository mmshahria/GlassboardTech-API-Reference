Retrieves a count of investors per state, the amount invested per state, and the date of the first investment for a valid identifier. Supply the unique `closeId` in the path parameter, and this endpoint will respond to the corresponding Blue sky fees details for the current user.

# Attributes

<strong>stateSummaries<strong> `[object]`

JSON Array Object descriptor that encloses the list of state summaries associated with this close. Each _array_ index consists of a count of investors per state and the amount invested per state.

<strong>firstInvestmentDate<strong> `date`

The date of the first investment for this close. Data type ISO 8601 format `YYYY-MM-DD`.


<strong>totalNASAAFee<strong> `number`

Total number of NASAA fee for this close.