# How to read a file's contents into a String

```rust
use std::env;
use std::fs;

fn main() {
    // --snip--
    println!("In file {}", file_path);

    let contents = fs::read_to_string(file_path)
        .expect("Should have been able to read the file");

    println!("With text:\n{contents}");
}
```

Source: [https://doc.rust-lang.org/book/ch12-02-reading-a-file.html](https://doc.rust-lang.org/book/ch12-02-reading-a-file.html)
