<div align="center">

# Chronolox Protocol

**Decentralized Digital Inheritance & Time-Locked Hardware-Grade Secrets**

[![Website](https://img.shields.io/badge/Website-chronolox.com-d4af37?style=flat-square)](https://chronolox.com)
[![Beta Access](https://img.shields.io/badge/Beta-Registration%20Open-10b981?style=flat-square)](https://chronolox.com/community)
[![Telegram](https://img.shields.io/badge/Telegram-Chat-0088cc?style=flat-square&logo=telegram)](https://t.me/chronolox_chat)
[![X](https://img.shields.io/badge/X-@ChronoloxVault-black?style=flat-square&logo=x)](https://x.com/ChronoloxVault)
[![Bluesky](https://img.shields.io/badge/Bluesky-@chronolox-0285FF?style=flat-square&logo=bluesky)](https://bsky.app/profile/chronolox.bsky.social)

*Secure today. Unlock tomorrow.*  
*What matters today, delivered in the future.*

</div>

---

### What is Chronolox?

Chronolox is a decentralized, privacy-first protocol engineered to solve digital inheritance and long-term secret delivery without custodial risk or recurring subscription traps. 

It provides an autonomous way for individuals (particularly parents, estate planners, and privacy advocates) to store passwords, hardware wallet recovery keys, legal directives, and personal archives that unlock automatically on a fixed calendar date—or remain safely sealed as long as the creator postpones the unlock date.

### Core Architecture Highlights

```
┌────────────────────────────────────────────────────────┐
│                   CREATOR (Desktop)                    │
│   • 7 Core Life Wizards · 13 Guided Templates          │
│   • Client-side encryption into .clox archive          │
│   • Mobile Upload Bridge (document camera capture)     │
│   • Fiat-paid prepaid Vouchers (zero crypto required)  │
└──────────────────────────┬─────────────────────────────┘
                           │
             Cross-Chain Relayer Delivery
                           │
                           ▼
┌────────────────────────────────────────────────────────┐
│               ON-CHAIN ENFORCEMENT & TEE               │
│   • Polygon: Payments (Credits), Gas Pools, Notary     │
│   • Oasis Sapphire (TEE): Hardware-isolated key vault  │
│   • Append-only Time-Locked Secret Journal             │
└──────────────────────────┬─────────────────────────────┘
                           │
             Unlock Date Arrives (or Threshold Met)
                           │
                           ▼
┌────────────────────────────────────────────────────────┐
│                   HEIR (Desktop / USB)                 │
│   • Heir Unlocker (Wails / Go) or M-DISC drive         │
│   • Zero crypto wallets, zero gas fees required        │
│   • Decryption runs 100% locally client-side           │
└────────────────────────────────────────────────────────┘
```

- **Zero-Custody TEE Decryption:** Encryption keys remain locked inside an Oasis Sapphire hardware Trusted Execution Environment (TEE). Neither Chronolox developers, validators, nor cloud hosts can inspect secret contents.
- **Wallet-Free Onboarding via Credits & Vouchers:** Non-technical creators purchase closed-loop Vouchers using standard credit cards (Stripe). Heirs require zero cryptocurrency, zero gas tokens, and zero wallet setups to unlock their inheritance.
- **Append-Only Time-Locked Secret Journal:** Creators can continually append chronological, encrypted updates and personal notes over decades without breaking sealed archive hashes.
- **Public Notary Timestamping (Proof of Existence):** Quantum-resistant SHA3-512 hashes anchored on Polygon for independent proof of existence, prior art documentation, and tamper-proof verification without revealing file contents.
- **Century-Grade Media Support:** Full support for dual USB drives and ISO/IEC 16963 M-DISC archival optical media for 100+ year data retention.

---

### Selected Public Repositories

We publish selected Chronolox repositories here to support technical transparency, architecture inspection, specification verification, and community participation:

| Repository | Role | Purpose |
| :--- | :--- | :--- |
| [**`specs`**](https://github.com/Chronolox/specs) | Architecture & Security Specification | Full protocol specification, cryptographic boundaries, consensus mechanics, and the source code escrow failsafe. |
| [**`releases`**](https://github.com/Chronolox/releases) | Binary Releases & Signatures | Official pre-compiled binaries (`chronolox-heir`, `chronolox-cli`, `secret-maker`), release verification GPG keys, and checksum ledgers. |
| [**`.github`**](https://github.com/Chronolox/.github) | Community & Security Governance | Organization profile, responsible disclosure policy (`SECURITY.md`), and issue templates. |

---

### Public Binaries & Tools

During our commercial beta phase, pre-compiled, verifiable release binaries are distributed via GitHub Releases:

| Artifact | Target Audience | Primary Function | Distribution |
| :--- | :--- | :--- | :--- |
| **`chronolox-heir`** | Heirs & Family Members | Portable standalone reader to verify and unlock `.clox` capsules client-side without gas or crypto. | [Releases](https://github.com/Chronolox/releases) |
| **`chronolox-cli`** | Engineers & Power Users | Cross-platform terminal tool for scriptable secret creation, capsule inspection, and notary anchoring. | [Releases](https://github.com/Chronolox/releases) |
| **`secret-maker`** | Creators & Test Cohort | Desktop studio for building 3-layer capsules, filling form templates, and formatting archival USBs. | [Releases](https://github.com/Chronolox/releases) |

*All release binaries are position-independent executables (PIE), stripped, compressed, and signed with the official Chronolox release key.*

---

### Source Code Availability & Archival Failsafe

Chronolox operates under a proprietary commercial license during its active beta and bootstrap phase. However, because our founding principle is **"mathematics over promises,"** the protocol does not rely on security through obscurity, nor does it leave users vulnerable to company abandonment:

1. **Standard Cryptographic Primitives:** All user-side operations use peer-reviewed, industry-standard algorithms: AES-256-GCM, Argon2id, SHA3-512 (FIPS 202), and X25519.
2. **Autonomous Blockchain Contracts:** Once deployed to Polygon and Oasis Sapphire, time-lock enforcement and access control rules are immutable and non-custodial.
3. **The Embedded Source Code Dead-Man's Switch:**  
   Every official binary (`chronolox-heir`, `chronolox-cli`, `secret-maker`) carries an embedded, AES-256 encrypted archive containing the complete source code repositories (`sdk`, `relayer`, `heir`, `secret-maker`, `cli`).  
   The decryption key for this archive is governed by a long-term on-chain time-lock on the Oasis Sapphire TEE, postponed regularly by our engineering team while active. If Chronolox ever ceases operations or fails to postpone the release, the unlock key reveals automatically on-chain—allowing any user to run `chronolox-cli extract-source` to inspect, build, fork, and self-host the entire infrastructure in perpetuity.

---

### Security & Responsible Disclosure

If you believe you have discovered a security vulnerability in the Chronolox protocol, smart contracts, client cryptography, or binary distributions, please report it privately:

- **Email:** [`security@chronolox.com`](mailto:security@chronolox.com)
- **Policy:** Read our complete [Security Policy (SECURITY.md)](https://github.com/Chronolox/.github/blob/main/SECURITY.md).
- **Please do NOT report security vulnerabilities through public GitHub issues, discussions, or pull requests.**

---

### Join the Beta & Community

We are actively recruiting **beta testers** and **founding contributors** (marketing, community leaders, legal/estate advisors, and technical reviewers):

- **Test the Protocol:** Request early beta access and receive a complimentary test Voucher code at [chronolox.com/community](https://chronolox.com/community).
- **Contribute & Collaborate:** Explore founding contributor roles and our on-chain contributor framework at [chronolox.com/contributors](https://chronolox.com/contributors).
- **Community Chat:** Join our public discussion channel on Telegram at [t.me/chronolox_chat](https://t.me/chronolox_chat).
- **Feedback & Issues:** Submit usability feedback, documentation corrections, and bug reports through [specs issues](https://github.com/Chronolox/specs/issues) and [releases issues](https://github.com/Chronolox/releases/issues).

---

<div align="center">

<sub>Chronolox is developed by Frontware International Co., Ltd. for commercial operations via SecretVault LLC (Wyoming, USA).</sub>

</div>
