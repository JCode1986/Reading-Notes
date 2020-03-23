# Things to know about static classes

## Notes
* Static classes always derive from object, you can’t specify a different base type
* Static classes cannot implement an interface
* Static classes cannot have any instance members
* Static classes can’t declare any constructors and the compiler doesn’t create a parameterless constructor by default
* Static classes are implicitly abstract, you can’t add the abstract modifier yourself
* Static classes may be generic
* Static classes may be nested, in either non-static or static classes
* Static classes may have nested types, either non-static or static
* Only static, top-level non-generic classes can contain extension method
