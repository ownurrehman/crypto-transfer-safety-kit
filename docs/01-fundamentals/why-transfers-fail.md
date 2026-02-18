# Why Crypto Transfers Fail

In 2026, the complexity of the crypto ecosystem has increased. While user interfaces have improved, the underlying risks remain tied to the irreversible nature of distributed ledgers. Understanding the mechanics of failure is the first step toward prevention.

## 1. Network Selection Incompatibility

The most common cause of lost funds is selecting the wrong network. A "network" is the rails on which your asset travels. Even if the asset name (e.g., USDT) is the same, the rails are not interoperable without a bridge.

**The Mechanical Error:** Sending an EVM-based token (like USDT on Ethereum) to a non-EVM address (like a Tron TRC20 address) or to a different EVM-compatible chain that the receiver does not support.

> **Example:** A user attempts to deposit USDT from an exchange. They select "Arbitrum" in the exchange withdrawal menu, but the destination wallet (or deposit address on a different exchange) only supports "Ethereum Mainnet."
> **Result:** The funds are moved to the user's address on Arbitrum. If the user owns the private keys to that address, recovery is possible by switching networks. If the user sent it to a Centralized Exchange (CEX) deposit address, the CEX may not credit the funds, often requiring a manual "cross-chain recovery" fee or resulting in permanent loss.

## 2. Missing Memo / Destination Tag

Many modern and legacy chains (XRP, XLM, TON, Cosmos) use a "shared" wallet model for exchanges. All users send funds to the same public address, and the exchange differentiates them using a unique ID called a **Memo** or **Destination Tag**.

**The Mechanical Error:** Forgetting to include this tag or entering it incorrectly.

> **Example:** User sends 10,000 XRP to a CEX. The address is correct, but the "Destination Tag" field is left blank.
> **Result:** The XRP ledger processes the transaction successfully. However, the exchange's internal accounting cannot determine which user account should be credited. Recovery requires intense KYC verification and support tickets, typically taking weeks.

## 3. Clipboard Malware (Address Hijacking)

Clipboard hijacking has evolved. Modern malware watches for any string of text that looks like a crypto address. The moment you "Copy," the malware replaces it with its own address.

**The Mechanical Error:** Trusting the clipboard blindly without visually verifying the address after pasting.

> **Example:** User copies their Ledger address. Malware instantly replaces it with a "Look-alike" address (same first 4 and last 4 characters).
> **Result:** User pastes into the exchange withdrawal field. They glance at the first 4 characters, see they match, and hit "Confirm." The funds are sent directly to the attacker.

## 4. ERC-20 to Smart Contract Confusion

Sending tokens (ERC-20) requires a different interaction than sending native coins (ETH). Some users inadvertently send tokens to a contract address intended only for internal logic or to an address that cannot handle that specific token standard.

> **Example:** Sending USDT directly to the USDT Smart Contract address instead of the intended recipient's address.
> **Result:** The tokens are effectively "burned" or locked in the contract forever, as most token contracts do not have a "withdraw" function for funds sent to themselves.

## 5. Expired or "Dropped" Transactions

High network congestion leads to gas price spikes. If a user sets the gas too low, the transaction sits in the "Mempool" (waiting room).

**The Risk:** Users often panic and send a *second* transaction with higher fees. If they don't use the correct "Nonce" (transaction number), the first transaction might eventually execute hours later, resulting in a double-spend of their budget or unintended consequences.

## 6. Fake Bridge Interfaces

Chain abstraction has led to an explosion of bridges. Attackers now create AI-generated clones of popular bridges (e.g., Stargate, Hop, Orbiter).

**The Mechanical Error:** Interacting with a malicious smart contract via a fake UI.
> **Example:** User searches "Bridge to Base" on a search engine. They click a sponsored ad. The site looks identical to the official bridge.
> **Result:** When the user clicks "Approve USDT," they are actually signing a "Permit2" or "Increase Allowance" transaction that gives the attacker full access to their wallet's balance.

## 7. Zero-Value Transfer Attacks (Address Poisoning)

Attackers use bots to send 0-value transactions to your wallet using an address that looks nearly identical to one you recently sent funds to. They do this so the fake address appears at the top of your transaction history.

**The Risk:** Many users copy addresses from their own "Recent Transactions" list rather than their actual contact list or the original source.
> **Result:** User copies the "poisoned" address from their history and sends the next batch of funds to the attacker.

---
**Next Step:** Learn how to verify networks in [Networks & Assets](docs/02-networks-and-assets/common-confusion.md).
