---
layout: post
title:  "The Journey Begins"
date:   2017-05-18 08:59:14 -0700
categories: blog
---
Some time ago, I started collecting Dota 2 match data, with the intent to create a predictive model for match victories. After putting the project aside and coming back to it multiple times over the last couple years, I finally have something that may start producing interesting results. I figured now was a good time to start sharing what I am doing, and what I am finding. 

My goal from the begining has been to try and answer a relatively simple question. How much is the outcome of a Dota 2 match determined by draft choices? Without some statistical analysis, this is not an easy question to answer. Obviously, individual player skill has a significant role in determining match outcomes, that's what makes the game interesting. However, if two teams are perfectly equal in skill, their choice of heroes may arguably determine the game. It is my goal to quantify the advantage, or disadvantage, each team has based on their draft choices.

Thankfully Valve makes Dota 2 match histories publically available, so it is easy to collect a large amount of match data. Since the question I am trying to answer deals with choices players make before the game technically begins, there are specific variables I intend to focus on first. For instance, how many carry or support heroes each team drafts, or how many stuns each team has. Essentially anything I can know about a team before the match begins. If these variables are used to create a predictive model, it should be possible to determine the probability of either team winnning. This is exactly what I have done, and intend to continue to refine.

My initial results have been modest, but promising. Overall, the model was able to predict ~58% of matches correctly. This is even less impressive when you know that ~53% of all matches are won by the radiant team... However, not all matches are created equal. For most matches, the model predicts each team has a roughly 50% probability of winning, which could be interpreted as each team drafting equally, leaving the result of the match up to player skill and in game actions. Where the model becomes intesting is when the teams do NOT draft equally. There are many matches where the model was able to predict the winner with 60-80% probability. The distribution of predicted win probabilities for the radiant team can be seen below.

![Radiant Win Histo](dotaseer.github.io/assets/radWinHisto_18May17.png)

These first findings show that it is possible to some degree to predict the outcome of a Dota 2 match. From here on out, there are a few things I am planning on doing. First and foremost is to work on increasing the accuracy of the model. I also plan on adding a page to this site which will summarize the findings of the model as it progresses. There are also a large number of smaller questions I intend to try and answer such as "What is the ideal combination of Ranged/Melee heroes?", "How important are support heroes?", or "How imporatant are base starting stats (Str/Agi/Int)?". If things go well, and I feel adventurous, I may even attempt to create a drafting tool which will show users the probability of winning for various draft combinations.

Things are very much in their infancy at this point, but if you find this at all interesting, please check back later to see how things progress. Feel free to send any questions or comments to the email listed at the bottom of the page.


