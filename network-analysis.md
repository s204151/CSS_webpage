---
title: Network analysis
prev: data-description
next: text-analysis
---

To get more information about the users i.e. nodes, the StackOverFlow API is used. Traffic is limited to 300 requests á day and information from up to 100 users can be retrieved per request.

> It is noted that a substantial amount of accounts no longer exist. For example, the user [100027](https://meta.stackoverflow.com/users/100027/) exists, while [100157](https://meta.stackoverflow.com/users/100157/) no longer exists. This means that out of the 30133 nodes in our network, only additional information pertaining to 17327 of them could be retrieved.
Retrieved features that are added as attribute nodes are username, location (might not be disclosed for all users), user_type (i.e. 'moderator' or just normal 'registered' user), badges_earned_today and reputation_today at the date 5/1/2023.

The directed-graph is the first thing created, nodes are users and a directed connection is when a person answers another persons question (also weighted such that multiple answers from one person to another are counted). 





<img src="/images/Network.png"/>