# How do you implement the Into trait for a parameter?

```rust
// Example 1: T can be converted to Vec<u8>
fn is_hello<T>(input: T)
where
    T: Into<Vec<u8>>
{
   let bytes = b"hello".to_vec();
   assert_eq!(bytes, s.into());
}

let s = "hello".to_string();
is_hello(s);

// Example 2: T can be converted to 2-element tuple
pub fn tuple_unzip<T, A, B>(items: Vec<T>) -> (Vec<A>, Vec<B>)
where
    T: Into<(A, B)>,
{
    let mut vec1 = Vec::new();
    let mut vec2 = Vec::new();

    for item in items {
        let (a, b) = item.into();
        vec1.push(a);
        vec2.push(b);
    }
    (vec1, vec2)
}
```

[Rust docs](https://doc.rust-lang.org/std/convert/trait.Into.html)
