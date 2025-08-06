# finaitech-oraclegate
Smart contract powering FAT token purchases via real-time DEX pricing on Polygon.

# FATOracleGate – The DeFi Gateway of Fin AI Tech

This repository contains the smart contract powering FAT token purchases using real-time DEX pricing logic on the Polygon blockchain.

The **FATOracleGateV5** contract enables users to buy $FAT tokens with supported cryptocurrencies (e.g., MATIC, USDC) at a fixed USD rate, while fetching accurate conversion data from decentralized exchanges.

---

## 🔗 Deployed Contract

- **Contract Name:** `FATOracleGateV5`
- **Address:** `0xd5503FF132056e5dc57351616BaDCbaFe1baD7be`
- **Network:** Polygon Mainnet (Chain ID: 137)
- **Compiler:** Solidity ^0.8.25 with Cancun optimization

---

## 💡 Key Features

- 💱 **DEX-Powered Pricing:** Uses Uniswap/QuickSwap LP reserves to calculate real-time token exchange rates.
- 🧮 **Fixed Rate:** 1 USD = 1,000 FAT tokens.
- 🔐 **No Minting:** FAT is pre-supplied and distributed from a treasury address.
- 🧰 **Failover Logic:** Robust `try/catch` blocks for LP calls, decimals, and fallback values.
- 🔍 **View-Only Market Cap:** Built-in `getMarketCap()` view function for transparency.
- 🔄 **Native MATIC + USDC Support:** Direct payments with Polygon-native tokens.

---

## ⚙️ Constructor Arguments (Deployed Instance)

| Parameter        | Address |
|------------------|---------|
| Treasury Address | *[Your FAT treasury wallet]* |
| USDC Token       | `0x3c499c542cEF5E3811e1192ce70d8cC03d5c3359` |
| FAT Token        | `0x398D9ae716ACb91122755d41B113b142E11Da60a` |

---

## 📁 Repository Structure

```plaintext
finaitech-oraclegate/
├── contracts/
│   └── FATOracleGateV5.sol
├── deployment/
│   └── deployment_notes.md
├── integrations/
│   └── supported_tokens.md (placeholder)
└── README.md

