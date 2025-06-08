---
description: Bitcoin Staking with Smart Vaults
---

# Bitcoin Staking

VaultLayer enables self-custodial Bitcoin staking on CoreDAO and unlocks liquidity by wrapping each vault in a transferable NFT that controls access and permissions. This page explains how native BTC staking works, how Smart Vaults preserve self-custody, and how VaultLayer simplifies the user experience for Bitcoin DeFi.

***

### 🔐 How Bitcoin Staking Works on CoreDAO

#### Non-Custodial Time-Locked Staking

CoreDAO allows BTC holders to stake their assets **directly on Bitcoin L1**, using a smart script based on **`OP_CLTV`** (CheckLockTimeVerify).

* You lock BTC into a **CLTV time-locked UTXO** to your **own wallet**, ensuring self-custody.
* An **OP\_RETURN** output is added to the same Bitcoin transaction. This carries metadata such as:
  * Core validator address ("candidate")
  * Ethereum address to receive rewards
* CoreDAO Docs: [https://docs.coredao.org/docs/Learn/products/btc-staking/design](https://docs.coredao.org/docs/Learn/products/btc-staking/design)
* Bitcoin CLTV: [https://en.bitcoin.it/wiki/Timelock](https://en.bitcoin.it/wiki/Timelock)

After some confirmations, CoreDAO relayers read this metadata and register the stake on Core chain contracts.

#### Validator Rewards

Core validators are scored by:

* Delegated CORE stake
* Delegated BTC stake (via CLTV)
* Delegated hashrate

Stakers receive **$CORE rewards** based on their contribution to these validator scores.

***

### 🧠 Smart Vaults for BTC Staking

VaultLayer users stake BTC via **Smart Vaults**, which are programmable vaults controlled by:

* A **Lit Protocol PKP** (decentralized key pair)
* A **Vault NFT** that represents ownership

#### How It Works

1. A user mints a Smart Vault and stakes BTC from its associated Bitcoin address.
2. The Smart Vault signs the CLTV staking transaction and includes VaultLayer’s dual delegator in the metadata.
3. The rewards are directed to VaultLayer contracts and credited to the Smart Vault.

This enables:

* 🔁 **Liquidity** — the Smart Vault NFT can be traded or used as collateral.
* ⚖️ **Composability** — Vaults plug into lending markets or agents.
* 🔒 **Self-Custody** — BTC never leaves L1 and stays locked to the user’s key.

***

### Built on top of CoreDAO

After a Smart Vault signs and broadcasts a BTC staking transaction with the correct `OP_CLTV` time-lock and `OP_RETURN` metadata:

* CoreDAO relayers monitor the Bitcoin network and automatically register valid staking transactions on CoreDAO's staking contracts.
* VaultLayer waits for these transactions to be confirmed and registered on CoreDAO.
* Every 10 minutes, the **Vaulter AI Agent** scans the CoreDAO contracts to detect new registered BTC staking transactions.
* Once identified, the agent records these on VaultLayer’s [vltCORE protocol](https://docs.vaultlayer.xyz/components/vltcore), linking them to the corresponding Smart Vault.
* Every 24 hours, the agent triggers the reward claim process on vltCORE, aggregating staking rewards from all registered BTC and CORE positions.

> ⚠️ Anyone can call the `registerBTCStake()` and `claimCoreRewards()` functions directly on the VaultLayer contracts. The Vaulter AI Agent automates this process for convenience, but it is permissionless and trustless.

This flow leverages CoreDAO’s native relayer infrastructure and ensures VaultLayer’s dual staking logic remains decentralized and transparent.

***

### 🤝 Using Staked BTC in DeFi

Smart Vault NFTs can be used across the VaultLayer ecosystem:

* **Borrow against staked BTC** on the [P2P Lending Markets](https://docs.vaultlayer.xyz/components/p2p-liquidity).
* **Automate vault actions** like reward claiming, swapping, or bridging via the [Vaulter AI Agent](https://docs.vaultlayer.xyz/components/vaulter-ai-agent).

For Smart Vault architecture and features, see: [Smart Vaults docs](https://docs.vaultlayer.xyz/components/smart-vaults).

***

### Summary

VaultLayer simplifies Bitcoin staking on CoreDAO by offering:

* A clean interface for time-locked BTC staking
* Smart Vaults with NFT control and secure signing via Lit Protocol
* Self-custodial, verifiable, and programmable Bitcoin DeFi infrastructure

Stake BTC. Stay sovereign. Verify everything.
