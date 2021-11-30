# t-SNE
t-Distributed Stochastic Neighboring Embedding Algorithm(t-SNE) is a non linear dimensionality reduction technique. It visualizes high-dimensional data by giving each datapoint a location in a two or three-dimensional map. It is particularly important for high-dimensional data that lie on several different, but related, low-dimensional manifolds, such as images of objects from multiple classes
seen from multiple viewpoints. t-SNE is capable of capturing much of the local structure of the high-dimensional data very well, while also revealing global structure such as the presence of clusters at several scales.

Key points:
1. t-SNE can generate differnet layouts for each experimental run

Reasons: At the beginning, t-SNE initializes the low dimensional Y values randomly. At each experimental run, this Y values can be initialized by different random numbers and may eventually generate different layout

Solution: Before running the code, we can set the random seed fix. So at every new experiment, it will get the same random Y values and generate same layouts.


2. Different perplexity can produce different layouts

In t-SNE, perplexity can be interpreted as a smooth measure of the effective number of nearest neighbors. Any particular value of σ_i induces a probability distribution, P_i, over all of the other datapoints. This distribution has an entropy which increases as σ_i increases. SNE performs a binary search for the value of σi that produces a Pi with a fixed perplexity that is specified by the user. 

Observation: 
-- If the dataset are large, perplexity between 30-50 may work better
-- If the dataset are dense and small, perlexity between 10-30 may work better

3. Application
-- Effective algorithm to embed high dimensional data to low dimensional space
-- Can be used to measure the quality control of data
-- Can be utilized to check how data are distributed in high dimensional space