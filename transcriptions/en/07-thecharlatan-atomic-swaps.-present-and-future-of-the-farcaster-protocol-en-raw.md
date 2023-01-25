# TheCharlatan

_**TheCharlatan - Atomic Swaps: Present and Future of the Farcaster Protocol**_

_Monero Konferenco 2022 #MoneroKon2022 Lisbon - Day 1 | Lightning Session 1_

[https://youtu.be/oxiJ7LBJfG0](https://youtu.be/oxiJ7LBJfG0)

---

_**TheCharlatan:**_ I'm going to talk on Farcaster, Bitcoin-Monero software implementation. Farcaster uses Rust implemented microservices, quite have used cryptography, and I'm going to talk about the past, present and future of the software.

So in short Farcaster is a CCS funded project. The goal of the CCS was to implement Bitcoin-Monero atomic swaps. The project was taken on initially by Crypt GmbH, the Swiss cryptocurrency R&D company, which I also work for. It's open source and MIT licensed. And we specced out the entire protocol and software in the 9-part RFC.

In short to recap on atomic swaps, for traditional swaps you usually require a trusted third party as an arbitrator, which ensures that no fraud occurs when the swap is taking place. So an arbitrator needs to take custody of the funds at some point in the swap. Atomic swaps use cryptography instead of this arbitrator to ensure that the swap can take place without any frauds accompanying it.

The CCS for Farcaster was funded with great enthusiasm. We originally expected delivery of the software in Q1 2021 and Q2 2021 and budgeted the effort for five software developers. However now we've so far completed 10 or 16 milestones, so the project is late since it's due to 2022 now. We also never had more than 3 developers added working at a time. And we also completed implementation released by commits of Bitcoin-Monero atomic swaps, though that's atomic swap software is currently unmaintained.

Next to commits being unmaintained at the moment, the other very good reasons for why we continue pushing on this project — first of all Farcaster swap implementation is symmetric, it handles both buying and selling XMR and BTC, in both directions. It's also possible to sweep Monero to a destination address once the swap is done. The core architecture and the core library of Farcaster is extendable towards future assets. And we built everything with this scalable microservices architecture. We also have support for the Monero light wallet server, and we developed the forecaster.dev website which acts as an automated swap offer maker.

Broadly our architecture are Rust implemented microservices, which can communicate with each other over ZeroMQ message classes. These services are isolated by functions, so we have a service that implements the swap state machine, service for the cryptography model, the database etc. And all these services can be managed by a single command line application.

Currently we're pushing for a mainnet release "soon", but seriously we can expect it in 1-2 months. So keep an eye out for that on the Monero subreddit. What we really have at the moment is ensuring that users can recover funds, no matter what. This is especially in a learning from our competitors, where we saw some users come into real troubles, when it came to recovering funds, and the early Lightning Network, where I also experienced some trouble myself, when I had to recover from a dead channel. The API is nearly complete, and we will commence GUI developments very soon.

In the future we want to tackle the Free Option problem. This is a problem that arises because in our protocol Bitcoin always has to lock first, meaning that somebody who wants to make a swap always has to lock the Bitcoin first, and therefore has to spend minimum one transaction fee without knowing that the counterparty will collaborate on the swap. We seek to solve this problem by either requiring an upfront cost to a reputable counterparty by the means of delay puzzles and proof of ownership or by putting an extra reputation networks on top of Farcaster. I've also been involved with specking out Monero transaction chaining, and there's going to be another talk that's going to go more into depth on this topic later in the conference. And obviously we want to at some point in time support more assets other than just Bitcoin to swap. Thank you.
