---
description: Enable data-driven smart-contracts.
---

# Decentralised Knowledge Graph

### Cayley as Graph Database

⦃param⦄ uses [Cayley Graph](https://cayley.io) for building decentralised knowledge graph, which is a open source graph inspired by the graph database behind Freebase and Google's Knowledge Graph.

As ⦃param⦄ records commerce documents with semantics using CDIF \(JSON-LinkedData\) format, which allows the enterprises \(local nodes\) to build decentralised knowledge graph from the documents which are sent/received via blockchain.

![](../.gitbook/assets/image%20%2811%29.png)

### Constructing local Knowledge Graph

Constructing knowledge graph is a basic feature of all the nodes \(light, private, protected, public node\) present on the ⦃param⦄ network. The steps are as follows:

* Each node is aware of its local public addresses
* All ⦃param⦄ transactions will follow Ethereum like behaviour
  * they emit events upon successful transaction on the chain
* Each node listens to the transaction events specific to its registered local public address
* Inserts them into the graph database whenever a new transaction to these address happens
* Whenever a state change happens or an knowledge extension transaction happens to the same, the node will update the local knowledge graph.

### Decentralisation ensures Data Privacy

Network harness the power of decentralisation to ensure data-privacy by construction. In a typical enterprise application, the private transactions are visible only to two nodes and its [subscribers](param-node.md#subscribers). Therefore it is impossible to build knowledge graph of transactions outside the node visibility as the public ledger does not contain the document except but the signature of the transaction. For more details refer [Data Privacy](param-node.md#data-privacy) section on [⦃param⦄ Node](param-node.md).



