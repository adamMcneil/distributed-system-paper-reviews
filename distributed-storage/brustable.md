# Burstable Cloud Block Storage with Data Processing Units
## Summary
This paper compares cloud block storage (CBS) and its physical counterpart (SSDs).
They propose a solution called BurstCBS which is a combination of hardware and software that is an I/O scheduler.

CBS is a data abstraction that allows you to have a virtual block of memory and attach a compute instance to that block of memory.
This is very related to disaggregation which allows for better elasticity.
The storage units can not only be created and destroyed but also resized.
The disaggregated architecture is quickly growing in popularity.

Two things that they consider in design are:
- Comprehensive resource utilization: they want to use all of the resources when they receive a large spike in workload.
- Base-level performance guarantee: SLO (service level objective) cannot be violated for other customers.

The I/O operation for a cluster of vms are processed at a different cluster.
This is probably due to the disaggregated nature of the data center.

They have customizable hardware where they burn the data path onto the FPGA.
Because "the burst capability of CBS compute nodes is a common bottleneck"
I am not sure what they mean by burst capability in this context.

## Pros
- They are working with a company and the project is deployed at that company.
- Archives 85% better average latency (interesting that they measure average latency and not something like tail latency)
- it 5x better though put

## Cons
- I wish that they would have given a better description of burst at the beginning of the paper.

## Other Comments
I do not exactly know what they mean by burst capability.

