---
description: P2P Liquidity with BTC as Collateral
---

# 🤝 P2P Liquidity

VaultLayer’s **P2P NFT Lending Market** allows users to unlock liquidity using staked Bitcoin or eligible NFTs as collateral — without selling the underlying asset. The system operates trustlessly across multiple EVM chains, creating a decentralized over-the-counter (OTC) marketplace for loans.

***

## 🌉 Multi-Chain Liquidity

VaultLayer has deployed the P2P Lending Market across multiple chains to enable cross-chain liquidity against staked BTC:

<table><thead><tr><th width="160.89605712890625">Chain</th><th width="160.84417724609375">Loan Token</th><th>Use Case</th></tr></thead><tbody><tr><td>CoreDAO</td><td>vltCORE</td><td>Stake BTC, borrow CORE using Vault NFT</td></tr><tr><td>Arbitrum</td><td>USDC</td><td>Access discounted BTC via lending markets</td></tr><tr><td>BSC</td><td>USDC</td><td>Institutional lending exposure to BTC staking</td></tr><tr><td>Avalanche</td><td>USDC</td><td>Bid on loans backed by staked BTC</td></tr><tr><td>Optimism</td><td>USDC</td><td>Get yield on BTC-backed NFT loans</td></tr><tr><td>Base</td><td>USDC</td><td>OTC loans for LSV holders</td></tr></tbody></table>

***

## ⚙️ How It Works

Borrowers lock eligible NFTs — like **Liquid Smart Vaults** or **CoreDAO NFTs (e.g., Coretoshi, Core Origin)** — as collateral and define loan terms:

* **Loan amount**
* **APR**
* **Maturity time**

Lenders bid using a **reverse auction** approach. The best bid (lowest interest rate) wins, providing liquidity in either $CORE or $USDC depending on the chain. If the borrower defaults, the lender claims the NFT.

> 🔄 Loans are **OTC**. Floor prices are **informational only** — **DYOR** is essential for both borrowers and lenders.

***

:warning: Loan requests are OTC (Over The Counter). Do Your Own Research (DYOR) both before requesting a loan (borrowers) or providing liquidity (lenders). NFT Collections' floor price are shown for information purposes. As a best practice, loans should be overcollateralized, meaning the value of the underlying asset (the NFT) should be bigger than the loan amount being requested.

For the detailed documentation on how to borrow or lend, check:

* [Use Bitcoin as collateral](../points/borrow-usdcore-with-nft.md)
* [Earn providing liquidity](../points/lend-usdcore.md)

:information\_source: Fees: Flat platform fee of 2% flat for all actions taken in the market: Loan request, bid, bid acceptance, repayment, withdraw, loan cancellation and bid cancellation.

***

P2P Liquidity is a foundational piece of VaultLayer’s broader vision:

> **Stake Bitcoin in L1. Get Liquidity in CORE & USDC everywhere.**
