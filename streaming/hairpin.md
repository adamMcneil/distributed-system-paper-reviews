# Hairpin: Rethinking Packet Loss Recovery in Edge-based Interactive Video Streaming
## Summary
This paper is concerned with increasing the bandwidth and decreasing the number of missed deadlines in video streaming processes.
Video streaming is almost always edge based because it always going to a end user (the person watching the video).
With video games the scene is processed on the server and then streamed back to the client to be displayed.

This paper is jointly optimizing retransmission and redundancy.
Retransmission is sending the message again because part of the message was not received.
Redundancy is adding extra information to the message so it can be reconstructed by the client or they can know to resend the packet.

The typical/acceptable latency for video conferencing would be 130ms. 
For video games, it would be lower at 96ms.

Most of the cost encrude by video game companies is the large amount of data that they need to transfer over the internet.
They define bandwidth cost to be the redundancy bytes plus the retransmission bytes divided by the data bytes.


## Pros
- This paper is interesting because it is rethink things that we have done in the solutions that we have used in the past and finding if there is a better solution.
- Reduces bandwidth cost by 40% and deadline miss rate by 32%
- This paper is very practical because the end user is an actual person and applies to video games, streaming content, and interacting with users in real-time.

## Cons
- Seems like they could have reported on the monetary benefits of the paper.

## Further Developments
A way to test the one way latency of network packet would be super useful even if it was not an exact number but something relative.

## Other Comments
This paper aims to achieve the same things that I am trying to achieve in my project.
This would be a good paper to cite in my project about video game development.
What would be a typical packet loss rate for application like this? And how would the rate change if the application was only using LAN?

