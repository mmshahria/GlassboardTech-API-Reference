Initiates a request to Add the specified role mappings for the user.Supply the unique `userId` in the path parameter to execute the create operation to a specific role mapping for the current user (API end-user).

> Role mappings specify which roles are allocated to each individual user. Each mapping comprises rules that identify users and a list of the roles provided to those individuals.

# Parameters

<strong>roles<strong> `[object]`

JSON array object descriptor that encloses an array list of user roles. Each _array_ index consists of a disparate user role.

<strong>id<strong> `string`

A unique internal identifier to locate this user role mapping.

<strong>name<strong> `string`

A unique role name used to identify this user role mapping.