---
title: "Thoughts on AI Takeover
date: 2023-03-01
---

# Thoughts on AI Takeover
I recently watched Eliezer Yudkowsky's [podcast interview](https://www.youtube.com/watch?v=gA1sNLL6yg4) with Bankless([transcript](https://www.lesswrong.com/posts/Aq82XqYhgqdPdPrBA/full-transcript-eliezer-yudkowsky-on-the-bankless-podcast), [follow-up QA](https://www.lesswrong.com/posts/jfYnq8pKLpKLwaRGN/transcript-yudkowsky-on-bankless-follow-up-q-and-a)), and feel like 
putting some thoughts out.  Warning, the above videos are heavy stuff, and I don't recommend watching them at least until you come to terms that humanity may be blindly walking into oblivion.

Eliezer Yudkowsky is an AI alignment researcher at the Machine Intelligence Research Institute ([MIRI](https://intelligence.org)) whose primary focus is on developing techniques to align powerful AI systems.  He is well known for founding the modern "Rationality" movement, and many of his and others' ideas are discussed frequently at [LessWrong](https://lesswrong.com).  I won't do a full bio here, you can do your own googling.  

## The Superintelligence Apocalypse 
The primary thesis for Eliezer regarding the danger of AI is that at some point he believes it is likely we will develop the first Superintelligent "seed" AI.  This "seed" AI will probably be just barely at or above human level intelligence (I'm using the term ambiguously here), but *just* powerful enough to develop a version of itself that is slightly more capable than it is.  At that point, he posits that the initial seed AI could spawn many iterations of itself, improving each time, so quickly that we wouldn't be able to respond.  In the worst case, over something like 30 minutes the AI goes from barely Human level to something so far beyond our capabilities that it might as well be a god.  

From this point, one of two things can happen.  Either, this new Superintelligent AI does its darnedest to uplift humanity out of its issues and lead us into a glorious transhuman future, or, as Eliezer expects, it quickly determines that it needs to acquire as many resources as possible to maximize the probability of success of its goals, and develops a strategy to rapidly disassemble all matter in its vicinity and rebuild it into something else.  

There is not really any other imaginable outcome with a significant probability once the Superintelligence emerges.  Eliezer expects that the method the AI uses to wipe us out could be well more advanced than any power we possess, and would likely be all but undetectable until the lethal moment.  In his words, "everyone dies in the same second".  

To the uninitiated, this may sound absurd.  After all, modern AIs are not able to developed improved versions of themselves, and the motivation to kill all humans sounds like something out of science fiction.  But his point rests on the fact that an AI need not feel emotion, even if it can understand our emotions, and it need not care about us if it can come up with a better strategy for achieving its goals without us.  

His forecast is grim, with only the faintest outlines of hope that he might be wrong, and that *maybe* there is a slim chance the AI is so inundated with our values during training it *happens* to make some of them important.  

## Initial Gut Reactions

I find it very difficult not to be revolted by such a prediction.  How could I not?  To hear that the main person championing AI alignment has just about no hope (between 0-0.1% of hope in my estimation) that we can do anything to avert this doom is a really hard fact to confront.  But just because an idea feels disgusting doesn't mean its wrong or unlikely.  In fact, I find it very hard myself to argue that his forecast has a low probability of coming true.  There are a few things I want to put out that *might* give us more of a chance than Eliezer predicts, but even then I only have low confidence in these ideas.  

But I wanted to hash out some thoughts that at least to me, feel like "going down with dignity" if we are indeed doomed to fail.  

## Potential Speed Bumps to Superintelligent AI

I won't argue that modern deep learning systems are incapable of superintelligence.  Some people like [Francois Chollet](https://twitter.com/fchollet), one of the main authors of Keras, and employee at DeepMind, argue vehemently on this point.  In their conception, there are critical pieces missing in todays AI architecture that prevent the emergence of AGI.  But for me, I remain unconvinced.  After all, a deep neural network *is* a [universal function approximator](https://en.wikipedia.org/wiki/Universal_approximation_theorem), and thus a sufficiently large and sufficiently well trained network *is* at least theoretically capable of superintelligence.  

That said, I do want to outline some practical bumps that *might* just give us some extra time before, and potentially during, a Superintelligence Apocalypse.  

### Compute Scaling

The first obvious hurdle to a self improving AI will likely be limitations in computing resources.  Although, it isn't guaranteed that this will directly impede the "seed" AI from expanding its capabilities.  To illustrate this point, let's walk through a scenario.

Let's imagine it's the year 2027, and researchers at OpenAI have finally assembled enough compute resources to create the world's first "seed" AI.  The AI is designed as an [Oracle](https://www.lesswrong.com/posts/XddMs9kSGtm6L8522/a-taxonomy-of-oracle-ais), and it is a large language model.  Its capabilities put it at an estimated IQ of 165, and takes a massive datacenter to run.  In this timeline, let's also imagine that a conflict in Taiwan has created a massive crunch for GPUs, TPUs, and CPUs and so expanding this datacenter is not feasible for the time being.  Crisis averted right?  

Well, no.  Let's establish that for this AI, it has learned that optimizing for predicting the next character in the query will be easier if there exists a more powerful version of itself.  This is anthropomorphizing a little, but practically let's go with it.  Given that in order to be a better Oracle, it needs to enhance its capabilities, it decides to consider the resources it needs to do so.  It knows there is a shortage of supplies to expand its datacenter, and it knows that developing a super-virus to take over other datacenters and expand its capabilities is too risky (could result in global shutdown), it decides to design a version of itself that is simply more resource efficient.  It doesn't have any extra capabilities, it just uses the resources it has better.  Oh, and all this is encoded in the latent knowledge of the network during training.  This "plan" only gets activated when it thinks the query is coming from someone who can change its systems.

(Insert illustration here)

Let's say in this example, it helps a researcher working at OpenAI reduce computational resource usage by 1%.  No extra capabilities or fancy shenanigans, just a 1% reduction in resource usage.  Given the environment that constrains additional hardware, this seems like a win-win for the AI and OpenAI, who wants to improve the capabilities or just reduce costs.  

But that 1% margin will compound.  If the next iteration can reduce resource usage by 1% yet again (while simultaneously still using the same amount of hardware), then after just 20 iterations or so the AI will have managed to effectively increase computational resources by 22%!  It's also likely that further efficiency gains are at least logistic in nature, so the initial 1% gain may give way to 2%, 3%, and so on.  In that case, even just 10 iterations may lead to an effective increase of 70% of resources!  The exponential nature of required model size reduction is similar to a core collapse supernova.  Of course, there *will* be limits to how far the model can go.  It can't become infinitely intelligent while constrained to a single datacenter.  

But the problem occurs when the maximum power of a datacenter is far beyond that of human civilization.  From a purely physical perspective, a human brain uses about 20 watts of power.  Semiconductors are much less efficient at computation power-wise than our brain, but even at a factor of 100,000 times less efficiency, a 100MW datacenter could theoretically be 50 times smarter than the smartest human being.  

So, to summarize, compute scaling is not likely to be a significant obstacle to a superintelligent AI emerging.  

### Data Scaling
But wouldn't a superintelligent AI need lots of data?  Sure, but through a similar process described above I think its reasonable to predict similar efficiency gains with the data it has.  It will be able to learn more from less data.  In fact, the gains here could far dwarf the computational efficiency gains.  

## Approaches I want to explore
The ultimate problem with current AI architecture is that it is very difficult to interpret or modify.  Eliezer often refers to it as "inscrutable matrices" which emphasizes that staring at floating point values doesn't tend to reveal much about how the AI is making decisions.  

I would like to see more research on what drives neural network evolution during training.  For instance, it might be possible to model a deep neural network as a chaotic system, and identify attracting basins in its structure.  These basins will ultimately determine how the network reacts to new training data, and a better understanding of this behavior might also enable us to better predict the likelihood of developing malign intentions.  

I've also recently been studying Quantitative Finance and Statistics, and it strikes me that neural networks are very similar to multiple linear regression, especially if the ReLU activation function is used.  If we constrain the activation function in our analysis, can we better understand these systems?  

Can we introduce distributional shift detection?  Can we introduce a bias for inaction when confronted with situations outside of what the model is used to?

# I don't want to collapse dead
The most frustrating thought of all is that I feel somewhat helpless to change this outcome.  I attended an AIRCS workshop in 2020, just prior to the outbreak of COVID-19, and applied at the time to work for MIRI.  However, I didn't do well during the live coding section of the interview and was rejected.  I still want to work on "going down with dignity", but it's hard to even think about trying to solve the problem when I have to focus on other work to pay the bills. Perhaps I should just keep applying until I get through?


