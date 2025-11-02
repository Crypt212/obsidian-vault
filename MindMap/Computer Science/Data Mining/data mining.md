# Terminology
- **Data**: Raw and unprocessed facts, numerical values, or other data that can be stored and processed in a computer system. Has some formats:
    - Operational/Transactional data: a set of records of events, transactions or other data that happen during a period of time.
    - Non-Operational/Non-Transactional data: data that is not used for operational or transactional purposes.
    - Metadata: data about the data, such as its structure, format, and content.
- **Information**: Ideas that hold meaning, can be concluded or inferred from patterns, associations or relationships among data.
- **Knowledge**: Information that has been acquired by a person, group or system, and is used to make predictions, decisions or to support decision-making.
# Why study data mining?
- Data is growing big and fast, while users demand more sophisticated information from their data.
- Data mining is a new field in computer science, which is used to extract useful information from data and to make predictions about the future.
# Performing data mining on databases
- [[SQL]] queries are not decent enough to extract useful information from data, data mining helps with that.
- Traditional database access is performed using a well-defined queries stated in a language (such as [[SQL]]), the output data is a subset of the database that satisfies the query, but it can also be an extracted view or may contain aggregations.
- Data mining access to DB differs in some ways:
    - Queries might not be well-formed or precisely stated.
    - Data accessed is usually a different version of the original database data (having undergone cleaning and other processing to be mined).
    - Output is not a subset of the database, but a different view of the data.

# Knowledge Discovery in Databases
- **KDD** is a process of discovering **valid**, **novel**, **useful** and ultimately **understandable** patterns in massive databases, these patterns are the information.
    - **valid**: the patterns must be statistically significant, meaning they hold true for most future data, not just a fluke.
    - **novel**: the patterns must hold new, important discoveries, not already known, trivial facts.
    - **useful**: the patterns must be useful for decision making, not only for reporting.
    - **understandable**: the patterns must be easy to understand and explain.
- **KDD** Process:
    [1] - **Learning the application domain** and deciding prior knowledge and goals.
    [2] - **Creating a target data set** by selecting the most important records from the database.
    [3] - **Data cleaning and pre-processing**, such as removing noise and outliers and deciding strategies for handling missing values.
    [4] - **Data reduction and transformation** using dimensionality reduction and transformation methods to reduce the number of variables and improve the quality of the data.
    [5] - **Choosing tasks of data-mining** to decide the goal of the **KDD process**.
    [6] - **Choosing the data mining algorithm** to perform the task.
    [7] - **Data mining** using the chosen algorithm.
    [8] - **Pattern evaluation and knowledge presentation**, with possibile return to any of steps 1-7 if needed.
    [9] - **Use of discovered knowledge for decision making**.

# Data Mining Tasks
- The tasks perform by data mining can be divided in two categories:
    - **Descriptive Mining**: used for summerizing or characterizing general properties of data in data repository (the "What happened?"). Examples:
        - Clustering, Association Rule Mining, Summarization.
    - **Predictive Mining**: used for deducing or inferring patterns from data for predicting future data. (the "What will happen?"). Examples:
        - Classification, Regression, Anomaly Detection.

## Association Rule
- Aims to extract the interesting correlations and frequent patterns among sets of items in a transactional database.
- Some algorithms: [[FPGrowth]], [[Apriori]].
## Classification
- Builds a model that creates predefined generalized classes from *training data set* (called "supervied learning") in order to automatically predict the class or category to which future data belongs based on similarity of attributes.
- Some algorithms: [[Decision Trees]], [[k-Nearest Neighbors]].
## Clustering
- The process of grouping existing data according to their similarities (similar to classification), but not with predefined classes, instead the classes (clusters) are formed based on the similarity of current existing data points.
- Some algorithms: [[k-Means]], [[DBSCAN]].
## Outlier Detection
- The process of identifying data points that deviate from the rest of the data classes or clusters, where every cluster or class has a boundry expected behaviour beyond which data points deviate, these boundries and data that deviate from them are both called outliers.
- Causes for outliers can be:
    - malicous activities (e.g., a fraud, cyber attack).
    - change in the environment or system.
    - instrumentation error (e.g., a faulty sensor providing incorrect readings).
    - human error (e.g., a human error in data entry).

