# How do you increment a value in a HashMap or insert it?

```rust
use std::collections::HashMap;

let mut letters = HashMap::new();

for ch in "a short treatise on fungi".chars() {
    *letters.entry(ch).or_insert(0) += 1;
}

assert_eq!(letters[&'s'], 2);
assert_eq!(letters[&'t'], 3);
assert_eq!(letters[&'u'], 1);
assert_eq!(letters.get(&'y'), None);
```

[Reference](https://stackoverflow.com/a/41420637)
