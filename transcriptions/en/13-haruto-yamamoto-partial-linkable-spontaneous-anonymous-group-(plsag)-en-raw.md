# Haruto Yamamoto

_**Haruto Yamamoto - Partial Linkable Spontaneous Anonymous Group (PLSAG)**_

_Monero Konferenco  #MoneroKon2022 Day 1_

[https://youtu.be/bZaX1hgv-6Q](https://youtu.be/bZaX1hgv-6Q)

---

_**Haruto Yamamoto:**_ Hi, everyone. My name is Haruto Yamamoto, and I was studying information security at Canada University in Japan. Today I would like to talk about, introduce my research on partial linkable spontaneous anonymous group signature for Monero.

So first I would like to explain about LSAG signatures. It’s kind of the digital signature in general digital signature to encrypt currency or cryptographic technique to prove the sender’s ownership. LSAG signature are created using a set of dummy transactions, and send us actual transaction on spontaneously and dummy transactions, make it difficult for the third party to identify the actual sender. The linkability is also necessary property for the Monero to detect the multiple use of the transaction private key and to avoid the double spending attacks. And that’s why the LSAG signature is unnecessary for Monero and the Monero users.

And Monero currently uses a concise LSAG signatures for Monero. This is a brief explanation of the LSAG signatures. And basically since all transaction data is stored in blockchain, including Monero, we should reduce the size of each transaction data for big scalability. The CLSAG signature accounts for the largest portion of the transaction data in Monero, therefore the reducing the size of CLSAG signature size is efficient way to reduce the size of the transaction data.

One possible problem in CLSAG current Monero signature require the same number of signature as the number of the transaction input. Considering there are a simple example if there are three transaction input, three CLSAG signature is necessary required. And the signature size increases finally. And it means each transaction required one CLSAG signature in current Monero.

To strip this problem the concept of partial LSAG signature is to reduce the number of signature to one, regardless of the transaction input. As you can see the figure below now classic signature uses two dimensional public key set, the first column, and shows the ownership of the transaction. And the second current and shows the public key for the month of the money transferred, known as our personal commitment, since linkability is only required for the first column and related to the transaction ownership, CLSAG signature can only add linkability to the first column and of the two-dimensional public key set.

However CLSAG signature cannot simply aggregate three transaction input into the one. On the other hand our partial areas is the signature algorithm can add linkability to their any columns. When we use PLSAG signature with three transaction input in Monero linkability is added to the odd number column, like one three and five. That’s why on PLSAG signature can reduce the number of the signature to run.

And let’s compare their signature size of existing CLSAG signature and multi-layers signature and PLSAG signatures. The horizontal axis of the graph represents the number of anonymity set and our vertical axis represents the size of the signature size. And we can see that our CLSAG signature is the smallest size signature, when the anonymity is set is greater than 5.

Let’s see the table below. It’s the comparison of its signature size. This is a reason why PLSAG signature is smaller than the CLSAG signature is. CLSAG signature include n times m, but PLSAG signature just include the m squared. In general the number of anonymity set is much larger than the number of the input m. That’s why PLSAG signature is smaller.

By the way Seraphis is not included in this comparison chart. I think that it would be more efficient, the smallest size, but I think there the advantage of our PLSAG signature algorithm is quite easy to implement, since the basic algorithm is quite similar to the CLSAG signatures.

Yeah that’s all for today. If you have questions, feel free to ask them.
