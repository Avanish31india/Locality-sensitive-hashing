# Locality-sensitive-hashing
Implementation of KNN using LSH from Scratch and Cosine Similarity
Implement LSH from scratch
In this assignment, you will implement LSH from scratch and predict the labels of the test data. You will then verify the correctness of the your implementation using a "grader" function/cell (provided by us) which will match your implmentation.

The grader fucntion would help you validate the correctness of your code.
Instructions:
Read in the train_data.
Vectorize train_data using sklearns built in tfidf vectorizer.
Ignore unigrams and make use of both bigrams & trigrams and also limit the max features to 4000 and minimum document frequency to 10.
After the tfidf vectors are generated as mentioned above, next task is to generate random hyperplanes.
Generate 5 random hyperplanes. And generate the hyperplanes using a random normal distribution with mean zero and variance 1.
We have set the numpy random seed to zero, please do not change it. And then you can make use of np.random.normal to generate the vectors for hyperplanes.
As mentioned in the course videos, compute the hash function and also the corresponding hash table for it.
Once the hash table is generated now take in each of the query points from the test data.
Vectorize those query points using the same tfidf vectorizer as mentioned above.
Now use the hash function on this query point and fetch all the similar data points from the hashtable.
Use cosine similarity to compute 11-Nearest Neighbours from the list of data points obtained in the above step.
Take a majority vote among the 11-Nearest Neighbours and predict the class label for the query point in the test data.
In case of a tie in the obtained labels from nearest neighbours, you can pick a label after sorting all the labels alphabetically(A-Z), i.e. for example labels starting with A would get more preference than labels starting with Z.
Repeat steps 9 to 13 for all the points in the test data and then finally return a list with all the predicted labels.
Note that there are a total of 10 data points in the test data so the final list you return should be of length 10.
Also note that the cosine similarity function should be written from scratch, you should not directly make use of existing libraries.
Please use the formula of cosine similarity as explained in the course videos, you can make use of numpy or scipy to calculate dot or norm or transpose.
