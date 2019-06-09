# directCommerce - Client

## Install ⦃param⦄.invoice wallet

Download the mac build from the following link and double click on the downloaded file from the Finder.

{% embed url="http://param.network/rel/param-network-wallet-beta-0.4.2.dmg" %}



{% hint style="info" %}
Since Beta software is distributed outside Apple app-store, you will get a Security Warning. You can override by following step

Please go "System Preferences" -&gt; "Security & Privacy" -&gt; "General" Tab and Open the app.

![](../.gitbook/assets/image%20%2823%29.png)
{% endhint %}

## Create new identity on the node

1. Click on "Create New Identity". This will create private-key/public-key on the remote node protected by password.

![](../.gitbook/assets/image%20%2836%29.png)

2. Set new "Password" to protect your wallet

{% hint style="warning" %}
Its your blockchain wallet password, there is no way to reset it.
{% endhint %}

![](../.gitbook/assets/image%20%2820%29.png)

3. If the identity is created successfully, you should see 12-phase recovery words. You can ignore this for now, beta release does not support this recovery. 

![](../.gitbook/assets/image%20%2818%29.png)

## Add contacts

Click on the "Manage Contacts" -&gt; "Create New"

![](../.gitbook/assets/image%20%2828%29.png)

You can add a business contact to whom you want to send invoice. For now, you can add some of the test account id as given below:

| Name | Param-Public-Id | Private ID |
| :--- | :--- | :--- |
| Vaidee | 0x8b30030d90b83565f2ecf77ad8b27a013a5175bd | -NA- |

![](../.gitbook/assets/image%20%282%29.png)

{% hint style="success" %}
You should get a success toast message 
{% endhint %}

## Add Item

1. Click on the "Manage Items" -&gt; "Create New"
2. You can add a product or service item, which you invoice for.
   1. Name could be "Mobile Phone" or "Software Services"
   2. Item "Id" could be any free-format text
   3. Type: Choose "Goods" or "Services"
   4. Purpose: Choose "Sell"

![](../.gitbook/assets/image%20%288%29.png)

{% hint style="success" %}
You should get a Success toast message
{% endhint %}

## Now you are ready to share Quotation \(as a Seller\)

1. Click on top-corner "⦃p⦄" logo for navigating to Home page
2. Click on "E-invoicing" -&gt; "Create New Quotation"
3. Enter Customer Name, its a drop-down, you must pick what you have added from the Contacts
4. Choose Quotation Type as "Private"
5. Enter Quotation Date by clicking on the Select date
6. Click on "Add Item"
   1. Choose ITEM you have added \("Mobile" or "Software Services"\) from the drop down
   2. Double Click "UNIT PRICE" and enter price of the item \(float field\)
   3. Double Click "QUANTITY" and type number of items \(integer field\)
7. Click on the SEND button

![](../.gitbook/assets/image%20%2825%29.png)

{% hint style="success" %}
Congratulations!! You have created your first quotation on the blockchain
{% endhint %}

## Receive Purchase Order \(Buyer\)

Now you need to wait for Customer to send you an purchase order, typically they do

![](../.gitbook/assets/image%20%2810%29.png)

## Send Invoice \(Seller\)

![](../.gitbook/assets/image%20%287%29.png)

## Record Payments \(Buyer\)

![](../.gitbook/assets/image%20%284%29.png)

![](../.gitbook/assets/image%20%2835%29.png)

## Built-in Chain Explorer

Click on the lower-right bottom to open up the explorer

![](../.gitbook/assets/image%20%289%29.png)

![](../.gitbook/assets/image%20%2824%29.png)

