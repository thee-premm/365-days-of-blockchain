# PBS & Flashbots — Separating Power to Contain MEV

### _How Ethereum Reduced Damage Without Breaking Itself_

---

## Gist

MEV exists because transaction order creates value.  
Validators had too much power over that order.

PBS didn’t remove MEV.  
It **separated power** so no single actor could abuse it.

Flashbots made this separation real.

---

## Start From the Core Problem (No Shortcuts)

A block is just:

- a list of transactions
- executed in a chosen order

That order matters.

So someone must:

- choose transactions
- choose the order
- propose the block

Originally, **validators did all three**.

That concentration of power caused problems.

---

## Why Validator Power Became Dangerous

When validators controlled everything, they could:

- reorder transactions for profit
- insert their own transactions
- censor others
- extract MEV silently

Nothing illegal.  
Nothing against protocol rules.

But:

- users got worse execution
- trust weakened
- centralization pressure increased

Ethereum faced a choice:

> **Remove MEV (impossible)**  
> or  
> **Reduce who controls it (possible)**

---

## The First-Principle Insight

> **The problem was not MEV.  
> The problem was concentrated ordering power.**

So the solution was obvious:

> **Split the job.**

---

## What PBS Actually Means

PBS = **Proposer–Builder Separation**

It separates roles:

- **Builders** → decide transaction order
- **Validators (Proposers)** → choose which block to publish

One builds.  
One proposes.

No single party controls both.

---

## Why This Separation Works

Builders:

- compete to build the most valuable block
- search for MEV
- optimize ordering

Validators:

- don’t reorder transactions
- don’t run MEV strategies
- simply pick the best-paying block

This turns MEV into a **competitive market**, not a hidden abuse.

---

## The New Flow (Very Important)

Users
↓
Mempool
↓
Searchers (find MEV)
↓
Builders (assemble blocks) (you must smell HFTs here)
↓
Validators (choose best block)
↓
Ethereum

---

## let us talk about this more

# The Original Problem Before PBS

In early Ethereum, **one actor did everything**:

- Collected transactions
- Decided the order
- Published the block

This actor was the **validator** (or **miner**, earlier).

---

## Why This Is a Problem

Because **ordering transactions equals power**.

If you control transaction ordering, you can:

- Put your own transaction first
- Sandwich other users (MEV extraction)
- Exclude transactions
- Extract unfair profit

### The Core Issue

Giving one party both **ordering power** and **publishing power** is dangerous.

---

## First-Principle Insight: The Newspaper Example

- **Reporter** → writes the article
- **Editor** → decides whether to publish it

If the same person performs both roles:

- They can publish biased or self-serving content
- No checks or accountability exist

Separation of roles creates accountability.

---

## How PBS Applies This Logic to Blockchains

PBS follows the same principle:

Never let the same party both decide transaction order and publish the block.

As a result, the job is split.

---

## The Two Roles

### Builders Decide How the Block Looks

Builders:

- Gather transactions
- Try different orderings
- Construct the most valuable block
- Package the block and say:  
  “Here is a finished block. You’ll earn X if you publish this.”

Important:

- Builders do **not** publish blocks

---

### Proposers / Validators Decide Whether to Publish

Proposers:

- Receive blocks from multiple builders
- Compare rewards and validity
- Choose the best block
- Publish it to the network

Important:

- Proposers do **not** decide ordering

---

## Why This Works: The Logical Chain

1. Ordering creates profit
2. Profit attracts competition
3. Builders compete to:
   - Create better transaction orderings
   - Offer higher rewards to proposers
4. Proposers simply choose the best valid offer

As a result:

- Power is split
- Abuse becomes harder
- MEV becomes competitive instead of monopolized

---

## The Key Mental Model

Builders compete. Proposers choose.  
No one gets to cheat alone.

---

## What PBS Does Not Do

PBS does **not**:

- Remove MEV
- Make transaction ordering fair
- Eliminate incentives

PBS **does**:

- Make MEV extraction transparent
- Make it competitive
- Prevent validators from accumulating excessive power

---

## One-Sentence Definition

Proposer-Builder Separation (PBS) is the separation of who decides transaction order from who finalizes the block to prevent concentrated power.

---

# What Do Builders Get?

Good question. Let’s answer it cleanly, from first principles, without hand-waving.

---

## The Core Question

Why would anyone want to be a **builder** at all?

Because builders get one thing only:

