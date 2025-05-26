---
description: >-
  VaultLAyer's SDK integrates different providers to control both the connected
  browser wallet used for login and the Smart Vault for Bitcoin and Ethereum
  Operations:
---

# Providers

| Provider                | Exports                                                                                                                                                                        | Description                                                                                                                                  |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **ConnectProvider**     | OKXConnector, UnisatConnector, XverseConnector, EthereumConnector, etc.                                                                                                        | React context for the wallet connect modal                                                                                                   |
| **useWalletProvider**   | connector, provider, accounts, getPublicKey(), signMessage(), getNetwork(), switchNetwork(), sendBitcoin(), sendInscription()                                                  | This is the provider for the connected wallet that was used to login.    It can only perform transactions supported by the connected wallet. |
| **useVaultProvider**    | smartVault, authMethod, vaults, getVaults()                                                                                                                                    | This is the provider for the Smart Vault.                                                                                                    |
| **useBitcoinProvider**  | btcNetwork, getNetwork(), switchNetwork(), btcAccounts(), getAccounts(), vaultBtcSigner(), signPsbt(), pushTx(), sendBitcoin(), getUtxos(), getNetworkFee(), getNetworkFees(), | This is the Bitcoin provider for the Smart Vault. It can sign Bitcoin transactions (pstb) and send Bitcoin.                                  |
| **useEthereumProvider** | vaultEthWallet, vaultEthClient, getAccounts(), switchEthChain(), chainId, pairToWalletConnect(),                                                                               | This is the Ethereum provider for the Smart Vault. It can sign EVM transactions and connect to Walletconnect.                                |

