---
description: VaultLayer's Core Dual-Staking Aggregation Protocol
---

# 🟠 Vaulter CORE (vltCORE)

### Overview

VaultLayer's Vaulter CORE (vltCORE) is a decentralized protocol that unlocks liquidity and accesses to max yield for Bitcoin staked on Layer 1 (L1) using Smart Vaults. The [`vltCORE`](https://github.com/VaultLayer/vaultlayer-protocol) contract represents tokenized shares of CORE collateral that users receive when they deposit CORE or Stake BTC using the VaultLayer protocol.

### Features

* **ERC-4626 Standard**: Implements `vltCORE` as an ERC-4626 vault shares token with minting and burning functionalities.
* **Bitcoin-backed yield**: Users earn optimized staking rewards by maintaining a 1:24000 BTC-to-CORE ratio.
* **Liquidity access**: Tokenized `vltCORE` shares can be traded, staked, or used as collateral.
* **Automated rebalancing**: Ensures rewards are dynamically distributed between BTC stakers and CORE depositors.
* **Staking and delegation**: Facilitates CORE staking via CoreDAO’s staking mechanism.
* **BTC transaction validation**: Records BTC stakes and tracks rewards through off-chain verification.
