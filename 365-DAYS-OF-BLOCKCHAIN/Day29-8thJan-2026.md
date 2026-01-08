# DAY 29 — How Ethereum Enforces Data Availability

### _Why “Posting Data” Is the Real Cost of Trust_

---

## Gist

Ethereum does not trust claims.  
It trusts **published data**.

Data Availability is enforced not by promises,
but by **forcing data onto the chain**.

That decision defines Ethereum’s scaling path.

---

## Start From the Core Question

We already know:

> Verification requires data.

Now the real question is:

> **How does Ethereum make sure data is actually available to everyone?**

The answer is surprisingly simple:

> **Ethereum makes data expensive to hide.**

---

## The Only Way to Enforce DA

Ethereum cannot:

- force honesty,
- force execution correctness,
- or force off-chain actors to behave.

But it _can_ force one thing:

> **If you want Ethereum to accept your result,  
> you must publish the data publicly.**

No data → no acceptance.

---

## What “Publishing Data” Means on Ethereum

Publishing data means:

- including transaction data in blocks,
- making it part of the canonical chain,
- letting every full node download it.

Once data is in a block:

- it is gossiped across the network,
- stored by nodes,
- accessible to anyone.

This is Data Availability enforcement.

---

## Why Ethereum Charges Gas for Data

Data takes:

- bandwidth,
- storage,
- propagation effort.

So Ethereum prices it.

Gas for calldata exists because:

> **Publishing data is the cost of decentralization.**

If data were free:

- blocks would explode in size,
- nodes would drop out,
- decentralization would collapse.

So DA must be **paid for**.

---

## Execution vs Data (Critical Separation)

Here’s a key realization:

- Execution is temporary
- Data is permanent

Ethereum doesn’t care _how_ you compute,
as long as:

- the inputs are visible,
- the outputs are verifiable.

This is why:

> **Execution can be outsourced,  
> but data cannot.**

---

## Why Rollups Post Data, Not State

Rollups do NOT post:

- full state,
- balances,
- internal databases.

They post:

- transaction data,
- compressed calldata,
- enough information for reconstruction.

Because:

> **Anyone must be able to recompute state independently.**

That independence comes from data.

---

## The Cost Problem Appears

As rollups grow:

- execution moves off-chain,
- but data still hits L1.

So Ethereum hits a new bottleneck:

> **Data availability bandwidth.**

Not CPU.  
Not memory.  
**Data throughput.**

This pressure leads directly to the next step.

---

## The Logical Conclusion (Do Not Skip)

Ethereum realizes:

> “If DA is the bottleneck,  
> we must scale DA itself.”

This realization leads to:

- blobs,
- sharding,
- sampling.

But those come later.

Today, we stop here.

---

## The Analogy (Lock This In)

### Ethereum Is a Public Notice Board

- Anyone can calculate privately at home.
- But if you want your result to matter,
  you must pin your work to the board.

Everyone can:

- read it,
- copy it,
- verify it.

The board gets crowded.
So space on it costs money.

That cost is **Data Availability gas**.

---

## Final Note

Today you learned:

- how Ethereum enforces DA,
- why data costs gas,
- and why execution is cheaper than trust.

Tomorrow, we ask the next inevitable question:

> **If DA is expensive, how do we scale it without breaking decentralization?**

That question gives birth to **blobs and sharding**.

**Now the ocean is yours.  
Dive in.**
