# Graphical Neural Network (GNN) Implementation on Terrorist Attack Dataset

## Introduction

This project focuses on implementing a Graph Neural Network (GNN) for analyzing a dataset related to terrorist attacks. The dataset contains two main components: information about the attack entities and the links connecting these entities to form a graph structure. The goal is to classify the attributes of these entities based on the provided data.

## Dataset Download

The project begins by downloading the dataset from an external source. 
This directory contains a subset of the data containing terrorism related information collected by the MIND Lab at UMD (http://www.mindswap.org/).

This subset of the dataset was designed for classification purposes and contains two types of information related to terrorism attack entities: the attributes of the entities and the links that connect various entities together to form a graph structure. Using the files in this directory one can construct two different graphs involving terrorist attacks, one based on co-located attacks and another, based on co-located attacks organized by the same terrorist organization. Please take a look at our paper (http://www.cs.umd.edu/~sen/pubs/sna2006/RelClzPIT.pdf) for more information about the experiment setup.

Below we give some more information about the files in this directory:
* terrorist_attack.labels: Contains the labels that we want to assign to each terrorist attack entity.
* terrorist_attack.nodes: Contains the various terrorist attack entities. Each line begins with the unique id of the entity followed by a 0-1 vector indicating the attributes that are present and the attributes that are absent. The last entry in the line is the correct class label of the entity.
* terrorist_attack_loc.edges: Each line contains two ids of terrorist attacks. This file defines the edges connecting co-located terrorist attacks.



## Data Preprocessing

1. The downloaded dataset is extracted from a compressed file, and the extracted files are listed to verify the extraction.

2. The data is transformed into a more suitable format. This includes converting the provided files into CSV format. Each data file is processed, and the resulting CSV files are used for subsequent analysis.

3. The labels in the dataset are mapped to integer IDs to facilitate classification tasks.

4. Nodes (entities) and features are organized to create a graph structure for further analysis.

## Graph Neural Network (GNN) Implementation

1. The GNN model is implemented using the DGL (Deep Graph Library) library. It is designed to work with graph-structured data.

2. The graph is created using node features, labels, and adjacency information from the dataset.

3. The dataset is split into training, validation, and test sets for model evaluation.

4. A GNN model is defined, and training is carried out with the specified number of epochs and learning rate.

5. The best validation and test accuracies are tracked during training.

6. The trained model is saved for future use.

## Model Inference

1. Input data, which may be in CSV format, is preprocessed to create a DGL graph structure.

2. The trained GNN model is used for inference on this input data.

3. Predicted class labels are obtained from the model's output.

4. The predicted class labels are mapped back to their original labels.

## Community Detection and Visualization

1. Community detection is applied to the graph data using Louvain community detection.

2. Nodes are assigned to different communities, and node colors are determined based on these community assignments.

3. The graph, with nodes colored by their community, is visualized for community analysis.

## Conclusion

This project demonstrates the implementation of a Graph Neural Network on a terrorist attack dataset. It covers data preprocessing, model training, inference, and community analysis. The final results may include classification accuracies, community information, and visualization.


