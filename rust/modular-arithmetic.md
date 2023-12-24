# Doing modular arithmetic in Rust

In Rust and similar languages (C, C++, C#, F#, Java), `%` is the remainder whereas in Perl, Python, Ruby, `%` is the modulus.

Two workarounds to get modulus in Rust:

1. `((a % b) + b) % b`
2. `a.rem_euclid(b)`
