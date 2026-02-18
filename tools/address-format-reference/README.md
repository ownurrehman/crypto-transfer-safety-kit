# Address Format Reference

Use this as a quick visual guide to ensure you are entering the correct format for the intended network.

## Major Network Prefixes

| Network | Address Prefix | Example Format |
| :--- | :--- | :--- |
| **Ethereum & EVM L2s** | `0x` | `0x123...abc` (42 chars, Hex) |
| **Tron** | `T` | `T123...xyz` (34 chars, Base58) |
| **Bitcoin (Legacy)** | `1` | `1BvBM...` |
| **Bitcoin (SegWit)** | `3` | `3J98t...` |
| **Bitcoin (Native SegWit)**| `bc1q` | `bc1qxy2...` |
| **Bitcoin (Taproot)** | `bc1p` | `bc1p5d...` |
| **Solana** | Base58 (No fixed prefix) | `7xKX...` (32-44 chars) |
| **XRP** | `r` | `rU2m...` |
| **Cosmos** | `cosmos` | `cosmos1...` |
| **TON** | `EQ` or `UQ` | `EQB...` |
| **Polkadot** | `1` | `15...` |
| **Cardano** | `addr1` | `addr1...` |

## Checksums

Many addresses (especially Ethereum) use Mixed-Case Checksums (e.g., `0xAbC...`).
**The Rule:** If you paste an address and the capitalization changes, or if your wallet says "Invalid Address," double-check the source. A single character change in capitalization can sometimes indicate a different address format or a mangled clipboard.

## Looking for "Vanity" Matches

Attackers will match the **first 6** and **last 6** characters of your address.

- **Safe Practice:** Always verify the **middle** 4 characters as well.
- **Better Practice:** Use an ENS name (`yourname.eth`) which the wallet UI will resolve and verify for you.
