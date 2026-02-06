# Portfolio / Wallet Analyzer  

![License](https://img.shields.io/badge/License-Custom-green) ![Version](https://img.shields.io/badge/Version-1.0-blue)

**Concept White Paper – Radix Ecosystem**  

**Author**: 73arte  
**Date**: January 27, 2026  

---

## Table of Contents

- [Purpose](#purpose)  
- [Core Problem Solved](#core-problem-solved)  
- [Scope & Design Principles](#scope--design-principles)  
- [Asset Coverage](#asset-coverage)  
- [Key Features](#key-features)  
- [Monetizable Features (Premium Tier – Optional)](#monetizable-features-premium-tier--optional)  
- [Security Model](#security-model)  
- [License (Custom – Dev Friendly)](#license-custom--dev-friendly)  
- [Challenges for Developers](#challenges-for-developers)  

---

## Purpose

The Portfolio / Wallet Analyzer is a read-only,  
community-driven tool designed to give Radix users a reliable,  
neutral and comprehensive view of the **real economic value**  
of their on-chain assets.

It addresses the core opacity of modern Radix DeFi:  

- Value hidden in composable derivatives (LSU, LSULP, LP tokens)  
- Stacked / compounded yields  
- Fragmented data across protocols  
- No meaningful insight from raw wallet balances alone  

---

## Core Problem Solved

Users cannot easily answer:  

- What do I truly own right now?  
- What is each position earning (or costing) per day?  
- What is the net value after debts and realistic liquidity?  

The Analyzer provides:  

- Instant snapshot of the full portfolio  
- Accurate translation of derivatives to underlying economic value  
- Multi-account aggregation with selective inclusion  
- Transparent yield & cost calculation at snapshot time  
- No projections, no hype, no transaction execution  

---

## Scope & Design Principles

- Read-only: no signing, no approvals, no custody  
- Protocol-agnostic: no hard dependency on any specific dApp  
- Future-proof: works as long as Radix exposes public state  
- Transparent limitations: data freshness, oracle latency, minor temporal discrepancies acknowledged  
- Community aggregation: consumes existing public endpoints & on-chain data (no duplication of analytics work)  

---

## Asset Coverage

- Native & standard fungible tokens (XRD, other native resources)  
- DeFi derivatives  
  - Liquid Stake Units (LSU) — fungible per validator  
  - Liquidity Provider tokens (LP)  
  - Composable LSU-LP derivatives (LSULP, etc.)  
  - Pool receipt tokens  
- Yield-generating positions (swap fees, lending interest, incentives — treated by economic origin)  
- NFTs  
  - Ownership / rights NFTs  
  - Temporary unstaking claim NFTs (validator withdrawal receipts)  
  - Other financial position NFTs  
- Potential future RWA (tokenized real-world assets — marked as optional)  

**Note on staking**: No separate "staking" category. On Radix Babylon,  
staking exposure is materialized exclusively through tokenized derivatives (mainly LSU fungible tokens). Unstaking claims are temporary NFTs.  

---

## Key Features

- Multi-account support with dynamic inclusion/exclusion  
- Class filtering (DeFi, NFTs, borrowing, etc.)  
- Current estimated value + daily yield/cost per position  
- Consolidated net value (XRD + fiat via user-chosen oracles)  
- User-controlled data refresh & snapshot timestamping  

---

## Monetizable Features (Premium Tier – Optional)

The tool can offer advanced, user-paid features that provide  
significant value for serious users, compliance needs,  
or long-term tracking:

- **Automated historical tracking**  
  - Scheduled snapshots (daily, weekly, monthly) via background bot  
  - Time-series view of portfolio evolution (gains/losses, yield changes, position shifts)  
  - Alerts for major changes (e.g., collateral ratio, large impermanent loss)  

- **Accounting & fiscal reporting**  
  - Exportable reports in CSV, Excel or PDF  
  - Realized gains/losses per position and per period (for tax declaration)  
  - FIFO/LIFO cost basis tracking (configurable)  
  - Compliance-oriented summaries (e.g., aligned with MiCA/DAC8 requirements in EU)  
  - Multi-currency fiat conversion history (user-fixed exchange rates for consistency)  

These premium features remain optional, fully user-controlled,  
with no impact on the free core functionality.  

---

## Security Model

- No private key access  
- No transaction capability  
- Wallet connection only for read access (state queries)  
- No smart contract interaction from the tool itself  

---

## License (Custom – Dev Friendly)

**Attribution + Non-Commercial + Royalties on Monetization**

You are free to:  

- Use, study, modify, fork this concept  
- Build tools, apps, extensions, dashboards inspired by it  

You must:  

- Keep the original attribution ("Concept by 73arte") visible in your project (README, about page, UI footer)  
- Not use it for purely commercial purposes without agreement  

If your implementation generates revenue  
(premium features, subscriptions, paid exports, ads, sponsorships, donations with perks, app-store monetization, etc.),  
you agree to pay **5% royalties** on net revenue to the author (73arte),  
paid in XRD to the following dedicated royalties wallet address:
```
account_rdx129fp4pq235uqedczchsluk3363q45x0u9s7f9h7tsw56pglpju6vue
```

This is a moral & community convention — not enforceable by smart contract,  
but expected in the Radix open ecosystem.  

---

## Challenges for Developers

1. Resolve real underlying XRD value of any LSULP / composable derivative in < 2s using public Radix API + pool state queries.  
2. Aggregate multi-account positions with dynamic filtering without performance degradation on mobile.  

---

Feedback or questions → open an issue on this repository.
