# InfiniGen: Efficient Generative Inference of Large Language Models with Dynamic KV Cache Management
## Summary
This paper concerns a more efficient caching system used by large language models.
There is a key-value store that the program needs to maintain.
This cache management framework is specifically designed for long-text generation.
It achieves speed-ups of about three times by prefetching essential KV cache entries.
It also offered better model accuracy.

A llm is a stack of transformer blocks.
For each transformer block the number of transformers in the stack is called the model dimension.
Each transform takes N number of input tokens.
There are two main stages in the llm inference prefill stage and decoding stage.
The prefill stage is when the model evaluates the context given the model.
As the program goes through execution each iteration relies on the relationship between the last token and all the previous ones.
This is the process that relies on the key-value store.
The reason that the process benefits long text generation is that the key-value store becomes very big for large inputs and batch inputs.
It consumes a lot of memory.
The cached key-value store needs to be transferred from the CPU cache to the GPU cache.

They rely on large amounts of CPU memory to store the key-value store.
Other works would simply discard these values.
Only the most important key-value pairs are sent to the GPU for processing.

## Pros
- 3X speed-ups and better accuracy.
- Uses a smarter way of sending key-value pairs to the GPU for caching.

## Cons
- it could increase complexity for small-scale jobs.

## Further Developments
What would happen when the CPU cache was not big enough to store the entirety of the key-value store?
More research could be done in this area to find effective solutions.


## Other Comments
Is this used will training the model or running the model?
I believe it is for running the model.
The paper says that it is ideal for long-text generation. What does long-text generation specifically mean?
I think this refers to the amount of input context that the model takes.
Why does the cached key-value store need to transfer from the CPU to the GPU?

