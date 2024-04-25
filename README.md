<p align="center">
<img src="https://github.com/ArthurSpirling/LargeLanguageArguments/blob/main/LLM_banner_2.jpg" width = "800" title="LLM politics image">
</p>


# Large Language Models Can Argue in Convincing Ways About Politics

This is the public facing project site for the work by [Alexis Palmer](https://lexipalmer13.github.io/) and [Arthur Spirling](http://arthurspirling.org/) on Large Language Models (LLMs) and argumentation. Specifically, their paper "Large Language Models Can Argue in Convincing Ways About Politics, But Humans Dislike AI Authors: implications for Governance".  That paper is [now published](https://www.tandfonline.com/doi/full/10.1080/00323187.2024.2335471) (online) as

> Palmer, A., & Spirling, A. (2024). Large Language Models Can Argue in Convincing Ways About Politics, But Humans Dislike AI Authors: implications for Governance. Political Science, 1–11. https://doi.org/10.1080/00323187.2024.2335471 

The abstract for the paper is

> All politics relies on rhetorical appeals, and the ability to make arguments is considered perhaps uniquely human. But as recent times have seen successful large language model (LLM) applications to similar endeavours, we explore whether these approaches can out-compete humans in making appeals for/against various positions in US politics. We curate responses from crowdsourced workers and an LLM and place them in competition with one another. Human (crowd) judges make decisions about the relative strength of their (human v machine) efforts. We have several empirical ‘possibility’ results. First, LLMs can produce novel arguments that convince independent judges at least on a par with human efforts. Yet when informed about an orator’s true identity, judges show a preference for human over LLM arguments. This may suggest voters view such models as potentially dangerous; we think politicians should be aware of related ‘liar’s dividend’ concerns.

You can find a preprint [here](https://github.com/ArthurSpirling/LargeLanguageArguments/files/15013693/preprint.pdf) and the Supporting Information [here](https://github.com/ArthurSpirling/LargeLanguageArguments/files/15013674/SI_LLM.pdf)



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

### Feedback and thanks
Patrick Chester, Yaoyao Dai and Philip Resnick provided very helpful comments on an earlier version of the paper.  We  thank audiences at APSA, Meta, MPSA and the Text as Data conferences for feedback.  Two anonymous referees helped improve our paper considerably.

Though now published, your comments are still very welcome: please send us an email, or open an issue here. 


