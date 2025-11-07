# Frequent Patterns Mining
- is the process of discovering associations and correlations among items in large transactional or relational data sets.
# Association Rules Mining
- it is a two-step process:
	- Find all **frequent itemsets**.
	- Generate **strong association rules** from the **frequent itemsets**.
> Frequent patterns mining and association rules mining are 2 data mining tasks that are often referred to interchangeably, since they most of time happen together in the same workflow.
# Formalization
- Let $I = \{I_1, I_2, I_3, ..., I_n\}$ be an *item set*, and $D = \{T_1, T_2, T_3, ..., T_m\}$ be set of transactions in a database where each transaction $T_i$ is a set of items such that $T_i \subseteq I$.
- Let $A$ be a set of items, a transaction $T_i$ is said to contain $A$ if $A \subseteq T_i$.
- **Association Rule** is an implication of the form $A \Rightarrow B$ where $A, B \subset I, A \cap B = \phi$.
- **Support** of association rule $A \Rightarrow B$ is the likelihood of a transaction in database to contain both $A$ and $B$.
$$support(A \Rightarrow B) = P(A \cup B)$$
- **Confidence** of association rule $A \Rightarrow B$ is the likelihood of a transaction containing $A$ to also contain $B$.
$$confidence(A \Rightarrow B) = P(B | A) = \frac {P(A \cup B)} {P(A)}$$
- A rule satisfying both a minimum **support** and **confidence** threshold is called a **strong rule**.
- A set of items is called **itemset**.
- An **itemset** with $k$ items is called **k-itemset**.
- Number of transactions containing an **itemset** is called **frequency**, **support count** or **count** of that **itemset**.
- **frequent itemset** is an **itemset** that satisfies the **minimum support** threshold.
# Frequent Itemset Problem
## The Challenge
- Mining frequent itemsets in a **large database** often generates an absurd amount itemsets that satisify minimum **support** (especially if it is set to a low value)
- *Why?* if an itemset is frequent, then every subset of it is also frequent.
- Say we got an frequent itemset of 100 items, that will make all its subsets frequent too, the amount of those subsets are all the combinations of this itemset's items, this will be:
$$\binom{100}{1} + \binom{100}{2} + \binom{100}{3} + ... +\binom{100}{100} = 2^{100} -1$$
- Thats a huge number for a relatively small amount of items!
## The Solution
- 
# Applications
## Market Basket Analysis
- this is the process of customer buying habits by finding associations between the different items that customers place in their “shopping baskets".
- can help retailers develop marketing strategies by gaining insight into which items are frequently purchased together by customers.