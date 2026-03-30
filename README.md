# ConfidPay Documentation

Confidential payroll and treasury rail for DAOs and Web3 teams — powered by Fhenix CoFHE + Privara SDK.

## Quick Start

```bash
# Preview documentation locally
npm i -g mint
mint dev

# Check for broken links
mint broken-links
```

## Documentation Structure

```
docs/
├── index.mdx              # Landing page
├── introduction.mdx      # What is ConfidPay
├── architecture.mdx      # System architecture
├── quickstart.mdx        # End-to-end quickstart
├── development.mdx       # Local development setup
├── contracts/
│   ├── overview.mdx      # Smart contracts overview
│   └── payroll-contract.mdx  # Complete contract reference
├── frontend/
│   └── react-hooks.mdx   # @cofhe/react integration
├── privara-integration.mdx  # Privara SDK integration
└── security/
    └── acl-best-practices.mdx  # ACL security guide
```

## Tech Stack

| Layer | Technology |
|-------|------------|
| Encrypted Compute | Fhenix CoFHE Coprocessor |
| Payment Rail | Privara SDK |
| Smart Contracts | Solidity + FHE.sol |
| Frontend | Next.js + @cofhe/react |
| Development | Hardhat + cofhe-hardhat-starter |

## Supported Networks

- **Base Sepolia** (Testnet)
- **Arbitrum Sepolia** (Testnet)

## Resources

- [Fhenix Documentation](https://docs.fhenix.io)
- [Privara SDK](https://github.com/reineiralabs/sdk)
- [CoFHE Hardhat Starter](https://github.com/confidpay/cofhe-hardhat-starter)

## License

MIT
