# MAST: Global Scheduling of ML Training across Geo-Distributed Datacenters at Hyperscale
## Summary
The basic problem here is that you have a program that you want to run in the cloud.
The program takes a large amount of data as input which is also stored in the cloud.
The state of the art is to upload the data to the cloud in a certain data center region and ensure that the program is run in the same data center region.
MAST is an abstraction that handles the distribution and scheduling of both the data and the program's workload.
A common use case of this type of application is a machine learning workload.

It lists three concepts that it covers in the papers:
- temporal decoupling: scheduling is divided into two different responsibilities fast path for real-time jobs and a slow path that continually optimizes the way the data and workload is distributed.
- scope decoupling: I am not sure what they are talking about here.
- exhaustive search: Since ML tasks take a long time to run is beneficial to do an exhaustive search to find the best machine to schedule the task.

The program's main challenge is to balance the amount of training data and workload at a specific machine.
You do not want to send too much data to a node such that it does not have the GPU resources to perform all of the computations.
There are further complications with the fact that the process is scheduling over ten different regions on machines that have CPUs and GPUs.

## Pros
- They reduce the GPU demand-to-supply ratio from 2.63 to 0.98 effectively eliminating the overload.

## Cons
- Adding a layer of abstraction is not always good for some simple applications it could be better to set up the training environment manually.

## Further Developments
Efficient ways of running workloads in the cloud is a very important area.
The main problem that they solve is the addition of the input data, so it could be a good idea to research what the solutions are without that problem.
Also, other papers make it run over different cloud providers.

## Other Comments
MAST: (ML Application Scheduler on Twine)
What is hyperscale deployment?
I think it just refers to the size of the deployment (very big)

