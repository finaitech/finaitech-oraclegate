# Supported Tokens – FATOracleGateV5

This file documents the cryptocurrencies supported by the `FATOracleGateV5` smart contract for purchasing $FAT tokens. The contract integrates with decentralized liquidity pools (DEXes) to fetch accurate price conversions in real time.

---

## ✅ Currently Supported Tokens

| Token        | Symbol | Address                                                                  | Type         | Status     |
|--------------|--------|--------------------------------------------------------------------------|--------------|------------|
| USD Coin     | USDC   | `0x3c499c542cEF5E3811e1192ce70d8cC03d5c3359`                             | Stablecoin   | ✅ Native   |
| MATIC        | MATIC  | Native (sent as msg.value)                                               | Native Coin  | ✅ Supported |

---

## 🧠 Logic Overview

- **USDC:**  
  Sent as an ERC-20 token. Amount is converted 1:1 USD to $FAT (1 USD = 1000 FAT).  
  Example: Sending 10 USDC mints 10,000 FAT (from treasury supply).

- **MATIC (Native):**  
  Sent as `msg.value`. The contract fetches current MATIC/USDC price from DEX LP pairs (e.g., QuickSwap).  
  Amount of FAT is calculated using the converted USD value.

---

## 🔜 Placeholder Tokens (Future Support)

| Token        | Symbol | Status       |
|--------------|--------|--------------|
| Ambrosia     | AMBR   | 🕐 Planned   |
| Wrapped ETH  | WETH   | 🕐 Planned   |
| Binance Coin | BNB    | 🕐 Planned   |
| DAI          | DAI    | 🕐 Planned   |

These tokens are pre-coded as placeholders in `FATOracleGateV5` for future expansion. They are currently not active but may be enabled in future releases.

---

## 🔒 Security Notes

- The contract uses try/catch logic and decimals handling to safely support various tokens.
- Unsupported or incorrectly configured tokens will not be accepted.
- Only pre-approved LP pairs will be trusted for pricing.

---

## 🌐 More Info

- Token Purchase Contract: [`FATOracleGateV5`](../contracts/FATOracleGateV5.sol)
- Main Token: [`FAT`](https://polygonscan.com/address/0x398D9ae716ACb91122755d41B113b142E11Da60a)
- Website: [https://finaitech.net](https://finaitech.net)

