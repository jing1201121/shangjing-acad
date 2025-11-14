# Knowledge Graph of Token Supply Mechanisms in Blockchain Tokenomics

This self-constructed dataset represents a **knowledge graph of token supply mechanisms** across approximately **300 blockchain systems** and models how decentralized economies design, issue, and regulate their native tokens — forming a structured representation of **blockchain-based monetary architectures**.

The database integrates textual and quantitative information from **official whitepapers**, **project websites**, and **tokenomics data** retrieved via a custom CoinMarketCap crawler.  Using a **large language model (DeepSeek-V3)**, unstructured textual descriptions were automatically extracted and transformed into structured fields, followed by **manual verification and analytical classification**.

This knowledge graph bridges **institutional narratives and economic parameters**, allowing comparative analysis of how blockchain networks embed monetary policy, issuance incentives, and deflationary adjustments within their protocol designs.

---

## Dataset Overview

| Field | Description |
|--------|-------------|
| **Chain** | Name of the blockchain system. |
| **ID** | Identifier for linking with the cryptocurrency dataset. |
| **Slug** | Standardized URL-friendly identifier used for cross-dataset matching. |
| **Chain_year** | Year when the blockchain mainnet was launched. |
| **if_layer2** | Whether the chain functions as an Ethereum Layer-2 network. |
| **overview** | Concise textual summary of the blockchain’s positioning and design. |
| **technology** | Description of the blockchain’s technical architecture or consensus mechanism. |
| **tokenomics** | Tokenomics-related data collected via the CoinMarketCap crawler — one of the main textual sources for model extraction. |
| **team** | Core development team or founding organization. |
| **issuance_detail** | Token issuance descriptions automatically extracted from whitepapers and official communications using DeepSeek-V3. |
| **issuance_mechanism** | Classified type of issuance method (e.g., PoS, PoW, airdrop, vesting). |
| **vesting_type** | Type of vesting schedule, if applicable (cliff or linear). |
| **supply_slowdown_detail** | Textual information describing token-burning, halving, or other supply-control mechanisms. |
| **supply_slowdown_mechanism** | Classified type of deflationary mechanism (e.g., fee burn, reward reduction). |
| **has_staking_mechanism** | Indicates whether the blockchain employs staking or delegation as part of its token utility. |

---
