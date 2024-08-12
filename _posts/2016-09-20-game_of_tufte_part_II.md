---
layout: post
title: A Games of Tufte
subtitle: Part II
date: 2016-09-20
author: Mirko Mazzoleni
categories: fun
tags: visualization R
description: Visualization of Game of Thrones battles
thumbnail: /assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-49-1.svg
---


The [first part]({% post_url 2016-08-06-game_of_tutfe %}) of the exploratory data analysis of the Games of Thrones dataset hosted at [Kaggle](https://www.kaggle.com/mylesoneill/game-of-thrones) dealt with data understanding and cleaning. This second post digs further into visualization, unveiling interesting aspect of the battles.

The entire code for this post can be found [here](https://github.com/MirkoMazzoleni/MirkoMazzoleni.github.io/blob/master/assets/code/2016-08-05-game_of_tutfe.Rmd).

---

## More questions

This section highlights and depicts more questions that arise from the data.

### Major deaths and captures rate

The following plot shows how the major deaths and captures are spread across the battle succession across the years. The major number of them happen in the year $$299$$, were almost each battle generates a major death. In the year $$300$$, it seems that no more major characters die in battle, with only one of them captured. It can bee seen that the majority of deaths and captures happen in the *Riverlands* and in the *North*. From the graph emerges that the cumulated number of deaths is always higher than the cumulated number of captures, symptom that the soldiers prefer to kill rather than take prisoners.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-39-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


### Number of battles won by each commander, when attacking

The plots shows the number of won battles by each king, thanks a specific commander, with a different color for each region where the battle was fought. It can be noticed that the Greyjoy's fought almost in the North, while the Lannister's and the Stark's fought all across Westeros. Gregor Clegane (the Mountain) is the commander who won more battles. Folks with no king fought only in the Riverlands.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-40-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


### Type of battles won  by each king, when attacking

The plots shows the number of won battles by each king, thanks a specific tactic, with a different color for each year in which the battle was fought. We can see that Robb Stark preferred to fight with ambushes, while the Lannister's with pitched battles since the year $$299$$, and  with sieges from the year $$300$$.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-41-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Number of battles fought in summer and winter

The plots shows the number of won battles by each king fought in summer (1) or winter (0), with a different color for each year in which the battle was fought. The poor Robb Stark died during the Red Wedding in year $$299$$, so he did not fight any battle during year $$300$$. We can see that winter has finally come in year $$300$$. Brace yourself!!

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-42-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>



### King vs. King

This plots shows the preferred king versus whose each king fought his battles.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-43-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


By inspecting the plot, it seems strange that *Balon/Euron Greyjoy* attack himself. The battle considered is the *Sack of Torrhen's Square*.  In fact, the defender king would be *Bran Stark*, since Robb is dead. I make the decision to substitute the defender king with *Robb Stark* indicating that the defenders are the Stark's.

```
                      name       attacker_king       defender_king
13 Sack of Torrhen's Square Balon/Euron Greyjoy Balon/Euron Greyjoy
```

The correct plot is the following. We can see that Robb Stark fought mainly versus Joffrey Baratheon and viceversa. The troops without a king fought each other. Stannis fought first versus his brother Renly and then versus the Lannister's.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-45-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


The previous plots do not change except for those of **Question Q4**, for which the answer remains unchanged. The correct plots are reported here.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-46-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


### Battle success given army forces

The plot seems to suggest that there is a linear relationship between the size of the attacking army and the size of the defending one, maybe due to information that each rival part has about the other. It seems that after a certain attacker size threshold, the loss is more probable. Maybe is difficult to coordinate such many men, versus a numerous defending army. Having a bigger army, therefore, does not mean to win for sure.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-47-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>



## Graph of Thrones

The following section (which owes a lot to the Kaggle's user [ColinFraser](https://www.kaggle.com/colinfraser/d/mylesoneill/game-of-thrones/battles-investigation)), deals with the use of graph algorithms to analyse the social relations between houses, during the battles. By using the variables *attacker_i* and *defender_i*, with $$i=1\dots 4$$, is possible to build a graph which vertices are the house names, and an edge is present between two of them if a battle has been fought between the two houses.

The direction of the edge is from a loser to a winner, and a darker edge color show how many battles are present with that edge direction (that is, with that battle outcome): the darker, the higher. It can be seen that the Frey's fought with many houses and won many battles, and how the Nigth's Watch are isolated from the rest of the world. Interestingly, even the Tyrell's fought only versus the Greyjoy's. Both the Tully's and the Stark's won more battles versus the Lannister's with respect to how many they lost versus them, but for the latter house, they are behind the Greyjoy as direct matches won. Interesting is the loop around house Baratheon, which represent the fights of Stannis versus his brother Renly.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-49-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


### Houses which won most

By counting the in-degree (number of battles won) and the total degree of a node (number of battle fought), is possible to compute how the house performed in terms of efficiency. Since the number of battles for each house is small, we employ the *Laplace correction* to correct for the small sample size:

$$p(win)=\frac{n+1}{n+m+2}$$

where $$n$$ is the number of won battles, $$m$$ is the number of lost battles and $$p(win)$$ is the probability to win a battle.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/posts/2016-08-06-games_of_tufte/unnamed-chunk-53-1.svg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>



### Most powerful houses

By using the **PageRank** algorithm, it is possible to assign a value to each node in the graph. In the case of Google, each node is a document, a web page, and the edges are links between pages. If a page has an incoming link from an important page, that link carries more value. In our context, we suppose this mean that win against the Lannister's, for example, carries more value than to win against the Glover's, and the algorithm is able to exploit this based on the graph structure of won and lost battles (again, incoming and outcoming edges).
From Wikipedia:

> The PageRank algorithm outputs a probability distribution used to represent the likelihood that a person randomly clicking on links will arrive at any particular page

Adapting the reasoning to our case, we can think of it as in terms of houses and battle outcomes. By walking through the Markov network following edge direction (which is from loser to winner), we discover the stationary probability distribution of the Markov chain. This represent the probability that, starting from a house at random and moving in the direction of battles outcome, after a while we expect to celebrate the victory of a house for that invariant amount of time.

The results show that the house Frey is the most powerful, and the $$11.7%$$ of times we expect to come to House Frey having a party for their victory.


```
                        Frey                   Lannister
                  0.11706463                  0.10476410
                      Bolton                   Baratheon
                  0.09134930                  0.08013144
               Night's Watch                     Greyjoy
                  0.06422775                  0.04357728
                       Stark          Brotherhood without Banners
                  0.04331037                  0.04023057
                     Bracken                       Tully
                  0.04023057                  0.03713693
                       Darry                    Karstark
                  0.03713693                  0.03440543
                     Mormont                      Glover
                  0.03440543                  0.03440543
            Brave Companions                   Mallister
                  0.02823198                  0.02823198
                   Free folk                      Tyrell
                  0.02823198                  0.02823198
                   Blackwood                      Thenns
                  0.02823198                  0.02823198
                      Giants
                  0.02823198
```

```r
# It has to output 1, being a probability distribution
sum(pr$vector)
1
```


# Acknowledgements

  * [Some analysis of Game of Throne data](https://www.kaggle.com/sergeycherkasov/d/mylesoneill/game-of-thrones/test-test) - Sergey Cherkasov
  * [Exploratory Analysis and Predictions](https://www.kaggle.com/shaildeliwala/d/mylesoneill/game-of-thrones/exploratory-analysis-and-predictions) - Shail Deliwala
  * [Systematic Analysis on GoT Battles](https://www.kaggle.com/gowrishankarin/d/mylesoneill/game-of-thrones/analysis-on-battles) - Gowri Shankar
  * [Battles investigation](https://www.kaggle.com/colinfraser/d/mylesoneill/game-of-thrones/battles-investigation) - ColinFraser
  * [Tufte in R](http://motioninsocial.com/tufte/) - Lukasz Piwek
