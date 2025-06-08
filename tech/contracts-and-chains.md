---
description: Deployed Contracts and Supported Chains
---

# Contracts & Chains

VaultLayer spans multiple EVM-compatible chains, offering Smart Vaults, Bitcoin staking optimization, and P2P NFT lending backed by staked Bitcoin. Below is a complete reference of deployed contracts by function and chain.

***

### 🧠 Liquid Smart Vaults Collection <a href="#liquid-smart-vaults-collection" id="liquid-smart-vaults-collection"></a>

These NFTs represent ownership and control of Smart Vaults.

<table><thead><tr><th width="143.74029541015625">Chain</th><th>Contract</th></tr></thead><tbody><tr><td>coreDao</td><td><a href="https://scan.coredao.org/address/0x2F55F3dEa47FDd3cf424F8678ef54650424f63C9"><code>0x2F55F3dEa47FDd3cf424F8678ef54650424f63C9</code></a></td></tr><tr><td>arbitrum</td><td><a href="https://arbiscan.io/address/0x4c004622C5f4d5E8917c679A121ABeFFffe45A9d"><code>0x4c004622C5f4d5E8917c679A121ABeFFffe45A9d</code></a></td></tr><tr><td>avalanche</td><td><a href="https://snowtrace.io/address/0x1f653C5075C015C312a86c94d41D7e3C52C1eeca"><code>0x1f653C5075C015C312a86c94d41D7e3C52C1eeca</code></a></td></tr><tr><td>base</td><td><a href="https://basescan.org/address/0x1f653C5075C015C312a86c94d41D7e3C52C1eeca"><code>0x1f653C5075C015C312a86c94d41D7e3C52C1eeca</code></a></td></tr><tr><td>optimism</td><td><a href="https://optimistic.etherscan.io/address/0x1f653C5075C015C312a86c94d41D7e3C52C1eeca"><code>0x1f653C5075C015C312a86c94d41D7e3C52C1eeca</code></a></td></tr><tr><td>bsc</td><td><a href="https://bscscan.com/address/0x0abF8558900db3CBb3Eb314Fb69a64Ba9CFD997f"><code>0x0abF8558900db3CBb3Eb314Fb69a64Ba9CFD997f</code></a></td></tr></tbody></table>

***

## 🏛️ vltCORE Contracts

Aggregation of CoreDao dual-staking rewards on the [vltCore](../smart-vaults/vltcore.md) protocol.

<table><thead><tr><th width="159.532470703125">Contract</th><th>Address</th></tr></thead><tbody><tr><td>BitcoinHelper</td><td><a href="https://scan.coredao.org/address/0xCc69633BA2C78d02bE9546D369B319bAc163FF2E"><code>0xCc69633BA2C78d02bE9546D369B319bAc163FF2E</code></a></td></tr><tr><td>CoreHelper</td><td><a href="https://scan.coredao.org/address/0xc99d60BB46560d3bC8120776470CF36Ba433C50e"><code>0xc99d60BB46560d3bC8120776470CF36Ba433C50e</code></a></td></tr><tr><td>VaulterCore</td><td><a href="https://scan.coredao.org/address/0xd2875bddb9011F93437D4A7635a68a7FcdB1F562"><code>0xd2875bddb9011F93437D4A7635a68a7FcdB1F562</code></a></td></tr><tr><td>DualDelegator 1</td><td><a href="https://scan.coredao.org/address/0xfdC04A0E3FfE458069ba08E77B9c5CE302E7a005"><code>0xfdC04A0E3FfE458069ba08E77B9c5CE302E7a005</code></a></td></tr><tr><td>DualDelegator 2</td><td><a href="https://scan.coredao.org/address/0xd77f5A62f8Ab79fDdbF01dAA20F1634D4130141e"><code>0xd77f5A62f8Ab79fDdbF01dAA20F1634D4130141e</code></a></td></tr><tr><td>DualDelegator 3</td><td><a href="https://scan.coredao.org/address/0xC250d7e327F11e9DcE4D876D090E912Bdc24e375"><code>0xC250d7e327F11e9DcE4D876D090E912Bdc24e375</code></a></td></tr></tbody></table>

