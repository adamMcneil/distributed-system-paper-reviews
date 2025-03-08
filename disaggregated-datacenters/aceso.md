# Aceso: Achieving Efficient Fault Tolerance in Memory-Disaggregated Key-Value Stores
## Summary
Key terms from the introduction:
- Disaggregated memory: spreading the data across different machines and having specific machines for computing and storage.
- Key value store: problems are memory space and performance overheads.
- Hybrid fault tolerant:
- checkpointing: this allows you to stop the program and then start it again.
- Erasure coding: this is an error correction

They propose a new checkpoint scheme that increases throughput and tail latency.
They claim that disaggregated memory is used widely in industry and academia.
Using checkpointing to restart the process can lead to problems with key-value pairs being dropped.
Checkpoints also introduce overheads into the system.
Erasure coding also complicates fault tolerance because it requires decoding calculations.

The problem that disaggregated memory solves is this.
When renting out computing power you do not want to rent out CPU power and storage that is fixed together.
This can lead to underusing certain components of the computer.
If you can rent a store and compute power you could save resources and money.

Enasure codes are a more efficient fault mechanism than replication because replicas have a lot of storage overhead.
This is just storing some parity data that allows you to reconstruct the data when it is lost.
Check-pointing is sometimes used for fault tolerance but is more commonly used just to stop and restart the application.
Erasure coding is ideal for KV pairs and checkpoints are ideal for indexes.
Aceso adapts the check-pointing scheme to be used for key-value stores.
The main issue that they need to tackle here is the large amount of space used to store the checkpoint.

## Pros
- "achieves up to 2.7× throughput improvement, up to 54% tail latency reduction, and 44% memory space savings compared with the state-of-the-art replication-based KV store on DM."

## Cons
- Overheads are created because we are accounting for faults even though they try to mitigate those in the paper.

## Further Developments

## Other Comments
This paper has been the closest to the stuff that we covered in cs 425.
This paper has some large similarity to the paper that we read last class about MAST.
They are both dealing with compute resources and store areas.
A lot of computer science deals with these two basic resources.


