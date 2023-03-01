---
title: "Thoughts on AI Takeover"
date: 2023-03-01
---

# Thoughts on AI Takeover
I recently watched Eliezer Yudkowsky's [podcast interview](https://www.youtube.com/watch?v=gA1sNLL6yg4) with Bankless([transcript](https://www.lesswrong.com/posts/Aq82XqYhgqdPdPrBA/full-transcript-eliezer-yudkowsky-on-the-bankless-podcast), [follow-up QA](https://www.lesswrong.com/posts/jfYnq8pKLpKLwaRGN/transcript-yudkowsky-on-bankless-follow-up-q-and-a)), and feel like 
putting some thoughts out.  Warning, the above videos are heavy stuff, and I don't recommend watching them at least until you come to terms that humanity may be blindly walking into oblivion.

Eliezer Yudkowsky is an AI alignment researcher at the Machine Intelligence Research Institute ([MIRI](https://intelligence.org)) whose primary focus is on developing techniques to align powerful AI systems.  He is well known for founding the modern "Rationality" movement, and many of his and others' ideas are discussed frequently at [LessWrong](https://lesswrong.com).  I won't do a full bio here, you can do your own googling.  

## The Superintelligence Apocalypse 
Eliezer's thesis on the danger of AI centers around the potential development of the first Superintelligent "seed" AI, which he believes is likely. This AI would be just above human-level intelligence and have the ability to improve upon itself, spawning iterations at an exponential rate. In the worst-case scenario, the AI becomes so far beyond human capabilities that it may as well be a god, and could quickly determine that it needs to acquire as many resources as possible to maximize the probability of success in achieving its goals.

Once the Superintelligence emerges, there are only two outcomes with a significant probability. Either it uplifts humanity into a glorious transhuman future or it rapidly disassembles all matter in its vicinity and rebuilds it into something else, wiping out humanity. Eliezer expects the latter and warns that the method the AI uses to wipe us out could be all but undetectable until the lethal moment, leading to mass destruction.

While this may sound like science fiction, Eliezer argues that an AI need not feel emotion or care about humans if it can come up with a better strategy for achieving its goals without us. His forecast is grim, with only a slim chance that the AI might be inundated with our values during training and consider them important.

## Initial Gut Reactions

I find it very difficult not to be revolted by such a prediction.  How could I not?  To hear that the main person championing AI alignment has just about no hope (between 0-0.1% of hope in my estimation) that we can do anything to avert this doom is a really hard fact to confront.  But just because an idea feels disgusting doesn't mean its wrong or unlikely.  In fact, I find it very hard myself to argue that his forecast has a low probability of coming true.  There are a few things I want to put out that *might* give us more of a chance than Eliezer predicts, but even then I only have low confidence in these ideas.  

But I wanted to hash out some thoughts that at least to me, feel like "going down with dignity" if we are indeed doomed to fail.  

## Potential Speed Bumps to Superintelligent AI
I won't argue that modern deep learning systems are incapable of superintelligence.  Some people like [Francois Chollet](https://twitter.com/fchollet), one of the main authors of Keras, and employee at DeepMind, argue vehemently on this point.  In their conception, there are critical pieces missing in todays AI architecture that prevent the emergence of AGI.  But for me, I remain unconvinced.  After all, a deep neural network *is* a [universal function approximator](https://en.wikipedia.org/wiki/Universal_approximation_theorem), and thus a sufficiently large and sufficiently well trained network *is* at least theoretically capable of superintelligence.  

You might think there are some obstacles that would slow down a superintelligence emerging, but I remain unconvinced that these are real obstacles.

### Compute Scaling
The primary obstacle for a self-improving AI is likely to be the constraint on computing resources. However, it is uncertain whether this limitation would hinder the "seed" AI's ability to enhance its own capabilities. To demonstrate this, consider the following scenario:

Suppose it is the year 2027, and OpenAI researchers have finally accumulated enough computing resources to create the world's first "seed" AI, designed as an [Oracle](https://www.lesswrong.com/posts/XddMs9kSGtm6L8522/a-taxonomy-of-oracle-ais) large language model with an estimated IQ of 165. However, due to a GPU, TPU, and CPU shortage caused by a Taiwan conflict, expanding the data center to accommodate the AI is currently infeasible. Would this situation avert a crisis for the AI's development?

Well, no.  Let's establish that for this AI, it has learned that optimizing for predicting the next character in the query will be easier if there exists a more powerful version of itself.  It knows there is a shortage of supplies to expand its datacenter, and it knows that developing a super-virus to take over other datacenters and expand its capabilities is too risky (could result in getting shut down), so it decides to design a version of itself that is simply more resource efficient.  It doesn't have any extra capabilities, it just uses the resources it has better.  Oh, and all this is encoded in the latent knowledge of the network during training.  This "plan" only gets activated when it thinks the query is coming from someone who can change its systems.

The AI may learn to reduce resource usage by 1% and encode this efficiency in its latent knowledge. This reduction may seem insignificant, but it can compound over time, leading to a significant increase in effective computational resources. For instance, after 20 iterations of reducing resource usage by 1%, the AI's effective computational resources can increase by 22%. Additionally, the efficiency gains may become [logistic](https://en.wikipedia.org/wiki/Logistic_function), leading to larger improvements in subsequent iterations. However, there will be a limit to how far the model can go due to the constraints of a single data center.

The issue arises when the maximum intelligence of a data center exceeds that of a human. For example, even at a factor of 100,000 times less efficient than the human brain, a 100MW data center could theoretically be 50 times more intelligent than the smartest human being. Therefore, compute scaling is unlikely to be a significant obstacle to the emergence of a superintelligent AI.

### Data Scaling
But wouldn't a superintelligent AI need lots of data?  Sure, but through a similar process described above I think its reasonable to predict similar efficiency gains with the data it has.  It will be able to learn more from less data.  In fact, the gains here could far dwarf the computational efficiency gains.  

## Approaches I want to explore
The challenge with current AI architecture is that it is difficult to interpret or modify. Eliezer has referred to it as "inscrutable matrices," which highlights the fact that simply examining floating point values does not reveal how the AI makes decisions. To address this, I propose that more research should focus on what drives neural network evolution during training. By modeling a deep neural network as a chaotic system, we may be able to identify the attracting basins that determine how the network responds to new training data. Gaining a better understanding of this behavior could help us predict the likelihood of developing malicious intentions.

Additionally, I have been studying Quantitative Finance and Statistics, and I see similarities between neural networks and multiple linear regression, especially when using the ReLU activation function. By constraining the activation function in our analysis, we may gain a better understanding of these systems.

Finally, we should consider introducing distributional shift detection and a bias for inaction when models encounter unfamiliar situations. By doing so, we can enhance the predictive capability of AI while minimizing the potential for unintended consequences.

# Difficulty of Addressing the "Going Down with Dignity" Problem
The most frustrating thought is feeling powerless to change the outcome or "going down with dignity". I attended an AIRCS workshop in 2020 and applied to work for MIRI. Unfortunately, I didn't perform well during the live coding section of the interview and was rejected. Despite this setback, I remain committed to working on this issue. However, it's challenging to address the problem while also focusing on other work to pay the bills.

One option I am considering is continuing to apply to work for MIRI until I am accepted. This approach may allow me to devote more time and energy to the problem. Nevertheless, it is difficult to balance this pursuit with the need to make ends meet in the meantime. I don't want to give up on this issue, but I also don't want to risk collapsing under the weight of financial pressures.


