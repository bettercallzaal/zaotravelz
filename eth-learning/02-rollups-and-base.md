# ETH Learning 02 - Rollups + Base (your home chain, explained properly)

You deployed $ZABAL on Base and hold Respect on Optimism. This lesson: what those chains actually are, so you can talk L2 architecture at camp and Devcon without hand-waving.

## The scaling problem in one line

L1 Ethereum does ~15-30 transactions/sec because every node re-executes everything. Rollups fix this by executing elsewhere and using L1 only as the court of final appeal + data bulletin board.

## What a rollup IS

A rollup is a separate chain that:
1. Executes transactions on its own (fast, cheap sequencer)
2. Posts compressed transaction DATA to Ethereum L1 (so anyone can reconstruct state)
3. Posts state commitments to an L1 contract
4. Inherits Ethereum security: if the rollup's operators vanish or cheat, users can exit using the L1 data

Two families, split on HOW cheating is caught:

| | Optimistic rollups | ZK rollups |
|---|---|---|
| Assumption | State is valid unless someone proves fraud | State proven valid with cryptography every time |
| Mechanism | 7-day fraud-proof challenge window | Validity proof (SNARK/STARK) verified by L1 contract |
| Withdrawals to L1 | ~7 days (or use a bridge that fronts liquidity) | Minutes-hours |
| Examples | **Base, Optimism, Arbitrum** | zkSync, Scroll, Linea, Starknet, Polygon zkEVM |
| Tradeoff | Simple, EVM-identical, mature | Faster finality, heavier prover math |

## EIP-4844 - why L2s got 10x cheaper (March 2024)

"Proto-danksharding" added **blobs**: cheap, temporary (~18 days) data space attached to blocks, purpose-built for rollup data. Rollups stopped competing with regular calldata. This is why Base transactions cost cents. Danksharding (more blobs) is the roadmap continuation. Say "blobspace" at Devcon and people nod.

## Base specifically

- Built by Coinbase on the **OP Stack** - Optimism's open-source rollup framework. Base and Optimism are siblings running the same software.
- **Superchain**: OP Stack chains (Base, OP Mainnet, Zora, Mode, Worldchain...) share standards + a collective security/governance vision, moving toward shared interoperability. Your podcast tagline "the Superchain" = this.
- No Base token. Fees paid in ETH. Coinbase runs the sequencer (centralized today - decentralizing sequencers is THE open problem; know this critique).
- Revenue model: sequencer margin (fees collected minus L1 data costs); Base contributes portion to Optimism Collective - which funds **RetroPGF** (retroactive public goods funding - relevant to ZAO grant hunting).
- Why builders pick it: Coinbase distribution (Smart Wallet, onramps), cheap, EVM-equivalent, huge consumer-crypto push (Farcaster ecosystem largely lives on Base; Clanker launched $ZABAL there).

## The stack of names people throw around

- **Sequencer**: orders + executes L2 transactions, gives instant "soft" confirmation. Centralized on almost every L2 today.
- **Bridge**: contracts moving assets L1<->L2. Canonical bridge = slow but trustless; third-party bridges front liquidity for speed.
- **Data availability (DA)**: WHERE transaction data lives. Ethereum blobs = real rollup. Alternatives (Celestia, EigenDA) = cheaper but different trust - those chains are technically "validiums"/alt-DA, not rollups. L2Beat.com grades this ruthlessly; check any chain there before trusting claims.
- **Stages (L2Beat)**: Stage 0 = training wheels (multisig can override), Stage 1 = fraud/validity proofs live with limited overrides, Stage 2 = fully trustless. Most majors are Stage 1. Good Devcon-fluency fact.

## Why this matters for ZAO/WaveWarZ specifically

- WaveWarZ runs Solana (different bet entirely: one fast L1, no rollups; monolithic vs modular is the eternal debate panel). WaveWarZ Base expansion = betting the consumer-crypto audience is where Farcaster/Base users are.
- Artist payments: cents-level fees make 0xSplits micro-splits + per-battle payouts viable - impossible on L1 at $2-10/transaction.
- Respect (Optimism) + $ZABAL (Base) are both Superchain - future interop makes cross-community reputation portable, which is a real talk topic for a music Community Hub.

## Camp-usable takeaways

1. Deploy to **Base Sepolia** testnet at the buildathon - free, fast, judges recognize it, faucets easy (Coinbase developer faucet).
2. Scaffold-ETH 2 targets any chain by changing `targetNetworks` in config - Base Sepolia is one line.
3. If asked "why Base": Coinbase distribution + Farcaster social graph + cheap consumer transactions. If asked the critique: centralized sequencer, Stage 1.

Next lesson: 03 account abstraction + ERC-4337 (smart wallets, passkeys, gasless UX - Aya Wallet's exact territory, and the single highest-value topic for camp small talk with hosts).
