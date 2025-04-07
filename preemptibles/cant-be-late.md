# Can’t Be Late: Optimizing Spot Instance Savings under Deadlines
## Summary
preemptiblity is a problem for process that have a strict deadline.
If you had a fast running process on a cloud spot instance you that had a strict time dead line it could be preempted by another process and the deadline could be missed.
The on-demand instances are more expensive then the spot instance which is why having a better algorithm to manage the use of the on demand instances is good.
Allowing the process to be preempted means the programmer needs to add checkpoints.
The algorithm that they propose is call Uniform Progress.
There is also a delay that is introduced when switching between processes.

## Pros
- They were able to make an algorithm that performed twice as good as the greedy algorithm.
- able to acheive 27%-84% cost savings AWS work loads.

## Cons
- the main idea of the paper seem very simple (just have a back up pool of on demand spot instance and use them when the deadline is close)

## Further Developments
How long are the tasks running for?
For very short tasks this algorithm could introduce high overheads.

## Other Comments
preemptible - means that the process is able to be preempted by another process.
What grauntees is the algorithm able to make about completion before the deadline?
They do go in the theoretical findings of the paper.
The greedy algorithm works by processing on the spot instance as long as possible until you need to switch to the on-demand to meet the deadline.
They claim that the greedy algorithm ensures that the process will meet its deadline.
However they assume that there is always a on-demand instance to fall back to.
Is this a service that the cloud providers would adopt or what a person using the cloud provider use?

