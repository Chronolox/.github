# Security Policy

## Reporting a Vulnerability

Chronolox considers the security of its decentralized time-locking protocol, smart contracts, and client software of paramount importance.

If you believe you have discovered a security vulnerability in any Chronolox repository, binary, contract, or infrastructure component, please report it privately.

**Do NOT report vulnerabilities through public GitHub issues, discussions, or pull requests.**

### How to Report Privately

1. **Email:** Send an email to **`security@chronolox.com`**.
2. **GitHub Private Vulnerability Reporting:** If enabled on the specific repository, you can submit a private security advisory through the repository's **Security** tab &rarr; **Report a vulnerability**.

### What to Include in Your Report

To help us triage and investigate the issue efficiently, please include:
- A clear description of the vulnerability and its potential impact.
- The affected repository, component, version, commit, or smart contract address.
- Step-by-step reproduction instructions or a minimal proof-of-concept (PoC).
- Any proposed remediation, if available.

### What Happens Next

- **Acknowledgement:** We will acknowledge receipt of your report within 48 hours.
- **Investigation:** Our engineering desk will investigate and assess the vulnerability severity.
- **Coordination & Fix:** We will coordinate remediation, test the patch across enclaves/contracts/binaries, and prepare release artifacts.
- **Disclosure:** We will coordinate with you on responsible public disclosure once fixes are deployed.

Please maintain confidentiality until an official fix is released.

## Scope & Cryptographic Boundaries

- **Oasis Sapphire TEE Enclaves:** Hardware-isolated consensus key custody.
- **drand Threshold Timelock:** Decentralized fallback time-locking mechanism.
- **Client AEAD & Calldata:** Local encryption in `secret-maker`, `chronolox-cli`, and `chronolox-heir`.
- **Polygon Smart Contracts:** Payment verification, Credits accounting, and Notary proof-of-existence registry.
