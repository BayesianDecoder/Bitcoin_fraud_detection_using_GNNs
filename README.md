# ₿ Bitcoin Transaction Analysis using Machine Learning

## 🧠 Project Overview
This project builds a graph-based fraud detection system for Bitcoin transactions using the Elliptic dataset.
Instead of treating transactions as independent rows, the system models them as a transaction network and applies community detection, node embeddings, clustering, and Graph Neural Networks (GNNs) to identify illicit activity.

The project demonstrates how graph-based learning can capture structural and behavioral patterns in financial transaction networks.

---

## Problem Statement

In cryptocurrency networks:

- Transactions are highly interconnected
- Fraud often occurs in clusters or chains
- Suspicious behavior emerges from network structure

This project uses graph analytics and GNNs to detect illicit transactions based on their relationships and behavior in the network.

---


## Dataset

Elliptic Bitcoin Dataset:
- Nodes: Bitcoin transactions
- Edges: Flow of funds between transactions
- Classes:
  1. Licit (legal transactions)
  2. Illicit (fraudulent transactions)
  3. Unknown (unlabeled)

The dataset represents real-world transaction behavior in a graph structure.

---

## 📊 Objectives
- Explore and visualize Bitcoin transaction datasets.
- Understand the distribution of transaction sizes, fees, and timestamps.
- Apply basic **machine learning** or **statistical techniques** for pattern recognition.
- Build a foundation for **fraud detection**, **fee optimization**, or **market activity prediction**.

---

## Project Pipeline

### 1. Graph Construction:

- Convert transaction data into a network graph.
- Each node represents a transaction.
- Each edge represents the flow of funds.

### 2. Network Analysis

Compute graph statistics and centrality measures to understand:

- Node importance
- Connectivity patterns
- Structural properties of the network

### 3. Community Detection
   
Louvain Method
- Detects dense clusters of related transactions.
- Result: 15 major communities

Label Propagation
- Spreads labels through neighboring nodes.
- Result: 52 smaller communities

Purpose:
- Identify suspicious transaction groups
- Detect potential fraud rings

### 4. Node2Vec Embeddings

- Convert each transaction into a 32-dimensional vector
- Based on graph structure and random walks

Purpose:

- Capture behavioral patterns
- Represent nodes numerically for clustering and learning

### 5. K-Means Clustering

Cluster Node2Vec embeddings into 5 groups

Purpose:
- Discover transaction behavior patterns
- dentify potentially suspicious clusters

### 6. Graph Neural Network Models

Three GNN architectures are trained:

- GCN – Graph Convolutional Network
- GAT – Graph Attention Network
- GIN – Graph Isomorphism Network

Task:
Classify transactions as licit or illicit

---

### Visualizations





---

### Tech Stack
- Python
- PyTorch
- PyTorch Geometric
- NetworkX
- Scikit-learn
- Matplotlib / Seaborn



### Results

- Community detection revealed structural transaction clusters.
- GNNs successfully classified illicit transactions.
- High agreement between all GNN models.

---







