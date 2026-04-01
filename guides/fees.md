# Fee Structure

Loadout uses a 5% trading fee — higher than typical DEXs, but that's the point. This isn't a trading platform with funding attached. It's a **funding platform with trading attached**.

<figure><img src="../diagrams/fee-structure.svg" alt="Fee Structure"><figcaption>How fees are distributed</figcaption></figure>

## The 5% Fee

Every swap on Loadout incurs a 5% fee. This fee is split:

| Recipient | Share | Purpose |
|-----------|-------|---------|
| **Project Treasury** | 4.75% | Funds game development |
| **Loadout Protocol** | 0.25% | Platform operations |

### Example Trade

If you buy 100 SOL worth of a game token:
- **4.75 SOL** → Goes directly to the game's development treasury
- **0.25 SOL** → Goes to Loadout protocol
- **95 SOL** → Executes your swap

## Why 5%?

Traditional exchanges charge 0.1-0.3%. DEXs charge 0.3-1%. Why does Loadout charge 5%?

**Because the fee IS the product.**

On Loadout, you're not just trading — you're funding. Every trade contributes meaningfully to the game's development budget. A few thousand trades can fund months of development.

### The Math

| Daily Volume | Treasury Fees (4.75%) | Monthly Treasury |
|--------------|----------------------|------------------|
| $10,000 | $475/day | $14,250 |
| $50,000 | $2,375/day | $71,250 |
| $100,000 | $4,750/day | $142,500 |

For a hyped game doing decent volume, the treasury can accumulate serious funding purely from trading activity.

## Fee Comparison

| Platform | Fee | Where It Goes |
|----------|-----|---------------|
| Pump.fun | 1% | Platform only |
| Uniswap | 0.3% | LPs |
| Binance | 0.1% | Platform |
| **Loadout** | **5%** | **95% to game dev** |

## How Fees Are Enforced

Loadout uses **Meteora DLMM pools** to enforce the 5% fee. When a project launches:

1. Token trades on bonding curve (pre-graduation)
2. At graduation, liquidity moves to a Meteora DLMM pool
3. The pool is configured with 5% base fee
4. Fees automatically split between treasury and protocol

This approach ensures consistent fee collection without requiring Token-2022 transfer hooks, keeping tokens compatible with the broader Solana ecosystem.

---

Next: [Graduation →](graduation.md)
