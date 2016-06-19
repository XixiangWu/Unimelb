### Data mining
* Data mining, machine learning, statistical learning
    Learning from data 

* Unsupervised (Descriptive) vs 
    Supervised (Unsupervised)

* Supervised Learning: some prior knowledge about what you want to find out (target variable) 

* Exploratory vs Explanatory

#### Data mining - unsupervised
* Provide broader view to get the “data landscape” or “interesting recurrent pattern”

* Association rule
    * Generate rules based on observations of the data-set

* Clustering
    * Groups data into sets of observations or clusters

> ### E.g.
* IF a patient is over 70
    * AND they have history of liver problems
    * AND they have low socio-economic status
        * THEN they are 70% likely to be diabetic


* <font color="green">Advantages:</font>
    * Easy to understand, actionable, good for large data
* <font color="red">Disadvantages:</font>
    * Categorical only, time-consuming to generate, many rules means priority to be worked out

#### Clustering

<p align="center">![C-73A84747-EA24-4BCF-B613-2B371AA78B6D.png](resources/D0D5B4A8430E1F3C2B5A35074A873444.png)</p>
K-Means Clustering
<font color="green">Advantages</font>: flexible, hierarchical approach possible
<font color="red">Disadvantages</font>: setting initial cluster number, can be slow, size limits

#### Data mining - supervised
* Supervised = using historical patterns to predict what will happen next…

* Class = $f(v1, v2, v3)$

* Regression
    * Mathematical model to predict a continuous response variable

* Classification
    * Allows observations to be assigned to different categories

### Classification

#### KNN Classification
* The class of an unknown instance is the majority of k closest sample/training data.
* Lazy method, the classifier model is the whole dataset.
<p align="center">![C-858FBAE1-18B3-43A0-A89D-D66FC556850A.png](resources/69A6B0658818E925EC279D5383A73D5A.png)</p>

### Decision Tree
* Classification on discrete values
* Classifier is modelled as a tree. Decision tree grows from the root downwards by selecting the next best attribute at each decision level.