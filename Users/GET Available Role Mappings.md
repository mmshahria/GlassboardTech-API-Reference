Retrieves the current and available role mappings for the specified user.Supply the unique `userId`, and this endpoint will respond to the corresponding role mappings for the specified user.
# Parameters

<strong>roleMappings<strong> `[object]`

JSON array object descriptor that encloses an array list of role mappings. Each _array_ index consists of a disparate user role mapping.

> Role mappings specify which roles are allocated to each individual user. Each mapping comprises rules that identify users and a list of the roles provided to those individuals.

* <strong>id<strong> `string`

A unique internal identifier to locate this user role mapping.

* <strong>name<strong> `string`

A unique role name used to identify this user role mapping.Example: `investor` , `view-consent` , `founder`.

* <strong>composite<strong> `boolean`

Has the value true if composite role is mapped to this user; otherwise, the value is false.

> Any realm- or client-level position can be transformed into a composite role. A composite role is a role that also has one or more other roles attached to it. When a composite role is mapped to a user, that individual also acquires the roles associated with that composite. Since this inheritance is recursive, any composite of composites also inherits.

* <strong>containerId<strong> `string`

ContainerId represents a globally unique identifier for a Container in the cluster for this role mapping.Container represents an allocated resource in the cluster.

* <strong>description<strong> `string`

Role mapping description.

