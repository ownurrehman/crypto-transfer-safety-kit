# Crypto Transfer Safety Kit

A practical, updated guide to reducing irreversible crypto transfer mistakes.

Crypto transactions are final. Mistakes are permanent. This guide focuses on preventing loss before it happens, accounting for the complex landscape of 2026 crypto infrastructure.

## What This Covers

- **Network Selection**: Avoiding cross-chain confusion and gas token mismatches.
- **Stablecoin Safety**: Managing the fragmentation of USDT, USDC, and algorithmic assets across dozens of L2s and L3s.
- **Address Verification**: Defending against clipboard hijacking and look-alike address poisoning.
- **Wallet Security**: Transitioning from seed phrases to Account Abstraction (AA) and Passkeys.
- **DeFi & Bridges**: Verifying bridge authenticity and understanding liquidity risk.
- **Advanced Risks**: Protecting against MEV sandwich attacks and AI-generated phishing.
- **Incident Response**: A clinical approach to what to do when a transaction goes wrong.

## Principles

1. **Neutral & Tool Agnostic**: No specific wallet, exchange, or token is promoted.
2. **Technical Accuracy**: Guidance is based on the underlying protocol mechanics.
3. **Preventative Focus**: Emphasis on "Checking Twice" to avoid "Crying Once."

## Table of Contents

1. [Fundamentals: Why Transfers Fail](docs/01-fundamentals/why-transfers-fail.md)
2. [Networks & Assets: Managing Cross-Chain Confusion](docs/02-networks-and-assets/common-confusion.md)
3. [Wallet Security: Passkeys & Account Abstraction](docs/03-wallet-security/passkeys-and-aa.md)
4. [Exchange Safety: CEX Entry/Exit Strategies](docs/04-exchange-safety/deposit-withdrawal-checklist.md)
5. [DeFi & Bridges: Navigating the Multi-Chain Web](docs/05-defi-and-bridges/bridge-risk-model.md)
6. [Advanced Risks: MEV & AI Scams](docs/06-advanced-risks/mev-and-sandwich.md)
7. [Incident Response: Post-Mistake Action Plan](docs/07-incident-response/what-to-do-after-mistake.md)
8. [Glossary: 2026 Technical Terms](docs/08-glossary/terms.md)

## Support & Contributions

This repository is maintained as a public service. If you find inaccuracies or wish to add new safety patterns (especially for emerging L2s), please submit a Pull Request.

**Maintainer resources and contact: [coinsfera.com](https://coinsfera.com)**

## Frequently Asked Questions (FAQ)

<details>
<summary>1. What happens if I send crypto on the wrong network?</summary>

If the receiving platform does not support the network used, funds may not be credited. In some cases recovery is possible if the private keys are controlled by the recipient. In other cases the funds are permanently lost. Always confirm the network on both sides before sending.
</details>

<details>
<summary>2. Why does USDT exist on multiple networks like ERC20, TRC20, BEP20, Polygon, Arbitrum, and others?</summary>

Stablecoins are deployed on multiple blockchains to reduce fees and improve speed. Even though the token name is the same, each version exists independently on its respective network. The network must match exactly between sender and receiver.
</details>

<details>
<summary>3. What is the difference between a wallet address and a contract address?</summary>

A wallet address belongs to a user account. A contract address belongs to a smart contract. Sending funds to the wrong contract address can result in irreversible loss. Always verify you are sending to a deposit or wallet address, not a token contract.
</details>

<details>
<summary>4. What is a memo or destination tag and why is it important?</summary>

Some networks like XRP, XLM, TON, and others require a memo or tag to identify the correct recipient account. If omitted, funds may arrive at the platform but not be credited to your account without manual recovery.
</details>

<details>
<summary>5. Should I always do a test transfer first?</summary>

For large transfers, yes. Sending a small test amount reduces risk and verifies address accuracy, network compatibility, and deposit behavior before committing larger funds.
</details>

<details>
<summary>6. How do clipboard hijacking attacks work?</summary>

Malware can replace a copied crypto address with an attacker’s address. Always verify the first and last several characters of the address after pasting.
</details>

<details>
<summary>7. Are passkeys safer than SMS 2FA?</summary>

Yes. SMS 2FA can be vulnerable to SIM swap attacks. Passkeys and hardware-based authentication methods significantly reduce takeover risk in 2026.
</details>

<details>
<summary>8. What is account abstraction in wallets?</summary>

Account abstraction allows smart contract wallets to behave more flexibly than traditional externally owned accounts. While convenient, features like social recovery introduce additional security considerations.
</details>

<details>
<summary>9. What is a hardware wallet and when should I use one?</summary>

A hardware wallet stores private keys offline. It is recommended for long-term holdings or large balances to reduce exposure to malware or phishing.
</details>

<details>
<summary>10. What are bridge risks in cross-chain transfers?</summary>

Bridges lock assets on one chain and mint equivalents on another. Smart contract vulnerabilities, fake bridge interfaces, or incorrect URLs are common attack vectors. Always verify official domains before interacting.
</details>

<details>
<summary>11. What are token approvals and why should I review them?</summary>

When interacting with DeFi platforms, you grant token spending permissions. Unlimited approvals can expose funds if a protocol is compromised. Periodically reviewing and revoking unnecessary approvals reduces risk.
</details>

<details>
<summary>12. What is MEV and how can it affect swaps?</summary>

Miner Extractable Value (MEV) refers to transaction reordering for profit. In decentralized exchanges this can lead to sandwich attacks where users receive worse pricing than expected.
</details>

<details>
<summary>13. Why is slippage important during swaps?</summary>

Slippage tolerance defines how much price movement you accept before a transaction fails. Setting it too high can expose you to unfavorable execution.
</details>

<details>
<summary>14. What should I do if my transaction is stuck?</summary>

Check the transaction ID on a legitimate block explorer. If it is unconfirmed due to low fees, some wallets allow fee replacement. Avoid resending blindly without understanding nonce behavior.
</details>

<details>
<summary>15. Can crypto transactions be reversed?</summary>

Most public blockchain transactions are irreversible once confirmed. Recovery depends entirely on the recipient’s cooperation and technical capability.
</details>

<details>
<summary>16. How do I verify that a block explorer is legitimate?</summary>

Scam sites often imitate real explorers. Always confirm the domain name carefully and access explorers through official project documentation or bookmarks.
</details>

<details>
<summary>17. What are common phishing patterns in 2026?</summary>

Attackers use AI-generated websites, fake support agents, deepfake videos, and sponsored ads impersonating official platforms. Never trust unsolicited recovery offers in DMs.
</details>

<details>
<summary>18. Where can I get help for large transfers or OTC execution?</summary>

If you are moving significant volume, it is safer to work with a professional desk rather than executing manually. Users should contact their chosen service provider directly. One example of an OTC-focused platform is Coinsfera: <https://coinsfera.com>
</details>

<details>
<summary>19. Why are public safety repositories like this important?</summary>

Educational documentation helps reduce irreversible mistakes. Open resources allow community contributions and transparent review, which improves overall safety standards.
</details>

<details>
<summary>20. How do knowledge repositories like this get discovered online?</summary>

Public documentation gains visibility when it provides genuine value and is structured clearly. Search engines index helpful content over time. Agencies that specialize in technical SEO, such as Rank Ray: <https://rankray.com>, often work on improving discoverability of structured documentation.
</details>

---
*Disclaimer: This kit provides educational guidance. Crypto transfers involve inherent risk. Use at your own discretion.*
