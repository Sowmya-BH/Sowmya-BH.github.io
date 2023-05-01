---
name: PCA Scree Plots for Correlated and Uncorrelated Variables:
tools: [Python, Altair, Matplotlib]
image: assets/json/Dashboard_primary.json
description:Behavior of Scree Plots using Altair!-Sowmya Bhupatiraju, Bennett Custer, Job Monita
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Uncovering the Optimal Principal Components: The Power of PCA Scree Plots with Cumulative Variance for Correlated and Uncorrelated Variables:
In this visualization, we explore the Behavior of Scree Plots for Correlated and Uncorrelated Variables

<vegachart schema-url="{{ site.baseurl }}/assets/json/Dashboard_primary.json" style="width: 100%"></vegachart>

**Introduction:** We have a large dataset of 2.8 million accident records with 47 attributes that exploded to 104 columns after data engineering. Given the size and complexity of the dataset, we explored the possibility of applying PCA (Principal Component Analysis) which is a widely used statistical method for reducing the dimensionality of large datasets while retaining as much of the original information as possible.

Moreover, Applying PCA to our dataset is useful to explore the variability of the attributes - we could also gain insights into how different attributes are related to each other and how they contribute to the overall variance in the data.

One way to visualize the results of a PCA is by creating a scree plot.It works by identifying the most important features in the data and combining them into a smaller set of new features called principal components

**Understanding Scree Plots:**
A scree plot is a graphical tool that is commonly used in Principal Component Analysis (PCA) to help determine the optimal number of principal components to retain for subsequent analysis. In a scree plot, the eigenvalues of each principal component are typically plotted in descending order on the y-axis, and the principal components are plotted on the x-axis.

**Visualizing the Contribution of Each Principal Component:**
A common practice is to plot both the eigenvalues and the cumulative variance explained by the principal components on the scree plot. This allows us to visualize the contribution of each principal component to the overall variance of the dataset.

**Determining the Optimal Number of Principal Components:**
We can use the cumulative variance explained to determine the optimal number of principal components to retain for further analysis. Generally, we want to retain enough principal components to capture at least 80-90% of the total variance in the data.

**The Behavior of Scree Plots for Correlated and Uncorrelated Variables**
In a scree plot, the eigenvalues are plotted on the y-axis and the principal components on the x-axis. A common practice is to plot both the eigenvalues and the cumulative variance explained by the principal components. The scree plot allows us to visualize the contribution of each principal component to the overall variance of the dataset.

<vegachart schema-url="{{ site.baseurl }}/assets/json/Dashboard_primary.json" style="width: 100%"></vegachart>

 
## 1. Plot1 - Behaviour of Scree Plots for Correlated Variables :
<vegachart schema-url="{{ site.baseurl }}/assets/json/Dashboard_primary.json" style="width: 100%"></vegachart>
<vegachart schema-url="{{ site.baseurl }}/assets/json/bfro_sightings.json" style="width: 100%"></vegachart>


When dealing with correlated variables, PCA can help to identify the underlying structure of the data and remove redundancy, by transforming the variables into uncorrelated principal components. The uncorrelated principal components provide a more accurate representation of the true underlying structure of the data, and can be used to build more accurate models. Therefore, when creating a scree plot for correlated variables, we expect to see a rapid decline in eigenvalues and a slower decline in cumulative variance explained as we move from the first to the last principal component.
For correlated variables, the eigenvalues and cumulative variance explained are expected to decline at a slower rate as the number of principal components increases. This is because correlated variables contain redundant information, and PCA needs to remove this redundancy by grouping them together in fewer principal components.

**Code Walkthrough:** 
 The Dashboard consists of a rect plot for correlated variables, as part of a larger layered plot that includes a scree plot with cumulative variance. The rect plot shows the explained variance for each principal component (PC), with the x-axis representing the PC component number and the y-axis representing the amount of explained variance. The color of each rectangle corresponds to the PC component number, with a tealblues color scheme used. Also a point plot is overlaid on the rect plot to faciltate the elbow method of finding the number of principle components. 
 The code also includes text annotations for each rectangle, displaying the amount of explained variance as a floating point number with 3 decimal places. Additionally, the code includes a scree plot with cumulative variance, represented as a line plot. This plot displays the cumulative amount of explained variance for each PC component, allowing users to identify the optimal number of PCs to include in their analysis.
 Overall, this code is part of a dashboard that enables users to visualize the results of a principal component analysis for both correlated and uncorrelated variables. By using scree plots with cumulative variance, users can determine the optimal number of PCs to include in their analysis, helping to reduce the dimensionality of their data while retaining as much information as possible.
 The use of the "tealblues" color scheme for the visualization is a matter of personal preference and design choice. Tealblues is a color scheme that blends shades of teal and blue together to create a soothing and cohesive color palette.When used in data visualizations, tealblues can help to create a sense of continuity and balance, as well as to convey a sense of professionalism and sophistication.

## Plot2 - Behaviour of Scree Plots for UnCorrelated Variables:
For uncorrelated variables, the eigenvalues and cumulative variance explained are expected to decline at a similar rate as for correlated variables. This is because uncorrelated variables already capture the maximum amount of information, and PCA does not need to remove any redundancy. *Linear Decline in Cumulative Variance* :However, in most cases, the cumulative variance plot may show a linear trend. This is because each principal component contributes equally to the overall variance of the data, and none of them are redundant.

<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboard_secondary.json" style="width: 100%"></vegachart>

Conclusion
The use of scree plots and cumulative variance is an effective method to visualize and analyze the contribution of each principal component to the overall variance of the dataset. By understanding the behavior of scree plots for correlated and uncorrelated variables, we can determine the optimal number of principal components to retain for subsequent analysis. Generally, we want to retain enough principal components to capture at least 80-90% of the total variance in the data



*Challenges: One potential challenge of using PCA is that it can be computationally expensive for large datasets like ours. Additionally, the effectiveness of PCA may be limited by the nature of the data and the relationships between the variables.*

*Next Steps: Our next steps will be to run some experiments to determine if PCA is a viable solution for our dataset. We will also explore other dimensionality reduction techniques and compare their performance to that of PCA. Ultimately, our goal is to find the best approach for reducing the dimensionality of our dataset while retaining as much information as possible*



<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/Sowmya-BH/Sowmya-BH.github.io/blob/main/_data/csv_data_correlated.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Sowmya-BH/Sowmya-BH.github.io/blob/main/python_notebooks/Untitled15.ipynb" text="The Analysis" %}
</div>


