json-stringify
======

Works exactly the same as the Go tool `stringer`, but instead of producing
methods that output the const as-is, it will hyphenate and lowercase the const
name.

For example, given the following constants:

```
type UserType

const (
  User UserType = iota
  AdminUser
  
)
```

The output will be `user` and `admin-user`, instead of `User` and `AdminUser`.

This tool is entirely to make my life simpler when dealing with JSON, which
normally deals with lower-cased & hyphenated names, instead of Go's CamelCase.
