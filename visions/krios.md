# Krios: Scheduling Abstractions and Mechanisms for Enabling a LEO Compute Cloud
## Summary
This paper is again about LEO satellites.
These satellites provide high speed internet, cellar communication, and internet of thing communication.
This paper is about LEO compute cloud which is interesting because normal you would think of the satellites as just moving data around.
The novel contribution that this paper makes is an abstraction were the application provide specifics where the user wants its application to be available.
They also introduce a prediction model that will predict the future location of the satellite to antisipate application handovers.

This paper assumes satellites on space and on earth.
In general the bandwidth between these different nodes are in terms of GB.
Computation is done on at the satellite to reduce the amount of time we have to spend sending data.
They describe Krois as the missing system because it provides services like Kubernetes.
Kubernetes is a orchestrator.
The system is built on top of Kubernetes which allows it to get the benefits of the state of the art, kubernetes.
It uses a just ahead of time handover to maximize up time.
During the hand off process there is a filter stage and a scoring stage.
The filter stage filters out nodes that are to far away.
During the scoring stage they try to find the node that will be available for the longest time.

## Pros
- They achieved a very high increase in availability to almost 100% from 5%.
- They also achieved very high speed up.
This is a similar trend to what we saw in the other paper LEO paper.

## Cons

## Further Developments
As we already have seen there are a lot of really big increase we have seen in the area of LEO, so there are a lot of new way to take this field.
Part of the research could be related to how the distribution of date site in the on earth affect the performance of the system.
Is there infrastructure to deploy this software to a real system.
If there is not then research how to do that would seem to be very beneficial.

## Other Comments
A term that they use is "orchestrator" I may not sure what exactly they need by this.

