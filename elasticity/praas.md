# Process-as-a-Service: Unifying Elastic and Stateful Clouds with Serverless Processes
## Summary
They propose a new abrstraction called a cloud process.
It contains all the benefits of the FaaS modole.
But it does not have the draw backs of being disagreted.
It offer benefits over FaaS by leveleaging data locality, fast invocations, and efficient communication.
There are application that are hard to make with the FaaS module like online map services, web-based editors such as LaTeX editors, and social networks.

This is a very helpful table that gives a good survey of the current application designs
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
The important features of this table are that PraaS gets aspect of both CaaS and FaaS.
It has the good elastics properties of FaaS, but has the benefits of having presitent storage.


## Pros
- 17× faster and reduces communication overhead by up to 99%

## Cons

## Further Developments

## Other Comments
Microservices and FaaS are not same thing.
I think the microservices are small servers but have storage but FaaS is no storage.
I am not sure of the difference but they seem similar to me.
Microservices are more like a small server the 

