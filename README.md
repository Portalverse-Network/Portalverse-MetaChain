# Portalverse

[![License](https://img.shields.io/badge/License-Apache%202.0-orange.svg)](#LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-blue.svg)](CONTRIBUTING.md)

<p align="center">
  <img src="/portalverse.png">
</p>

[Portalverse](https://www.portalverse.net/) is a decentralized cloud gaming and rendering network for immersive metaverses where everyone can access at any time, from any device and anywhere.


## Related Projects

- [Portalverse Pallets](https://github.com/Portalverse-Network/portalverse-pallets) is a set of [Substrate](https://substrate.dev) pallets of Portalverse.
- [Octopus Network](https://github.com/octopus-network) powers us.

## License
[APACHE2-LICENSE](LICENSE)


### Rust Setup

First, complete the [basic Rust setup instructions](./docs/rust-setup.md).


### Build

The `cargo run` command will perform an initial build. Use the following command to build the node
without launching it:

```sh
cargo build --release
```

### Single-Node Development Chain

This command will start the single-node development chain with non-persistent state:

```bash
./target/release/portalverse --dev --enable-offchain-indexing true
```

Purge the development chain's state:

```bash
./target/release/portalverse purge-chain --dev
```

Start the development chain with detailed logging:

```bash
RUST_BACKTRACE=1 ./target/release/portalverse -ldebug --dev --enable-offchain-indexing true
```




### Run

Use Rust's native `cargo` command to build and launch the template node:

```sh
cargo run --release -- --dev --enable-offchain-indexing true
```


### Embedded Docs

Once the project has been built, the following command can be used to explore all parameters and
subcommands:

```sh
./target/release/portalverse -h
```

## Run

The provided `cargo run` command will launch a temporary node and its state will be discarded after
you terminate the process. After the project has been built, there are other ways to launch the
node.


### Connect with Polkadot-JS Apps Front-end

Once the node template is running locally, you can connect it with **Polkadot-JS Apps** front-end
to interact with your chain. [Click
here](https://polkadot.js.org/apps/#/explorer?rpc=ws://localhost:9944) connecting the Apps to your
local node template.