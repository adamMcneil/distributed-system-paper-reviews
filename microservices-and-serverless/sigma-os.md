# Unifying serverless and microservice tasks with SigmaOS
## Summary
This paper compares two different common approaches to cloud computing: serverless functions and container orchestration.
Parallelism in the cloud is achieved by using multiple instances of a machine instead of making the program run in parallel on one machine.
Typically a pipeline of microservices that call other microservices is created and the user data flows through that system instead of the traditional server approach.
One common way to achieve this parallelism is to use stateless microservices services like Amazon web services, lambda, and Azure functions.
There are benefits from the server stateful model that are helpful.
This paper proposes the operating system SigmaOS that combines both of those concepts.

- proc: is a computation in the SigmaOS.
- sigma EPs: communication endpoints the way that procs talk to each other.

AWS Lambda provides strong isolation for their process but allows some processes to share a microVM.
The core points of the paper:
- faster containers
- isolation
- fast application start
- single system image
- schedulers
- improve serverless

## Pros
- creates a proc in 7.7 msec and can create 36000 procs a sec.
These are important metrics because they reduce the latency of API calls.
- provides the benefit of both the serverless and the microservers approach to cloud computing.
- provides a simple API definition in the paper that is easy to follow.

## Cons
- The main problem with the microserver model is that they have slow start times because the system needs to setup an entire Linux system to. They also need to communicate over the overlaying network with an IP address.
- I would have liked to have more discussion on the differences between serverless and microservices.

## Further Developments
This is an area that I am interested in.
Which is the more practical side of running more traditional applications on the cloud.
Like technologies like Docker, Kubernetes, and AWS.

## Other Comments
Serverless functions (serverless) and container orchestration (microservices) seem very similar it would be helpful to have a clear description of what each of them is.
How would you use this operating system and what would It be like to install?
Would you install it on the remote machine? Would it run on top of something like AWS?
