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



Exact match and inexact match:

The code is comparing named entities from two RDF files using three different methods: exact matching, inexact matching, and AI-based semantic matching.

In the exact matching function, the code is comparing named entities by directly comparing their string labels. It loops through each named entity from the first RDF file and checks if it exists in the second RDF file. If a match is found, it adds the entity to a list of matched entities and removes it from the second RDF file. At the end of the loop, it returns the lists of matched and unmatched entities.

In the inexact matching function, the code is using fuzzy string matching to compare named entities. It is using the fuzzywuzzy package to calculate a similarity score between the string labels of the entities. It loops through each named entity from the first RDF file and checks if there is a similar entity in the second RDF file (i.e., a match with a similarity score above a certain threshold). If a match is found, it adds the entity to a list of matched entities and removes it from the second RDF file. At the end of the loop, it returns the lists of matched and unmatched entities.

In the AI-based semantic matching function, the code is using spaCy to compare the semantics of the named entities. It loads a pre-trained spaCy model and loops through each named entity from the first RDF file. For each entity, it finds the most similar entity in the second RDF file using spaCy's semantic similarity function. If a match is found (i.e., a similarity score above a certain threshold), it adds the entity to a list of matched entities and removes it from the second RDF file. At the end of the loop, it returns the lists of matched and unmatched entities.

The matched and unmatched entities are returned as dictionaries, where the keys are the URIs of the named entities and the values are the corresponding labels. This allows for easy handling of matched and unmatched entities, for example for insertion or deletion in a knowledge graph.



Mapping predicts (Check predict functionality. When we conduct predict mapping, we need to consider whether domains are matching or not, ranges are matching or not, and functionalities are matching or not). The function would return matched and unmatched (to decide how to handle unmatched, e.g. for insertion or deletion)


This code defines a class called MappingPredictor which is used to compare two RDF graphs (graph1 and graph2) and predict their property mappings.

The __init__ method initializes two RDF graphs, graph1 and graph2, by parsing the RDF/XML files specified by graph1_path and graph2_path respectively.

The predict_mapping method loops through all properties in graph1 and graph2 and compares them using the _match_properties method. If a match is found, the property names are appended to the matched_properties list. If a match is not found, the property name is appended to the unmatched_properties list.

The _match_properties method checks if two given properties match based on their name, domains, ranges, and functionalities. If all of these attributes match, the method returns True, otherwise it returns False.

The _match_domains and _match_ranges methods check if the domains and ranges of two given properties match. If one of the properties does not have a domain or range, it is considered to match.

The _match_functionalities method checks if the two properties are functional (i.e., whether they can have only one value per instance) or not. If the two properties have different functionalities, the method returns False.

Overall, this code can be used as a basic starting point for comparing two RDF graphs and predicting their property mappings, but it may need to be extended or modified depending on the specific requirements of the use case.










