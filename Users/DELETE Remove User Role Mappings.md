Removes the specified role mappings for the user. Supply the unique `userId` in the path parameter to execute the delete operation to a specific role mapping for the current user (API end-user).

# Parameters

<strong>roles<strong> `[object]`

JSON array object descriptor that encloses an array list of user roles. Each _array_ index consists of a disparate user role.

<strong>id<strong> `string`

A unique role name used to identify this user role mapping.Example: `investor` , `view-consent` , `founder`.

<strong>name<strong> `string`

A unique role name used to identify this user role mapping.