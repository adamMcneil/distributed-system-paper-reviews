# FBDetect: Catching Tiny Performance Regressions at Hyperscale through In-Production Monitoring
## Summary
This is an improvement in state-of-the-art performance regression detection.
It does this by catching regressions that affect performance by 0.005% percent.
The reason that it is important to catch these regressions is that these applications are running at the hyper-scale, so small regressions can result in the waste of many servers.
It is made to detect these small regressions because compared to the noise in the application they may be similar in size.
This makes it hard to see the regression graphically.
One of the ways they detect these small regressions is by using subroutine-level regression detection.
It is easy to detect small regressions at the subroutine level because there is less noise at that level making them more noticeable.
However this does pose challenges because there can be false positives that need to be filtered out.
It is also hard to add subroutine level profiling to all of the subroutines because it is on such a small scale.


## Pros
- furthers the state of the art by catching small performance regressions.
- is concerned with production systems and making them faster.
- They test on a variety of different workloads.

## Cons
- Does not provide a good definition of performance regressions.
- very incremental they summarize their contributions as being able to detect small regressions better than before and they do not have strong performance increases to justify this.

## Other Comments
How are regressions resolved when they are detected?
They say that "A single code change can lead to anomalies" but what are these code changes?

What is a Performance Regression?
This is the definition form Wikipedia:
"A software performance regression is a situation where the software still functions correctly, but performs more slowly or uses more memory or resources than before."

