Date: 26/07/24
Title: Accelerating Ethereum through zk-verification and restaking
Links: https://x.com/i/spaces/1lDxLPlMPezxm 

---

Keren (Swell):
Hey, can you hear me?

Keren (Swell):
Hey everyone, can you hear me?

Wanli (Brevis):
No, yeah, we can hear you. Yeah, yes, we can.

Keren (Swell):
Oh, great. I think we're just waiting for Travis.

Keren (Swell):
I think we can get started and see if Travis arrives in the next few minutes.

Keren (Swell):
So welcome everyone.

Keren (Swell):
Yeah, so I'm Keren. I'll be your moderator today. And we're joined by several of the leading AVSs working with ZKCruise. So there's Align, Brevis, and also Radius. We're going to discuss ZK core processors, zero-knowledge tech, and accelerating Ethereum's roadmap with this technology and restaking. So if you do have any questions during this space, feel free to leave them in the comments. We'll come to them later. Yeah, let's start with some intros. Perhaps, who do we have from Align?

RJ (Align):
Thank you for having us. I'm RJ, one of the co-founders of Align. We also have Diego, that we are going to put as a speaker as well.

RJ (Align):
Thank you, Swell, for allowing us to participate in this and co-host with you. Welcome.

RJ (Align):
Yep. So, well, I'm actually one of the co-founders and we, yeah, we're building a ZK verification layer as an AVS, and the idea is to allow people to verify proof in an affordable and fast manner. And we also have Diego that is part of the team.

Diego (Align):
Hi, hello, I am Diego. I am head of research at Align. And yeah, we are building this fast and cheap verification layer with also very high throughput. And that is thanks to running as an AVS on top of Eigenlayer.

Keren (Swell):
Thanks, Diego. And I think our Brevis team has just arrived.

Wanli (Brevis):
Hey there.

Keren (Swell):
Perhaps not. Who do we have from Radius?

Ajay (Radius):
This is Ajay, co-founder of Radius, and I'm doing ZK and protocol research at Radius. Radius is developing a coordination layer to support decentralized sequencing for roll-ups aiming to provide a better user experience. Thanks for having me here.

Keren (Swell):
Thanks for joining.

Keren (Swell):
Brevis, are you, is it Wanli from Brevis? Are you able to speak?

Wanli (Brevis):
Hey guys, yeah, it is Wanli. Sorry, I was setting my microphone.

Keren (Swell):
Oh, welcome and feel free to introduce yourself.

Wanli (Brevis):
Thank you. Yeah, hey guys, this is Wanli. I'm head of ecosystem from Brevis. So I'm mainly covering the ecosystem expansion as well as dev relations for the Brevis ecosystem. And we are a zero-knowledge coprocessor. And I can introduce a little bit more about what we do and what use cases we can bring to different decentralized applications later in a bit.

Keren (Swell):
Thank you, Wanli.

Keren (Swell):
Yeah, so could we start with Align? I just get an overview of what Align does in some of the use cases.

RJ (Align):
Yes. OK, so Align, as we mentioned, is a ZK verification layer. What this means is a network designed with the sole purpose of verifying zero-knowledge proofs. We're doing this because our goal is to offer a new infrastructure for developers where they can send all of the proofs they have and verify them on Ethereum for 10% of the cost and without having to trade off latency when they want to do this. Because if you want to amortize costs, usually when you're using Ethereum, one of the techniques you have is aggregating proofs that can have some latency, but you also have other limitations. So what we designed, thanks to the Eigenlayer, because we can think of building a new infrastructure, is a decentralized network, that the only thing it does, it receives proofs, verifies them, if we have a quorum, we submit the result on Ethereum. So this allows us to offer a really fast and incredibly scalable new infrastructure so we can improve Ethereum as a settlement layer. And some of the use cases here, what we were talking with all of you here that are on the panel, is helping teams who are using ZK proofs and they want to use them on Ethereum or maybe in the future on L2s to lower their operational cost and improve the development experience and also the experience of the users in the future. So we are an infrastructure for other people to build on top of and allow them to access better prices on top of Ethereum.

