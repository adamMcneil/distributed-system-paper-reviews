# Heet: Accelerating Elastic Training in Heterogeneous Deep Learning Clusters
## Summary
HEterogeneity-aware system explicitly developed for Elastic Training
The problem is that deeply learned clusters are heterogeneous in terms of their communication and computation.
They make two main contributions to this paper.
The first is the make a process that can measure the efficiency increase of scaling up or scaling down the cluster.
The second is a price function that is used to balance efficient scheduling and efficient scaling.

They are trying to achieve minimized job completion time.
One of the challenges here is the communication speed between GPUs.

Heet is a cluster-wide elastic scheduler specifically for GPUs.
Heet does this by providing an API to schedule tasks.
Heet uses a new 3-D collaborative filtering scheme for profiling.
The profiling tasks are short-run tasks.

## Pros
- reduces the overall job completion time (JCT) by up to 2.46× and makespan by up to 3.96× compared to existing solutions.
- uses machine learning to dynamically tune application parameters.

## Cons
- very poorly named (in my opinion).
- Seems to be an incremental paper and does not add a lot to the research field.

## Other Comments
How does the fact that the system is heterogeneous change the design of the paper? Compared to a homogeneous system architecture?
Are there any homogeneous system schedulers?
AFS, Elasticflow, Lyra, and Themis are some of the technologies that are already used in the industry.
What companies are using these technologies and what is the user experience like?

