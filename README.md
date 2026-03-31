# ConfidPay Documentation

**Confidential payroll and treasury rail for DAOs and Web3 teams**  
Built with **Fhenix CoFHE** (Fully Homomorphic Encryption) + **Privara SDK**

This repository contains the official documentation for ConfidPay — a privacy-by-design payroll and treasury platform currently in development for the Fhenix Privacy-by-Design Buildathon.

## What is ConfidPay?

ConfidPay allows DAOs and Web3 teams to manage salaries, bonuses, contractor payouts, and treasury movements **while keeping all sensitive data fully encrypted during computation**.

Using Fhenix’s Fully Homomorphic Encryption (FHE), the smart contract can perform complex logic — such as time-based releases, vesting calculations, and milestone gating — directly on encrypted data (`euint256`) without ever decrypting it on-chain.

Only the intended recipient (or authorized auditor) can decrypt their own information client-side. This creates true end-to-end confidentiality while maintaining full on-chain verifiability and composability.

## Core Concept

- **Encrypted State**: Salaries, recipients, vesting schedules, and milestone conditions are stored as encrypted values.
- **Homomorphic Computation**: The contract uses CoFHE to run operations (`add`, `sub`, `lte`, `ifThenElse`) on encrypted data via the off-chain coprocessor.
- **Access Control**: Strict ACL system (`FHE.allowThis()` and `FHE.allow()`) ensures only permitted parties can decrypt.
- **Private Payments**: Privara SDK handles confidential USDC transfers and escrow logic.

This approach solves the fundamental problem of transparent blockchains: exposure of sensitive financial data, while still allowing programmable, trustless execution.

## Key Technical Features

- Encrypted payroll records using `euint128` fields
- Programmable rules computed homomorphically on encrypted state
- Selective disclosure for compliance and audits
- Full EVM composability with other contracts
- Client-side encryption/decryption using `@cofhe/react`

## Documentation Structure

This documentation is structured to clearly explain the vision, architecture, and implementation path:

- **Introduction** — Problem statement and privacy-by-design approach
- **Architecture** — System design and data flow
- **Smart Contracts** — Contract architecture and `ConfidPay.sol` skeleton
- **Integrations** — How CoFHE and Privara work together
- **Frontend** — Planned React integration with `@cofhe/react`
- **Security** — ACL best practices and critical warnings

## Current Status

We are currently in **Wave 1** of the Fhenix Buildathon.  
This repository contains the detailed concept, architecture, and technical documentation.  
Implementation of the working prototype (contract deployment + end-to-end flow) is planned for Wave 2 and beyond.

## Tech Stack

- **Encrypted Compute**: Fhenix CoFHE Coprocessor + `FHE.sol`
- **Payment Layer**: Privara SDK (`@reineira-os/sdk`)
- **Smart Contracts**: Solidity + `@fhenixprotocol/cofhe-contracts`
- **Frontend (planned)**: Next.js + `@cofhe/react`
- **Development**: Hardhat + cofhe-hardhat-starter

## Supported Testnets

- Base Sepolia
- Arbitrum Sepolia

## Resources
- ConfidPay Documentation: https://confidpay-50c7598f.mintlify.app
- Fhenix Documentation: https://docs.fhenix.io
- CoFHE Documentation: https://cofhe-docs.fhenix.zone
- Privara Documentation: https://reineira.xyz/docs

## License

MIT
