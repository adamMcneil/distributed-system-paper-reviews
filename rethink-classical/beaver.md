# Beaver: Practical Partial Snapshots for Distributed Cloud Services

## Summary
This team of students developed a piece of software called Beaver for taking partial snap shots of systems in a cloud computing setting.
This is a classic problem but they add to the field an algorthim that takes in to account external traffic that is not part of the system taking the snapshot.
Beaver does not create large ammounts of network bandwidth.

A high level overview of the algorithm is this: Beaver sets up a "Monolithic gateway overlay" to monitar internal and external before the data is processed.
Each machine has a virtual and a direct IP address.
The system uses software load balancers to map in between the two IPs.

They cleaverly define a partial snapshot.
In the classic snapshots it assumes that the machines in the snapshots are the only machines in the network.
This assumption is usually not true because a the internet is very large.
This work removes that assumption making the thing that used to be fell snapshot partial snapshots.

The monolithic gateway overlay has only two jobs tagging incoming packets with snapshot tags and intiating snapshoting.

## Pros

## Cons
- I thought that starting with an overview of how the algorithm works would make the paper more interesting and easier to follow.
- 

## Further Developed

## Other Comments

