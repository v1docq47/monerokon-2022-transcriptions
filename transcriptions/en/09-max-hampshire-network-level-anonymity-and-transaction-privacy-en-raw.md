# Max Hampshire

_**Max Hampshire - Network-level Anonymity and Transaction Privacy**_

_Monero Konferenco  #MoneroKon2022 Day 1 | Lightning Session 1_

[https://youtu.be/RSCziwwIvoc](https://youtu.be/RSCziwwIvoc)

---

_**Max Hampshire:**_ I'll try and and smash through five minutes how the Nym Mixnet works to grant network level anonymity and transaction privacy, and then very briefly talk about how you would use this with Monero.

So what is the Nym Mixnet. The Mixnet is an anonymous overlay network similar to something like Tor or I2P, and it shares certain similarities with those things. So first of all traffic is multiply encrypted, and then rooted and unpacked according to the public keys of the nodes in the network. Where it starts to differ is that all of the nodes that are online in the Nym Mixnet, so this is clients as well as the nodes that are actually doing the kind of mixing, which I'll show in the next slide. What these basically do is they send cover traffic between themselves. And this is a way that the Mixnet tries to prevent traffic analysis, because when data leaves a Nym client then what happens is it's actually all chopped up into identically sized strings packets. So then suddenly the kind of traffic analysis that you can start doing, when you can just see as a global passive adversary, you know, can look over a whole network and they can maybe see the pattern of TCP or UDP packets going in and out of a network, then they can maybe start to kind of like make assumptions regarding the sender and recipient based on that metadata. But this is our way of basically making that a lot harder or impossible. Furthermore we add timing obfuscation, and what I mean by this is that before each hop, so like I said, you know, it's like onion rooting, you have packets that are moderately encrypted, a Mixnet node will take it, unwrap one layer of that encryption, and then pass it somewhere else much like in Tor. But what we have is we add a small variable timing delay basically to each of these hops. And what this does in combination with the cover traffic is makes it a lot harder to actually follow traffic through this system.

So it's not quite a deep dive, I'm not sure why it's called a deep dive, but you can basically see this traffic will leave your local Nym client, so that's either something in an app or something that you're kind of just running as a persistent process on your phone or laptop, it will then take three hops through the Mixnet, each of these Mixnet nodes is passing dummy traffic, fake identically sized traffic between themselves, and there's a very small timing obfuscation added to it. And then what happens is all of these anonymized packets leave the Mixnet exactly the same way. And they go to either a service provider which is there or another user. So if you have a chat, I want to be talking to you via the Mixnet.

So how would you then use Monero with the Mixnet to kind of get some of these anonymity and privacy affordances. So what you would do right now is there's a lot of Monero wallets that speak socks5, and we have a socks5 client, which is basically a binary, you run it as a process on your desktop machine, and what it does is you basically pass all of your traffic into this socks5 client, and that will then ping it through the Mixnet. But what's at the other end, what's this service provider that's on the right hand side there? And that is kind of where my call to action comes. So I'm actually the developer relations for Nym, and it's my job basically to get people to build with it.

So what we need, actually after I wrote these slides I find out there is actually a proof of concept of this on GitHub, which is great — I don't know who made it, but please keep working on it — you basically need something that would then broadcast an RPC transaction that you've kind of sent through the Mixnet. And then whatever node actually takes in that RPC call, it doesn't know what your IP address is, it can't make any kind of timing analysis based on when it hits the node. So it's kind of basically obfuscating your metadata. So this is the most immediate way, but we're also looking for people to integrate with us natively. So having this built into desktop and mobile wallets that when they start up you can choose to send it through the Mixnet and send it through a local Nym client basically.

And that's my five minutes. So yeah we have a grants program that's coming up. If you want to build on it, get in touch either right here or at max@nymtech.net or grant@nymtech.net. Cheers.