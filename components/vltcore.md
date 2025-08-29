---
description: VaultLayer's Core Dual-Staking Aggregation Protocol
---

# 🔶 vltCORE

### Overview

**vltCORE** is VaultLayer’s dual-staking aggregator and yield optimizer protocol. It enables users to stake Bitcoin (BTC) on CoreDAO’s Layer 1 while depositing CORE to maximize rewards by hitting CoreDAO’s highest yield tier. The protocol issues **vltCORE tokens** representing proportional shares of pooled CORE deposits, creating a liquid, tradeable yield-bearing asset that helps users access DeFi functionality without compromising Bitcoin’s security or liquidity.

### Features

* **ERC-4626 Standard**: Implements `vltCORE` as an ERC-4626 vault shares token with minting and burning functionalities.
* **Bitcoin-backed yield**: Users earn optimized staking rewards by maintaining the Satoshi (max) tier of Core's dual-staking BTC-to-CORE ratio.
* **Liquidity access**: Tokenized `vltCORE` shares can be traded, staked, or used as collateral.
* **Automated rebalancing**: Ensures rewards are dynamically distributed between BTC stakers and CORE depositors.
* **Staking and delegation**: Facilitates CORE staking via CoreDAO’s staking mechanism.
* **BTC transaction validation**: Records BTC stakes and tracks rewards through off-chain verification.

## Why We Built vltCORE

Imagine Alice stakes her BTC via CoreDAO. It’s safe but **locked** for months, and she's stuck waiting. Meanwhile, CoreDAO offers **higher rewards** if you also stake CORE, maintaining CoreDAO's **maximum** dual-staking **BTC:CORE ratio (Satoshi Tier)**. Most users don’t meet that, leaving rewards on the table.

So VaultLayer asked:

> “What if we could make staked BTC liquid and optimize rewards—without extra work for users?”

This led to:

* **Smart Vaults**: Wallets controlled by NFTs, enabling BTC staking from programmable, non-custodial vaults.
* **vltCORE**: A tokenized aggregator that balances CORE deposits to unlock the **top reward tier** and make staking **DeFi-friendly**.

***

## How It Works

<figure><img src="https://lh7-rt.googleusercontent.com/slidesz/AGV_vUcpdPfA0z5KVgF_cmGPHsGG1IECYouVjuz2ZmsF9BsgPd8MmNvGtbAts01lKzrJ6gZ2ggdhUqlNY5FkVallTvn7eyM_b4nI8q8Y1j95IyczjJzNgpSxXzl6OQowog2ebsRWMZz9FQ=s2048?key=728Fir4Ro5h7MzzA__d2yg" alt=""><figcaption><p>vltCORE Architecture</p></figcaption></figure>

### Smart Vaults

* Each Smart Vault is an NFT-bound decentralized wallet (via Lit Protocol).
* Users mint a Smart Vault, deposit BTC, and initiate a **time-locked CLTV** transaction to stake BTC on CoreDAO.
* BTC remains **non-custodial**—you retain full ownership.

### CORE Staking via vltCORE

* Other users can deposit CORE into the VaultLayer protocol.
* In return, they receive **vltCORE** tokens, which:
  * Represent a share of the pooled staking rewards.
  * Are liquid and tradeable.
* The deposited CORE is staked on CoreDAO via delegated smart contracts.

### Dual Staking Aggregation

VaultLayer pools:

* BTC staking transactions from Smart Vaults.
* CORE deposits from vltCORE users.

It then uses this combined position to hit **CoreDAO’s top staking tier**, maximizing reward distribution for all participants.

***

## Rewards Mechanism

### Balanced Incentives with Tiers and Grades

To keep things fair and efficient:

* VaultLayer measures the **BTC:CORE ratio**.
* A **Grade System** adjusts how rewards are split:
  * Too much CORE? BTC stakers get more.
  * Too much BTC? CORE depositors get more.
  * Balanced? Everyone earns optimal rewards.

***

## Delegator Sub-Contracts

CoreDAO has limits on how many BTC transactions a single address can handle. VaultLayer solves this by:

* Creating a **pool of DualDelegator sub-contracts**.
* Spreading BTC txIDs across them.
* Aggregating all staking rewards back into the **vltCORE vault**.

This design ensures scalability and compliance with CoreDAO infrastructure.

***

## Key Benefits for Users

| User Type | Action                     | Outcome                                                         |
| --------- | -------------------------- | --------------------------------------------------------------- |
| Alice     | Stakes BTC via Smart Vault | Earns yield, keeps custody, receives tradable NFT               |
| Charles   | Deposits CORE              | Receives vltCORE, earns rewards from both CORE and BTC staking  |
| Everyone  | Uses vltCORE or NFT        | Access liquidity, trade or lend without stopping reward accrual |

***

## Technical Architecture

* **Smart Vaults** (NFTs): Hold BTC and initiate staking transactions.
* **vltCORE Contract**: ERC-4626 vault contract issuing liquid yield-bearing shares.
* **Oracle Agent**: Verifies BTC txIDs and syncs rewards cross-chain.
* **DualDelegator Contracts**: Scale BTC validation per CoreDAO limits.

***

## Use Cases

1. **Yield Maximization**: Combine BTC + CORE to hit the best reward tier.
2. **Liquidity Access**: Use BTC staked positions as collateral in VaultLayer’s NFT loan market.
3. **Cross-Chain Exposure**: EVM users can mint Smart Vaults from Arbitrum, Avalanche, etc.
4. **Automation**: Delegate strategy to Vaulter AI for passive BTC yield farming.

***

## Conclusion

VaultLayer’s **vltCORE** system turns passive BTC staking into an active, yield-maximizing, liquid strategy—powered by Smart Vaults, automated agents, and a scalable dual staking model.

> Stake BTC. Deposit CORE. Earn more—together.
