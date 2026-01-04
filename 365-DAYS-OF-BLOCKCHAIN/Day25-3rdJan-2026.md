# Flashbots — Making MEV Visible, Ordered, and Less Harmful

### _The Missing Layer That Made PBS Work in Practice_

---

## Gist

PBS is the idea.  
Flashbots is the machinery.

PBS says: _separate power_.  
Flashbots shows **how that separation actually happens** in the real network.

---

## Start From the PBS Problem

PBS sounds clean on paper:

- builders build blocks
- validators choose blocks
- power is separated

But here’s the real question:

> **How do builders and validators coordinate  
> without trusting each other?**

They still need:

- communication,
- competition,
- payment settlement.

This coordination layer did not exist.

That gap is where Flashbots enters.

---

## What Flashbots Actually Is

:contentReference[oaicite:0]{index=0} is **not a protocol** and **not a validator**.

Flashbots is:

- an **MEV coordination infrastructure**
- a neutral marketplace
- connecting searchers, builders, and validators

It doesn’t remove MEV.  
It **organizes it**.

---

## The First-Principle Insight

Before Flashbots:

- MEV extraction happened chaotically
- via gas wars
- via public mempool abuse
- via network congestion

The core issue:

> **MEV competition happened _inside_ Ethereum blocks.**

Flashbots moved that competition **outside the block**.

---

## The Flashbots Pipeline (Clean Logic)

Users
↓
Searchers (detect MEV)
↓
Flashbots Relay
↓
Builders (construct blocks)
↓
Validators (choose best-paying block)
↓
Ethereum

Key idea:

> **MEV is auctioned, not fought.**

---

## Who are these searchers

The searchers are the ones who keep on looking into the opportunities and the possible and worth MEV and after that they bundle all those info and gives to the builder, and we have already seen who a Builder is in the previous blog.

## What the Flashbots Relay Does

The relay:

- receives bundles of transactions
- keeps them private
- forwards them to builders
- prevents mempool leakage

This means:

- no front-running in public mempool
- no gas wars
- no blind competition

Execution becomes predictable.

---

## Why Builders Matter Here

Builders:

- receive many MEV bundles
- choose the optimal ordering
- create the most profitable valid block

They specialize in:

- block construction
- MEV optimization
- constraint satisfaction

Validators don’t do this work anymore.

---

## What Validators Do Now (Very Important)

Validators:

- receive block bids from builders
- compare payouts
- choose the highest-paying valid block

They **do not know**:

- how MEV was extracted
- which users were involved
- which transactions were reordered

They only see:

> “This block pays more.”

This keeps validators **neutral**.

---

## Why This Reduces Harmful MEV

Flashbots:

- reduces sandwich attacks in public mempool
- reduces gas spikes
- reduces network instability
- makes MEV extraction transparent at a system level

MEV still exists.
But it is **less toxic**.

---

## What Flashbots Does _Not_ Do

Important clarity:

Flashbots does NOT:

- eliminate MEV
- guarantee fairness
- protect careless users
- decentralize everything instantly

It is **damage control**, not perfection.

---

## How Flashbots Completes PBS

PBS without Flashbots:

- theory
- no coordination
- no incentive alignment

Flashbots without PBS:

- centralized influence
- validator dominance

Together:

- builders specialize
- validators stay neutral
- MEV becomes structured

---

## The Key Insight (Lock This)

> **PBS split power.  
> Flashbots built the marketplace that lets the split work.**

Without Flashbots,
PBS would remain academic.

---

## Final Note

You now understand:

- why Flashbots exists,
- how it connects to PBS,
- and why Ethereum chose this path.

MEV didn’t disappear.
It **grew up**.

Full PBS Flow (Step-by-Step)

->User submits a transaction

->Searcher detects MEV opportunity

->Searcher creates a bundle

->Bundle sent privately to a builder

->Builder assembles best block

->Builder bids ETH to validator

->Validator chooses highest bid

->Block is proposed on Ethereum

## Summary about the FlashBots

### 1. A Protocol Designer

- Designed **Proposer-Builder Separation (PBS)**
- Designed **MEV auction mechanisms**
- Designed the **bundle abstraction** for private transaction ordering

### 2. A Software Provider

- **MEV-Boost** → software used by validators to outsource block building
- **Flashbots Relay** → infrastructure connecting builders and validators
- **Private RPCs** → protect users and searchers from front-running and mempool exposure

### 3. A Neutral Coordinator (Not a Middleman)

- Cannot steal funds
- Cannot reorder blocks
- Cannot force transaction inclusion
- Enforces rules and transparency rather than control

**Now the ocean is yours.  
Dive in.**
