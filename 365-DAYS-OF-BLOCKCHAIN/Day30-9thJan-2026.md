# DAY 30 — When Data Becomes the Bottleneck

### _Why Ethereum Needed a New Data Lane_

---

## Gist

Ethereum solved execution pressure.  
But in doing so, it exposed a deeper problem:

> **Data, not computation, became the real bottleneck.**

DAY 30 is about understanding **why calldata stopped scaling**  
and why Ethereum had to rethink _how data lives on-chain_.

---

## Recap the Situation (Very Important)

By now, Ethereum has done something radical:

- Execution → moved off-chain (rollups)
- Verification → stays trustless
- Data → still posted on Layer-1

This worked.

But success created pressure.

---

## The New Reality Ethereum Faced

Rollups started growing.

More users → more rollup transactions  
More transactions → more data  
More data → more calldata on L1

Ethereum L1 was no longer CPU-bound.

It became **data-bound**.

---

## Why Calldata Became a Problem

Calldata has three properties:

1. It is **fully stored**
2. It is **forever accessible**
3. It is **paid for with normal gas**

This was fine when:

- Ethereum executed everything itself

But rollups changed the game.

Now:

- L1 doesn’t need calldata forever
- It only needs it **long enough to verify**

Yet calldata forced Ethereum to:

- store rollup data permanently
- price it like execution data

That was inefficient.

---

## First-Principle Question (Key Moment)

Ethereum asked:

> **Do we really need rollup data forever?  
> Or do we only need it temporarily?**

The answer was clear:

- For verification → yes
- For long-term storage → no

This insight changes everything.

---

## The Core Insight of DAY 30

> **Data availability ≠ permanent storage**

Ethereum doesn’t need to remember rollup data forever.
It only needs to:

- make it available
- long enough for anyone to verify or challenge

After that, it can disappear.

---

## Why This Matters for Decentralization

Permanent data:

- grows chain size endlessly
- pushes out smaller nodes
- increases hardware requirements

Temporary data:

- preserves verifiability
- limits long-term state growth
- keeps nodes lightweight

Ethereum always chooses:

> **Verification over convenience**

---

## The Design Direction Becomes Obvious

Once Ethereum accepts that:

- rollup data is temporary
- DA is the bottleneck
- calldata is the wrong tool

A new requirement appears:

> **We need a cheaper, temporary, high-throughput data lane.**

Not for execution.  
Not for contracts.  
Only for availability.

This requirement leads directly to the next concept.

---

## What DAY 30 Does _Not_ Do

Today we do NOT:

- introduce blobs by name
- talk about EIPs
- discuss implementation details

We only establish **necessity**.

Architecture follows necessity.

---

## The Analogy (Seal It)

### Ethereum Is a Court Archive

- Important laws → stored forever
- Case evidence → kept only until appeals close

Rollup data is **evidence**, not law.

Keeping evidence forever:

- clogs archives
- slows the system
- adds no new trust

Temporary availability is enough.

---

## Final Note

DAY 30 is the turning point.

You now understand:

- why calldata hit a wall
- why DA became the scaling limit
- why Ethereum needed a new data lane

Tomorrow, we finally name it.

> **DAY 31 — Blobs: Temporary Data with Permanent Trust**

**Now the ocean is yours.  
Dive in.**
