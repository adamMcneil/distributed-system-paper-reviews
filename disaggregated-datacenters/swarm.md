# SWARM: Replicating Shared Disaggregated-Memory Data in No Time
## Summary
SWARM (Swift WAit-free Replication in disaggregated Memory)
In this paper, they use SWARM to create a key-value store.
This key-value store is designed to be strongly consistent and highly available.
They compare it against the state-of-the-art FUSEE which is another replicated disaggregated key value store.
They also compare it against key values that do not have replication and they report comparable overheads.

They identify two main problems with the current disaggregated memory key-value store.
1. They require multiple network round trips because they were not designed to be used with the "low latency high throughput fabric."
Though these technologies are getting fast they are not nearly as fast as looking something up on RAM.

- 2. They also assume you can run code next to the data for concurrency control.
This does not fit with the disaggregated memory because the computation power and the compute power are separated.

It provides a linearizability form of consistency.
And a strong liveness in the form of wait-freedom.
- 1. The first challenge that they needed to overcome was making concurrent reads and writes to the same object.
- 2. Cannot run computations at the memory module because of the disaggregated nature of the key-value store.
- 3. Must be capable of performing atomic operations on larger things than the standard data size to perform atomic operations on.

They make two important contributions: Safe-Guess is In-n-Out.
- Safe-Guess: an important property is that the atomic operation needs to happen in one network round trip.
- In-n-Out: is a protocol for doing an atomic update in one round trip without using large amounts of computing at the storage node.
There are two ways to achieve this in-place updates with locks and out-of-place updates with atomic pointer swing.


## Pros
- They can achieve comparable overheads to key-value stores that do not use replication.

## Cons
- Disaggregated memory is slow because the computer and the memory are stored in physically different places.
This problem seems like it is not going to be solved.
The problem of transferring data though the network instead of over a bus seems like it is not going to be as good.

