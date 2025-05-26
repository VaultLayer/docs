---
description: Introduction to Chain Abstraction
---

# 💡 Chain-Abstraction

Chain abstraction simplifies interactions across multiple blockchains, hiding complexities like key management, gas fees, and transaction processing. This concept is vital for improving user experience and accessibility in the DeFi space.

### **The CAKE Framework**

The CAKE framework (Chain Abstraction Key Elements) provides a reference structure for chain abstraction. It includes:

* **Permission Layer:** Manages user account interactions and authorizations. The user connects their wallet to a dApp and requests the quote for a user intent, such as swapping BTC for USDC or depositing BTC into a yield-generating strategy. The wallet can read user assets and execute transactions on target chains.
* **Solver Layer:** Estimates fees and execution speed based on the user's initial balance and intent. This involves asynchronous transactions and solving for optimal execution paths while managing fees, execution speed, and guarantees.
* **Settlement Layer:** Ensures the execution of transactions by bridging assets to the target chain and completing the intended operations. This includes handling liquidity and mitigating risks associated with asynchronous transaction settlements.

Achieving Chain Abstraction means integrating these layers into a unified product. This involves a sophisticated approach to transferring information and value across chains, balancing security, cost, and execution speed.

VaultLayer applies these CAKE concepts to create a cohesive and powerful solution for Bitcoin DeFi.

### **VaultLayer’s Chain-Abstraction**

<figure><img src="../.gitbook/assets/VaultLayer - CAKE.png" alt=""><figcaption></figcaption></figure>

VaultLayer operates as part of the Permission Layer in the CAKE framework, managing user interactions and authorizations. Unlike other chain abstraction solutions that rely on Ethereum's ERC-4337 standard for contract wallets, VaultLayer creates a Bitcoin-native smart account.&#x20;

VaultLayer leverages Lit Protocol’s MPC network to create an off-chain smart account, simplifying the permission layer. This integration ensures seamless, secure transactions and asset management across Bitcoin L1 and L2.&#x20;

The VaultLayer SDK, which is part of this layer, provides developers with tools to integrate VaultLayer's functionalities seamlessly into their applications. This SDK will facilitate the creation and management of Bitcoin-native smart accounts, bridging, swapping, and other DeFi operations.

#### Conclusion

VaultLayer is set to transform the Bitcoin DeFi landscape by offering a unified, user-friendly platform that eliminates the complexities and frustrations of the current ecosystem. By applying the CAKE framework concepts, VaultLayer ensures a streamlined and secure experience for users. With "One Account, One Portfolio, Any Wallet," VaultLayer makes Bitcoin DeFi accessible to everyone, from beginners to seasoned crypto investors.

