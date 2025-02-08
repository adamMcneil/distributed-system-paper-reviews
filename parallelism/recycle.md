# ReCycle: Resilient Training of Large DNNs using Pipeline Adaptation

## Summary
Recycle is a process of training Deep Neural Networks (DNN) in the presence of failures.
Since DNN take a long time to train failure are a large problem and a system for haldingly failures is very benefical.
Recycle does not relie on other server so hint the name recycle it is reusing stuff that is already in use or has been used.
This is all happening in a distributed setting.

A failure in the training process will cause a domino effect of GPUs that are not able to contiune execution.
Three of the things that the paper focus on is fault detection, checkpointing, and efficient execution.
Recycle is similar to both Bamboo and Oobleck.
In so far is that all of them relie on pipeline parallelism.
They differ in that Recycle " utilizes the inherent functional redundancy across pipelines in hybrid-parallel training systems"
It use something called bubbles in the pipeline to do extra work with little to no overhead.
Bubbles happen in the start up and cool down phase of the pipeline.
Bubbles are idle spots in the pipeline.
recycle uses this bubbles to schedule computation that failed.
Each GPU uses a simple heatbeat protocal to communicate with the main sevrer when it has failed.

## Pros
- It may not offer a large speed up but it is also offers a decrease in the number of GPUs that are needed.
This is because it is a common pratice to have a rack of backup severs that take over for failed GPUs.

## Cons
- A 1.46 and 1.64 speed up to not seem like very large speed ups compared to other papers.
- The algoritms relies on bubbles being in the pipeline.
  These seem ideal there would be no bubbles in the pipeline.

## Further Developments
Way to haldle failures that did not relie on bubble could potentially be better.

## Other Comments
Other things to research would be Bamboo and Oobleck.
Both of these project relie on pipeline parallelism.
We have distributed system that handle failure why is training DNN any different.
I assume that it has to do with the fact that they are trained on GPUs.

