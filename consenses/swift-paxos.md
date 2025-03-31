# SwiftPaxos: Fast Geo-Replicated State Machines
## Summary
This is an incremental paper about making the paxos algorthim work in a geo replicated setting.
They show that they increase the efficency of the algorithm by 2.9 times.
Paxos was originally proposed by Lieslle Lamport a while ago and is still used I many distributed system settings.

The paper is more generally about state-machine replication which is the idea of having a copy of a state machine at each of the nodes in the network.
Another common algorithm is Raft which is much simpler then Paxos.
Both of these protocals funnel all of the command though a leader.
They focus on both increasing the speed of Paxos and not affecting the tail latency.
Mean that they do not want to make the worst case take longer.

The system model does not consider malicious processes.
The program that they propose in this paper satisfies linearizability.
Here are some of their design priciples:
Validity ensures that no command is processed before it is created.
Integrity ensures that each machine executes that command at most once.

## Pros
- increases the speed of paxos in geo-replicated setting by 2.9 times.

## Cons
- The paper is incremental
- I would have like to see how this is used in production and the seen it tested on real bench marks but this probably not the main focus of the paper.
And It would be much harder to get real bench marks.

## Further Developments
There will always be areas to increase the speed of Paxos since the problem is very general.
And it is important to consider that the acheiture for the cloud is growing and adapting and so will the implenmentation of Paxos to remain fast.

## Other Comments
I think the most important part of this paper is the evaluation because it is important to do a fair comparison to veify the speed up that they claimed they got in the beginning of the paper.
More specifically that they run it on a diverse range of test case to prove that it is better in all cases and not just a specific test set.