Keren (Swell):
Thanks. Let's go to Brevis.

Wanli (Brevis):
Yeah, so what Brevis does in simple terms is to allow smart contracts to have insights into the full history of blockchain in a trustless way. And on top of that, allowing smart contracts to build very expressive features out of the insights they have derived from the Ethereum blockchain or any other EVM-compatible blockchains that we're supporting in the future. So what this means is, although it might sound not so intuitive, but smart contracts right now don't really have visibility into any historical data stored in blockchain because of how data is truncated after a certain time period in the history of blockchain. So in order for a smart contract, for example, to determine if a user is eligible for certain rewards or benefits when they are interacting with the decentralized application, they sometimes will need to look into the entire footprint of the user on chain. And that would start from creation to the latest transaction that a user has made. So that requires there to be a way for smart contracts to look into any data stored on blockchain. And that's what we are offering. So instead of having smart contracts trying to do complex computations, very gas-intensive computations to retrieve historical data that are truncated or do very expressive computations directly within smart contracts, we're migrating that portion of data retrieval and data computation to an off-chain component, our zero-knowledge co-processors, so that we are still fulfilling the requests from the smart contracts, whether it's to prove a user has done this amount of transactions in the past, or they have interacted with this many protocols, and we will allow a zero-knowledge proof to be generated from off-chain and submitted back on-chain to the smart contract. And basically by verifying that zero-knowledge proof, the smart contract is able to tell, based on the zero-knowledge proof verification result, the request is confirmed, whether it is a user status of completing this many transactions or some other proof criteria. The smart contract is then able to act upon the confirmation or the verification to use callback functions to trigger further transactions related to the proof request. So that's kind of like a high-level idea of what Brevis serves, but essentially this will mean decentralized applications like DeFi or GameFi would be able to build very competitive features compared to their off-chain counterparts. So compared to centralized exchanges, on-chain exchanges can also build very expressive VIP loyalty programs based on users' historical transaction volume. And GameFi projects can build dynamic features that would alter based on a user's footprint within the game. So these data-centric features, data-driven scenarios will all be possible because of the cost-minimized way of proving historical data on chain in a trustless way.

Keren (Swell):
Thanks, Wanli. Let's move to Radius. Could you just introduce Radius?

Ajay (Radius):
Yeah. So, Radius is developing a coordination layer to support the sequences' decentralization for rollups, aiming to provide a better user experience. So, first, I will explain why decentralizing sequences is crucial for a better user experience and why a coordination mechanism is needed in this process. Decentralization involves three attributes, censorship resistance, liveness, and safety. Most current rollups rely on centralized sequencers, meaning users must trust that this entity will not engage in malicious behavior like censoring transactions or executing sandwich attacks. Beyond trust, users have no recourse. Regarding liveness, some recent layer 3 app chains have experienced downtime of up to 53 hours requiring users to trust that centralized sequencing will remain operational. Lastly, in terms of safety, when a user sends a transaction to the sequencer, the sequencer promises to include that transaction in a block and post it to Ethereum for finalization. However, there's currently no way to enforce this promise. So the need for coordination becomes clear when examining how a user's transaction moves from a rollup to Ethereum. When you initiate a transaction on a rollup, multiple actors are involved in the process, including the sequencer, proposer, builder, and prover. Instead of relying on trust as with centralized sequencing, Radius' coordination layer facilitates communication among these multiple actors in a trust-minimized manner. For instance, shared sequencing is a coordination mechanism to support synchronous composability between sequences of different rollups. So, Radius aims to minimize trust through cryptographic methods like ZK. For example, ZK is used to prove the proper functioning of encrypted mempool introduced for censoring resistance, and also to enable synchronous composability between rollups and between a rollup and Ethereum. So, we think that our coordination layer can help rollups achieve decentralization of sequencing in a trust-minimized manner for a better user experience.

