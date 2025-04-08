# Falcon
## Summary
FALCON (Flexible Autoscaling for Latency-aware Cloud Optimization via Nonlinear Programming)
This paper discusses creating a system to handle busty workloads in disaggregated cloud architectures.
They propose a novel utility function to optimize for the following: minimize completion time, maximize resource utilization, and minimize resource waste.
They also survey the existing solutions describing load balancer and autoscale in the architecture of an autoscaling load balancing system.

## Strengths
- You mention the work that is already in the area.
- Figure 1 in Section 3 does a good job of diagramming the current solution.
- Many of the papers do not include the specifics of how they test their application, but you do include it which is helpful.
(I am referring to Section 5.1.1 specifically)

## Improvements
- The graphs in the result section are hard to read and understand.
- I think it would be helpful to include more background positioning of your work concerning the application of the process.
What workloads did you use to test your application?
- It would be helpful to include a baseline to compare our solution to, especially for the graph in the result section.

## Detailed Comments
The abstract and the introduction do a good job of describing what the paper is about and outlining what you achieved.
You do a good job of explaining why an algorithm like FALCON is needed.
With the related works section, I would have liked to see more of a survey of the existing solution.
How did you determine that the utility function is the best?
Discussing this would be helpful.
The experiment setup is well-written and easy to understand.
In the results section, I think you should interpret your graphs more for the reader.
Do not assume that the reader is going to take the time to study them closely and interpret the graphs.
Make them plain and simple.
I also think they had to follow because there was not a baseline to compare them to.
What are the existing solutions and how do they compare against FALCON?

