# Resiliency at Scale: Managing Google’s TPUv4 Machine Learning Supercomputer
## Summary
TPUv4 (Tensor Processing Unit).
This paper is about how the team at Google develops and maintains its supercomputers.
The supercomputer is used for machine learning training.
They talk about automatic fault resiliency and hardware recovery.

The main challenges of maintaining the computer are making the process parallelizable and keeping the machine reading (availability).
Availability is the main focus of this paper.
They compare the problem that they solve is similar to map reduction.
The machine learning train workloads require a lot of hardware, which means that the system is prone to many failures.
It brings the mean time between failure down to hours or minutes.
These are usually running in a cloud environment which means that the resources need to be shared.

The supercomputer has things called cubes that are 4x4x4 TPUs.
At the lower level, there are 4 TPUs grouped into 16 groups.
Each supercomputer or pod has 64 cubes.
These chips are connected with an inter-chip interconnect (ICI).
This ICI layer is reconfigurable which allows different cubes to talk to each other.
This increases availability by a lot because the system can adapt when a cube does down.
There is a process called Borg that is responsible for scheduling and managing jobs.
Pod Manager connects cubes that need to talk to each other based on Borg.

They are trying to achieve the following: scalability, availability, resiliency, and cost.

## Pros
- They achieve 99.98% availability by creating a system reconfigurable.
- Gave a very good introduction to the field.

## Cons
Would be cool if the supercomputer was able to do more general-purpose computing.

## Other Comments
They created a torus network which is like a donut.
To make this topology you only need to organize the nodes in a 2-D array and connect the nodes at the top and bottom and connect the nodes at the left and right.
I would have thought that they would try to optimize for speed and fast execution, but they chose things like scalability and cost.

