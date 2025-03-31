# SwiftPaxos: Fast Geo-Replicated State Machines
## Summary
This is an incremental paper about making the Paxos algorithm work in a geo-replicated setting.
They show that they increase the efficiency of the algorithm by 2.9 times.
Paxos was initially proposed by Leslie Lamport a while ago and is still used in many distributed system settings.

The paper is more generally about state-machine replication which is the idea of having a copy of a state machine at each of the nodes in the network.
Another common algorithm is Raft which is much simpler than Paxos.
Both of these protocols funnel all of the commands through a leader.
They focus on both increasing the speed of Paxos and not affecting the tail latency.
Meaning that they do not want to make the worst case take longer.

The system model does not consider malicious processes.
The program that they propose in this paper satisfies linearizability.
Here are some of their design principles:
Validity ensures that no command is processed before it is created.
Integrity ensures that each machine executes that command at most once.

## Pros
- increases the speed of Paxos in geo-replicated settings by 2.9 times.

## Cons
- The paper is incremental
- I would have liked to see how this is used in production and to see it tested on real benchmarks but this is probably not the main focus of the paper.
And It would be much harder to get real benchmarks.

## Further Developments
There will always be areas to increase the speed of Paxos since the problem is very general.
It is important to consider that the architecture for the cloud is growing and adapting and so will the implementation of Paxos to remain fast.

## Other Comments
I think the most important part of this paper is the evaluation because it is important to do a fair comparison to verify the speed up that they claimed they got at the beginning of the paper.
More specifically they run it on a diverse range of test cases to prove that it is better in all cases and not just a specific test set.
