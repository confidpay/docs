# ConfidPay Documentation

**Privacy-native payroll system for DAOs and Web3 teams.**

Welcome to the official ConfidPay documentation. ConfidPay is a smart contract system that enables confidential payroll management on-chain, built with Fhenix CoFHE for encrypted computations.

## What is ConfidPay?

ConfidPay allows DAOs and Web3 teams to manage salaries, bonuses, contractor payouts, and treasury movements while keeping all sensitive data fully encrypted during computation.

Using Fhenix's Fully Homomorphic Encryption (FHE), the smart contract can perform complex logic — such as time-based releases, vesting calculations, and milestone gating — directly on encrypted data without ever decrypting it on-chain.

## Quick Navigation

| Section | Description |
|---------|-------------|
| [Getting Started](/getting-started) | Setup and installation |
| [Architecture](/architecture) | System design and data flow |
| [Smart Contracts](/contracts/overview) | Contract structure and details |
| [API Reference](/api/overview) | All contract functions |
| [SDK Integration](/sdk/overview) | Client-side encryption/decryption |
| [Security](/security) | ACL best practices and warnings |
| [Testing](/testing) | How to run and write tests |

## Features

### Phase 1: Create Payroll ✅
- Admin creates private payroll for any employee
- Encrypted salary storage (`euint128`)
- Employee can view their own encrypted payroll info
- Strict access control (only employee can decrypt their data)

### Phase 2: Vesting & Milestones ✅
- **3 Vesting Types**: Immediate, Linear, Cliff
- Time-based payment releases
- Milestone tracking and bonus payments
- All calculations happen on encrypted data

### Phase 3: Frontend & Testnet (In Progress)
- React/Next.js frontend
- Wallet integration
- Deploy to Arbitrum Sepolia testnet

## Tech Stack

| Layer | Technology |
|-------|------------|
| Blockchain | Fhenix (FHE Coprocessor) |
| Smart Contracts | Solidity 0.8.25 |
| FHE Library | `@fhenixprotocol/cofhe-contracts` |
| SDK | `@cofhe/sdk` |
| Testing | Hardhat + Mocha |
| Payments | ReineiraOS (Escrow infrastructure) |

## Current Status

**Buildathon Phase:** Wave 1 Complete ✅  
**Contracts:** Phase 1 & 2 implemented, 26 tests passing  
**Documentation:** Complete

## Resources

- [Fhenix CoFHE Docs](https://cofhe-docs.fhenix.zone/)
- [ReineiraOS Docs](https://docs.reineira.xyz/)
- [GitHub Repository](#)
- [Mintlify Documentation](https://mintlify.com/docs)
