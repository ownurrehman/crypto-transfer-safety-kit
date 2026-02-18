# Exchange Safety: Deposit and Withdrawal Checklist

Centralized Exchanges (CEXs) are the gateways to the crypto world. Most "lost" funds occur during the interface between self-custody wallets and these platforms.

## 1. The Pre-Withdrawal Checklist

Before moving funds *out* of an exchange:

- [ ] **Verify Network Support:** Does the destination wallet support the network you selected? (e.g., Do not send to a "Base" address if you are using a legacy "Ethereum" wallet).
- [ ] **Check Maintenance Windows:** Is the network currently undergoing an upgrade? Exchanges often pause deposits/withdrawals during "Hard Forks."
- [ ] **Address Whitelisting:** Use the CEX's "Address Book" feature. Set a 24-hour delay on new addresses. This prevents an attacker from instantly draining your funds if they gain access to your account.
- [ ] **Anti-Phishing Code:** Enable this in your CEX settings. It adds a secret word to every email sent by the exchange, so you know it's not a fake support email.

## 2. The Pre-Deposit Checklist

Before moving funds *into* an exchange:

- [ ] **Generate a NEW Address:** Exchanges often rotate addresses for privacy and security. Never send funds to an address you used 6 months ago without checking the "Deposit" page first.
- [ ] **Match the Asset EXACTLY:** USDC is not the same as USDC.e (bridged). Sending bridged assets to a native-only deposit address will result in a loss.
- [ ] **Memo/Tag Requirement:** If the exchange says a Memo is required, it is NOT OPTIONAL.
- [ ] **Minimum Deposit Amount:** Some exchanges (like Kraken or Poloniex) have minimums (e.g., "Minimum 50 TRX"). If you send 49 TRX, it will not be credited, and the cost of recovery usually exceeds the value.

## 3. API Key Security

If you use trading bots or portfolio trackers:

- **Withdrawal Permissions:** Never enable "Withdraw" permissions on an API key unless you are a developer building a specific automated bridge.
- **IP Binding:** Only allow the API key to be used from your specific home or server IP address.

## 4. Withdrawal Throttling and Limits

CEXs in 2026 have aggressive AI-driven security. If you suddenly try to withdraw your entire balance to a new address:

- Expect a "Security Freeze" for 24-48 hours.
- Expect a "Video Verification" (Liveness check) request.
- **Plan ahead:** For large purchases (like a house), start your withdrawals 3-5 days in advance.

## 5. Recovering "Wrong Network" CEX Deposits

If you used the wrong network for a CEX deposit:

1. **Document everything:** Save the Transaction Hash (TXID) and screenshots.
2. **Check the Self-Service Recovery Tool:** Major exchanges (Binance, Coinbase) now have automated tools where you can pay a service fee (usually 50-200 USDT) for them to use their internal keys to send the funds back to you.
3. **Avoid Fake Support:** Real exchange support will NEVER ask for your password or a "security fee" via Telegram.

---
**Next Step:** Understand the bridge risks in [DeFi and Bridges](docs/05-defi-and-bridges/bridge-risk-model.md).
