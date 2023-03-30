# Knowledge-Graphs
Progress on Knowledge graphs


GCN:
GCN is a type of neural network designed to work with graph-structured data, where the data is represented as a graph consisting of nodes and edges. GCNs can be used for various tasks such as node classification, link prediction, and graph classification. In this notebook, the GCN is applied to a node classification task.

The notebook uses the Cora dataset, which is a citation network consisting of scientific publications and their citations. The task is to classify each paper into one of seven categories based on the citation links between papers.

The notebook first loads the dataset and preprocesses it to create a graph adjacency matrix and feature matrix, which are the inputs to the GCN. The GCN model is then defined using PyTorch, with a specified number of hidden layers and activation function.

The model is then trained using backpropagation and stochastic gradient descent to minimize the cross-entropy loss between the predicted and true labels. The accuracy of the model is evaluated on a test set, achieving an accuracy of around 81%.

Overall, the notebook provides a clear implementation of a GCN for node classification on a real-world dataset, demonstrating the power of GCNs for graph-based machine learning tasks



ENTITY EXTRACTION:
The notebook appears to contain code for extracting entities related to addresses from text using natural language processing (NLP) techniques and creating a knowledge graph based on the extracted entities.

The notebook uses the Python programming language and popular NLP libraries such as spaCy and NLTK. The code reads in a dataset of text documents and processes each document using spaCy's NLP pipeline. The pipeline identifies entities in the text and categorizes them into predefined types such as persons, organizations, and locations.

Next, the notebook focuses on extracting entities related to addresses, such as street names, cities, and zip codes. It does this by first identifying the location entities and then using regular expressions to extract specific address components. The extracted entities are then used to build a knowledge graph that represents the relationships between the entities.

The notebook also provides examples of how the knowledge graph can be queried and visualized using the NetworkX and Matplotlib libraries.

Overall, the notebook demonstrates how NLP techniques can be used to automatically extract entities from text and create a knowledge graph that represents the relationships between the entities. 


KNOWLEDGE GRAPH(1):
The notebook starts by loading a dataset of text documents and processing each document using spaCy's NLP pipeline. The pipeline identifies entities in the text and categorizes them into predefined types such as persons, organizations, and locations.

Next, the notebook focuses on creating a knowledge graph based on the identified entities. It does this by first defining the nodes and edges of the graph and then iterating through the documents to add nodes and edges to the graph based on the entities and their relationships.

The notebook also provides examples of how to query and visualize the resulting knowledge graph using the NetworkX and Matplotlib libraries.

Overall, the notebook demonstrates how NLP techniques and knowledge graphs can be used to automatically extract and represent information from text documents. The resulting knowledge graph can be a powerful tool for exploring relationships and patterns in the data.




