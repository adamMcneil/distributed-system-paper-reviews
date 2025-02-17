# Fairness in Serving Large Language Models
## Summary
With an application like ChatGPT, it receives a natural language query.
Then it has some model or program in other words that takes the query as input and spits out an answer.
That answer is then sent over the network back to the client.
This paper addresses how to make that process fair.
Some of the trade-offs are computation power vs fairness.
For example, you could come up with an execution plan that is fair but does not utilize all of the computing power.

Current solutions use a first come first serve solution.
They impose a request per-minute limit so that one client making a lot of requests does not hog the server.
A solution that is proposed for networking and os scheduling is fair queueing.
Fair queueing ensures that each client gets $1/n$ resources.
This paper applies fair queueing to LLMs.
It does this at the token level instead of the request level.
One of the challenges is that the input size and output size are not known beforehand.
This is not true for the other applications of fair queueing like networking.
They propose a Virtual Token Counter (VTC) the compare the cost of different requests.
They think that they are the first people to address this problem.

Though requests can be answered one at a time it is much more efficient to answer a lot of them together.
This is an important quote from the paper:
"Intuitively, VTC tracks the services received for each client
and will prioritize the ones with the least services received,
with a counter lift each time a client is new to the queue."

## Pros
- It uses an existing solution to solve a current problem.
- Uses tokens to track fairness instead of requests.

## Cons
- Does not talk about the severe structure of LLM applications.
- Had trouble understanding the results. It seems a rather difficult problem to show the improvements.

## Further Developments
There is a lot of room for development in this area because there are not any LLM-specific fairness strategies.


## Other Comments
I have a question about the underlying network architecture of this system. What is it?
I think that part of the answer is that there is fairness across multiple machines that are all running the LLM.
There is also fairness at each machine which is batch tokens.

