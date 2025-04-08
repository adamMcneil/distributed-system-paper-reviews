# Cake
## Summary
In this paper, they create a reinforcement learning model to optimize key-value store caching.
They use Llama-3.2-3B-Instruct to train the model.
They optimize for an LLM key-value store that stores context tokens.

## Strengths
- The abstract and the introduction are both very solid and well-written.

## Improvements
- I think a statement like this should be taken out for the final paper "Focus in the first half of the project was successful"
- The axis on the graph could be labeled better. The average of what? I think it would be good if the graph could stand by itself and still be understood.
- What are the other solutions to making a caching policy?
- One thing that a lot of the paper do that I like is putting a quick summary of their results in the abstract or introduction.
- The first paragraph of the abstract seems more like it fits in a Related Works section and not an abstract.
I would move it to a new section.

## Detailed Comments
I would rework the first two paragraphs into three paragraphs by adding a Related Works section.
The authors do a good job setting up the paper and describing what they are doing.
I would have like to see a better discussion of what the industry standard is in the beginning of the paper.
Additionally, a discussion of what makes your work novel or distinct from other works would be good.
The Methods and RL Problem sections were hard to follow.
I think it was because you were explaining other work and your work at the same time.
It might help to add a figure or table diagramming what you are talking about.
I think it would be better to explain the related work and then explain how your application was built on top of it.
The graph in the results section could have been explained better.
Remember I did not do the work and am looking at it with a fresh set of eyes.

