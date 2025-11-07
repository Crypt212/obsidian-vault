- this is an algorithm used for search association rules in a frequent itemset.
- **Apriori property**: All non-empty subsets of a frequent itemset are also frequent itemsets.
# History
- this algorithm was proposed by R. Agrawal and R.Srikant in 1994 for mining **frequent itemsets** for boolean **association rules**.
- the name of the algorithm is based on the fact that it uses prior knowledge of frequent itemset properties.
# How it works
- it employs an iterative approach known as **level-wise search**, where k-itemsets are used to explore (k+1)-itemsets, starting by k=1, there are 2 steps involved in each iteration:
	- **join**: to find the new set of k-itemsets, called $L_k$, we first join $L_{k-1}$ with itself, this is done by joining every two distinct itemsets from $L_{k-1}$ that has first $k-2$ items in common, there result set of joining $L_{k-1}$ with itself is the set of candidate k-itemsets called $C_{k}$
	- prune: $C_k$ could be the next set of k-itemsets in the iteration, but it would be so huge, thanks to the **apri