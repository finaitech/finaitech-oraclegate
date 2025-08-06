# Deployment Notes – FATOracleGateV5

## 🔗 Contract Address
- `0xd5503FF132056e5dc57351616BaDCbaFe1baD7be`

## 📅 Deployment Details
- **Deployed on:** Polygon Mainnet (chainId: 137)
- **Deployed via:** Remix IDE
- **Compiler Version:** Solidity ^0.8.25
- **EVM Target:** Cancun (Optimized)

## ⚙️ Constructor Arguments
- **Treasury address:** 0x994150F1f32BF6308D0E724433aA3F3e718fEd5d
- **USDC token:** 0x3c499c542cEF5E3811e1192ce70d8cC03d5c3359
- **FAT token:** 0x398D9ae716ACb91122755d41B113b142E11Da60a

## 🧠 Key Features
- Real-time price conversion using DEX LPs
- Fallback pricing logic with robust try/catch
- Fixed rate: 1 USD = 1000 FAT
- View-only `getMarketCap()` function
- Handles native MATIC and USDC
- Future placeholder tokens (e.g. AMBR, BNB) are included

## 📝 Notes
- Pre-approved FAT allowance from treasury to OracleGate
- Contract interacts with QuickSwap/Uniswap LP pairs
- Designed for extensibility

