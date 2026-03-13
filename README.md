## Perceptron

A binary perceptron implemented in Rust with production tooling: static typing, integrated CI, and reproducible testing.

## Structure

```
├──Cargo.toml
├──src/
│    ├── main.rs
│    └── model.rs
├──tests/
│    ├── integration-tests.rs
│    └── cases.json
└──.github/
    └── workflows/
        └── pipeline.yml
```

## Why Rust

Previous iterations of this model were written in Python. This implementation explores the same algorithm with a systems-level language, gaining:

- Compiled, no runtime overhead
- Weight/input mismatches caught at compile time
- Memory safety without a garbage collector
- CI/CD, integration tests, and reproducible builds out of the box

## Model

The perceptron computes a weighted sum of inputs plus a bias, then applies a step function to produce a binary label.

$$
f(x) = sum(w_i * x_i) + b
$$

## Integration Tests

Builds and tests every commit to main, auto-reverting on failure.

*https://github.com/dylan-sutton-chavez/perceptron-rust/actions/workflows/pipeline.yml*

## Usage

```bash
cargo run # Inferenece.
cargo test # Run integration tests.
```

## Requirements

```txt
cargo
```
