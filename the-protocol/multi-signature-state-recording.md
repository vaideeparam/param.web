---
description: 'States: Quotation >> Purchase Order >> Invoice >> Payments >> Digital Receipt'
---

# Multi signature state recording

Commerce transactions has more states as compared to typical financial transaction. Any state change would involve minimum two parties to fulfil the associated contractual obligations. In order to bring this into universal commerce blockchain, where most of the contracts can be build seamlessly on a single chain, ⦃param⦄ records the transaction states and transitions on the ledger natively.

![](../.gitbook/assets/image%20%2819%29.png)

⦃param⦄ protocol records states after necessary validations such as:

* Quotations are always initiated by party-Seller to a party-Buyer, which serves as the base for rest of the state-change validations
* Create Purchase Order transaction can only be initiated by Buyer
* Create Invoice transaction can only be initiated by Seller
* Create Record Payment  transaction can only be initiated by Buyer
* Create Digital Receipt transaction can only be initiated by Seller
* Only Buyer or Seller can add subscribers to the transaction, which is detailed in [later](param-node.md) section.

Although the network is permissioned, for spam protection, the creating Quotation on the network would come at a stake or a cost.

> Its worthwhile to note, a single "_commerce transaction"_ is equal to multiple ⦃param⦄ transaction on the chain



