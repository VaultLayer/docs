---
description: 'Below is a comprehensive guide on how to use the VaultLayer SDK:'
---

# Quick Start

## Installation

To get started with VaultLayer SDK, you need to install the required package. Use the following command:

{% tabs %}
{% tab title="yarn" %}
```sh
yarn add @vaultlayer/sdk
```
{% endtab %}

{% tab title="npm" %}
```sh
npm install @vaultlayer/sdk
```
{% endtab %}
{% endtabs %}

## Configuration

After registering your app on the VaultLayer Dashboard, obtain your apiKey. Replace `xxxx` with your project configuration in the following setup:

```javascript
'use client';

import {
  ConnectProvider as VaultConnectProvider,
  OKXConnector,
  UnisatConnector,
  XverseConnector,
  MetamaskConnector,
} from '@vaultlayer/sdk';

export default function ConnectProvider({ children }: { children: React.ReactNode }) {
  return (
    <VaultConnectProvider
      options={{
        apiUrl: '',
        apiKey: '',
        domain: 'localhost',
        showVaultButton: true,  // optional
        walletConnect: { // optional
          projectId: ''
          metadata: {}, 
        },
      }}
      connectors={[new UnisatConnector(), new XverseConnector(), new MetamaskConnector()]}
    >
      {children}
    </VaultConnectProvider>
  );
}

```

Then, wrap your application with `ConnectProvider`:

```javascript
const App = () => {
  return (
    <ConnectProvider>
        {/* Your App */}
    </ConnectProvider>
  );
};

```

## Usage

### Connecting Wallets

VaultLayer supports connecting various wallets, including Bitcoin and EVM-compatible wallets. Here’s how you can open the connect modal and handle wallet connections:

```javascript
import { useEffect } from 'react';
import { useConnectModal, useConnector } from '@vaultlayer/sdk';

const { openConnectModal, disconnect } = useConnectModal();

const onOpenConnectModal = () => {
    openConnectModal();
}

const onDisconnect = () => {
    disconnect();
}

const ConnectComponent = () => {
  const { connectors, connect } = useConnector();
  return (
    <div>
      {connectors.map((item) => {
        return (
          item.isReady() && (
            <div key={item.metadata.id} onClick={() => connect(item.metadata.id)}>
              {item.metadata.name}
            </div>
          )
        );
      })}
    </div>
  );
};

```

### Getting Accounts

```javascript
import { useEffect } from 'react';
import {
  useVaultProvider,
  useBitcoinProvider,
  useEthereumProvider,
  useWalletProvider,
} from '@vaultlayer/sdk';

// Connected wallet accounts:
const { accounts } = useWalletProvider();

// Smart Vault accounts:
const { smartVault } = useVaultProvider();
console.log('SmartVault:',smartVault):
/*
SmartVault:
{
    "tokenId": "62352376932128708742798204730977811543787403889774573695687970019904132004838",
    "publicKey": "0x04a70a20509cee26090235b9f2287c861fe595ad3b2f5d7f1a235de1ef8af765ee42989948d320ce9a02e47e4da5d41a69fbc564db9018e236110c36a3440a8553",
    "ethAddress": "0xe07175770af1F501718797A148fd9dC2Ac342F00",
    "btcPubKey": "03a70a20509cee26090235b9f2287c861fe595ad3b2f5d7f1a235de1ef8af765ee"
}
*/

// Ethereum address
const ethProvider = useEthereumProvider();
const ethAccounts = ethProvider?.getAccounts() // option 1
const ethAddress = smartVault?.ethAddress // option 2

// Bitcoin address
const btcProvider = useBitcoinProvider();
const btcAccounts = btcProvider?.getAccounts()  // option 1
const btcAddress = btcProvider?.btcAccounts[0].address // option 2
```

## Transactions

### Bitcoin Transactions

```javascript
import { useEffect } from 'react';

const btcProvider = useBitcoinProvider();

// Will show a confirmation Modal:
const res = await btcProvider?.sendBitcoin(
    fromAddress: string;
    toAddress: string;
    satoshis: number; 
    options: {
        fee: "slow" | "avg" | "fast";
        bitcoinRpc: '';
        forceHideConfirmModal?: boolean;
    }
);

// Or directly sign a PSBT bitcoin transaction:
const txHex = await btcProvider??.signPsbt(psbt, { forceHideConfirmModal: false });
const txID =  await btcProvider?.pushTx(txHex);
```

### Ethereum Transactions

```javascript
import { useEffect } from 'react';

const ethProvider = useEthereumProvider();

// Will show a confirmation Modal:
const res = await ethProvider?.vaultEthClient?.signMessage({
      account: smartVault.ethAddress as any,
      message: 'Hello VaultLayer!\n\nChain-Abstraction for 1 click Bitcoin DeFi'
    });
    
// Or directly sign an Ethereum transaction:
const res = await vaultEthWallet?.signMessage('Hello VaultLayer!\n\nChain-Abstraction for 1 click Bitcoin DeFi');
```
