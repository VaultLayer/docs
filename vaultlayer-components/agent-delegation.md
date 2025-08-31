---
description: Secure AI Delegation for NFT-Owned Smart Vaults
---

# 🟠 Architecture

## 🤖 Vaulter Agents

#### What are Vaulter Agents?

**VaultLayer is building Vaulter Agents:**  
The 🏁 **first autonomous AI Agents that grow your crypto while you sleep** — using delegated Smart Vaults with verifiable on-chain policies.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Delegate your Smart Vault to a Vaulter Agent</p></figcaption></figure>

Vaulter Agents are built for secure, programmable automation of cross-chain strategies such as staking, DCA, and yield farming.

* ✅ **Secure**: Operate only with your Smart Vault’s on-chain permissions.  
* 🔄 **Automated**: Execute yield strategies continuously without manual input.  
* 🧠 **AI-First**: Built on the [ElizaOS](https://github.com/elizaos) Agent Framework.  
* 📬 **User-Friendly**: Send Telegram updates about what’s happening.  
* 🌐 **Cross-Chain**: Work across Bitcoin L1 and EVM protocols.  

**Vaulter Agents** execute predefined and AI-augmented strategies like:

1. 🧲 **Bitcoin Liquid Staking** — claim & reinvest CoreDAO rewards via `vltCORE`  
2. 📈 **Smart DCA** — AI-assisted accumulation using [Allora](https://allora.network) forecasts  
3. 💰 **Stablecoin Yield Farming** — lending & liquidity across @Colend, @Aave, @Morpho  

More strategies and tools will be added over time. You’ll shape each agent’s behavior with prompts, triggers, and on-chain policies.

---

### ⚠️ Why We Built It

Today’s AgentFi alternatives come with risks:

* 🤯 AI hallucinations  
* 🧑‍💻 Developer rugpulls  
* ❌ 1-wallet-per-agent models that don’t scale  

#### 🔐 So how do we safely trust an AI Agent to automate DeFi?

We solved this by introducing:

> **Delegated Smart Vaults with NFT ownership and enforceable on-chain policies.**

---

### 🧠 What is a Smart Vault?

A **Smart Vault** is a programmable, decentralized wallet—built to be:

* 🔑 **Decentralized**: Powered by Lit Protocol’s PKPs & threshold ECDSA  
* 💧 **Liquid**: Tradable and composable as NFTs on EVM markets  
* 🧠 **AI-First**: Designed for delegated strategies like staking, swapping, or lending  

📘 [Learn more about Smart Vaults →](vaultlayer-components/smart-vaults.md)

---

### 🛠️ How It Works

When you delegate a Smart Vault to a Vaulter Agent:

1. You define a **VlStrategy** policy (strategy type, trigger, optional prompt).  
2. The agent reads your policy and tracks execution conditions.  
3. Once triggered, it:  
   * 🧠 Evaluates allowed tools & market data (e.g. Allora forecasts, price feeds)  
   * ✅ Enforces policy constraints (chain, contract, functions, limits)  
   * 🔁 Executes your strategy via secure on-chain tools  
4. 💬 Sends you a Telegram update with results  

All execution is **asynchronous, auditable, and automated**.

📘 [Strategies Reference →](/vaulter-agents/strategies/README.md)

---

### 💡 Modular & Evolving

The agents are built using [ElizaOS](https://github.com/elizaos), enabling:

* 🧩 Modular strategy plugins  
* 🗣️ Custom prompts that shape behavior  
* 🛡️ Strong policy enforcement to prevent abuse  
* 🔄 Ongoing updates with new tools and integrations  

You’re in control. We’ll keep adding more options—so you can tell Vaulter Agents **exactly how to grow your assets**.

---

### ✅ Key Benefits

| Feature      | Description |
|--------------|-------------|
| 🛡️ Trustless | Only executes within allowed chains, contracts, and limits |
| 🔁 Automated | Executes strategies daily/continuously without user input |
| 🧠 Intelligent | Uses ElizaOS AI with memory, planning, and Allora forecasts |
| 📬 Connected | Sends execution summaries via Telegram |
| 🌐 Scalable | One agent, many vaults. No separate wallets required |

---

### 📬 Stay in Touch

* Twitter: [@VaultLayer](https://x.com/VaulterAgents)  
* Telegram: [@bitcoin_defi_strategy](https://t.me/bitcoin_defi_strategy)  

---

VaultLayer is building the future of autonomous DeFi.  
**Vaulter Agents** AgentFi - everywhere.
