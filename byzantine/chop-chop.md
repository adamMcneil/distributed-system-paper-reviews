# Chop Chop: Byzantine Atomic Broadcast to the Network Limit
## Summary
To achieve state machine replication one of the basic primitives that you need are 
They compare their solution to big names like Twitter, YouTube, and Google searches.
How do they make fair comparisons with these different types of solutions?
There was a proof of concept on two different applications.
The applications include an auction house system, a payment system, and an application called "Pixel War".
State machine replication is the same as making the entire internet a single computer.
The field is trying to reach a line rate at which data can be transferred as quickly as the network layer or the physical lines can carry them.
Chop-chop uses the fundamental idea of batching but compared to other solutions it does it smarter.
Where the current solution would have header information in each message of the batch chop-chop removes that duplicated data.
The duplicated data could be stuff like individual public keys, signatures, and sequence numbers.
The paper gives these batches the name "distilled batches".
Brokers are the ones responsible for distilling batches.
It is easy to tell when a batch was maliciously formed which means that brokers do not have to be trusted.
Brokers can be started by anybody.
The paper identifies authentication and deduplication as the main bottlenecks in batched Atomic Broadcast.
The main contribution of the paper is distillation. 

## Pros
- processes 43 million messages a second.
- these messages have an average latency of 3.6 seconds.
- one nice design choice for developers is that chop chop provides the authentication and duplication and the developer does not need to define this in the application layer but can focus on the core logic.

## Cons
- I think that they assume that the reader knows what an atomic broadcast is and the paper would do well to explain what it is.

## Other Comments 
Overall it is a well-written paper in a field that I am interested in.
It also seems like the paper is a larger step than most of the papers we read and they achieve some good speed-ups.

