# Cryptocurrency Dataset Schema

This dataset provides a **comprehensive overview of cryptocurrency and token-level fundamentals** across more than **10,000 assets** collected via a custom-built web crawler that systematically retrieved and parsed data from [**CoinMarketCap**](https://coinmarketcap.com/).  
The data has been **systematically parsed, cleaned, and enriched** to integrate descriptive, economic, and tokenomic dimensions — including token allocation, unlock schedules, and historical market performance.

---

## Dataset Overview

| Field | Description |
|--------|-------------|
| **id** | A unique identifier assigned to each cryptocurrency or token. |
| **name** | Official name of the cryptocurrency or token. |
| **slug** | URL-friendly version of the name (standardized unique name after removing special characters). |
| **whitepaper** | Link to the project’s official whitepaper (PDF). |
| **about** | A detailed description of the cryptocurrency, including its purpose, technology, tokenomics, team, and real-world use cases. |
| **website** | Official website URL of the cryptocurrency or project. |
| **add_time** | Launch date or listing timestamp of the cryptocurrency or token. |
| **explorers** | Blockchain explorer links where users can verify transactions and token data (e.g., Etherscan for Ethereum). |
| **team** | Core development team or founding organization behind the project. |
| **tags** | Categorical labels describing the token’s domain or use case (e.g., DeFi, Layer 2, Gaming, Infrastructure). |
| **price** | Monthly historical price series of the cryptocurrency or token (in USD). |
| **market_cap** | Monthly historical market capitalization, calculated as `price × circulating_supply`. |
| **volume** | Monthly historical trading volume (in USD). |
| **total_supply** | Total number of tokens ever created, excluding burned tokens. |
| **max_supply** | Maximum number of tokens that can ever exist (if capped). |
| **circulating_supply** | Monthly historical circulating supply — the number of tokens currently in active circulation. |
| **allocation** | Initial allocation rules describing the token distribution among entities such as Early Investors, Public Investors, Team, Community, Foundation, and Partners. |
| **unlock_progress** | Unlock rules and schedules, including detailed parameters such as `subject` (allocation entity), `unlock_type` (cliff or linear), `vesting_duration`, and `cliff_duration`. |

---


