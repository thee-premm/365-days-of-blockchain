# MEV & Validators: Where Ordering Power Actually Lives

## Gist

Validators don’t steal value.  
They **choose order**.

And choosing order is enough to change outcomes.

That’s where MEV enters.

---

## Start From First Principles

A blockchain block is not magic.  
It is just:

- a list of transactions
- arranged in a specific order
- executed one by one

Someone must decide that order.

That someone is the **validator**.

---

## What Validators Actually Do

In Proof-of-Stake systems (like Ethereum):

Validators:

- collect transactions
- choose which ones go into the block
- decide the execution order
- propose the block to the network

This power is necessary.
But it has consequences.

---

## Why Ordering Creates Value

Because transactions are **state-dependent**.

Example:

- a swap changes price
- a liquidation changes balances
- an arbitrage fixes mispricing

If you go **before** a transaction:

- you see old state

If you go **after**:

- you see new state

That difference can be worth money.

---

## Where MEV Enters for Validators

Validators can extract MEV by:

- reordering transactions
- inserting their own transactions
- excluding some transactions
- choosing blocks that pay them more

They don’t break rules.
They use the rules.

> **MEV is value extracted from _how_ blocks are built,  
> not from breaking consensus.**

---

## Why Validators Rarely Do It Directly

In practice:

- writing MEV strategies is complex
- running bots is expensive
- competition is fierce

So a market formed.

Validators outsource MEV extraction.

---

## The Real MEV Pipeline (Simplified)

Users → Mempool → Searchers → Builders → Validators → Block

- **Searchers** find MEV opportunities
- **Builders** assemble optimized blocks
- **Validators** choose the most profitable block

Validators don’t hunt MEV.
They **auction block space**.

---

## Why Validators Accept MEV Blocks

Validators are rational.

They:

- want maximum rewards
- are paid to propose blocks
- choose blocks that pay more

If a block contains:

- better ordering
- more value
- extra payments (tips / side payments)

Validators will prefer it.

This is not corruption.
It’s incentive alignment.

---

## Why This Matters to Users

Users think:

> “I paid gas, so I’m done.”

But:

- gas pays for inclusion
- MEV affects execution quality

Validators don’t care _who_ you are.
They care **what the block is worth**.

---

## The Key Insight

> **Validators don’t extract MEV because they’re greedy.  
> They extract MEV because the protocol rewards them for it.**

This is system design, not bad actors.

---

## Why This Cannot Be Removed

To remove validator MEV, you would need:

- no ordering choice, or
- private transactions, or
- random execution

Each breaks:

- liveness
- transparency
- decentralization

So MEV is constrained, not eliminated.

---

## Final Note

Once you understand validators,
MEV stops feeling mysterious.

It becomes obvious.

Ordering power → value → incentives → behavior.

That’s blockchain reality.

**Now the ocean is yours.  
Dive in.**
