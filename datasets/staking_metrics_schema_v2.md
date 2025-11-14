# Blockchain Staking Metrics Dataset Schema (2015–2025)

This dataset compiles the **historical staking metrics** of major Proof-of-Stake (PoS) blockchains from **2015 to 2025**, covering nearly **80 networks**.  
The data is primarily sourced from [**Staking Rewards**](https://www.stakingrewards.com/), obtained via its public API and standardized into a **monthly time-series panel**.

The dataset captures the **economic parameters and incentive structures** of PoS ecosystems, allowing analysis of validator behavior, inflation dynamics, and long-term return profiles across different blockchain networks.

The dataset captures the **economic parameters and incentive structures** of Proof-of-Stake (PoS) ecosystems, enabling analysis of validator returns, inflation dynamics, and staking participation across blockchain networks. It provides macro-level indicators of how network rewards, staking ratios, and inflation rates shape validator incentives and long-term yield sustainability.  In contrast, the [**Block-Level Economic Activity Dataset**](block_level_economic_activity_dataset.md) records **micro-level block production data**, detailing each block’s validator, rewards, gas usage, and transaction composition.

---

## Dataset Overview

| Field | Description |
|--------|-------------|
| **annualized_rewards_usd** | Average staking rewards in USD, computed as native reward rate × staked tokens × token price. |
| **block_reward** | Average number of tokens distributed per block to stakers (30-day rolling average if not directly available). |
| **circulating_percentage** | Circulating supply divided by total supply — indicates liquidity of staked assets. |
| **circulating_supply** | Portion of the total supply that is freely transferable on the market. |
| **inflation_rate** | Annualized monetary expansion rate of the token supply, based on reward emissions and total supply change. Higher values imply stronger dilution; lower values indicate scarcity. |
| **real_reward_rate** | Nominal reward rate adjusted for inflation — reflects actual, inflation-adjusted returns for validators and delegators. |
| **reward_rate** | Current annualized average staking reward rate across the network. |
| **staking_ratio** | Share of eligible tokens currently staked or delegated — measures network participation and security. |
| **total_staking_wallets** | Total number of unique wallet addresses actively staking or delegating — proxies decentralization and community engagement. |
| **total_validators** | Total number of validators participating in network consensus. |

---

