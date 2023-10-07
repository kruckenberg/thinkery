# Variables
- Initialized with keyword `let`
- By default, variables are immutable.
- Can be made mutable with additional keyword `mut`
- Scalar types and a few fixed-size composite types are stored on the stack; everything else is stored in the heap.
- An in-scope (immutable) variable can be re-initialized with keyword `let` and "shadow" the prior initialization.

# Ownership & Borrowing
Ownership model (including borrowing) make it possible to let the compiler handle most memory management in a safe way without needing a runtime garbage collector. By enforcing rules about how values are used and passed around, memory allocations and de-allocations need not be manually coded.

## Ownership rules
  - Each value in Rust has an owner.
  - There can only be one owner at a time.
  - When the owner goes out of scope, the value will be dropped.

Coda:
- Stack-stored values (which seems, more or less, to mean values with the `Copy` trait) are shallow copied on assignment (including passing the value as an argument to a function). Therefore there's no real concern about ownership.

## Borrowing
Rules:
- At any given time, you can have *either* one mutable reference *or* any number of immutable references to a value.
- References must always be valid. (Here valid means: point to the appropriate value in memory.)

Instead of transferring ownership, you can "borrow" a value by passing a *reference* to the value. (A reference is like a pointer in that it's an address we can follow to access the data stored at that address; that data is owned by some other variable. Unlike a pointer, a reference is guaranteed to point to a valid value of a particular type for the life of that reference.)

A variable that is borrowing another variable's value can refer to that value without taking ownership of it. When the borrowing variable falls out of scope, the value will not be dropped.

**Borrowed values cannot be mutated unless the owning variable is mutable and the borrower asks for a mutable reference.** At any time, only one mutable reference can point to a value. Mutable borrowing is also not allowed while an immutable reference to the same value is in scope. This restriction allows for controlled mutation and avoids runtime race conditions. 

The borrow checker will also block compilation if the source creates a "dangling" reference -- a reference to a dropped value. We'd create a dangling reference, for example, by initializing a variable with a reference returned from a function when the reference returned by that function would fall out of scope when the function was popped off the stack. (Returning a reference wouldn't keep the value from being dropped since the reference doesn't own the value.)

Special cases:
- string slices create an immutable (?) reference to the original string
- If a struct contains any non-`Copy` values, the struct update syntax "moves" ownership to the newly created struct instance.
- A struct owns all its own data. You can store in a struct instance a reference to data owned by something else, but only with the use of lifetimes.

# Type System
Rust is **not** duck typed. 

# Structs & Enums
Structs are kind of like classes where the data attributes are defined on the struct itself and any methods are defined separately, in an `impl` block. The `impl` block can define methods proper and "associated" functions that become part of the struct's namespace.

Enums are kind of like a matcher over related types.

# match
A control-flow construct that chooses which code to execute based on how a value *matches* a set of patterns. "the power of `match` comes from the expressiveness of the patterns and the fact that the compiler confirms that all possible cases are handled."

`if let` allows for a more concise block when you want to do something if a single condition is met and handle all other possibilities in the same way (typically ignoring them).