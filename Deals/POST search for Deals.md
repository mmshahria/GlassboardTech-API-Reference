Search API (POST method) uses the POST method to search the deals for the current users. It searches the deals based on the input parameters that are provided in the JSON format. The advantage of using the search API (POST method) over the search API (GET method) is that you can use any slot names to search the deals.

# Parameters

**perPage** `number`

The  total count of the list of search results returned per page. Specify the number of deals per page that the API call shall return.

**page**  `number`

The total count of the search results page. Specify number of page returned for the API call. 

**search** `[object]`


**sort** `[object]` 

Sort search results by the specified field, in either ascending or descending order.

- **field** `string` </br> 	Slot name based on which the search results are sorted For example, if the value of attributeName parameter is CLASS and the value of `direction` parameter is _ASC_, the search results are sorted in the ascending order based on the values of class slot.
- **direction** `enum` </br> Type of sorting. It can either be ascending or descending. The supported values are as follows `ASCENDING┃DESCENDING┃ASC┃DESC.`

**includes** `[object]`
Use case not defined.