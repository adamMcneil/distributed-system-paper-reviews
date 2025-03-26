# Anvil: Verifying Liveness of Cluster Management Controllers
## Summary
This paper is the first to apply formal verification to controller correctness.
These controllers manage critical cloud infrastructure systems.
Most of the verification work that has been done in distributed systems has dealt with safety but this paper focuses on correctness.
Controllers are systems that manage other systems.

The paper makes two important contributions:
- 1. eventually stable reconciliation
- 2. they also propose a framework for implementing practical controllers and verifying them.

They create a specification that is generally enough that it can be used on a wide range of controlled but still specific enough that it can be used to verify correctness.
The specification ensures ESR which is eventually sable reconciliation which means that the controller will approach the correct state and "eventually" reach the correct state.

## Pros
- Tested on a variety of controllers: ZooKeeper, RabbitMQ, and FluentBit.

## Cons
- I find it helpful when a paper lists the numerical improvement in the beginning of the paper. This paper does not do that but that is partly because they were not concerned with speed increases.
- gets very repetitive in the beginning of the paper.

## Further Developments
It uses TLA which is a cool technology that could be explored more.

## Other Comments
Written by people from UIUC (kinda cool).
It would be interesting to see how many of the papers that we have read have been trying to increase the speed of the application in question.

