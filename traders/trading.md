# Trading Mechanics

Loadout uses two trading mechanisms depending on where a project is in its lifecycle.

## Pre-Graduation: Bonding Curve

Before a project graduates (hits 150 SOL treasury), trading happens on a bonding curve.

### How It Works

- **Price follows a curve** — More buying = higher price, more selling = lower price
- **Liquidity is always available** — You can always buy or sell (no waiting for matching orders)
- **No LP required** — The curve itself provides liquidity
- **Instant settlement** — Trades execute immediately on-chain

### The Math (Simplified)

The bonding curve is a mathematical function that determines price based on supply. As more tokens are purchased, price increases along the curve. As tokens are sold back, price decreases.

You don't need to understand the math. Just know: buy pressure = price up, sell pressure = price down, and there's always liquidity on both sides.

## Post-Graduation: Meteora DLMM

Once a project graduates, trading moves to a Meteora DLMM (Dynamic Liquidity Market Maker) pool.

### What Changes

- **Deeper liquidity** — More efficient trading with less slippage
- **Fee enforcement built-in** — 5% fee handled by the pool
- **Standard AMM behavior** — Works like any other Solana DEX pool
- **LP position locked** — Liquidity is permanent, fees go to project

### What Stays the Same

- **5% trading fee** — Same split (4.75% treasury, 0.25% protocol)
- **Your tokens** — Nothing changes about what you hold
- **Ability to trade** — Buy and sell anytime

## Fee Breakdown

Every trade, whether on bonding curve or DLMM:

| Component | Percentage |
|-----------|------------|
| Project Treasury | 4.75% |
| Loadout Protocol | 0.25% |
| **Total** | **5%** |

This fee applies to both buys and sells.

### Example

You want to buy 100 SOL worth of a project token:
- **5 SOL** goes to fees (4.75 SOL to project, 0.25 SOL to protocol)
- **95 SOL** worth of tokens you receive

You want to sell tokens worth 100 SOL:
- **5 SOL** taken as fees
- **95 SOL** you receive

## Price Discovery

Price on Loadout is set by the market, not by anyone else.

- **No presale prices** — First trade sets the initial price
- **No VC discounts** — Everyone pays the same curve price
- **Real-time repricing** — Market reacts to news, updates, sentiment

When a team ships an update, the market can reprice immediately. When a project goes quiet, price reflects that too. This is the point — let the market express conviction continuously.

## Slippage

On bonding curves, slippage increases with trade size. Large buys will move the price more than small buys.

On Meteora DLMM, slippage depends on liquidity depth. Post-graduation pools generally have better liquidity than pre-graduation curves.

If you're making a large trade, consider breaking it into smaller chunks to reduce price impact.

## Solana Considerations

- **Fast finality** — Trades confirm in seconds
- **Low fees** — Network fees are minimal (fractions of a cent)
- **Wallet support** — Phantom, Solflare, Backpack, etc.

---

Next: [Rewards & Rebates →](rewards.md)
