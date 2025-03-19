# Process-as-a-Service: Unifying Elastic and Stateful Clouds with Serverless Processes
## Summary
They propose a new abstraction called a cloud process.
It contains all the benefits of the FaaS model.
But it does not have the drawbacks of being disagreted.
It offers benefits over FaaS by leveraging data locality, fast invocations, and efficient communication.
Applications that are difficult to make with the FaaS module include online map services, web-based editors such as LaTeX editors, and social networks.

This is a beneficial table that gives a good survey of the current application designs.
|                         | IaaS               | CaaS               | PraaS              | FaaS               |
|-------------------------|--------------------|--------------------|--------------------|--------------------|
| **Computation Unit**    | Virtual machine    | Container          | Process            | Function           |
| **External Interface**  | SSH, TCP, HTTP, RPC, RDMA | SSH, TCP, HTTP, RPC | HTTP, TCP         | HTTP              |
| **Lifetime**            | Months            | Days, hours       | Minutes, hours    | Seconds           |
| **State Duration**      | Persistent        | Persistent        | Persistent        | Ephemeral         |
| **State Location**      | Local disk, memory | Memory, cloud storage | Memory, cloud storage | Cloud storage  |
| **Provisioning**        | Manual, minutes   | Semi-automatic, secs | Automatic, msecs | Automatic, msecs  |
| **Compute Resources**   | Persistent        | Persistent        | Ephemeral         | Ephemeral         |
| **Billing**             | Provisioned       | Provisioned       | Pay-as-you-go     | Pay-as-you-go     |
| **Scaling Down To Zero**| No               | No               | Yes               | Yes               |

Provisioning is the amount of time it takes to start the process.
The important feature of this table is that PraaS gets aspects of both CaaS and FaaS.
It has the good elastics properties of FaaS, but has the benefits of having presitent storage.


## Pros
- 17× faster and reduces communication overhead by up to 99%.

## Cons
- the solution consisted of like 13.5 thousand lines of C++ code.

## Other Comments
Microservices and FaaS are not the same thing.
I think the microservices are small servers that have storage but FaaS is no storage.
Overall a very good paper on a topic that I am interested in.
It is very interesting how each of these software designs has emerged when at the end of the day everything is only ever run on a computer.
There are a lot of different abstractions that make that happen in a sometimes very complex way.

