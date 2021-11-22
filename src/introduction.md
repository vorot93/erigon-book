# Introduction

[Erigon](https://github.com/ledgerwatch/erigon) is a next-generation Ethereum implementation that introduces several new concepts:
- A modular client design, enabling parallelized development of the client
- New (“flat”) model of storing Ethereum state, allowing a lower disk footprint
- Preprocessing of data outside of the storage engine, making database write operations faster by a magnitude
- Staged synchronization technique, allowing very fast synchronization

This brings the following benefits to the node operators:
- Much lower disk footprint
  - 1.2TB for archive node, 430GB for pruned node.

- Faster sync speed
  - Over 300 Mgas/s at tip of Ethereum mainnet.
  - An archive node can be bootstrapped in under 3 days.
  - Performance improvements allow Erigon to run even on HDD.

- Crash resilience
  - Forceful shutdown or power failure cannot damage Erigon’s database.

- New vision of modularity
  - P2P and web3 RPC services can be run as separate components on a remote machine.

- Full support for OpenEthereum/Parity `trace_` API, including `trace_filter`

This book documents some of the know-hows that made these achievements possible.
