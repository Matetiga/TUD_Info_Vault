## Single mutable borrow
- At any given time: there can be <span style="color:#ffff00">EITHER</span> <span style="color:#1fffc7">ONE mutable reference</span> or <span style="color:#1fffc7">MANY immutable references</span> (<span style="color:#ffff00">NOT BOTH</span>)

## References must be valid
- It is important for the complete lifetime of a variable pointing to a memory location (heap) that that memory remains valid (no deallocated or moved memory).

## Mutable borrow exclusivity
- When having a mutable reference to a piece of data. There can no be other mutable o immutable references, while the mutable reference exists

## No Mutation through immutable references
- if we have an immutable reference to something, we cannot take a mutable reference and change the value.
