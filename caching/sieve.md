# Sieve is Simpler than LRU: an Efficient Turn-Key Eviction Algorithm for Web Caches
## Summary
Sieve is a typical cache replacement strategy that they claim is simpler than a least recently used algorithm (LRU) and first in first out.
Netflix has over 18000 servers caching user data.
Some of the algorithms can require parameter tuning to work efficiently.
Simple is beautiful.
Because of this a lot of the large caching libraries use LRU and FIFO caching algorithms.
Caching is tested on the efficiency and the throughput.
They also keep track of the object miss ratio and the byte miss ratio.
Caches typically follow a zipfian distribution when accessed.

The algorithm works by having a visited flag associated with each object that is in the cache.
This flag gets set to one if it is read from the cache.
This flag is set to zero if while trying to put something in the cache you is see that it is one.
If you see the flag is zero while trying to put some thing you remove that cache entry and replace it with the new one.
The hand always just goes through the linked list one at a time.
The algorithm is easy to follow as described in the Algorithm 1 section.

## Pros
- only required approximately 20 lines of modified code to make a system use the Sieve algorithm
- the simplicity of the algorithm provides better scalability
- does not need to lock on cache hit which means that the program can be paralellised easier.

## Cons
- profiling the solution can be tricky because just because you do not get a lot of cache misses for a specific workload does not mean that it would be good in all seneriors. (they test it against web workload)
- They claim that the algorithm is simpler but that seems somewhat subjective.
- The beginning part of the paper is very repetitive.
- They claim that it is simpler then LRU but they also say that they implepent it on top of LRU.

## Other Comments
This is a good paper it gives a lot of practical benefits and is not in a super small area of research.
The actually idea of the paper is very simple, but they spend most of the time analysising how the algorithm works.

