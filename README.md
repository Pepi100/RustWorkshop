# Rust Workshop

### How Rust works

- Ownership

```rust

let s1 = String::from("A String");

//s2 now owns "A String", s1 doesn't own anything
let s2 = s1;

println("{}", s1); //error: use of moved value 's1'
```

- Borrowing 

```rust
let s = String::from("string");

//s_ref is a reference to s
let s_ref = &s;

//use s_ref to acces the data in the String s
//rust auto dereferences variables
assert_eq!(s.chars().nth(1), s_ref.chars().nth(1));


```
The borrow checker is the last check that runs.

When a value is borrowed, it cannot be modified by it's owner.