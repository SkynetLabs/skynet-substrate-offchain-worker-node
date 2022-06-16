# Skynet Substrate Offchain Worker Node

Example Substrate node featuring Skynet offchain worker example pallet.

## Trying it out

See the example Skynet offchain worker [here](https://github.com/SkynetLabs/skynet-substrate-offchain-worker-node/tree/skynet-substrate/frame/examples/offchain-worker). Follow the instructions there to try it out!

## Substrate

See the official repository [here](https://github.com/paritytech/substrate).

## License

- Substrate Primitives (`sp-*`), Frame (`frame-*`) and the pallets (`pallets-*`), binaries (`/bin`) and all other utilities are licensed under [Apache 2.0](LICENSE-APACHE2).
- Substrate Client (`/client/*` / `sc-*`) is licensed under [GPL v3.0 with a classpath linking exception](LICENSE-GPL3).

The reason for the split-licensing is to ensure that for the vast majority of teams using Substrate to create feature-chains, then all changes can be made entirely in Apache2-licensed code, allowing teams full freedom over what and how they release and giving licensing clarity to commercial teams.

In the interests of the community, we require any deeper improvements made to Substrate's core logic (e.g. Substrate's internal consensus, crypto or database code) to be contributed back so everyone can benefit.
