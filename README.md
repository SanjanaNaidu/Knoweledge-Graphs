# Knowledge-Graphs
Progress on Knowledge graphs
GCN:
GCN is a type of neural network designed to work with graph-structured data, where the data is represented as a graph consisting of nodes and edges. GCNs can be used for various tasks such as node classification, link prediction, and graph classification. In this notebook, the GCN is applied to a node classification task.

The notebook uses the Cora dataset, which is a citation network consisting of scientific publications and their citations. The task is to classify each paper into one of seven categories based on the citation links between papers.

The notebook first loads the dataset and preprocesses it to create a graph adjacency matrix and feature matrix, which are the inputs to the GCN. The GCN model is then defined using PyTorch, with a specified number of hidden layers and activation function.

The model is then trained using backpropagation and stochastic gradient descent to minimize the cross-entropy loss between the predicted and true labels. The accuracy of the model is evaluated on a test set, achieving an accuracy of around 81%.

Overall, the notebook provides a clear implementation of a GCN for node classification on a real-world dataset, demonstrating the power of GCNs for graph-based machine learning tasks
