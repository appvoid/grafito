# Memory
**Why is memory even something relevant?**
For a complete user experience, a chatbot should be able to remember past interacions and keep them as long as they keep meaning to user's intentions.

### Structure

The basic node of a simple cluster structure is called "concept", a concept could be anything. Concepts can be and are related to other concepts till certain threshold. The basic structure of these nodes is a graph brain.

## Importance

The concepts are related to each other based on: 

- Frequency of emergence
- Semantic similarity
- Importance of close-enough nodes when emergence occur
- Frequency of rewards and penalties

Frequency of emergence is, how much this new concept (word) appears, semantics similarity is how much contextual meaning do they share, importance of close-enough nodes when emergence occur means how frequent we penalize or reward the model when it tries to "talk" about something new related to previous words and the frequency of rewards and penalties involves the human giving an overall rating to the model itself for each interaction regardless the word.

Based on the four core ideas above, we can create a system that evaluates which connections should be weak and removed, and which should stay and become stronger. This way of optimizing memory makes it perfect to learn in realtime scenarios where important things should remain.

But how can a machine learn what's important? Saying the word important a lof of times will make it important but that won't make it understand the concept. Well, that's where frequency of rewards comes in. If you have a machine that learns to understand which things should always be done no matter what, you should give it some kind of survival sense where the model wants to know what's best for it.

Best means the goal. Meaning that it should infer its own main "general" goal that makes it possible to achieve the original goal we set at the begining. This can be done by taking the goal we give to it, sketching out some ideas using prompt engineering and fine-tuning a small model for that specific goal. This approach it's painfully slow, but it ensures that the model is learning from its own output.

On this phase, the goal is to retrieve by itself how to learn and remember effectively, which in principle, should be possible to do now that we have open-source models with pretty decent reasoning.
