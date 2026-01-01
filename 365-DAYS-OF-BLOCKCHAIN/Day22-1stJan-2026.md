# MEV — Maximal Extractable Value (From First Principles)

### _The Hidden Layer That Changes Everything_

---

## Gist

Every blockchain has an order.  
Whoever controls that order can extract value.

MEV is not a bug.  
It is a **natural consequence of transparency + incentives**.

---

## Start From Zero: The Ordering Problem

Blockchains process transactions in **some order**.

That order matters.

If two transactions interact with the same state:

- swapping tokens,
- liquidating positions,
- updating prices,

then **who goes first** can change outcomes.

This creates value.

---

## Who Decides the Order?

At a basic level:

- users submit transactions,
- transactions sit in a public pool (mempool),
- someone chooses which transactions go first.

That “someone” is:

- miners (in Proof-of-Work),
- validators (in Proof-of-Stake),
- or sequencers (in Layer-2s).

Ordering power = leverage.

---

## The First Principle Behind MEV

> **If transactions are public before execution,  
> they can be observed, copied, reordered, or blocked.**

This is unavoidable in transparent systems.

MEV emerges the moment:

- state is shared,
- execution is sequential,
- and profit opportunities exist.

---

## A Simple Mental Example

Imagine a DEX pool:

- ETH / USDC

You submit a large trade:

- buying ETH,
- which will push the price up.

Anyone watching can:

- see your transaction,
- place their own transaction before yours,
- benefit from the price movement you cause.

Nothing illegal happened.
Nothing broke.

Value was extracted from **ordering**.

That is MEV.

---

## The Three Core MEV Actions

Almost all MEV falls into three patterns:

### 1️⃣ Front-Running

Someone places a transaction **before** yours
to profit from the change you cause.

### 2️⃣ Back-Running

Someone places a transaction **after** yours
to profit from the new state you create.

### 3️⃣ Sandwiching

Someone places:

- one transaction before yours,
- one transaction after yours,

extracting value from both sides.

This is the most common MEV strategy.

---

## Why MEV Is Inevitable

MEV exists because:

- blockchains are transparent,
- transactions are ordered,
- incentives are financial.

To remove MEV, you would need:

- private transactions,
- random ordering,
- or no financial incentives.

Each of these breaks something else.

> **MEV is not removable.  
> It is only manageable.**

---

## MEV Is Not Always Bad

Important distinction:

- **Harmful MEV**

  - sandwich attacks
  - user exploitation
  - unfair slippage

- **Beneficial MEV**
  - arbitrage
  - liquidations
  - keeping prices aligned
  - protocol safety

Many DeFi systems rely on MEV to function correctly.

The problem is **who captures it**.

---

## Who Captures MEV?

Initially:

- miners / validators captured MEV directly.

Over time:

- searchers compete for MEV,
- builders construct optimized blocks,
- validators choose the most profitable blocks.

This created a new invisible market.

MEV became **professionalized**.

---

## Why Gas Fees Are Not the Full Cost

Users think:

> “I paid gas, that’s my cost.”

Reality:

- you may also lose value to MEV,
- through worse execution,
- hidden slippage,
- or sandwiching.

MEV is an **invisible tax**.

---

## MEV and Layer-2s

Layer-2s don’t remove MEV.
They **change who controls it**.

- Sequencers replace validators
- Ordering becomes centralized (temporarily)
- MEV still exists, just reshaped

Design choices matter here.

---

## The Big Insight

> **MEV is not about stealing.  
> It is about ordering power.**

If you can choose the order,
you can choose the outcome.

---

## Why MEV Changes How You Think

Once you understand MEV:

- you see why private RPCs exist,
- why batch auctions are proposed,
- why fair ordering is hard,
- why “cheap gas” doesn’t mean “cheap trades”.

You stop thinking in transactions.
You start thinking in **game theory**.

---

## Final Note

MEV is the shadow of transparency.

It cannot be eliminated —
only redirected, constrained, or shared.

If you understand MEV,
you understand how blockchains behave under pressure.

# Summary in short

# Understanding MEV — Simple & First Principles

Let’s strip this down to **first principles**, no jargon, no crypto hype.

---

## The Basic Idea

When you trade on a blockchain, **your transaction is public before it is finalized**.

That single fact explains everything.

Because others can _see_ your trade coming, they can **rearrange transactions** or **trade around you** to extract value from _your_ action.  
That extracted value is called **MEV (Maximal Extractable Value)**.

You don’t pay MEV directly — **you lose value indirectly**.

---

## Think of It Like a Real-World Market

Imagine you walk into a fruit market and loudly announce:

> “I’m about to buy 1,000 apples at whatever the price is.”

Before you finish:

- Sellers raise prices
- Middlemen buy apples first and resell to you
- You end up paying more, without realizing why

That’s MEV.

---

## Breaking Down Each Point

### 1️⃣ You May Lose Value to MEV

**Meaning:**  
Someone else can profit _because you made a transaction_.

Your trade creates an opportunity → others exploit it → you get a worse deal.

No magic. Just incentives.

---

### 2️⃣ Through Worse Execution

**Execution = the price you actually get**

You expect:

> “I’ll buy at price X”

You get:

> “You bought at price X + extra”

Why?

- Someone traded **before you**
- Or rearranged the order of transactions
- Or pushed the price against you

You didn’t choose a worse price — **the system allowed it to happen**.

---

### 3️⃣ Hidden Slippage

**Slippage = price changes while your trade is happening**

Hidden slippage means:

- The UI says: _“Price impact: small”_
- Reality: the final price is worse

Why?

- Other transactions jump ahead of yours
- Liquidity shifts before your trade executes
- You can’t see this happening in real time

You only notice **after** the trade settles.

---

### 4️⃣ Sandwiching

This is literal.

Someone:

1. **Buys before you** (pushes price up)
2. **Lets your trade execute** (you pay a higher price)
3. **Sells after you** (price drops back)

You’re the filling in the sandwich 🥪

They profit.  
You overpay.  
The protocol works “as designed”.

---

## First-Principle Summary

At the deepest level:

- Blockchains are **transparent**
- Transactions are **ordered by incentives**
- Whoever controls or influences ordering can extract value
- That value often comes from **regular users**

So:

> MEV is not a bug  
> It’s a consequence of public, incentive-driven systems

---

## One-Sentence Mental Model

**“If others can see your move before it happens, they can trade against you.”**

**Now the ocean is yours.  
Dive in.**
