# FaaSGraph: Enabling Scalable, Efficient, and Cost-Effective Graph Processing with Serverless Computing
## Summary
Infrastructure as a service is used for a lot of graph computing in the cloud.
IaaS minimizes the hardware maintenance cost.
However it does not provide the best elasticity meaning that there is a lot of extra resources that are wasted resulting in wasted money.
FaaS functions as a service.
This offers a very high elasticity and a pay-as-you-go model.
They tested a graph processing workload on top of a FaaS service and they reported bad performance.
They did this with Gemini.
This sentence from the paper is important:
"Our main insight is that the primary reason for poor performance is the mismatch between the data and communication-intensive nature of graph processing and the lightweight tasks targeted by the current FaaS architecture."
- requires a lot of resources and iterative computations.
- query spikes result in allocating too many resources.
- the jobs are made to be run on machines that have more resources than the standard FaaS service.

FaaSGraph is a graph-as-you-go model (seems like it is poorly named).
The user creates a graph by "uploading functions" with the data of the graph.

- identify the inefficiency of the graph process on serverless computation platforms.
- designed a solution for this process.
- re-visited design choices of graph processing.

They treat the processing of the subgraph as a parallel task.

## Pros
- end-to-end performance increased by 8 times.
- reduce memory usage by 50% and reduce cost by 82.7%.
- clearly defines their contributions at the end of the introduction.
- They denominate how they are not able to do what they achieved in this paper (this is particularly helpful for proving that their research was novel).


## Cons
- The topic of the paper is very specific compared to the other paper about SigmaOS

## Further Developments
Since microserves seem to be the most costifitive way to run stuff in the cloud there is a lot of niche research that can be done in this area.
More improvements can be made to this technology to further decrease the cost.

## Other Comments 
Where is the entire graph stored? 
It seems like it cannot be stored only with the FaaS service because those are short-lived processes.

