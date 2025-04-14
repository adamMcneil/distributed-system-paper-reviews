# Massively Parallel Multi-Versioned Transaction Processing
## Summary
OLTP - online transaction processing
This paper proposes Epic as "the first multi-versioned GPU-based deterministic OLTP database".

There is a need to process 10000 transactions a second.
One possible solution is to have an in-memory database, these have benefits over traditional disk-based databases.

There are two types of databases multi verison and single verison.
Multi-version systems have multiple versions of a piece of data.
Having a multi-version system allows for a more significant degree of parallelism.
However, there is no free lunch there are still other concerns like the overhead that is introduced by having a multi-variable system.
Versions are stored in linked lists and transversing a linked list is slow.

Epic batches transactions into epochs before transaction executing the transaction.
This natural split creates two different phases the transaction phase and the execution phase.

Deterministic databases have been increasing in demand because they are needed at a larger scale.
A transaction is a section of code that needs to be executed altogether.
If any of it is executed it all needs to be executed.

They compare performance with other things like STOv2, Caracal, GaccO, and Aria.
This database uses a combination of multi-version, deterministic, and in-memory and out-of-memory.

## Pros
- Their design leverages the new technology in GPUs that allows for zero overhead for context switching.
- The design works for CPUs and GPUs.
- minimizes the cost that comes with multiversioning because of version storage, lookup, and garbage collection.

## Cons
- They give very general benefits in the abstract
- Seems to be only compared with the artifact of other research projects (missing a practical aspect)

## Further Developments

## Other Comments
What are the limitations of using a GPU for general-purpose computing? 
Why have there not been more applications like this that make traditional applications run on a GPU?

