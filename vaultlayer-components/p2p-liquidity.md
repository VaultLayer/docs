---
description: Stake Bitcoin in L1. Get liquidity in CORE and USDC.
---

# 🤝 P2P Liquidity

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>Get liquidity in CORE &#x26; USDC</p></figcaption></figure>

VaultLayer’s **P2P NFT Lending Market** allows users to unlock liquidity using staked Bitcoin (and other assets) as collateral. The system operates trustlessly across multiple EVM chains, creating a decentralized over-the-counter (OTC) marketplace for loans.

* The P2P Liquidity market allows Smart Vault NFT holders of selected collections, with L1-staked Bitcoin, CORE and other supported chains, to get access to liquidity without having to sell.
* Users in need of liquidity make a loan request instead, using the assets in their Smart Vault NFT as collateral, set their terms (amount, APR and maturity time), and lenders bid using a reverse auction approach.
* The lender with the best bid, provides liquidity and earns yield or the Smart Vault NFT collateral in case of default.

***

## 🌉 Multi-Chain Liquidity

VaultLayer has deployed the P2P Lending Market across multiple chains to enable cross-chain liquidity against staked BTC and other assets:

**CORE (vltCORE)**

* Stake BTC and use it as collateral.
* Earn more for CORE staking and get BTC on discount.

#### Other EVM L2s (USDC)

* Get exposure to BTC staked on L1 and use it as collateral.
* Get access to discounted BTC via P2P.

<table><thead><tr><th width="160.89605712890625">Chain</th><th width="160.84417724609375">Loan Token</th><th>Use Case</th></tr></thead><tbody><tr><td>CoreDAO</td><td>vltCORE</td><td>Stake BTC, borrow CORE using Smart Vault NFT</td></tr><tr><td>Arbitrum</td><td>USDC</td><td>Access discounted BTC via lending markets</td></tr><tr><td>BSC</td><td>USDC</td><td>OTC loans for LSV holders</td></tr><tr><td>Avalanche</td><td>USDC</td><td>Bid on loans backed by staked BTC</td></tr><tr><td>Optimism</td><td>USDC</td><td>Get yield on BTC-backed Smart Vault NFT loans</td></tr><tr><td>Base</td><td>USDC</td><td>Institutional lending exposure to BTC staking</td></tr></tbody></table>

***

## ⚙️ How It Works

Borrowers lock eligible NFTs — like **Liquid Smart Vaults** or **CoreDAO NFTs (e.g., Coretoshi, Core Origin)** — as collateral and define loan terms:

* **Loan amount**
* **APR**
* **Maturity time**

Lenders bid using a **reverse auction** approach. The best bid (lowest interest rate) wins, providing liquidity in either $CORE or $USDC depending on the chain. If the borrower defaults, the lender claims the Smart Vault NFT.

> :warning: Loans are **P2P** (Peer-To-Peer) and **OTC** (Over The Counter). Floor prices are **informational only** — **DYOR** is essential for both borrowers and lenders.
>
> :warning: As a best practice, loans should be over-collateralized, meaning the value of the underlying assets should be bigger than the loan amount being requested.

For the detailed documentation on how to borrow or lend, check:

* [Use Bitcoin as collateral](../points/borrow-usdcore-with-nft.md)
* [Earn providing liquidity](../points/lend-usdcore.md)

:information\_source: Fees: Flat platform fee of 2% flat for lend and borrow.

***

P2P Liquidity is a foundational piece of VaultLayer’s broader vision:

> **Stake Bitcoin in L1. Get Liquidity in CORE & USDC everywhere.**
