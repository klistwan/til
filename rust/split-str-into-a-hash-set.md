# How do you split &str into a HashSet?

```rust
use std::collections::HashSet;
fn main() {
    let example = "The lazy brown fox";
    let hash_set: HashSet<&str> = example.split(" ").collect();
    assert_eq!(hash_set.contains("The"), true);
}
```

[Rust docs](https://doc.rust-lang.org/std/iter/trait.Iterator.html#method.collect)
