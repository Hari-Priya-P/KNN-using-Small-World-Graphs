# KNN-using-Small-World-Graphs

Implementation of the K-Nearest Neighbors (KNN) algorithm using navigable Small World Graphs and classification of IRIS flower data set using this approach. KNN algorithm is widely used for classification problems. The normal KNN algorithm would look at all the training data points, compute the distance from each of them and classify the new point based on its K nearest neighbors. This approach would need an iteration over entire dataset which makes it inefficient if the data is large. The proposed approach of finding K nearest neighbor for a new point is an optimization over the original KNN algorithm. We use Small World Graph to find the nearest neighbors. This is more efficient as compared to the normal approach as we iterate over lesser number of nodes (start at a random node and only explore its unexplored neighbors until the set of k-nearest neighbors does not get updated anymore). This no longer requires us to look at all the data points making it much more efficient. The only trade-off with this approach would be the occurrence of false positives, that is, the set of data points returned by this algorithm might be the actual k-nearest neighbors or they might be false positives (local maxima with respect to the new data point given as input/query). This depends on the initial data point which is randomly chosen as the entry vertex.

This algorithm is divided into three sub-parts:<br/>
- Data Insertion : Construct the graph using the given data points
- KNN Search : Search the graph for k-nearest neighbors
- KNN Classifier : Classify new data points based on the k-nearest neighbors

### Working of the Algorithm

![flowchart](https://github.com/Hari-Priya-P/KNN-using-Small-World-Graphs/blob/master/knn_swg.png)
