# Unsupervised_Machine_learning

<b>Part 1: Prepare the Data</b>

Read myopia.csv into a Pandas DataFrame.

Remove the "MYOPIC" column from the dataset.

Note: The target column is needed for supervised machine learning, but it will make an unsupervised model biased. After all, the target column is effectively providing clusters already!
Standardize your dataset so that columns that contain larger values do not influence the outcome more than columns with smaller values.
<br/>

![images/DataLoadClean.PNG](images/DataLoadClean.PNG)
<br/>
<br/>
<b>Part 2: Apply Dimensionality Reduction</b>

Perform dimensionality reduction with PCA. How did the number of the features change?
Hint: Rather than specify the number of principal components when you instantiate the PCA model, state the desired explained variance. For example, say that a dataset has 100 features. Using PCA(n_components=0.99) creates a model that will preserve approximately 99% of the explained variance, whether that means reducing the dataset to 80 principal components or 3. For this assignment, preserve 90% of the explained variance in dimensionality reduction.
Further reduce the dataset dimensions with t-SNE and visually inspect the results. To do this, run t-SNE on the principal components, which is the output of the PCA transformation.

Create a scatter plot of the t-SNE output. Are there distinct clusters?

![images/DataLoadClean.PNG](images/Reduction.PNG)
<br/>
<br/>
<b>Part 3: Perform a Cluster Analysis with K-means</b>

Create an elbow plot to identify the best number of clusters. Make sure to do the following:

Use a for loop to determine the inertia for each k between 1 through 10.

If possible, determine where the elbow of the plot is, and at which value of k it appears.

![images/DataLoadClean.PNG](images/ClusterK.PNG)
![images/DataLoadClean.PNG](images/ClusterKScatter.PNG)
<br/>
<br/>
<b>Part 4: Make a Recommendation</b>

Based on your findings, write up a brief (one or two sentences) recommendation for your supervisor in your Jupyter Notebook. Can the patients be clustered? If so, into how many clusters?