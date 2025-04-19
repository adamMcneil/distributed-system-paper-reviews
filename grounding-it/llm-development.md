# Characterization of Large Language Model Development in the Datacenter
## Summary
They introduce two concepts:
- fault-tolerant pretraining 
- decoupled scheduling 

Training LLM is complicated and requires many resources.
Because of this companies have created large data centers with large-scale GPUs.
However, there are a lot of problems that these data centers face.

- Paradigm Transition ()
- Tailored Software Stack
- Unified Architecture


They list four main findings:
- shorter job duration and unfair queuing delay
- imbalance resource usage
- long GPU idle time in evaluation workload
- frequent job failures

This paper is not primarily about proposing a new solution but giving a survey of the problems that are in the current state of the art.
One of their surprising findings is that LLM workloads are not as long as they commonly are thought to be but they found deep learning workloads to have longer running jobs than LLM workloads.

## Pros
- This paper is beneficial to be used as a reference and to spark new solutions that are highlighted in the paper.
- The paper addresses a wide variety of things that could be improved.

## Cons
- the four key insights that they present in the paper seem that they have already been discussed in a lot of the papers that we read already in this class.
- their findings are from a specific data center, Acme, and they pick up specific quirks of the data center in their collection of data.

## Further Developments


## Other Comments
They say that adding TL;DR to the input prompt can improve model performance for summarizing tasks.
This is an example of learning from human feedback or reinforcement learning from human feedback.
Because TD; LR usually is found where somebody is going to summarize something.
