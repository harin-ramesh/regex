# regex

A small, dependency-free regular-expression engine written in Rust. It exposes a single `find` function that returns the byte position and byte length of the first match.

> This is a learning project, not a replacement for the production [`regex`](https://crates.io/crates/regex) crate.

## Features

The engine currently supports:

| Syntax | Meaning |
| --- | --- |
| `abc` | Literal text |
| `.` | Any single character |
| `[abc]` | One character from a set |
| `(ab\|cd)` | Alternation/grouping |
| `?` | Zero or one repetition |
| `*` | Zero or more repetitions |
| `+` | One or more repetitions |
| `^` | Start of input |
| `$` | End of input |
| `\\a` | ASCII alphabetic character |
| `\\d` | ASCII digit |

Repetition is greedy and backtracks when needed to match the remainder of an expression.

