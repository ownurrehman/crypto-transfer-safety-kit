# Networks and Assets: Common Confusion

In 2026, the distinction between "Asset" and "Network" is the most critical technical concept for a user to master. A single asset like USDT can exist on 50+ different networks.

## The Multi-Chain Matrix

| Asset | Common Networks | Format | Recoverability |
| :--- | :--- | :--- | :--- |
| **USDT/USDC** | Ethereum, Tron, Polygon, Arbitrum, Base, BSC, Solana, TON | Varies (0x, T, Base58) | High (if self-custody) / Low (if CEX) |
| **ETH** | Ethereum, L2s (Arb, OP, Base, ZK), Sidechains | 0x... (EVM) | High (same private key works) |
| **BTC** | Bitcoin (Native), WBTC (EVM), BTCB (BSC) | 1..., 3..., bc1... | Zero (if sent to wrong chain) |
| **SOL** | Solana Mainnet | Base58 | Medium (check SPL vs Native) |

## Comparison of Major Networks

### 1. Ethereum (Layer 1)

- **Gas Token:** ETH
- **Address Format:** 0x...
- **Speed:** ~12 seconds to 15 minutes (finality)
- **Safety Note:** Highest fees. Best for large amounts.

### 2. Tron

- **Gas Token:** TRX
- **Address Format:** T...
- **Speed:** ~1 minute
- **Safety Note:** Widely used for USDT (TRC-20). Often confused with Ethereum because of the similar "ERC-20" name. **TRC-20 addresses are not compatible with ERC-20 addresses.**

### 3. Layer 2s (Arbitrum, Optimism, Base, ZKsync)

- **Gas Token:** Usually ETH (Native)
- **Address Format:** 0x... (Same as Ethereum Mainnet)
- **Speed:** Seconds
- **Safety Note:** Because the address is the same as Ethereum, users often send funds to an L2 thinking it is L1. If the receiving exchange doesn't support the L2, the funds are stuck.

## Specific Cases of Irrecoverable Loss

### The "Burn" Address

Sending funds to `0x0000000000000000000000000000000000000000`. This address has no private key. Any funds sent here are gone forever. This often happens due to copy-paste errors or interaction with broken smart contracts.

### Cross-Standard Mismatches

- **Sending Omni-USDT (Legacy) to TRC-20:** Irrecoverable.
- **Sending Native BTC to an Ethereum Address:** The exchange withdrawal may allow it if it uses a bridge internally, but if you do it manually, the transaction will likely fail to broadcast. If it *is* sent (using a wrapped BTC method to a non-wrapped wallet), it is gone.

## The "Same Chain Family" Rule

If you own the private key (seed phrase) for an address starting with `0x...` on Ethereum, you also own that same address on Polygon, BSC, Arbitrum, and Base.

**Recovery Path:**
If you accidentally sent USDC to your own Polygon address instead of Ethereum, you simply add the Polygon network to your wallet (e.g., MetaMask, Rabby) using the same seed phrase, and your funds will be there.

**Exception:**
This does **not** apply to Centralized Exchanges. If you send USDC to a CEX on a network they don't support, they own the private keys, and they usually refuse to perform manual recovery for safety/policy reasons.

---
**Next Step:** Secure your entry and exit points in [Exchange Safety](docs/04-exchange-safety/deposit-withdrawal-checklist.md).
