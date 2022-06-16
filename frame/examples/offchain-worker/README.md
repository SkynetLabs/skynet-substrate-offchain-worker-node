<!-- markdown-link-check-disable -->
# Skynet Offchain Worker Example Pallet

The Skynet Offchain Worker Example: A simple pallet demonstrating
simple interaction with the Skynet Substrate SDK in the context of an offchain workers.
Based on the Offchain Worker Example Pallet

Run `cargo doc --package pallet-example-offchain-worker --open` to view this module's
documentation.

**This pallet serves as an example showcasing Substrate off-chain worker using
Skynet and is not meant to be used in production.**

## Overview

In this example we are going to build a very simplistic, naive and definitely NOT
production-ready off-chain data publisher and consumer using Skynet.

Offchain Worker (OCW) will be triggered after every block, fetch the "historical
block heght" saved by this node and then update this value using the current
block height before persisting to Skynet. By using a resolver skylink, access to
the latest value is consistent across any Skynet portal. You could also change
the "data key" to, for example, save historical blockheight per a day, at
predictable resolver skylinks for your web application. In the example, we have
hard-coded keys, but you will likely want to incorporate ed25519 keys from your
node.

License: Unlicense

## Prerequisites

Install Rust:

```
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

Other dependencies:

```
sudo apt install build-essential
sudo apt-get install -y clang
```

Make sure you are using Rust nightly with the wasm toolchain installed.

**NOTE:** you need a specific nightly version for this example!

```
rustup install nightly-2021-12-15
rustup default nightly-2021-12-15
rustup target add wasm32-unknown-unknown
```

## Running the Node

```
cd bin/node-template/node
cargo run --release -- --dev --offchain-worker --tmp
```
