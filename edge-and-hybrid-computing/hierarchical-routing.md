# Stable Hierarchical Routing for Operational LEO Networks
## Summary
This paper is about a stable network routing system that include satellites and datacenters on earth.
SHORT Stable Hierarchical Orbital Routing Technique
Short is a method of getting a stable hierarchy over a dynmanic network specifically with LEO (low earth orbite) satellites.
Obviously the network on the earth are not moving but the satellites that they are talking to are moving.
This paper is concerned with how to create a stable routing despite the dynamic nature of the satellites.

There is a certian level of unavoidable chun that comes with using applications like this.
The first step of the process is to have the satellites communicate there position with other satellites.
The satellites can use latitudes/longitudes, cellular cells, space-filling curves, or Geohash.
SHORT uses a orbital-geodetim coordinate to track location.
It essiantial looks like a chart that has been stretched over the entire world.
The next step in the process is to assign each node a hierarchical address based on its location.
The reason that they use the scheme that they do is because it resilient to orbital maneuvers.
They decentralize the interla LEO routing by using the hierarchy that the node are structured in.
They use ground stations for routing to external networks.
They measured SHORT's preformance of stability, availability, efficiency, and resiliency.

## Pros
- SHORT saves 9–31,816 X routing table updates and 3–31,908 X global route control costs.
They claim to have some very large speed ups.

- This has implications for technologies like star link.

## Cons
- It looks like they only collected data from a simulation.

## Other Comments
How do they test and deploy their program?
How did they develop there simulation and how good of a representation of the real world is it?
How much of the network trafic that I create is going through satellites.
I feel like this is specifically useful for getting network to remote location, and is part of the reason they say the speed ups that they did.

