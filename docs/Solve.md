---
sidebar_position: 3
---

## 3.1 Problem: Low Initial Liquidity

**Traditional Issue**: New prediction markets often suffer from high slippage and poor price discovery due to insufficient liquidity at launch.

**Our Solution**: Virtual Liquidity AMM Model

```math
Virtual Liquidity = 100,000 (configurable)
Initial Price = (0 + 100,000) / (0 + 0 + 2 × 100,000) = 0.5
```

## 3.2 Maximizing Capital Efficiency: The "Idle Capital" Problem

Traditional prediction markets suffer from **opportunity cost**, where user funds sit unproductive for weeks or months.

| **Traditional Issue** | **AroundMarket Solution** |
| :--- | :--- |
| Liquidity remains static and unproductive until resolution. | Pools are integrated with **Aave V3** to generate real-time yield. |
| Capital is locked away from DeFi ecosystems. | Funds earn lending interest *while* backing prediction positions. |

:::tip Self-Yielding Advantage
By routing idle collateral into Aave, AroundMarket creates a "win-win": LPs earn trading fees **plus** lending yields, without sacrificing market liquidity.
:::

---

## 3.3 Establishing Trust: Solving Oracle Centralization

Relying on a single data source is a critical failure point in decentralized finance. We move from "Trust Me" to "Verify Me."

### The EchoOptimisticOracle Framework
Our solution replaces centralized decision-making with a robust, game-theory-backed process:

* **🕵️ Multi-Source Verification**: Multiple independent data providers submit results.
* **⚖️ The Challenge Period**: A mandatory 2-hour window allows anyone to dispute suspicious results.
* **🗳️ Decentralized Arbitration**: If a dispute arises, the final outcome is decided via decentralized community voting.
* **💰 Economic Incentives**: Data providers earn rewards for accuracy, while malicious actors face slashing/penalties.



---

## 3.4 Streamlining Adoption: Reducing Barriers to Creation

In many protocols, creating a market is a technical hurdle. AroundMarket simplifies this into a **4-step automated pipeline**.

### Quick-Start Market Creation
Our factory-based architecture ensures that anyone can launch a market in minutes:

1.  **Deploy Pool**: Use the `AroundPoolFactory` to create a dedicated liquidity pool for your chosen token.
2.  **Oracle Injection**: Link your specific event question to the `EchoOptimisticOracle`.
3.  **Guarantee Deposit**: Pay a calculated guarantee amount based on your desired initial virtual liquidity.
4.  **Live Trading**: Your market goes live immediately with an initial price of **0.5**, powered by our AMM.

:::info Automated Pricing
Thanks to our **Virtual Liquidity** model, your market doesn't need to wait for the first trade to have a price—it's ready for action the moment it's born.
:::

## 3.5 Problem: Inefficient Fee Structures 💰
Traditional Issue: Inefficient cost allocation.

Our Solution: AroundMarket implements a transparent and sustainable fee model to incentivize all ecosystem participants.

| Fee Type | Percentage | Destination & Purpose |
| :--- | :--- | :--- |
| **Official Fee** | `0.20%` | Platform maintenance and security |
| **Liquidity Fee** | `0.15%` | Reward for Liquidity Providers (LPs) |
| **Oracle Fee** | `0.10%` | Reward for data providers and verifiers |
| **Lucky Fee** | `0.075%` | Distributed via the LuckyPool lottery |
| **Creator Fee** | `0.075%` | Incentive for market originators |

---

### 📊 Fee Summary

> ### **Total Standard Fee: 0.6%**
> 
> 💡 **Holder Benefit:** Users holding an **ELF NFT** enjoy a **50% discount** on all trading fees, reducing the total to only **0.3%**.