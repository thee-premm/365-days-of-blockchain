# DAY 28 — Data Availability: The First Non-Negotiable Layer

### _Why Rollups Cannot Exist Without This_

---

## Gist

Before scaling execution,  
before rollups,  
before shards,

there is one question Ethereum must answer:

> **How can anyone verify what they cannot see?**

That question creates **Data Availability**.

---

## Start From Absolute Zero

A blockchain is not:

- smart contracts
- tokens
- applications

At its core, a blockchain is:

> **a public state machine**

State changes only when:

- transactions are executed
- in a specific order
- using specific data

If that data is hidden,
the system stops being trustless.

---

## The First Principle

> **Verification requires data.  
> No data → no verification.**

This is not a blockchain rule.  
This is logic.

You cannot verify:

- balances
- proofs
- fraud
- correctness

without the underlying data.

---

## What “Data” Actually Means

Data is:

- transactions
- inputs
- calldata
- anything required to recompute state

Not:

- final balances
- state roots
- hashes alone

Hashes prove integrity.  
They do NOT provide information.

---

## The Critical Distinction

Ethereum separates two things:

- **Data Availability**

  - Can I _get_ the data?

- **Data Validity**
  - Is the data _correct_?

Validity is useless without availability.

You cannot check correctness  
of data you don’t have.

---

## Why This Problem Appears Only at Scale

When Ethereum executes everything itself:

- data is local
- execution is local
- verification is trivial

But once execution moves elsewhere:

- rollups
- off-chain computation
- outsourcing work

Ethereum must still guarantee:

> **Anyone can independently verify outcomes.**

That guarantee begins with DA.

---

## What Happens If DA Is Weak (Logical Failure)

Imagine this claim:

> “Here is the new state root.  
> Trust me — execution was correct.”

If the data is missing:

- fraud proofs cannot be generated
- validity proofs cannot be checked
- users are forced to trust operators

The system becomes permissioned.

DA failure = trust failure.

---

## Why DA Must Live on Layer-1

Only Layer-1 has:

- consensus security
- economic finality
- decentralization guarantees

So DA must be enforced by L1.

Not because L1 is fast —  
but because L1 is **credible**.

---

## The First Conclusion (Lock This)

> **Before Ethereum can scale execution,  
> it must guarantee data availability.**

This is why DA comes **before** rollups  
in the topological order.

---

## What This Unlocks (Not Yet Done)

Once DA is guaranteed:

- execution can move elsewhere
- verification remains trustless
- rollups become possible

But that comes **after**.

Today, we only laid the foundation.

---

## The Analogy (Simple & Permanent)

### DA Is a Public Ledger Book

- Execution = accountants doing calculations
- DA = the ledger book open on the table

You don’t trust accountants because they speak confidently.
You trust them because:

- every number is written down
- anyone can check
- mistakes are provable

No book → blind trust.

---

## Final Note

Today you didn’t learn a feature.  
You learned a **constraint**.

Constraints define architecture.

Tomorrow, we ask:

> **How Ethereum enforces data availability in practice.**

**Now the ocean is yours.  
Dive in.**
