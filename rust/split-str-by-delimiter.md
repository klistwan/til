# How do you split &str by a delimiter?

```rust
let v: Vec<&str> = "The quick brown fox jumps over the lazy dog".split(' ').collect();
assert_eq!(v, ["The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog"]);

let v: Vec<&str> = "lion::tiger::leopard".split("::").collect();
assert_eq!(v, ["lion", "tiger", "leopard"]);
```

[Rust documentation](https://doc.rust-lang.org/std/primitive.str.html#method.split)
