# Block-Level Economic Activity Dataset

This dataset provides a comprehensive record of block-level production and economic activity from three major blockchain networks — **Ethereum**, **BNB Smart Chain**, and **Solana**.  
It systematically documents validator identities, reward structures, and key indicators of network operation, enabling analysis of network activity, validator incentives, and validator concentration.

The dataset covers approximately **2.0 million blocks from Ethereum**, **2.2 million blocks from BNB Smart Chain**, and **1.0 million randomly sampled slots from Solana** (about 1% of all blocks between slot heights 200,000,000 and 300,000,000).  Each record corresponds to a single block (or slot, for Solana) and includes structural, transactional, and economic variables derived directly from on-chain data.

All data were collected using **custom-built Python crawlers** that directly interact with official blockchain RPC endpoints — **Alchemy** (Ethereum), the **official BNB Smart Chain RPC**, and **Helius** (Solana).  

The crawlers retrieve raw block metadata and transaction-level gas or reward information in parallel, ensuring reproducibility and consistency across networks. It enables in-depth empirical research on **validator reward structures**, **block production efficiency**, **transaction fee mechanisms**, and **network decentralization patterns** under different consensus protocols (*PoW*, *PoSA*, *PoH*).

---

## Ethereum Dataset Structure

| Field | Description |
|--------|-------------|
| **block_number** | Sequential block height on the Ethereum mainnet. |
| **miner_address** | Address of the validator or miner responsible for producing the block. |
| **timestamp_bj** | Block timestamp converted to Beijing Time (UTC+8). |
| **extra_data** | Raw metadata embedded by miners or validators (may contain client or pool identifiers). |
| **entity_name** | Normalized name of the mining pool or validator entity. |
| **base_fee_per_gas** | Base gas fee (in Gwei) defined by EIP-1559 — the minimum fee per gas unit. |
| **burnt_fees** | Total ETH permanently burned in the block (`base_fee_per_gas × gas_used`). |
| **priority_fee** | Aggregate priority (tip) fees paid to validators by users. |
| **gas_used** | Total gas consumed by all transactions within the block. |


---

## BNB Smart Chain Dataset Structure

| Field | Description |
|--------|-------------|
| **block_number** | Sequential block height on the BNB Smart Chain. |
| **timestamp_bj** | Block timestamp converted to Beijing Time (UTC+8). |
| **miner_address** | Validator address responsible for producing the block. |
| **size_bytes** | Raw size of the block (in bytes). |
| **tx_count** | Total number of transactions included in the block. |
| **gas_used** | Total gas consumed by all transactions. |
| **gas_limit** | Maximum gas limit for the block. |
| **error** | Indicator flag showing whether a block contained execution errors. |
| **block_reward** | Total reward distributed to the validator (in BNB). |


---

## Solana Dataset Structure

| Field | Description |
|--------|-------------|
| **slot** | Slot number (analogous to block height in Solana). |
| **timestamp_beijing** | Slot timestamp converted to Beijing Time (UTC+8). |
| **leader** | Slot leader (validator) responsible for block production. |
| **staking_reward_SOL** | Total staking rewards distributed (in SOL). |
| **voting_reward_SOL** | Voting rewards earned by validators (in SOL). |
| **fee_reward_SOL** | Rewards from transaction fees (in SOL). |
| **rent_reward_SOL** | Rent rewards (in SOL). |
| **fee_total_SOL** | Total transaction fees collected within the slot. |
| **transactions_count** | Number of transactions executed in the slot. |
| **reward_count** | Number of reward events recorded. |
| **reward_type_summary** | Aggregated summary of reward types (e.g., “Staking:500; Voting:480”). |

---
