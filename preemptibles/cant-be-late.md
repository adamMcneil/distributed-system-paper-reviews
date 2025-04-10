# Can’t Be Late: Optimizing Spot Instance Savings under Deadlines
## Summary
preemptiblity is a problem for processes that have a strict deadline.
If you had a fast-running process on a cloud spot instance with a strict time deadline, it could be preempted by another process, and the deadline could be missed.
On-demand instances are more expensive than spot instances, which is why it is good to have a better algorithm to manage their use.
Allowing the process to be preempted means the programmer needs to add checkpoints.
The algorithm that they propose is called Uniform Progress.
There is also a delay that is introduced when switching between processes.

## Pros
- They were able to make an algorithm that performed twice as well as the greedy algorithm.
- able to achieve 27%-84% cost savings in AWS workloads.

## Cons
- the main idea of the paper seems very simple (just have a backup pool of on-demand spot instances and use them when the deadline is close)

## Further Developments
How long are the tasks running for?
For very short tasks this algorithm could introduce high overheads.

## Other Comments
preemptible - means that the process can be preempted by another process.
What grantees is the algorithm able to make about completion before the deadline?
They do go into the theoretical findings of the paper.
The greedy algorithm works by processing on-the-spot instances as long as possible until you need to switch to the on-demand to meet the deadline.
They claim that the greedy algorithm ensures that the process will meet its deadline.
However, they assume that there is always an on-demand instance to fall back to.
Is this a service that the cloud providers would adopt or what does a person using the cloud provider use?

