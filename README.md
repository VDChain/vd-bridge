<div align="center">

<img src="https://raw.githubusercontent.com/VDChain/brand-assets/main/logo_256.png" width="80" height="80" alt="VDChain Logo" />

# VD Bridge

### Official Cross-Chain Bridge — BSC ↔ VDChain

[![Live](https://img.shields.io/badge/Status-Live-22C55E?style=for-the-badge)](https://bridge.vdscan.io)
[![BSC](https://img.shields.io/badge/From-BSC-F59E0B?style=for-the-badge)](https://bridge.vdscan.io)
[![VDChain](https://img.shields.io/badge/To-VDChain-3B82F6?style=for-the-badge)](https://bridge.vdscan.io)
[![Chain](https://img.shields.io/badge/Chain%20ID-882022-8B5CF6?style=for-the-badge)](https://vdscan.io)

**[Launch Bridge](https://bridge.vdscan.io)** · **[Explorer](https://vdscan.io)** · **[GitHub](https://github.com/VDChain)**

</div>

---

## Overview

VD Bridge is the official cross-chain bridge connecting Binance Smart Chain (BSC) and VDChain Mainnet (Chain ID: 882022). It enables seamless transfer of tokens between the two networks using a lock-and-mint / burn-and-release mechanism secured by smart contracts on both chains.

Users can bridge USDT, WBNB, and WETH from BSC to VDChain, where they are represented as VD20-wrapped ERC-20 tokens — fully tradeable on VDSwap and usable across the VDChain DeFi ecosystem.

---

## Supported Assets

| Token | BSC Contract | VDChain Contract |
|-------|-------------|-----------------|
| USDT | BSC Native USDT | `0xA64bebb4Fc97383FE05492AF94A08fcfA3adbF2A` |
| WBNB | BSC Native WBNB | `0xF0E0E3fa91591b7d5F86dD22E1e21a5c56022A33` |
| WETH | BSC Native WETH | `0x2f231e39d2267b5a26d5c87d65A991e060071120` |

---

## How It Works

### BSC → VDChain (Deposit)

User approves token on BSC
User deposits token to Bridge Vault on BSC
Relayer detects deposit event
Equivalent wrapped token minted on VDChain
Token arrives in user wallet on VDChain


### VDChain → BSC (Withdraw)

User burns wrapped token on VDChain
Relayer detects burn event
Original token released from Bridge Vault on BSC
Token arrives in user wallet on BSC


---

## Smart Contracts

### BSC Contracts
| Contract | Address |
|----------|---------|
| Bridge Vault | `0xf6F665A8ddAE95fFDe719a3EB1B732b3e5962150` |

### VDChain Contracts
| Contract | Address |
|----------|---------|
| Bridge Controller | `0xB5e568d091820DDe97A81FE3845EF7F66472ac92` |
| USDT (VD20) | `0xA64bebb4Fc97383FE05492AF94A08fcfA3adbF2A` |
| WBNB (VD20) | `0xF0E0E3fa91591b7d5F86dD22E1e21a5c56022A33` |
| WETH (VD20) | `0x2f231e39d2267b5a26d5c87d65A991e060071120` |

---

## Token Standard — VD20

All bridged tokens on VDChain follow the **VD20** standard — an ERC-20 extension with controlled mint and burn:

- `mint(address to, uint256 amount)` — Called by bridge on deposit
- `burn(address from, uint256 amount)` — Called by bridge on withdrawal
- Only the Bridge Controller can mint or burn tokens
- Fully ERC-20 compatible — works with MetaMask, VDSwap, and all VDChain DApps

---

## How to Use

### Deposit (BSC → VDChain)

1. Visit [bridge.vdscan.io](https://bridge.vdscan.io)
2. Connect MetaMask — ensure you are on **BSC Network**
3. Select token to bridge (USDT, WBNB, or WETH)
4. Enter amount
5. Click **Bridge to VDChain** and confirm transactions:
   - Transaction 1: Approve token spending
   - Transaction 2: Deposit to bridge vault
6. Wait for confirmation (~1-3 minutes)
7. Token appears in your wallet on VDChain

### Withdraw (VDChain → BSC)

1. Visit [bridge.vdscan.io](https://bridge.vdscan.io)
2. Connect MetaMask — ensure you are on **VDChain Network**
3. Select token to withdraw
4. Enter amount
5. Click **Bridge to BSC** and confirm transaction
6. Wait for confirmation (~1-3 minutes)
7. Original token released to your BSC wallet

---

## Network Setup

### Add VDChain to MetaMask
Network Name: VDChain
RPC URL:      https://rpc.vdscan.io
Chain ID:     882022
Symbol:       VDC
Explorer:     https://vdscan.io

### BSC Network
Network Name: BNB Smart Chain
RPC URL:      https://bsc-dataseed.binance.org
Chain ID:     56
Symbol:       BNB
Explorer:     https://bscscan.com

---

## Security

- Smart contracts deployed and verified on both networks
- Bridge Controller uses `onlyBridge` modifier — only authorized relayer can mint/burn
- No admin upgrade keys — contracts are immutable after deployment
- All bridge transactions visible on VDScan and BSCScan

---

## Links

| Resource | URL |
|----------|-----|
| Bridge App | https://bridge.vdscan.io |
| VDChain Explorer | https://vdscan.io |
| BSC Vault on BSCScan | https://bscscan.com/address/0xf6F665A8ddAE95fFDe719a3EB1B732b3e5962150 |
| GitHub Organization | https://github.com/VDChain |
| Smart Contracts | https://github.com/VDChain/smart-contracts |

---

<div align="center">

**Built on VDChain Mainnet · Chain ID: 882022 · Powered by VDC**

</div>
