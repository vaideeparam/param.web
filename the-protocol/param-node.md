# ⦃param⦄ Node

### Ethereum + Quorum Tessara + Cayley Graph

⦃param⦄ is a Quorum-based \(Ethereum\) blockchain protocol that has been developed to provide the Commerce Industry with a permissioned public implementation of Quorum that supports sharing documents such as Quotations, Purchase Orders, Invoices and more to _zero-infrastructure_ enterprises without a need for consortium and with utmost data-privacy.

![](../.gitbook/assets/image%20%2810%29.png)

The full node consists of:

* Modified Geth client from Quorum node - will have ledger structure changes to record commerce transaction states
* Modified Tessera transaction manager with support for sending PGP encrypted documents on public network with subscribers support
* Cayley Graph to construct node-level knowledge graph based on network events
* Ready-made libraries & services for integration with enterprise resource planning \(ERP\) softwares

### Transactions Processing and Privacy

⦃param⦄ supports three modes of document transfer between nodes. 

#### Private mode

This mode is used for transferring the documents between two private nodes securely without leaving any trace on the public blockchain except for the signature of the transaction for future validation. The steps followed are:

* The local node sends the documents to transaction manager
* Transaction manager generates a random symmetric key for encrypting the document
* Document is encrypted using random symmetric key
* Later, symmetric key is encrypted using RSA with receiver's public address for sharing the key via the network
* Private nodes will create a dedicated point-to-point secure connection
* Both encrypted key and the document are shared via secure connection
* The receiver acknowledges the document transfer
* Signature hash including the acknowledgement and the document is created
* Finally, upon successful private document transfer, the transaction is sent to P2P public network

#### Protected Mode

Protected Mode of transfer mimics the private mode of transfer except that the documents are stored on the public nodes. This enables the small/medium enterprises and consumers to store documents such as invoices and purchase receipts securely on blockchain and claim ownership for forward use-cases, such as insurance, resale, etc... The steps are:

* Documents are encrypted using symmetric keys like Private mode
* Encrypted keys and documents are stored as part of the public ledger
* Transaction is processed and block is mined like public transaction
* Nodes that are opted for storing protected transaction will sync as part of the block sync mechanism

#### Public mode

Public mode is in compliance with Ethereum like transaction, where the documents are open-format, included as part of the transaction and all nodes syncs this data.

### **Smart Contracts**

Largely Smart contracts behaviour at a node level remains same, but as a network it would look different depending on the mode of transfer. Smart-contracts that involve Private/Protected documents, the contracts can be executed only on the sender and receiver nodes, who have access to these documents. Whereas, for public documents, multiple node can participate in execution and consensus.

### Data Privacy

⦃param⦄ provides enterprise level data-privacy, additionally it democratize the data equally between the sender and receiver, empowering them with the right data ownership. Below tables gives the overview of the data access across parties.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Transfer Type</th>
      <th style="text-align:center">
        <p>Buyer Node</p>
        <p>(all node-type)</p>
      </th>
      <th style="text-align:center">
        <p>Seller Node</p>
        <p>(all node-type)</p>
      </th>
      <th style="text-align:center">
        <p>Protected Node</p>
        <p>(non-party)</p>
      </th>
      <th style="text-align:center">
        <p>Public Node</p>
        <p>(non-party)</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Private</td>
      <td style="text-align:center">Visible</td>
      <td style="text-align:center">Visible</td>
      <td style="text-align:center">Not Applicable</td>
      <td style="text-align:center">Not Applicable</td>
    </tr>
    <tr>
      <td style="text-align:left">Protected</td>
      <td style="text-align:center">Visible</td>
      <td style="text-align:center">Visible</td>
      <td style="text-align:center">Not-Visible</td>
      <td style="text-align:center">Not-Visible</td>
    </tr>
    <tr>
      <td style="text-align:left">Public</td>
      <td style="text-align:center">Visible</td>
      <td style="text-align:center">Visible</td>
      <td style="text-align:center">Visible</td>
      <td style="text-align:center">Visible</td>
    </tr>
  </tbody>
</table>### Subscribers

Subscribers is the concept of ownership of the documents that are shared on the network. In private/protected mode, the sender and receiver becomes subscribers automatically and equal access on the data to execute smart-contracts on their nodes which has the private key access. 

The existing subscribers can add more subscribers to share the documents. For example, a buyer can share the invoice document with financial institutes for loan processing.

### Consensus

> Raft based Consensus