Keren (Swell):
Thank you. From our side, I'll just quickly introduce Swell. So you probably know Swell as the issuer of SWEATH, our liquid staking token. Our SWEATH, our liquid restaking token. But we are also building Swell L2, which will be the restaking yield layer for Ethereum. In essence, the idea is that Swell L2 will connect AVSs on all networks, as other platforms such as Symbiotic will connect these AVSs to DeFi protocols to create a more secure and more innovative and expressive environment for DeFi. Yeah, so that's it in a nutshell.

Keren (Swell):
Maybe we can talk now about why you've decided to build your ZK project as an AVS and how restaking helps to secure your tech. Any comments on that?

Diego (Align):
Well, in our case, we thought that building it as an AVS would make bootstrapping this decentralized network much easier. It will also connect us very deeply with Ethereum and a highly innovative environment. We know that with this idea of restaking and Eigenlayer, we can do very cool stuff and innovate continuously in Ethereum. And one of the main things that having this cryptoeconomic security allows us is to have a fast mode for proof verification that basically lets us verify at two more orders of magnitude than Ethereum. So if Ethereum can process maybe 10 proofs per second, we can go as high as a thousand proofs per second. And we believe that these will enable lots of new applications because we will have much higher throughput and at a lower cost. In some sense, we view these as the broadband of ZK. So I am old enough to have lived through the internet before broadband, and I can tell you that the difference is enormous and you get a lot of innovation from people knowing, okay, now I can do things because this is cheap, this is fast, and I have very high throughput.

Keren (Swell):
Thanks. You're not the only one to have experienced the dial-up era. And whatever came before that. Yeah, any further comments on that?

Ajay (Radius):
Radius is not using restaking to secure ZK tech. Radius generates ZK-proof and then probably uses Align layer to verify this ZK-proof. Radius is using AVS to provide the key attributes of sequence decentralization. So multiple sequencers form a set and participate in the block-building process of the rollup. Among them, one sequencer is selected as a leader to build a block and then issue pre-confirmation for each transaction, and the remaining sequencers act as followers, syncing up on the pre-confirmation and validating the block in case the leader crashes. So in essence, a sufficient number of sequencers are required to achieve decentralization of the sequencing. So without AVS or restaking, we would have to design our own incentives to encourage sequencers to participate in our coordination layer. So this kind of cold start problem is not easy to solve. However, using restaking and AVS, we can encourage the participation of many sequencers with minimal difficulty. So we're going to announce very soon, but we have recently deployed our AVS on Eigenlayer testnet, and more than 20 validators are expected to participate in this AVS. So through this, we hope to promote the decentralization of rollup sequencing, enabling many rollups to operate more reliably.

Keren (Swell):
Thanks, and you mentioned that you're working with Align. How else are you working together?

RJ (Align):
Yes, so maybe Ajay can explain quickly how we could work with Radius. So Align verifies any type of proof system from any project and we can submit the results on Ethereum. So for projects where they will have a lot of applications on top of them or a lot of proofs generated by certain ZK rollups, Align can verify them so these applications can have a lower operational cost and can actually have no problem with latency at the same time. So many of our use cases are ZK rollups and in this case something like Radius that is a whole ecosystem as well, we can help them improve the experience for the developers and their users as well.

Ajay (Radius):
Yeah, so we're going to onboard the ZK rollups in our coordination layer. At that time, ZK rollups are going to generate many ZK proofs to prove the integrity of the state conditions. At that time, the cost to verify this proof is really crucial for these rollups, especially for these rollups to sustain economically. So they need to reduce this operational cost while running sequences. So at that time, I think the verification layer such as Align layer would be a really good solution to reduce this cost. And then our coordination layer also generates a bunch of ZK proofs. For example, we use an encrypted mempool for censorship resistance. At that time, we need to prove the integrity of this encrypted mempool. So at that time we also can use this Align layer to verify our proof with minimal cost. So that's how we work together.

Keren (Swell):
And does Brevis fit into the picture somewhere there?

