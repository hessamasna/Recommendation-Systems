## **Collaborative Filtering Systems**

### **Intuition**

Collaborative filtering is the process of predicting the interests of a user by identifying preferences and information from many users. This is done by filtering data for information or patterns using techniques involving collaboration among multiple agents, data sources, etc. The underlying intuition behind collaborative filtering is that if users A and B have similar taste in a product, then A and B are likely to have similar taste in other products as well.

There are two common types of approaches in collaborative filtering, memory based and model based approach.

1.  Memory based approaches — also often referred to as neighbourhood collaborative filtering. Essentially, ratings of user-item combinations are predicted on the basis of their neighbourhoods. This can be further split into user based collaborative filtering and item based collaborative filtering. User based essentially means that like minded users are going to yield strong and similar recommendations. Item based collaborative filtering recommends items based on the similarity between items calculated using user ratings of those items.
2.  Model based approaches — are predictive models using machine learning. Features associated to the dataset are parameterized as inputs of the model to try to solve an optimization related problem. Model based approaches include using things like decision trees, rule based approaches, latent factor models etc.

### **Implementation**

1.  Import data from generate\_data function (function provided above) or download the CSV from [here](https://github.com/vatsal220/medium_articles/blob/main/rec_sys/data/data.csv)
2.  Generate a pivot table with readers on the index and books on the column and values being the ratings
3.  Calculate similarity between items and users using [svds](https://docs.scipy.org/doc/scipy/reference/generated/scipy.sparse.linalg.svds.html)
4.  Generate item recommendations based on user\_id
5.  code is in main.py

©️ [vatsal220](https://gist.github.com/vatsal220) 