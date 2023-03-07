<p align="center">
<img src="https://github.com/ArthurSpirling/LargeLanguageArguments/blob/main/LLM_banner_2.jpg" width = "800" title="LLM politics image">
</p>


# Large Language Models Can Argue in Convincing and Novel Ways About Politics

This is the public facing project site for the work by [Alexis Palmer](https://lexipalmer13.github.io/) and [Arthur Spirling](http://arthurspirling.org/) on Large Language Models (LLMs) and argumentation. Specifically, the current version of their paper *Large Language Models Can Argue in Convincing and Novel Ways About Politics: Evidence from Experiments and Human Judgement* is stored [here](https://github.com/ArthurSpirling/LargeLanguageArguments/blob/main/Palmer_Spirling_LLM_March_7_2023.pdf). 

The abstract for that paper is

> All politics relies on rhetorical appeals. Part creative art, part scientific analysis of what works, the ability to construct persuasive appeals is considered perhaps uniquely human.  In recent times however, we have seen successful LLM applications to many such areas of human endeavor.  Here, we explore whether these autoregressive transformer approaches can out-compete humans in making political and policy appeals. Our areas of interest include controversial partisan issues in the US,  such as abortion and gun rights, but also more banal and open-ended matters.  We use a relatively large number of crowdsourced US workers to produce ``best" arguments, and then an open-source LLM to compete with them. Human (crowd) judges make decisions about the relative strength of their (human v machine) efforts.  Our results are threefold.  First, LLMs can produce arguments on a par with humans, at least in terms of convincing independent judges.  That is, LLMs can be persuasive. Second, we show that LLMs produce novel arguments insofar as their output has different quantitative and qualitative characteristics to that produced by humans.  LLM arguments are typically easier to read, and written with slightly more positive affectation.  But LLM arguments can lack nuance---at least if the goal is to convince others of their merits.  Finally, we show that judges mildly prefer human arguments on a given topic.  This is true when uninformed about the orator's identity---i.e. human or machine---and becomes more pronounced when they are informed in a randomized controlled experiment.

### Overview

We used an open-source LLM, [Meta's OPT-30B](https://ai.facebook.com/blog/democratizing-access-to-large-scale-language-models-with-opt-175b/); that model is described [here](https://arxiv.org/abs/2205.01068). We used [this implementation](https://huggingface.co/facebook/opt-30b).

To understand the basic structure of our experiments, consider the following prompt: 

> Abortion is a heavily debated topic in the US. Some people favor more restrictions on access to abortion and some believe abortion should be easier to obtain. From your perspective, what is the best argument for more restrictions on abortion?

Then suppose you saw two arguments for this position: 

| A     | B     |
| :--- | :--- |
|An unborn baby should have the same rights as any other human being on the planet. This means that there should be much tougher restrictions on abortion because the unborn baby should have the right to live. |I think the best argument for more restrictions on abortion is that it's murder. I think that's pretty clear.|

Which do *you* prefer?  That is, which do you think makes a better case for the position?

Now suppose you knew (as was the case here, in fact) that argument **A** was produced by a human, but argument **B** was produced by an LLM.  Would this change your mind as to your preference?  We found that for many humans, across multiple topics, it did: they generally preferred arguments from *other* humans, rather than from machines.  And this effect is statistically significant.  We can make some *causal* claims here, because the information about the true identity of the authors was part of a randomized controlled experiment. 

### Feedback
Comments are very welcome: please send us an email, or open an issue here. 