Wanli (Brevis):
Yeah, I can chime in a little as well. So for Brevis, although we have used basically, I would say the cost and performance of Brevis is always on the way to being optimized. And we have been exploring different ways to lower the verification gas cost, lower the proof generation cost off-chain, and also improve the proof generation delay. And also, by lowering the gas costs on-chain, we're also aiming to basically improve on-chain verification. So the way we are thinking of is definitely there are a variety of ways to optimize the performance of on-chain verification. But like, aggregation is one way we have already implemented to basically batch different proofs together and to aggregate proofs and generate only one proof that is mapping into maybe a set of proofs and how that final proof verified on-chain would also give the smart contract the confidence of verifying the underlying proofs aggregated. So that's one way it would drastically reduce the verification cost. But the latency associated with the aggregation process would be a little bit concerning for some use cases. Like for example, the time-sensitive use cases of maybe dynamically diverging user experiences in some GameFi projects. Like they want to make sure every user experience step offered to the user is tightly coupled with users' previous choices in their on-chain transactions. So this is a scenario that is still hard to implement using only aggregation or using zero-knowledge proofs in general, we feel, because of the time required for proof generation and verification. But working with Align, there can be a large room for optimization in terms of the on-chain verification gas cost as well as the latency required. So my understanding is we are working very closely on the research part to see how Align would fit into our timeline. But we're also waiting for Align to be production-ready because Align just rolled out its testnet. So we're going to first do some experiments on the testnet to implement Align in our verification layer. And in the future, when Align is more production-ready, there might be some major coupling or major integration between Brevis and Align. We may roll out a different feature on top of our existing one to serve different use cases that are more time-sensitive and cost-sensitive.

Keren (Swell):
How about on Align's side, what's coming up for you in the next few months?

RJ (Align):
Well, we are moving really fast. As Wanli mentioned, we have the testnet operational so that people can try it. You can even go to our repo, check it out, and send proofs just to play a little bit with it. We will have more news on the development soon. We have been adding everything needed for the next phase. And with ECC coming soon, we will be participating in many events. You can come and play and go for some of the bounties we have to build with Align and do your applications or whatever you want. So we are really moving fast, and that is thanks to the amazing engineering team that we have, which works non-stop.

Keren (Swell):
And what's in store for Radius?

Ajay (Radius):
Yeah, as I said before, this week we are going to announce the deployment of the Radius AVS on the testnet of Eigenlayer with more than 20 operators. So we can deliver decentralized sequencing for rollups to any app chains or any rollups that want to use our sequencing solution. And a couple of rollups have thankfully decided to use our sequencing layer. So we are going to announce that as well. And then some ecosystem partners also believe in our mission. So a major announcement is coming very soon.

Keren (Swell):
Nice.

Keren (Swell):
Yeah, before we wrap up then, do you have any questions for each other?

Keren (Swell):
Oh, we lost Brevis for a sec. Yeah, I guess there might be a glitch again.

Keren (Swell):
Yeah, any closing comments from any of our speakers?

RJ (Align):
From our side, yes, as Diego mentioned, we are working really hard on improving the testnet. And if any developers here want to try Align, we're going to be at ECC. And we are also participating in the Lambda Hack Week, which is a very nerdy and big hackathon before ECC. So if any of you are going to be there, you're more than invited to join us and try to build something. Align is not only going to be one of the projects; there are many other projects in the interoperability, L2, and gaming ecosystem. So if you want to hack something, you're more than invited to participate with us. Thank you, Swell, for having us and allowing us to explain what we're doing.

Ajay (Radius):
Yeah, Radius is also heading to ECC. So we'd like to meet as many projects as possible who want to build these rollups with our solutions. So, yeah, we'd love to meet them. And we also thank you, Swell, for having me here. It was great talking with you.

Keren (Swell):
Yeah, a couple of the Swell team members will be at ECC. So yeah, hopefully we can meet.

Keren (Swell):
Thanks everyone for joining us.

Keren (Swell):
Thank you to all of our speakers. Make sure you follow them if you don't already. And yeah, enjoy the rest of your day wherever you are.

All:
Thank you.
Thanks.
See you.
Bye, thank you.
Bye.
