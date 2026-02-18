# Wallet Security 2026: Passkeys and Account Abstraction

The era of the 12-word seed phrase as the *only* way to secure funds is ending. In 2026, we utilize **Account Abstraction (AA)** and **Passkeys** to eliminate the single point of failure that has led to billions in losses.

## 1. What is Account Abstraction (ERC-4337)?

Traditional wallets (like the original MetaMask) are **EOAs (Externally Owned Accounts)**. A private key controls them directly. If you lose the key, you lose the funds.

**Smart Contract Wallets (AA)** are different. The wallet is a smart contract. You can program rules into it:

- **Daily Spend Limits:** "Don't allow more than $500/day to be sent."
- **Social Recovery:** "If I lose my access, let my 3 chosen friends/guardians vote to give me a new key."
- **Gas Abstraction:** "Pay for transaction fees in USDT instead of ETH."

## 2. Passkeys: The Seed Phrase Killer

Passkeys (WebAuthn) use the secure enclave of your phone or laptop (FaceID, TouchID) to sign transactions.

### Why Passkeys are Superior

- **Phishing Resistant:** You cannot "type" a passkey into a fake website. The browser only provides the passkey to the legitimate domain.
- **No Seed Phrase to Steal:** There is no physical list of words to be found by a burglar or accidentally uploaded to iCloud.
- **Biometric Security:** Access requires your physical biometric presence.

## 3. The 2026 "Gold Standard" Security Model

For maximum safety, sophisticated users now use a **Hybrid Hardware + Passkey AA Model**:

1. **Operation Key:** A Passkey on your mobile device for daily transactions (up to a limit).
2. **Vault Key:** A Hardware Wallet (Ledger, Trezor, Keystone) stored in a safe for large transfers.
3. **Guardian Set:** Three trusted entities (family members, a legal firm, or a backup hardware wallet) that can recover the account if the Operation Key and Vault Key are both lost.

## 4. Risks of Social Recovery

While "Guardians" help you recover funds, they introduce a new attack vector: **Collusion**.
If your guardians are compromised or turn against you, they can vote to transfer ownership of your Smart Contract wallet.

**Safety Tip:** Use a mix of "Human Guardians" (friends) and "Institutional Guardians" (trusted security companies) with a **Time Lock**. A transaction to change guardians should always have a 48-hour delay during which you can cancel it.

## 5. Why SMS 2FA is Obsolete

In 2026, SMS-based 2FA is considered a "critical vulnerability" due to **SIM Swapping**. Attackers bribe telecom employees or use AI voice cloning to trick support into porting your number to their SIM.

**Always Use:**

- **App-Based Auth:** Authy, Google Authenticator (with cloud backup disabled).
- **Yubikeys / FIDO2 Hardware:** The only method that is 100% resistant to remote phishing.

## 6. Blind Signing: The Final Trap

Even with the best wallet, you can still lose funds by "Blind Signing" a transaction. This happens when your wallet displays a "Signature Request" with unreadable hex data.

**The Rule:** Never sign a transaction if the wallet interface doesn't show exactly what is happening (e.g., "Giving app.uniswap.org permission to spend 500 USDC").

---
**Next Step:** Learn how to bridge safely in [DeFi and Bridges](docs/05-defi-and-bridges/bridge-risk-model.md).
