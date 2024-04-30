# What's the difference between `iter()` and `into_iter()`

`iter` yields all items from start to end ([docs](https://doc.rust-lang.org/std/vec/struct.Vec.html#method.iter))

`into_iter` creates a consuming iterator (values are moved out of the vector) ([docs](https://doc.rust-lang.org/std/iter/trait.IntoIterator.html#tymethod.into_iter))
