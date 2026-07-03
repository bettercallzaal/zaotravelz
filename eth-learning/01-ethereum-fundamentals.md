# ETH Learning 01 - Fundamentals for Build Camp (Jul 4-5 material)

Target: be ahead of camp days 1-2 (Welcome to Ethereum, Solidity + smart contracts). You already know Base/Optimism as a user and token deployer; this is the mental model underneath.

## Accounts - only two kinds

1. **EOA (externally owned account)** - keypair-controlled. Your wallets. Can initiate transactions.
2. **Contract account** - code + storage at an address. Cannot initiate; only reacts when called.

Every transaction starts at an EOA (account abstraction blurs this - later lesson). An address is the last 20 bytes of keccak256 of the public key. Contract addresses are derived from deployer address + nonce (CREATE) or salt (CREATE2, deterministic - how factories predict addresses).

## Transactions and gas

- A transaction: from, to, value (ETH in wei, 1 ETH = 10^18 wei), data (calldata), gas limit, fee fields.
- **Gas** = metered computation. Every EVM opcode costs gas. You pay gas_used x gas_price.
- **EIP-1559** (the modern fee market): fee = base fee (burned, protocol-set, moves with demand) + priority tip (to validator). Wallets show maxFeePerGas + maxPriorityFeePerGas.
- Out-of-gas = revert, state rolled back, gas still spent. Reverts are safe - state never half-applies.
- L2s (Base, Optimism, Arbitrum) execute off L1, post data to L1, inherit security. Fees cents instead of dollars. Camp will likely deploy to an L2 testnet or Sepolia.

## The EVM in one paragraph

Stack machine. Contracts are bytecode; Solidity compiles to it. Contract state lives in **storage** (persistent, expensive: ~20K gas per new 32-byte slot), **memory** (per-call scratch, cheap), **calldata** (read-only input, cheapest). Reads from the chain via a node are free (view functions, no transaction). Writes always cost a transaction.

## Solidity contract anatomy (what camp day 2 teaches)

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.24;

contract TipJar {
    address public owner;                      // public = free getter
    mapping(address => uint256) public tips;   // key-value storage

    event Tipped(address indexed from, uint256 amount);  // logs, indexed = filterable

    error NotOwner();                          // custom errors < require strings (gas)

    constructor() { owner = msg.sender; }      // runs once at deploy

    modifier onlyOwner() {
        if (msg.sender != owner) revert NotOwner();
        _;
    }

    function tip() external payable {          // payable = can receive ETH
        tips[msg.sender] += msg.value;
        emit Tipped(msg.sender, msg.value);
    }

    function withdraw() external onlyOwner {
        (bool ok, ) = owner.call{value: address(this).balance}("");
        require(ok, "transfer failed");
    }
}
```

Key globals: `msg.sender` (caller), `msg.value` (ETH sent), `block.timestamp`. Since 0.8.x arithmetic reverts on overflow by default (no SafeMath needed).

Standards you will touch at camp: **ERC-20** (fungible token - $ZABAL is one), **ERC-721** (NFT), **ERC-1155** (multi-token - your $ZOR is one). Never hand-write these: import OpenZeppelin.

## Security reflexes (judges look for these)

1. **Checks-effects-interactions**: update state BEFORE sending ETH/calling out. Prevents reentrancy (the DAO hack pattern).
2. Use `call{value:}` not `transfer` for ETH sends; check the bool.
3. Custom errors + reverts over silent failure.
4. Don't trust `block.timestamp` for randomness; no onchain randomness without oracle/VRF.
5. Anything `public`/`external` can be called by ANYONE, in any order, including contracts. Design for hostile callers.

## The modern stack (camp day 3-4, maps to your skills)

| Layer | Tool | Your equivalent |
|---|---|---|
| Contract dev | **Foundry** (forge test in Solidity, fast) or Hardhat (JS tests) | your test runner |
| Contract libs | OpenZeppelin | npm packages |
| Client | **viem** (TS library, replaces ethers.js) | supabase-js |
| React hooks | **wagmi** (useAccount, useReadContract, useWriteContract) | React Query - wagmi is literally built on it |
| Wallet UI | RainbowKit or ConnectKit | Auth UI |
| Scaffold | **Scaffold-ETH 2** = Next.js + wagmi + viem + RainbowKit + Foundry/Hardhat wired together | create-next-app |
| Testnet | Sepolia (L1) or Base Sepolia (L2) | staging |

Mental mapping: contract = your Postgres schema + RLS + API routes fused into one deployed object. Reads (view functions) = SELECT, free via RPC. Writes = transactions, cost gas, need wallet signature. Events = your webhook/audit log; frontends and indexers subscribe to them instead of polling state.

## 30-minute hands-on (tonight if time, else during camp day 1)

```bash
cd scaffold-eth-2 && yarn install
yarn chain     # local anvil/hardhat node
yarn deploy    # deploys sample contract
yarn start     # Next.js frontend on localhost:3000
```
Change one thing in `packages/hardhat/contracts/YourContract.sol`, redeploy, watch the frontend hot-pick it up. That loop IS the camp workflow.

## Vocabulary that signals fluency

nonce (per-account tx counter), ABI (contract's JSON interface - what wagmi needs), RPC (node endpoint, e.g. Alchemy), mempool, finality (~13 min L1; L2 soft-instant), calldata, proxy/upgradeable (contracts are immutable; upgrades = proxy pattern pointing at new implementation), account abstraction / ERC-4337 (smart-contract wallets - Aya Wallet's whole world, relevant to hosts).

Next lesson candidates: 02 rollups + Base deep-dive (your home chain), 03 account abstraction + ERC-4337 (host flattery + consumer UX), 04 Solidity testing patterns w/ Foundry, 05 splits/royalty contracts (0xSplits - ZAO Music relevance).
