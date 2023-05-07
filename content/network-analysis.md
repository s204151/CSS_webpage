---
title: Network analysis
prev: data-description
next: text-analysis
---

The directed-graph is the first thing created, nodes are users and a directed connection is when a person answers another persons question (also weighted such that multiple answers from one person to another are counted). 

The communities are detected using Louivain-method, and visualized with netwulf:
<img src="/images/Network.png"/>
In the image, it is shown that 1079 communities has been created where each represents a color. On the outskirt of the image there are also nodes but without edges, this must mean that they are questions which hasn't been answered, but Louivains-method was still able to categorize them into communities. This must be based on the tokens they contain which can be read more about on the next page.

Looking closer at the modularity, it is calculated as 0.25. The Wald 95% CI for the expected modularity in a sampled community is 0.25 +- 0.0036. Therefore a non-parametric boostrap with N = 1000 is calculated and a 95% CI found using quantiles 2.5% and 97.5% quantiles: [0.153, 0.389]

<img src="/images/Bootstrap.png"/>

* Since our 95% non-parametric bootstrapped confidence interval is [0.153, 0.389], which is both positive but not very high. Statistically, we can assess that underlying distribution of the sampled the social network is not tightly knit, nor very sparse as both numbers are not very high and both are not negative.
* Modularity is significantly different from 0. 
* Does not contain 0 in confidence interval


(ADD MORE INFO HELP)

The degree distribution shows how many nodes have a particular degree. The highest degree in this network is 775, but a cutoff point of 30 has been chosen for the plot because of the sparsity of degrees above this point(Very few nodes have more than 30 edges). The degree distribution is visualized below:

<img src="/images/Degree.png"/>
In the image, there can be seen some counts with 0 degrees. This proves that there are questions which hasn't been answered in the network. Other than that there are a lot of questions who have received few answers, and it decreases with the questions receiving answers. This is normally due to a potential right answer appears, so there would be no need to answer a question where someone else already answered something that seems right.


> It is noted that a substantial amount of accounts no longer exist. For example, the user [100027](https://meta.stackoverflow.com/users/100027/) exists, while [100157](https://meta.stackoverflow.com/users/100157/) no longer exists. This means that out of the 30133 nodes in our network, only additional information pertaining to 17327 of them could be retrieved.
Retrieved features that are added as attribute nodes are username, location (might not be disclosed for all users), user_type (i.e. 'moderator' or just normal 'registered' user), badges_earned_today and reputation_today at the date 5/1/2023.

>To get more information about the users i.e. nodes, the StackOverFlow API is used. Traffic is limited to 300 requests á day and information from up to 100 users can be retrieved per request.