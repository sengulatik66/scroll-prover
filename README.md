# scroll-common
[![Unit Test](https://github.com/scroll-tech/common-rs/actions/workflows/unit_test.yml/badge.svg)](https://github.com/scroll-tech/common-rs/actions/workflows/unit_test.yml)
![issues](https://img.shields.io/github/issues/scroll-tech/common-rs)

Scroll common rust crates.

## Usage

### Libraries
Import as an dependency to use.

### Binaries

Setup 
```shell
cargo build --release --bin setup   

./target/release/setup --params <params-file-path> --seed <seed-file-path>
```

## Test
By default, prover tests are disabled due to heavy computations, if you want to run the prover test, please run:
```
RUST_LOG=info cargo test --features prove_verify --release test_evm_prove_verify
```

or
```
RUST_LOG=info cargo test --features prove_verify --release test_state_prove_verify
```

(Please don't run `test_evm_prove_verify` and `test_state_prove_verify` concurrently.)
