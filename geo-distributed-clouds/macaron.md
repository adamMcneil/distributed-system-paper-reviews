# Reducing Cross-Cloud/Region Costs with the Auto-Configuring MACARON Cache
## Summary
Terms to define:
- cross-cloud: Running an application on multiple different cloud providers.
- cross-region: Running an application in different geographical regions within the same cloud provider.
- multi-cloud: Running an application on multiple different cloud providers (same as cross-cloud).

The key insight of the paper is that cache size is tied to cost and not the limits of the hardware.
It is becoming increasingly popular to distribute your workload in both a cross-cloud and cross-region way.

They propose an auto-configuration system called Macaron (which I believe is a type of cookie) that dynamically adjusts the configuration for the caching system.
Instead of greedily allocating the cache they use cost meterics to determine how to configure the cache.
This is important because it is running in a cross cloud and different cloud provide have different cost for there services.
They try to minimize both cost and efficiency.

Design objectives:
- They need to design a schema that is between also performing remote calls and caching every call that minimizes cost and performance.
The new part of this is minimizing the cost.
- Since typical cloud objects are not queried with a high rate it makes the most sense to have large cache sizes.
Otherwise, the cache would hardly ever have a cache hit.
- The program needs to monitor the workload and reconfigure the cache accordingly.

Macaron Architecture
- Macaron client
- Cache engine cluster
- OSC manager
- Macaron controller

Macaron assumes the data to be immutable which is consistent with the assumptions made by data lakes which it interfaces with.

## Pros
- "reduces cross-cloud workload costs by 65% and cross-region costs by 67%"
- minimizes cost
- able to be across different cloud provides

## Cons
- They use data from Uber to test their application but it might be good to use a wider range of test data

## Other Comments
An area of caching that I would benefit from studying more is layered caching.
Object storing is typical in a datalake.
