# DeFi and Bridges: Risk Model

Bridges are the "choke points" of the multi-chain ecosystem. Historically, bridge exploits have been the largest source of stolen funds in crypto history.

## 1. Types of Bridges

- **Canonical Bridges:** Built by the chain creators (e.g., The Arbitrum Bridge, The Polygon PoS Bridge). These are the safest but often have the longest withdrawal times (e.g., 7 days for Optimistic Rollups).
- **Liquidity Bridges (Third-Party):** Use pools of funds on both sides (e.g., Stargate, Hop, Orbiter). These are faster (minutes) but introduce "Smart Contract Risk" from the bridge provider.
- **Burn-and-Mint Bridges:** They lock assets on Chain A and mint a "Wrapped" version on Chain B. If the vault on Chain A is hacked, the assets on Chain B become worthless (unbacked).

## 2. The "Fake Bridge" Scam Template

Scammers use SEO and Social Media ads to promote "Official Bridges" that are actually drainage scripts.

**How to verify an official bridge:**

1. **Check the Chain Documentation:** Go to the official website of the network (e.g., optimism.io) and find their "Ecosystem" or "Bridge" link.
2. **Verify via Block Explorer:** Search for the bridge contract on Etherscan. If it's a legitimate bridge, it will have a "Verified" badge and millions in TVL (Total Value Locked).
3. **Use a Trusted Aggregator:** Services like **Lifi** or **Bungee** aggregate legitimate bridges. While they add their own layer of contract risk, they prevent you from landing on a phishing site.

## 3. Slippage and Transaction Reverts

When bridging, you are swapping assets. If the liquidity is low, you might experience **Slippage** (getting a much worse price than expected).

- **The Trap:** A bridge interface might tell you that you'll receive 1,000 USDC but set the "Minimum Received" to 900 USDC.
- **The Solution:** Always check the "Receive" amount manually. If it's more than 0.5% different from your input, don't bridge or find a deeper liquidity pool.

## 4. Allowance Risk (Infinite Approvals)

To use a bridge, you must "Approve" the contract to spend your tokens.

**The Danger:** Many dApps ask for an "Infinite Approval" so you don't have to sign a second time in the future. If that bridge is ever hacked, the hacker can drain your *entire* wallet balance, not just what you were bridging.

**Safety Rule:** Only approve the **exact amount** you are bridging. Use tools like `revoke.cash` regularly to clean up old approvals.

## 5. Liquidity Crunches

Sometimes a bridge works mechanically, but the "Destination Side" is out of funds. Your assets are "in flight" and you have to wait for someone else to bridge in the opposite direction for you to be paid out.

**Prevention:** Check the "Bridge Liquidity" status on the UI. If it looks low (under $100k), use a different provider.

---
**Next Step:** Learn about MEV and AI scams in [Advanced Risks](docs/06-advanced-risks/mev-and-sandwich.md).
