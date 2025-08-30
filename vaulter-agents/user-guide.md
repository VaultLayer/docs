# 📘 User Guide

Welcome to Vaulter Agents, your AI-powered, non-custodial vaults that run DeFi strategies on autopilot across chains like CoreDAO, Base, and Ethereum. This guide walks you through launching an agent, funding it, linking Telegram, and managing strategies, properties, and tools.

* [Overview](user-guide.md#overview)
* [Prerequisites](user-guide.md#prerequisites)
* [Launch an Agent](user-guide.md#launch-an-agent)
* [Fund Your Agent](user-guide.md#fund-your-agent)
* [Link Your Telegram](user-guide.md#link-your-telegram)
* [Manage Your Agent](user-guide.md#manage-your-agent)
  * [Start/Stop Agent](user-guide.md#startstop-agent)
  * [Update Strategy](user-guide.md#update-strategy)
  * [Update Properties (Name & Avatar)](user-guide.md#update-properties-name--avatar)
  * [Manage Tools & Tokens](user-guide.md#manage-tools--tokens)
* [Monitor Activity, Assets, NFTs, and DeFi Positions](user-guide.md#monitor-activity-assets-nfts-and-defi-positions)
* [Troubleshooting](user-guide.md#troubleshooting)
* [FAQ](user-guide.md#faq)
* [Support & Legal](user-guide.md#support--legal)

## 🧭 Overview

Vaulter Agents are smart, self-custodied vaults that execute yield strategies using AI. You choose a strategy, fund the agent, and it automates the rest—staking, lending, claiming rewards, and more—while keeping you in control.

Key capabilities:

* Automated strategies (e.g., BTC staking rewards, Stablecoin farming, RWA staking)
* Multi-chain vault addressing (BTC + EVM)
* Non-custodial operations (your vault addresses are visible and verifiable)
* Telegram alerts and summaries
* Fine-grained tool and token permissions

## 🧰 Prerequisites

* A Web3 wallet (e.g., MetaMask) and a small amount of native gas token on your selected chain
* Supported chains today include CoreDAO (1116), Base (8453), and Ethereum (1)
* Optional: ASX RWA NFTs for the RWA staking strategy

## 🚀 Launch an Agent

1. Open the Agents tab and click “Launch your own DeFi AI Agent!”.
2. Connect your wallet if prompted (the “Connect to Launch” button triggers the wallet modal automatically).
3. Choose a strategy from the list and click “Launch Agent”.
4. In the modal:
   * Upload an optional agent image (stored on IPFS)
   * Select Strategy and enter your Agent Name
   * Provide a deposit amount (optional for most strategies)
   * For RWA staking, select ASX NFTs instead of a numeric deposit
   * For Bitcoin strategies, a BTC deposit address is shown
   * Review the Launch Service Fee (chain-dependent) displayed in the modal
   * Accept Terms of Service and Privacy Policy
5. Click “Mint & Launch Agent”.

Progress is shown with a step-by-step animation. If a step fails (mint, receipt confirmation, create, delegate, deposit), you’ll see a contextual Retry button to resume from the failed step.

Tip: Strategy defaults can automatically set your agent image and expected APY based on live protocol stats.

## 💳 Fund Your Agent

You can fund during launch or later from the Agent page under “Add Funds”.

* BTC strategy (or when BTC is the accepted asset):
  * Copy the BTC address shown and send BTC from your wallet
  * Minimums may apply for certain operations
* EVM assets (e.g., CORE, USDC):
  * Copy the Ethereum vault address and transfer the asset on the correct chain
  * Or use the in-app Deposit flow (when connected) to send tokens or native coin
* RWA strategy (ASX NFTs):
  * Use the “Add Funds” NFT selector to transfer ASX NFTs into your vault

The selected asset to accept depends on the active strategy. For example, RWA staking accepts ASX NFTs; BTC staking accepts BTC; other strategies accept specific tokens.

## 🔗 Link Your Telegram

Link Telegram to receive notifications and daily summaries.

1. Go to User Settings → Profile
2. Click “Link Telegram Account”
3. Your wallet generates a short-lived code and opens Telegram at `@VaulterAgents_bot`
4. Send the pre-filled code to the bot
5. The app auto-detects linking and shows “Telegram Linked” with your handle

Notes:

* Codes expire after \~10 minutes; if it expires, click “Link Telegram Account” again
* A Lit-based signature may be requested for additional security
* The same Telegram can be linked to multiple wallets

## 🛠️ Manage Your Agent

Open a specific Agent to manage it. You can always see your vault’s addresses, balances, and activity.

### Start/Stop Agent

* If inactive, click “Start Agent” to delegate permissions and start executing the strategy
* If active, click “Stop Agent” to unpermit strategy and policy apps (fully stopping execution)

### Update Strategy

Go to Settings & Apps → Strategy tab:

* Strategy Type: choose from available strategies (display names map to internal strategy types)
* Daily Trigger Amount: set the per-day threshold in the correct unit (e.g., BTC or USDC)
* Custom Prompt (Pro feature): refine execution rules. A lock icon takes you to Billing to upgrade.
* Click Update/Start; the UI confirms and refreshes strategy status

### Update Properties (Name & Avatar)

At the top of Settings & Apps:

* Click the gear next to the agent name to edit the name inline, then save
* Click the camera icon on the avatar to upload a new image (stored on IPFS), then save

### Manage Tools & Tokens

Go to Settings & Apps → Tools tab:

* Max Amount: set a per-transaction cap your agent can spend
* Protocols: enable/disable DeFi protocols per chain; quick-select all/deselect/reset defaults
* Tokens: toggle allowed token contracts; quick-select all/deselect
* Click “Update Tools” to apply. Tool updates translate into precise contract/function permissions the agent can use.

## 📊 Monitor Activity, Assets, NFTs, and DeFi Positions

Inside the Agent view:

* Activity: chronological feed of actions (stake, redeem, strategy executed/failed, updates), with View Tx links to chain explorers; some entries include multiple tx links
* Assets: balances by asset with actions (Deposit, Stake, Withdraw, Send)
* NFTs: vault-held NFTs with View/Send actions
* DeFi Positions: consolidated positions including BTC staking, ASX staking, and Aave; contextual actions (Redeem when BTC timelock expires, Withdraw/Claim for ASX, Withdraw from Aave)

APY shown in the header is derived from live protocol stats when available; if stats are unreachable, default APYs display.

## 🛟 Troubleshooting

* Wallet not connected: use the “Connect to Launch” or connect button in the header
* Launch failed: ensure you have gas for the selected chain and use the Retry button for the failed step
* No APY values: protocol stats may be temporarily unavailable; APY will default until refreshed
* NFT list empty: ensure you’re on the right chain and wallet; the UI refreshes and caches for performance
* Custom Prompt disabled: upgrade to Pro in Billing to enable advanced prompts
* Terms checkbox disabled launch: make sure you accept Terms and Privacy before launching

## ❓ FAQ

* Where do my assets live? Your agent is a non-custodial vault with on-chain BTC and EVM addresses visible in the UI.
* What chains are supported? CoreDAO, Base, and Ethereum today. More chains may be added over time.
* Is there a launch fee? A chain-dependent Launch Service Fee is shown in the launch modal.
* Can I change strategy later? Yes. Use Settings & Apps → Strategy to update or stop/start.
* How do I view transactions? Activity items include “View Tx” links to the appropriate chain explorer.

## 🛡️ Support & Legal

* Terms of Service: https://docs.vaultlayer.xyz/legal/terms
* Privacy Policy: https://docs.vaultlayer.xyz/legal/privacy
* Support: contact@vaultlayer.xyz
* Telegram Support: [@bitcoin\_defi\_strategy](https://t.me/+Q58TzLXmvGM0MGFh)

—

💡 Tip: Share your progress! The Activity feed includes shareable items and generated cards (e.g., for strategy executions) that look great on social media.
