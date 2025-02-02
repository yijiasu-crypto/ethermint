<!--
parent:
  order: false
-->

<div align="center">
  <h1> Ethermint </h1>
</div>

<div align="center">
  <a href="https://github.com/cosmos/ethermint/releases/latest">
    <img alt="Version" src="https://img.shields.io/github/tag/cosmos/ethermint.svg" />
  </a>
  <a href="https://github.com/cosmos/ethermint/blob/development/LICENSE">
    <img alt="License: Apache-2.0" src="https://img.shields.io/github/license/cosmos/ethermint.svg" />
  </a>
  <a href="https://pkg.go.dev/github.com/cosmos/ethermint?tab=doc">
    <img alt="GoDoc" src="https://godoc.org/github.com/cosmos/ethermint?status.svg" />
  </a>
  <a href="https://goreportcard.com/report/github.com/cosmos/ethermint">
    <img alt="Go report card" src="https://goreportcard.com/badge/github.com/cosmos/ethermint"/>
  </a>
  <a href="https://codecov.io/gh/cosmos/ethermint">
    <img alt="Code Coverage" src="https://codecov.io/gh/cosmos/ethermint/branch/development/graph/badge.svg" />
  </a>
</div>
<div align="center">
  <a href="https://github.com/cosmos/ethermint">
    <img alt="Lines Of Code" src="https://tokei.rs/b1/github/cosmos/ethermint" />
  </a>
  <a href="https://discord.gg/AzefAFd">
    <img alt="Discord" src="https://img.shields.io/discord/669268347736686612.svg" />
  </a>
  <a href="https://github.com/cosmos/ethermint/actions?query=workflow%3ABuild">
    <img alt="Build Status" src="https://github.com/cosmos/ethermint/workflows/Build/badge.svg" />
  </a>
  <a href="https://github.com/cosmos/ethermint/actions?query=workflow%3ALint">
    <img alt="Lint Status" src="https://github.com/cosmos/ethermint/workflows/Lint/badge.svg" />
  </a>
</div>

Ethermint is a scalable, high-throughput Proof-of-Stake blockchain that is fully compatible and
interoperable with Ethereum. It's build using the the [Cosmos SDK](https://github.com/cosmos/cosmos-sdk/) which runs on top of [Tendermint Core](https://github.com/tendermint/tendermint) consensus engine.

> **WARNING:** Ethermint is under VERY ACTIVE DEVELOPMENT and should be treated as pre-alpha software. This means it is not meant to be run in production, its APIs are subject to change without warning and should not be relied upon, and it should not be used to hold any value. We will remove this warning when we have a release that is stable, secure, and properly tested.

**Note**: Requires [Go 1.15+](https://golang.org/dl/)

## Quick Start

To learn how the Ethermint works from a high-level perspective, go to the [Introduction](./docs/intro/overview.md) section from the documentation.

For more, please refer to the [Ethermint Docs](./docs/), which are also hosted on [docs.ethermint.zone](https://docs.ethermint.zone/).

## Tests

Unit tests are invoked via:

```bash
make test
```

To run JSON-RPC tests, execute:

```bash
make test-rpc
```

There is also an included Ethereum mainnet exported blockchain file in `importer/blockchain`
that includes blocks up to height `97638`. To execute and test a full import of
these blocks using the EVM module, execute:

```bash
make test-import
```

You may also provide a custom blockchain export file to test importing more blocks
via the `--blockchain` flag. See `TestImportBlocks` for further documentation.

## Running a localhost node with EVM support

```bash
./init-evm-node.sh
```

With this terminal window open, please go ahead to run you `truffle` scripts or connect MetaMask to `localhost:8545`.

If you need WebSocket support, use `localhost:8546` instead.


Notes:

1. Logs from `ethermintd` are stored at `./ethermintd.log`
2. If you need to change the `MNEMONIC`, update trailing lines of `./init-evm-node.sh`. The default 24-mnemonic words are: `yard similar hotel exercise calm cousin forget wisdom swallow fatal afraid what dog panther nose age ramp portion floor scene cruise soul strong rose`
3. The default private key is `0x49a2c89120ffdf59157e6a29b7bb3210899915adc9ae758bf1a22b0f33000d05` with an address on `0x90FdB51c13Ce085cE7F9c0dA8683B7327711b064`. If you need to interact with MetaMask, use this account (it's with balance by default)


### Community

The following chat channels and forums are a great spot to ask questions about Ethermint:

- [Cosmos Discord](https://discord.gg/W8trcGV)
- [Cosmos Forum](https://forum.cosmos.network)
