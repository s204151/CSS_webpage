---
title: Text analysis
prev: network-analysis
---


Throughout the dataset, question body text, question title text and answer body text is tokenized and stopwords are removed. Bi-grams are also found for semi-contextual visualization of discussed topics in different communities using WordClouds.


To measure importance of terms, TF-IDF is used. The (non-normalized) Term Frequency is used,

$$ \text{TF}(t,d) = f_{t,d} $$

Where f_{t,d} is simply the term count in document. The Inverse Document Frequency is calculated as 

 $$ \text{IDF}(t,D) = log(\\frac{N}{1 + n_t}) + 1 $$

where $n_t = |{d \\in D: t \\in d}|$ is the number of documents $D$ where the term $t$ appears at least once. N is total number of documents in corpus. The logbase used is in our case log10.

We then tried comparing our results when weighting question titles higher than when calculated using TF-IDF, since a notion we had was that good question titles might contextualize the problem quite well but not be weighted very high when using the ordinary TF-IDF since question titles are short compared to body text. Thus we compare our results when using modified/reweighted TF-IDF,

$$ 
\text{TF-IDF}_{\text{modified}}(t,d,\alpha) = 
\begin{cases}
        \text{TF-IDF}(t,d) \cdot \alpha &  \textbf{if} \ \   t \in Q_{\text{title}} \\
        \text{TF-IDF}(t,d) & \textbf{else}
\end{cases}
$$
Where we let $\alpha = 3$, which is the equivalent to adding 2 more artifical term counts for every term in question titles. So $\alpha$ is only mulitipled for term occurences inside $Q_{title}$. It is also noted that TF and IDF is calculated community-wise, not document-wise, as we are interested in finding largest differences in communities.



