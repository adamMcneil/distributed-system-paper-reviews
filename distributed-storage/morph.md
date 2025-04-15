# Morph: Efficient File-Lifetime Redundancy Management for Cluster File Systems
## Summary
File storage systems have thousands of nodes but files typically have 3-way replication.
This paper is about changing a file's replication strategy over its lifetime to reflect that the file is fetching uniformly.
The paper makes 5 important contributions: (they are listed in the last paragraph of the introduction)
- hybrid redundancy scheme:
- data and parity placement policy:
- combines Convertible Codes with a real-world system:
- Shows that morph can be implemented efficiently:
- Shows that Convertible Codes can be used in the real world and not just in theory: (This is a very important contribution)

Typically client will read from the 3 different replicas in parallel.
This reduces the tail latency.
Typically files are the most popular at the beginning of their life and get read a lot.
They use temperature to describe how often the data is being read.
I think the quentitional application that this is used for is something like Google Drive.
This makes sense of the data lifetime cycles that they talk about.
These storage systems seem like they could be very dynamic.
For example, since failures happen all the time that means that files on Google Drive are not just stored statically on some machine out there in the cloud.
They split the lifetime of the file into two main parts:
- when it is first created and the transition to mid-life
- The rest of the process is from midlife until when the file is very cold.

Convertible Codes are a class of erasure codes. 
Their main goal is to reduce transcode IO overhead.

## Pros
- They give a good description of distributed file storage in the first paragraph of the introduction.
It gives you a good idea of the type of scale that the distributed file system works at.
- Tested with data collected by Google and they showed that 

## Cons
- One of the assumptions is that old files will not be read as often.

## Other Comments
Reread this paper if you want to get a good survey of the generic distributed file system.
What is a transcode?

