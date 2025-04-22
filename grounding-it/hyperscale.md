# Optimizing Resource Allocation in Hyperscale Datacenters: Scalability, Usability, and Experiences
## Summary
This paper is about the optimization that Meta performs on their data centers that run at hyperscale.
Meta maintains their private cloud with millions of servers.
These are very complex environments, and this paper provides a survey of several ways that the Meta team has optimized their production systems.
This paper focuses specifically on resource allocation.
In another paper, Mete proposed Rebalancer which is their resource-allocation framework.
Rebalancer is a high-level specification language.

They summarize five basic problems that they face in optimizing at such a large scale.
- deciding physically where to put more hardware.
- deciding what servers are going to be deployed to which service (all of the services are sharing the same cloud).
- How do you share shards across the data center?
- routing traffic to the correct geographical data center.
- effectively schedule function and collection of servers to take advantage of the just-in-time (JIT) cache.
What language are they using that uses JIT?
A quick Google search says that they primarily use C++, Rust, Python, and Hack.
They use C++ and Rust for perforant-sensitive solutions.
Python is used for data science stuff.

All of the above problems are similar in the sense that they are trying to optimally assign a set of balls to a set of containers.
There is already a solution to this problem called MIP (Mixed-Integer Programming).
An important observation that they include is that hand-crafted heuristics are hard to maintain.
It is better to have an abstraction where you can change what you are optimizing for without having to change the algorithm that you are developing.
Their solution is broken into three different parts: model specification, model representation, and model solving.

## Other Comments
They say that they have their own private cloud, but is there any public cloud that is not owned by anybody?
How spread apart is the Meta Cloud?
I assume that not all of the servers are in the same location?