***

## 🤝 NFT P2P Lending Markets

Lend and borrow against staked BTC Smart Vaults.

<table><thead><tr><th width="161.19482421875">Chain</th><th>Contract</th></tr></thead><tbody><tr><td>coreDao</td><td><a href="https://scan.coredao.org/address/0x96ff8135890f4B65DCd19f613F35E2b8A0a18585"><code>0x96ff8135890f4B65DCd19f613F35E2b8A0a18585</code></a></td></tr><tr><td>arbitrum</td><td><a href="https://arbiscan.io/address/0x12500049BDC5CD660B806697D7e82eea41c433eC"><code>0x12500049BDC5CD660B806697D7e82eea41c433eC</code></a></td></tr><tr><td>bsc</td><td><a href="https://bscscan.com/address/0xea252DA102748C84152260615D7E76958FE09597"><code>0xea252DA102748C84152260615D7E76958FE09597</code></a></td></tr><tr><td>avalanche</td><td><a href="https://snowtrace.io/address/0xBb7A6Ddb6ED2089Cc2AB9A67F31c08E702F444b0"><code>0xBb7A6Ddb6ED2089Cc2AB9A67F31c08E702F444b0</code></a></td></tr><tr><td>base</td><td><a href="https://basescan.org/address/0xBb7A6Ddb6ED2089Cc2AB9A67F31c08E702F444b0"><code>0xBb7A6Ddb6ED2089Cc2AB9A67F31c08E702F444b0</code></a></td></tr><tr><td>optimism</td><td><a href="https://optimistic.etherscan.io/address/0xBb7A6Ddb6ED2089Cc2AB9A67F31c08E702F444b0"><code>0xBb7A6Ddb6ED2089Cc2AB9A67F31c08E702F444b0</code></a></td></tr></tbody></table>

***

## 🔐 Vaulter Tool Policy Contracts

These contracts manage permissioned automation via the [Vaulter AI Agent.](../smart-vaults/vaulter-ai-agent.md)

<table><thead><tr><th width="127.94805908203125">Chain</th><th>Contract</th></tr></thead><tbody><tr><td>coreDao</td><td><a href="https://scan.coredao.org/address/0xb03DC1DBC35619B56c8d6A17d202c2B6d5EA6e3d"><code>0xb03DC1DBC35619B56c8d6A17d202c2B6d5EA6e3d</code></a></td></tr><tr><td>arbitrum</td><td><a href="https://arbiscan.io/address/0xff9Edb48f006C4dF02853F90f9ce23078C0AeCD3"><code>0xff9Edb48f006C4dF02853F90f9ce23078C0AeCD3</code></a></td></tr><tr><td>bsc</td><td><a href="https://bscscan.com/address/0x7567A8eF8AECdb98504eBB8fb9B1e9Ff14dE7384"><code>0x7567A8eF8AECdb98504eBB8fb9B1e9Ff14dE7384</code></a></td></tr><tr><td>avalanche</td><td><a href="https://snowtrace.io/address/0x1db8E00bb7055741681dda16a405ff506678840f"><code>0x1db8E00bb7055741681dda16a405ff506678840f</code></a></td></tr><tr><td>base</td><td><a href="https://basescan.org/address/0x1db8E00bb7055741681dda16a405ff506678840f"><code>0x1db8E00bb7055741681dda16a405ff506678840f</code></a></td></tr><tr><td>optimism</td><td><a href="https://optimistic.etherscan.io/address/0x1db8E00bb7055741681dda16a405ff506678840f"><code>0x1db8E00bb7055741681dda16a405ff506678840f</code></a></td></tr></tbody></table>
