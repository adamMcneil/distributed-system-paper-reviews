# Autobahn: Seamless high-speed BFT
## Summary
There are already byzantine fault-tolerant consensus protocols however this paper highlights some of the problems with those solutions.
They define something called blips which are "recovery from events that interrupt progress".
The current solutions either do not account for blips.
Or if it does account for blips the performance for the rest of the application is not very good.
Autobahn tries to fix this oversight by making a system that can effectively hand blip and offer a good baseline performance.
- (i) avoids the hangovers incurred by traditional BFT protocols
- (ii) matches the throughput of state-of-the-art DAG-based BFT protocols while cutting their latency in half, matching the latency of traditional BFT protocols.
The present is a Byzantine Fault Tolerant (BFT) state machine replication (SMR) system.
They offer abstractions of a centralized trusted and always available server.
This intersects with technologies like blockchains because the blockchain solves the same problem but assumes a decentralized architecture.

Most of today's solutions assume a patrial synchrony model.
These systems are always safe but do not provide aliveness.
They assume the GST (Global Stabilization Time).

They create two concepts to better understand the performance of partially synchronous protocols in practice, hangovers and seamless.
They propose Autobahn which is a novel seamless partially synchronous BFT consensus protocol.

## Pros
- They compare their solution to the industry standard Bullshark and can achieve similar results but also handle blips.
- They implement a prototype of Autobahn in Rust.

