* [[Go]] is a compiled language
* Go run compiles the source code from one or more source files whose names end in .go, links it with libraries, then runs the resulting executable file.
* A package consists of one or more .go source files in a single directory that define what the package does.
* Package main is special.
* It defines the standalone executable from the language.
* Program does not compile on unused imports ( to reduce unneeded references )
* No semicolons needed unless we need to have two or more statements on the same line
* For loop is the only loop statement in Golang
* A map holds a set of key/value pairs
* Provides constant-time operations to store, retrieve, or test for an item in the set.
* The key may be of any type whose values can compared with == strings being the most common example;
* The value may be of any type at all.
* The order of map iteration is not specified, but in practice it is random, varying from one run to another.
* This design is intentional, since it prevents programs from relying on any particular ordering where none is guaranteed.
* In Go there is no such thing as an uninitialized variable
* `var name type = expression` of these either type or expression can be omitted but not both
* The Zero value of an array or struct is the zero value of all its elements
* `:=` is a declaration while `=` is an assignment
* A short variable declaration `:=` does not necessarily declare all the variables on its LHS, the ones in scope are just assigned
* Not every value has an address but every variable does
* Each component of a variable of an aggregate type is a variable itself and hence each of those has an address
* Perfectly fine for a function to return a pointer to a variable. The pointer will remain be in scope even when the function returns.
* `new` is a method not a keyword hence it can be overwritten within code
* to check if variable X can be reclaimed, check whether there is a path from all active variables to X, if not reclaim it
* A named type is an alias of the reference type, seperation of incompatible usages from base type
* Conversion from one type to another is allowed only if both have the same underlying type or both are pointers to variables of the same underlying type. Basically the internal represnetation of the values should not change by type conversion
* A conversion never fails at run time
* Each package serves as a separate namespace for its declarations
* `init` functions within each file can contain initialization statements for the go file
* Initialization works from bottom up, `main` package is the last to be initialized
* number of set bits in a value is called its `population count`
* Scope is a region of code where a use of a variable refers to that declaration
* Lifetime of a variable is the range of time when the variable can be referred by other programs
* Scope is a compile time property, Lifetime is a run time property
* The compiler when it encounters reference to a variable starts from the nearest scope first and moves to universal scope
* Hence, variables can be shadowed