**The right to compete to extract value from transaction ordering.**

Nothing more.

---

## What Builders Actually Get (Precisely)

### 1. The Right to Order Transactions

Builders:

- See the public transaction pool
- Choose which transactions go into a block
- Choose the order of those transactions

This is the **only technical power** they have.

Builders do **not**:

- Publish blocks
- Finalize blocks
- Decide consensus

---

### 2. The Right to Compete for MEV

Transaction ordering creates opportunities such as:

- Arbitrage
- Liquidations
- Backrunning

Builders:

- Detect these opportunities
- Construct blocks that capture them
- Turn them into value

But this is crucial:

> Builders must share most of this value with proposers to win.

---

### 3. The Right to Make an Offer (Not a Guarantee)

A builder sends a proposer an offer that effectively says:

> “If you publish my block, you will earn **X ETH**.”

That is all.

The proposer can:

- Accept it (choose the block)
- Reject it (choose another builder)

Builders have **no guarantee** their block will be chosen.

---

## What Builders Do _Not_ Get

Builders do **not** get:

- Control over block inclusion
- Control over finality
- Control over the chain
- Guaranteed profits
- Any protocol authority

They are **pure market participants**.

---

## Why This Is Enough Incentive

From first principles:

- MEV exists naturally
- Someone will extract it
- PBS decides _who competes_ for it

Builders form the **competitive layer**.

Instead of validators extracting MEV quietly:

- Builders extract it openly
- Competition pushes profits down
- Proposers (and indirectly users) benefit

---

## A Simple Analogy

Builders are like **market makers**:

- They do not own the exchange
- They do not control settlement
- They profit by being faster and smarter
- If they fail, someone else replaces them

---

## One-Sentence Answer

Builders get the right to compete for MEV by constructing transaction orderings, and nothing else.

# Builders Are the Real Gamers for Crypto HFTs

Yes. That intuition is exactly right.

Builders are the natural home for **high-frequency trading (HFT) firms** in crypto.

Let’s explain this cleanly, from first principles.

---

## The Core Insight

HFT firms care about **one thing**:

Speed + ordering = profit.

PBS creates a role whose entire job is:

- See transactions first
- Reorder them optimally
- Extract tiny but repeatable edges

That role is the **builder**.

---

## Why Builders Map Perfectly to HFT Firms

### 1. Builders Compete on Speed and Precision

HFT firms already specialize in:

- Ultra-low latency systems
- Fast mempool ingestion
- Sophisticated optimization algorithms

Builders do the same:

- Observe transactions in real time
- Simulate multiple orderings
- Submit the highest-value block before rivals

This is classic HFT behavior.

---

### 2. MEV Is On-Chain Microstructure

In traditional markets, HFTs exploit:

- Order book dynamics
- Arbitrage gaps
- Liquidations and forced flows

On-chain, MEV is the same idea expressed differently:

- DEX arbitrage
- Liquidations
- Backruns and priority ordering

Builders operate directly on this microstructure.

---

### 3. Builders Monetize by Sharing Profits

HFT firms do not need monopoly power.

They need:

- A competitive arena
- Clear rules
- Predictable settlement

Builders earn by:

- Capturing MEV
- Sharing most of it with proposers
- Keeping a thin margin

This mirrors how HFTs operate in traditional exchanges.

---

## Why PBS Attracts Large, Sophisticated Players

PBS favors actors who can:

- Invest heavily in infrastructure
- Optimize across many strategies
- Operate on razor-thin margins

That profile matches:

- Large trading firms
- Professional MEV shops
- Crypto-native HFT desks

Small, unsophisticated actors get competed away.

---

## What This Means for the Ecosystem

Instead of:

- Validators secretly extracting MEV
- Opaque, unaccountable behavior

We get:

- Professional competition
- Transparent bidding for blocks
- Clear separation of power

Builders become the battlefield.

---

## The Key Mental Model

Validators secure the chain.  
Builders play the trading game.

Each does one job.

---

## One-Sentence Summary

Builders are the on-chain equivalent of high-frequency traders: they compete on speed and strategy to extract MEV, while sharing most of the value with proposers.

---

### The thing the Builders are the one who get hire in crs in India and plays a viatal role, thier job is to compete with time and other builders to get that edge for the arbitrage and max profit for the HFT, example writting an algo for which both the Firm and the validator gets the profit and they choose that, this was one of the thing we have many more

## we will look into Flashbots tmrw, stay hard !