# MEV, Sandwich Attacks, and AI Phishing

In 2026, transactions are no longer just "Send and Receive." They are part of a predatory financial environment where bots scan every transaction for profit.

## 1. MEV (Maximal Extractable Value)

MEV is the profit that miners/validators can make by reordering transactions within a block.

### The Sandwich Attack

A bot sees your large swap or transfer on a DEX (like Uniswap).

1. **Front-run:** The bot buys the asset just before you, driving the price up.
2. **Your TX:** You buy the asset at the higher price.
3. **Back-run:** The bot sells the asset immediately after your purchase, pocketing the difference.

**How to Prevent:**

- **Slippage Limits:** Set your slippage to 0.1% or 0.5%. If the bot tries to push the price higher, your transaction will simply fail, protecting your funds.
- **Private RPC (Flashbots / MEV-Blocker):** Use an RPC URL that sends your transaction directly to a validator instead of the public "Mempool." This makes your transaction invisible to sandwich bots.

## 2. AI-Generated Phishing (The 2026 Threat)

Scams have moved beyond misspelled emails.

### AI Voice & Deepfakes

You receive a call from "Support." The voice sounds exactly like the CEO of your exchange or a friend. They claim your account is "compromised" and ask you to move funds to a "Safety Wallet."

- **The Defense:** Never trust a voice or video call for financial instructions. Use a **Pre-Agreed Password** with friends/family.

### AI Website Clones

Attackers use AI to generate 10,000 unique phishing sites per hour. Each site has a slightly different URL and a slightly different UI to avoid automated blacklists.

- **The Defense:** Never use Search Engines for your wallet or exchange. Use **Bookmarks only**.

### Browser Extension Injection

Malicious extensions can "inject" a fake transaction screen into your legitimate wallet (like MetaMask). You think you are signing a $1 transfer, but the extension has changed the data to a "TransferAll" function.

- **The Defense:** Use a dedicated browser (like Brave or a fresh Chrome profile) *only* for crypto. Install zero other extensions.

## 3. Poisoning & Look-Alike Addresses

Attackers use "Vanity Address Generators" to create addresses that match yours for the first 6 and last 6 characters. They send you 0.0001 ETH so this address appears in your history.

**The Mistake:** Users assume that if the first and last few characters match, the address is theirs.
**The Rule:** Verify **every single character** of an address for large transfers. Or use an **ENS (Ethereum Name Service)** or **Unstoppable Domain** which is much harder to "fake" in a UI.

---
**Next Step:** What to do if the worst happens in [Incident Response](docs/07-incident-response/what-to-do-after-mistake.md).
