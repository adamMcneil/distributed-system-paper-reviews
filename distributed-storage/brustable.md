# Burstable Cloud Block Storage with Data Processing Units
## Summary
This paper compares cloud block storage (CBS) and its physical counter part (SSDs).
They propose a solution called BurstCBS that is a combination of hardware and software that is an I/O scheduler.

CBS is a data abstraction that allows you to have a virtual block of memery and attach a compute instanst to that block of memory.
This is very related to disagregation which allows for better elasticity.
The storage units can not only be created and destroyed but also resized.
The disagregated architure is quickly growing in populatity.

Two thing that they condsider in design are:
- Comprehensive resource utilization: they what to use all of the resources when they recieve a large spike in workload.
- Base-level performance guarantee: SLO (service level objective) cannot be violated for other customers.

The I/O operatioen for a cluster of vms are processed at a different cluster.
This is probably due to the disagregated nature of the datacenter.

They have customizable hard ware were they burn the data path on to the FPGA.
Because of "the burst capablitity of CBS compute nodes are a common bottleneck"
I am not sure what they mean by burst capablitity in this context.

## Pros
- They are working with a company and the project is actually deployed at that company.
- Acheives 85% better average latency (interesting that they measure average latency and not something like tail latency)
- 5x better though put

## Cons
- I wish that they would have given a better discription of burst in the beginning of the paper.

## Further Developments

## Other Comments
I do not really know what they mean by burst capability.

