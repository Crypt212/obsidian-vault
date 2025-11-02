- **Dimensionallity reduction** transforms high-dimensional data into a meaningful representation in a lower-dimensional space.
- Benefits include improved visualization, computational efficiency, and better model performance by eliminating noise and redundancy while preserving essential patterns.

# Examples
**Example 1: Customer Data**
- **Original:** 50 features (age, income, number of purchases, browser type, time on site, etc.)
- **After Dimensionality Reduction:** 3 main "concepts":
    1. "Spending Power" (combines income, purchase value)
    2. "Engagement Level" (combines time on site, frequency)     
    3. "Demographic Profile" (combines age, location)
# Common Techniques You Might Encounter
- **PCA (Principal Component Analysis)** - finds the directions of maximum variance
- **t-SNE, UMAP** - great for visualization
- **Feature Selection** - simply removing unimportant features (the simplest form)