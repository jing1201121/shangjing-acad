# Blockchain Proposal Dataset Schema

This dataset collects **all publicly available proposal documents** from major blockchain ecosystems — including **Ethereum**, **Solana**, and **BNB Chain** — and parses their original Markdown (`.md`) files into a unified, machine-readable **CSV format**.  
It enables structured analysis of protocol innovation, governance evolution, and inter-proposal dependency networks.

---

## Source Description

| Ecosystem | Repository | Example File |
|------------|-------------|---------------|
| **Ethereum (EIPs & ERCs)** | [ethereum/EIPs](https://github.com/ethereum/EIPs) | `EIPS/eip-1.md` |
| **Solana (SIPs)** | [solana-foundation/solana-improvement-documents](https://github.com/solana-foundation/solana-improvement-documents) | `sips/sip-1.md` |
| **BNB Chain (BEPs)** | [bnb-chain/BEPs](https://github.com/bnb-chain/BEPs) | `BEPs/BEP1.md` |

Each proposal file follows a standardized Markdown structure:

1. **Front Matter (YAML headers)** — structured metadata such as ID, title, type, status, author(s), and creation date.  
2. **Main Body** — narrative content including *Abstract*, *Motivation*, *Specification*, and *Rationale* sections.

Example (from **EIP-1**):

```markdown
---
eip: 1
title: EIP Purpose and Guidelines
status: Living
type: Meta
author: Martin Becze <mb@ethereum.org>, Hudson Jameson <hudson@ethereum.org>
created: 2015-10-27
---
```

---

## Conceptual Background

Improvement proposals (IPs) serve as formal governance and coordination mechanisms for blockchain ecosystems.

- **EIPs (Ethereum Improvement Proposals)** define changes to the Ethereum protocol, interfaces, and applications.  
  - **ERCs (Ethereum Request for Comments)** are *application-level* EIPs specifying standards like ERC-20 and ERC-721.  
  - In this dataset, ERCs are categorized within EIPs under `category = "ERC"`.  
- **SIPs (Solana Improvement Proposals)** describe proposed enhancements to Solana’s runtime, consensus, or development layers.  
- **BEPs (BNB Chain Evolution Proposals)** formalize protocol and token-standard changes within the BNB ecosystem.

All proposals progress through stages such as  
`Idea → Draft → Review → Last Call → Final → Living / Withdrawn`,  
capturing the technical and governance lifecycles of blockchain standards.

---

## File Table Structure

| Field | Description |
|--------|-------------|
| **id** | Unique proposal identifier (e.g., `EIP-1559`, `ERC-20`, `SIP-12`, `BEP-2`) |
| **title** | Short, descriptive title of the proposal |
| **type** | Proposal type (`Standards Track`, `Meta`, `Informational`, etc.) |
| **status** | Lifecycle status (`Draft`, `Review`, `Final`, `Living`, `Withdrawn`, etc.) |
| **created** | Proposal creation date (ISO 8601 format) |
| **requires** | List of proposal IDs that this proposal depends on |
| **author** | Author name(s) or GitHub handle(s) |
| **in_degree** | Number of proposals citing this one |
| **out_degree** | Number of other proposals cited by this one |
| **citation** | List of referenced proposals (outgoing citations) |
| **cited** | List of proposals that cite this one (incoming citations) |
| **abstract** | Concise technical summary from the Markdown *Abstract* section |
| **category** | Top-level classification (`Core`, `Networking`, `Interface`, `ERC`, etc.) |
