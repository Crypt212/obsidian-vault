# Frequent Patterns Mining
- is the process of discovering associations and correlations among items in large transactional or relational data sets.
> Frequent patterns mining and association rules mining are 2 data mining tasks that are often referred to interchangeably, since they most of time happen together in the same workflow.
# Formalization
- Let $I = \{I_1, I_2, I_3, ..., I_n\}$ be an *item set*, and $D = \{T_1, T_2, T_3, ..., T_m\}$ be set of transactions in a database where each transaction $T_i$ is a set of items such that $T_i \subseteq I$.
- Let $A$ be a set of items, a transaction $T_i$ is said to contain $A$ if $A \subseteq T_i$.
- An **Association Rule** is an implication of the form $A \Rightarrow B$ where $A, B \subset I, A \cap B = \phi$.
- A rule $A \Rightarrow B$ has a two properties:
	- **support**: the likelihood of a transaction in database to contain both $A$ and $B$. 
$$support(A \Rightarrow B) = P(A \cup B)$$
	- **confidence**: the likelihood of a transaction containing $B$ to also contain $A$.
$$confidence(A \Rightarrow B) = P(B | A)$$
# Applications
## Market Basket Analysis
- this is the process of customer buying habits by finding associations between the different items that customers place in their “shopping baskets".
- can help retailers develop marketing strategies by gaining insight into which items are frequently purchased together by customers.