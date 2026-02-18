# Incident Response: After a Mistake

If you have sent funds to the wrong address or network, speed and clinical accuracy are your only allies. Panic usually leads to a second, larger mistake.

## 1. Immediate Technical Audit

Stop. Do not send another transaction. Document the following:

1. **Transaction ID (TXID) / Hash:** The unique 64-character string of your transfer.
2. **Sender Address:** Your wallet address.
3. **Recipient Address:** Where the funds actually went.
4. **Network Name:** (e.g., Ethereum Mainnet, BSC, Tron).
5. **Asset:** (e.g., ETH, USDT, USDC).

## 2. Identify the Destination Category

### A. It went to a "Self-Custody" address you own (Wrong Network)

This is the best-case scenario. If you sent USDT to your own Polygon address instead of Ethereum, you own the keys.

- **Action:** Add the Polygon network to your wallet. Use the same seed phrase. Your funds will be there.

### B. It went to a Centralized Exchange (CEX)

- **Action:** Contact their support **immediately**. Provide the TXID.
- **Reality Check:** If it's a "Wrong Network" deposit (e.g., sending to Coinbase via a network they don't support), it is technically possible for them to recover it, but they may refuse for policy reasons. Be prepared to pay a "Recovery Fee."

### C. It went to a Smart Contract (e.g., the USDT contract)

- **Action:** Check if the contract has a "Rescue" function.
- **Reality Check:** 99.9% of the time, tokens sent to a contract address are permanently locked. No one, not even the contract creator, can get them out.

### D. It went to a Scammer / Phisher

- **Action:** Report the address to `etherscan.io` and `chainabuse.com`.
- **Reality Check:** Funds are gone. No legitimate "Recovery Agent" on Instagram or Telegram can get them back. Anyone claiming to be a "Hacker for Hire" to recover scammed funds is a second-stage scammer.

## 3. The "Recovery Scam" Warning

Once you post about a lost transfer on Reddit, Discord, or Twitter, you will be flooded with DMs:

- "Contact @TechRevover on Instagram, he helped me get my 10 BTC back!"
- "I am from MetaMask Support, please provide your seed phrase for verification."

**These are all scams.** Blockchain transactions cannot be reversed. Only the person holding the private keys to the destination address can move the funds.

## 4. Documentation for Legal / Tax Purposes

If the loss is significant:

1. **Police Report:** In some jurisdictions, you can file a cybercrime report which may be required by your insurance or for tax write-offs.
2. **Tax Professional:** Consult an expert. In many countries, "lost or stolen" crypto can be claimed as a capital loss, reducing your tax burden on future gains.

---
**Next Step:** Familiarize yourself with the [Glossary](docs/08-glossary/terms.md).
