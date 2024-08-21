- Date: 20/08/24
- Title: Aligning an Interoperable Multi-Chain Future
- Participants: @nodekitorg, @union_build, @alignedlayer
- Links: https://x.com/alignedlayer/status/1825939500855603273

---

**Boris:**  
Hello everybody, Nick and Karel. How are you guys doing?

**Boris:**  
Yeah, pretty solid. I just wanted to do a little bit of a sound check audio test before we got started to make sure that my audio's come in through nice and clear and you guys as well.

**Nick:**  
Yep, good for me. How am I sounding?

**Karel:**  
Loud and clear.

**Nick:**  
Lovely. Super clear. All right, so how about me?

**Karel:**  
Perfect. Mic wise, yeah. It's good.

**Boris:**  
Yeah, and I can see guests filtering in and joining. So we're gonna start in like three, four, five minutes, give people a bit of time to get in. And I think the notification usually just goes out on the hour or whenever it's supposed to start. So yeah, hang tight and we'll get things started. And it's nice to meet you guys in person and nice to see some familiar faces in the crowd as well.

**Boris:**  
So just while people are starting to filter in, just so we're not sitting here in silence. I mean, since this is my first time chatting with either of you, I guess I'm just curious, like, where are you guys based? Time-wise, like, what time of day is it for you?

**Nick:**  
Yeah, I'm out in New York. 1 p.m. right now. Been on a couple calls back to back to back, so looking forward to lunch after, but hungry for knowledge, perhaps, for this space.

**Boris:**  
Hungry for knowledge and hungry to share some insights, I'm sure. How about you, Karel?

**Karel:**  
I'm in Portugal, Porto to be exact. So nearing the end of the day for me, although there's so much to be honest, I work all night, the heat is much better tolerable then.

**Boris:**  
Yeah, I can only imagine. Porto is a beautiful city. I visited last year for a couple of days for Eat in Porto.

**Karel:**  
in Lisbon for the winter. Yeah, yeah, it's very relaxed.

**Boris:**  
Yeah, it was really rainy when I was there, which was too bad. Yeah, I got to do a port wine tasting tour on a nice day, but it was raining most of the time, but I guess it was like March, so.

**Karel:**  
I had to do it. Yeah.

**Karel:**  
Yeah, for me, I enjoy the area. There's some good rock climbing nearby. In general in Portugal, there's good rock climbing, especially near the ocean. So that's usually what I do in the summer.

**Boris:**  
Interesting. I didn't know there was a big rock climbing scene in Portugal. I'm not a rock climber though, so it's not exactly something I keep tabs on.

**Karel:**  
Yeah, it's also kind of nearing the end of the day for me. I'm normally based in Toronto, so I'd be in the same time zone as Nick, but right now I'm spending some time in London. So if anyone listening is in London, hit me up. I'm looking to meet more people in space here.

**Nick:**  
How is it out there? I was there a couple months ago. Hopefully the weather's improved over the summer.

**Boris:**  
Yeah, I mean, the one other time I really spent time in London was this winter and it was pretty gray and rainy the whole time. And I'm happy to say that it's like a balmy sort of like mid-20s most of the time right now. Pretty nice. People here have been complaining that it's been too hot. Most houses here don't have air conditioning.

**Nick:**  
that I've really made for hot weather. So everyone's pretty happy right now. So yeah, pretty good.

**Boris:**  
Okay, well, I'm sure some more people are going to start joining, but instead of just yapping about the weather, maybe we'll get started. Before we begin though, is there anyone else we're waiting for, like Nick or Karel from your teams, or is it going to be you two?

**Nick:**  
Just me from our side.

**Karel:**  
Yep, good for me.

**Boris:**  
Okay, awesome. And originally, Diego, our co-founder and head of research was going to be here representing the line, but he had an in-person speaking engagement that conflicted with this. So I will be talking about the line and answering questions related to that as well as moderating and kind of hosting the space. So I guess might as well get started. I'll start off just like introducing what we're going to be talking about today. And then I'll give you guys each a chance to talk about yourselves and your projects just as like a quick intro.

**Boris:**  
Got a bunch of questions lined up. Yeah, I mean, I guess in general today, first of all, thank you for joining. Today, we put together this space to kind of highlight our partners. So when I say our, I mean, aligned, our partners who are solving this very important problem of interoperability within crypto and between blockchains. And in particular, we'd like to explore and discuss the role that ZK, so Zero Knowledge Proofs, Zero Knowledge cryptography plays in all of this. And we have, you know, we're really, really excited to be working with both Union and NodeKit and trying to make Crypto UX better.

**Boris:**  
So I guess with that, you guys are the experts on interoperability. So how about we start with Nick, tell me about yourself, tell me about NodeKit, tell me about your views on interop and how you guys are approaching this problem or how you see this problem.

**Nick:**  
Yeah, absolutely. So firstly, obviously, thank you for having me on. It's great to be here. Excited for the conversation. But I'm Nick. I'm one of the co-founders of NodeKit. NodeKit enables synchronous communication between chains. So basically what we enable is as easily as two dApps on a single chain can communicate, two chains using NodeKit can communicate.

**Nick:**  
And so the way that we do that is through Javelin. And Javelin is a super builder. So a super builder, you can think of like a block builder on Ethereum, where a block builder on Ethereum builds a block, takes a bunch of transactions, makes the block out of it, and then submits it to the chain. The only difference between a regular block builder and a super builder is that a super builder builds blocks across multiple chains at the same time. And so what you get with that is that,

**Nick:**  
is the ability to have atomic execution of transactions across chains. So, like I said, the ability that you have on just one chain, a single L1, like Ethereum, for example, for two apps to communicate synchronously, to have composable actions between them, you can have between two apps that are on different chains, so long as they share the same super builder. And so that's what we're building out. We also have a shared sequencer called Seq,

**Nick:**  
but we can also plug into different sequencers or interoperability protocols or anything like that to enable atomic execution between all of them. Really the thesis behind it is, we're gonna have a bunch of different fragmented things at different levels as well. Like it began as fragmentation of chains specifically. So there's a bunch of chains and then there's no good way to communicate between all these different chains. L2s for example.

**Nick:**  
We created so many L2s, but there's no fantastic way to communicate between the L2s. So then we created different interoperability protocols. And there's a bunch of different interoperability protocols that you have in the super chain or in that ag layer or orbit or all these different ecosystem specific interoperability protocols. But the problem is you're just creating more fragmentation just between different interoperable solutions.

**Nick:**  
So what NodeKit can provide and what Superbuilders can provide is atomic execution that not only unifies chains, but can unify ecosystems of chains as well, providing true global composability rather than being siloed off in our own ecosystems. So that's a little bit about us. I'm sure we'll talk a little bit more about it, but also excited to be chatting with Union today. So I'll lay it up for Karel to take it over.

**Karel:**  
Yeah, I'm not sure we're gonna be able to follow up your amazing description of NodeKit, but Union is basically one of the interop protocols you mentioned, except we're completely ecosystem agnostic. So we don't require to be the center as a super chain or like with Polkadot for chains to opt into XCM and a specific stack. We kind of support almost anything that's out there. So really give builders

**Karel:**  
full sovereignty in what they want to build, what they want to use. So they don't need to give up their sequencing. They can use whatever execution layer they want to use. And on top of that, we facilitate this in a trust minimized way, which means that the protocol itself doesn't rely on Union branding, an Oracle or a multi-sig relay or anything like that. If Union Labs disappears, the Union itself will still function.

**Karel:**  
which is something that we really pride ourselves in. At its core, we generate ZKPs to facilitate the secure transfers and allow anyone to settle those two different chains. So basically, any party can generate one of the ZKPs and send it to another chain to submit a batch of transfers. Even technically, you could generate them in your browser and self-relay your transfers, which means that Union is about as decentralized as you

 can get. Right now.

**Karel:**  
really focused on actually going to mainnet. So I'm sure a lot of you guys have played around with our test nets, as well as supporting some new networks. We have a new one coming out probably next week on test nets.

**Boris:**  
Thank you guys, really amazing introductions to your projects and also how you're approaching interoperability. I am definitely not an expert in interoperability, but I had a lot of fun recently sort of digging into the topic, exploring how both of your projects are approaching this. The other small blog post about our partners, which include both of you, who are trying to solve interoperability. So a quick intro to Align. We are a ZK verification layer for Ethereum.

**Boris:**  
I'm not going to get into what CK is exactly, but I will say a couple of things that I think are relevant to just get everyone on the same level here. Basically, zero-knowledge proofs, CK. This is a cryptographic primitive that has two parties involved. We have a prover and we have a verifier. The prover is generally a proof of some computation, and verifier is verifying that proof. This has some really great properties, very sustained. Basically, you can just verify that the computation was done.

**Boris:**  
correctly without needing to re-execute the entire computation. So this property is very important. And I think a lot of you listening are probably familiar with the idea of ZK rollups, which are basically using the ZK to allow transactions to be done off-chain on a rollup, and then have that state-proof verified on, for example, Ethereum.

**Boris:**  
Something that's probably important to mention is that verifying these proofs on Ethereum is actually a really big bottleneck. The cost of verification is very high. What I mean by this is it's computationally expensive, which means it costs a lot of gas. And basically Aligned exists to find a much faster, much cheaper, and more scalable way to verify zero-knowledge proofs on Ethereum. So Ethereum can continue being this kind of settlement layer, not only for assets and account balances, but also for proofs.

**Boris:**  
So interoperability solutions are one of the many use cases that we're excited to bring very cheap and fast CK proof verification to. And it's great to have two awesome projects here today to talk about ZK plays and kind of their master plan. And it's also, I think, what's interesting is that you are kind of approaching interop in different ways, one on one hand we have NodeKit with sort of shared sequencing and block building that allows composability, and then we have Union's more like interchain messaging.

**Boris:**  
So with that kind of introduction here, either of you guys, if you want to go first, I mean, if you think you can jump right into the role that ZK plays in, I mean, Karel, you already mentioned this, but if you want to expand on that a little bit, ZK in the context of Union, I'd love to hear more.

**Karel:**  
Yeah, of course. So in the lifecycle of a user transfer, we have really two components in UnionStack. One is where the edge of transfers, so many users, many packets, many messages, are all verified by a single CKP. And then after that verification is done, the messages themselves are supplied through storage proofs. That has really nice scaling behavior. Because if you look, for example, at

**Karel:**  
XLR or Layer 0, they verify messages individually. Well, with UnionStack, because we use ZK, we can basically verify an arbitrary amount of messages, like hundreds of thousands, basically, with a single CKP. However, if you're going to wait until you've accumulated hundreds of thousands, the latency will be quite high. So the actual number is lower. I think right now, in Testnet, each CKP we submit does something like 30 transfers.

**Karel:**  
With interop, there's one thing we all want, and that's to make it fast and cheap. So there's two things we really look at within Union, and that is one, how fast can we generate our CKPs, and how cheap can we make this on-chain. Now, don't hold me on this, but I think right now on the verification side, we spent about 400K gas in total to verify a batch of transfers, and off that, there's about 200K for the CKP. That means that if you use something like Aligned, you actually have a significant cost reduction.

**Karel:**  
about 50% on your verification, which all of a sudden makes Union from quite a price competitive one, but not the cheapest intro protocol to actually one of the cheapest out there regarding on-chain gas costs, while not losing anything out security wise. So to us, this isn't just like a fancy tech or cool buzzwords that we like to throw in, it actually makes a lot of sense for our end users and the protocols using us to leverage this type of technology.

**Boris:**  
I love that you mentioned that. And something that I maybe want to add is that, and I'm not trying to sit here and chill this, but this is exactly the kind of use case that we have in mind. Um, as we're building aligned, we're actually undergoing audits right now. So hopefully we'll have mainnet soon, but our fast mode, which is an eigen layer AVS, I mean, basically the more proofs that are submitted into a batch to be verified at once. Um, basically what happens is the, the on-chain verification cost gets

**Boris:**  
amortized. If you have 100 proofs going into this one batch, verification cost will be one hundredth of the cost of verifying a single proof. So we're working with sort of like projects that can use scale and allow your users to do as many transactions they need at a super low cost.

**Karel:**  
Yeah, exactly, and at least on the union side, like founders on the Cosmo side, so actually like Peacock, and Epchains, Blockchain, State Machines, but in the end kind of believe in...

**Karel:**  
Horizontal scalability is the main mode for scaling crypto. We don't really believe in one global computer to rule them all. But the thing is, if we build the world around thousands of blockchains and robots existing, we just cannot be spending 50% of our block space on what we like to call system level messages, or interop and such, all of these chains communicating with each other. We need a good way to amortize this cost, right? And ZK really so far is the only way.

**Karel:**  
to do this to get the scaling behavior and make sure we don't drown in fed monolithic chains spending all of our block space on just verification of interop messages.

**Boris:**  
Totally. Love to hear it. So Nick, NodeKit, I want to hear more about your simplest communication between blockchains, the shared sequencer, the super builder. My understanding is that we're going to be working together to help ZK Rollups that are part of your shared sequencer or your super builder, basically, you know, slow on Ethereum, much cheaper and much faster. But I wonder if you can expand on any of that and give us a little more insight into how that whole setup works.

**Nick:**  
Yeah, absolutely. So we at NodeKit don't do any of the ZK part of it. That's what we're outsourcing, and that's where we use, that's where a line comes in, is we're providing synchronous communication between chains, but there's no real sense of settlement within that, within a shared sequencer, or a super builder, or a super builder plugged into a shared sequencer. There's no sense of settlement. And that's what something like...

**Nick:**  
a line there can actually provide is the ZK proofs behind our synchronous communication that provides further security to ensure that the cross-chain transactions that are being guaranteed are actually transactions that should be executing and are executing on the chains that we're sending messages to. So an example of this would be if a user wants to bridge from chain A to chain B and they want to use a node kits super builder and they want to have it.

**Nick:**  
be secured by ZK proofs as well. Then they would create a bundle of two transactions. They would burn on one chain, mint on the other chain, and then they would send that bundle to NodeKit for the synchronous communication atomic execution across the chains. But we would also route the bundle to a line layer and allow for the ZK proofs of those bundles to be of the transactions.

**Nick:**  
to be generated so that the user can be certain that the transactions that they're doing across those chains are valid and are safe so that they can have more surety around the execution of the transactions rather than just sending it off and trusting some entity within the Javelin network of builders.

**Boris:**  
Gotcha. So let me make sure I'm understanding this correctly. I mean, the sort of value prop here is that using ZK, users can be guaranteed some sort of faster finality of these transactions. They'll be able to verify this on Ethereum or read the verified proof, or that the proof has been verified on Ethereum and kind of use that in downstream apps or some sort of smart contract logic.

**Nick:**  
Yeah, exactly. Exactly. Just providing proofs behind the actions that we're taking, more or less.

**Boris:**  
Very cool. So I'm curious, I know that you guys launched Javelin recently. What's your roadmap and timeline kind of looking at all that?

**Nick:**  
Yeah. So most recently we just announced that we're expanding out Javelin. So before we had Seq, which is our shared sequencer, and Javelin only

 plugged into Seq, but now we're expanding it out to plug into everything else.

**Nick:**  
any chain which is centralized, decentralized, any sequencer, anything like that. So right now we already had the demo built out a couple of months ago. You can go back, scroll down on the Twitter to go and find that of synchronous single block bridge transaction across chains. But right now we have an internal DevNet going actually, a little bit of alpha in that one and working towards getting the private DevNet as well for some of our partners.

**Nick:**  
Hopefully going to get a test out here sometime within the next few quarters. So really excited about that, but stay tuned for more on that.

**Boris:**  
Super cool, super cool. And of course, I don't think I need to say this to everyone listening, but of course, you know, give these projects a follow and keep updated because they're working on super cool stuff and they post really good content. Great branding, by the way, I just saw the new NodeKit branding the other day. Looks awesome.

**Nick:**  
Thank you, appreciate it.

**Boris:**  
For Union, that like movie poster you guys did, super cool. We were talking about it in our internal Slack a lot. We're like, we love it.

**Karel:**  
Yeah, it's so funny. We recently have a new guy who joined just full time, actually, ex-military, now turned designer. And he actually whipped up the first version of that in about two hours. And we were just amazed by that, because we're, to be honest, all devs who took a design. So just seeing someone actually build that, I feel very cool.

**Boris:**  
That is awesome. Well, since we're showing our designers some love, we have Damla listening in. She is our extremely talented designer behind all of our visual identity.

**Boris:**  
and all the stuff you might see Aligned posting. So, shout out to Danla. Okay, cool, cool. So, this is, I mean, I think we've covered a lot of the key points, right? Like interoperability is obviously important for blockchains to reach mass adoption, for crypto to reach mass adoption. Fragmentation of liquidity and everything else is a huge problem that I think anyone who's used a bunch of different roll-ups and done crypto stuff is well aware of.

**Boris:**  
something I'm really well aware of.

**Boris:**  
There's a lot of ways to approach this and I want to ask both of you what you think of this whole chain abstraction narrative that is really picking up steam. How do you see your place in that context? There's a lot of stuff that's going to be happening in the near future about this and Twitter Space is planned. There's been stuff at recent conferences, but I'm really curious to hear your takes on chain abstraction and where you position yourself in that world.

**Karel:**  
Yeah, I think in general, at least what I've observed is that builders that build app-specific chains or app-specific rollups have a real competitive advantage and mode over others. If you build a state machine specific for your product, it's just going to perform better than smart contracts. So it almost seems like we're moving to a world where, in the end, most products will become kind of like microservices, all doing their own specialist thing and communicating with each other. And Union's role, we're looking forward to be here.

**Karel:**  
is to be kind of the Kafka, the decentralized message queue between all of these individual microservices. Because in the end, what you want is for this swarm of individual services to feel like one whole, to feel like one basically big monolithic chain that's just scaled out horizontally. So to me, this chain abstraction, what I see is almost a message format for this decentralized queue. How you communicate the types of messages that you send.

**Karel:**  
And as it turns out, DeFi is very structured, right? Like we do loads of swaps, we do LAMs, LPs, stakes, unstakes, et cetera. And that's very close to DTCC, which is kind of used in the threat firewalls to do almost the same, just send structured messages between different financial institutions to be executed. And so that at least is where I think most interop is actually going to move to, just sending these structured messages across the stack.

**Nick:**  
Yeah, much agreed there. Chain abstractions are really cool and a very natural fit for somewhat of the modular ecosystem where you have too many chains doing too many things across too many different places. You need a way to keep track of it and make it so that the users aren't afraid to interact with crypto because we have too many things going on on too many different chains. The way we kind of fit into it is by providing communication between the chains.

**Nick:**  
on the backend, we can kind of provide the synchronous ability to not notice what you are, what chain you're on from a DevEx perspective. So where you can have a wallet kind of focused on the user experience, not marking what chain your assets are actually on, we're providing the backend experience for that to enable the bridging of tokens or the moving of assets across the different chains and allowing for the true...

**Nick:**  
opposable feeling of a single chain across multiple different chains at the same time, which is the underlying goal for all the projects working towards chain abstraction at the moment.

**Boris:**  
Thanks guys, that's very insightful. I think I completely agree. I had a lot of fun going down the whole modular blockchain, rabbit hole, ZK rabbit hole, better understanding everything that's going on in space and how we can ultimately use this to build better apps for people. So all the main points that I think I wanted to cover, we probably got through and we have a bit of time still.

**Boris:**  
We don't need to drag this on for a super long time, but we have almost 50 listeners in the audience. So if you guys are okay with it, I was gonna say we can invite people up if they have questions. If anyone has some questions in the audience, yeah, Nick, you're cool with that. Sweet. If not, that's also fine. I mean, I have tons of things I'd like to ask both of you, just like jamming on the state of the modular ecosystem and interop and the competitive landscape here, because I'd like to nerd out on this.

**Boris:**  
So I can definitely keep talking, but let's see if there's anyone in the audience that has any questions.

**Boris:**  
Well, if not, then I do have maybe one more question, kind of open end, big picture kind of thing. I want to ask both of you. I'm really curious to hear what kind of apps or services or products you are most excited to see built using what you guys are building.

**Karel:**  
So on the Union side right now, we're actually shortly announcing our grants program for different builders to start building specific products. Really what I want to see more is, and sounds very dumb because we already have a few of these, but they just don't work that well yet on existing infra, the kind of cross-chain dexes and such. Because I overall like have kind of fast bridging right now with the Union with other products as well.

**Karel:**  
But still need to figure out the whole ecosystems before I can start doing what I want to do there. I'm not just transferring USDC, but I'm figuring out how to buy stars first, that type of thing. So making that experience a little better, I think, will unlock a lot of use cases, such as me being able to ape into a polymarket clone much quicker than I can right now.

**Nick:**  
Yeah, definitely. I think like the cool thing about what we do, both NodeKit and Union, is that we're enabling what was previously able to only exist on a single chain across every single chain. And with that, you know, what actually led to DeFi Summer, you know, the real ramp up of Ethereum. And basically, the reason that we're all here is the ability to transact

**Nick:**  
quickly between different pieces, different apps that all exist within the same chain. And now with the ability to expand out to multiple chains, I think the things that we're most excited about seeing is just the Cambrian explosion of new use cases that are going to be building out with cross-chain and composability at their heart.

**Nick:**  
So yeah, I think absolutely like a DEX is a perfect example of where you're gonna see a ton of UX improvement for going across chains where instead of having to trade against the liquidity that only exists on your chain you're trading against the liquidity of All crypto because you're able to access the liquidity of all of crypto all at once I think that's like a great example of what's actually what the underlying thesis here is is the

**Nick:**  
unification of everything and everyone from everywhere with still the ability on the chain level to specialize and provide different user experiences and provide different developer experiences. So you're never actually abstracting away chains as a concept, but you're abstracting away the headaches that users face with interacting with different chains. And I think that's an important differentiation for the.

**Nick:**  
when we're talking about chain abstraction and what we're building out on top of it, which is that you're only abstracting away the chain from the user perspective, but you're still able to have specialization at the chain level to improve user experience and aggregate all the liquidity, all the users across multiple different chains and compete as a smaller chain without the need to bootstrap liquidity because it can be on a composable network from day one.

**Boris:**  
Love those images guys. Something that you both mentioned that I really want to echo because it's very important to us here at Al

igned is the importance of developer experience. I think we all agree that we need more developers building on blockchains and that's how we're going to see internet scale apps, blockchains as their underlying infrastructure, which for obvious reasons is a good thing. Developer experience, making it easy for builders to create new things. We're here for it.

**Boris:**  
For any devs listening, if you're ever looking at our docs or anything that we have, experiment with a testnet and you have feedback, we would love to hear it. It's part of my role to gather feedback from the ecosystem and make sure that we are providing the best product, best service for you. So yeah, I guess we can probably wrap up now. I want to thank all the listeners for joining in, and of course, Nick and Karel for joining and sharing your views and stances and opinions and some alpha.

**Boris:**  
around interoperability and how we can create a better user experience in the multi-chain future that we're already living. Congrats on all the recent announcements. Good luck with everything else. You guys have any closing notes? Go for it, but it was great meeting you and I'm hoping to see you around at some conferences soon.

**Nick:**  
Thank you so much for having me and excited to continue building with you guys.

**Karel:**  
Yeah, likewise here. And I'm excited to keep building out. We're all, you know, trying to solve the same problems and doing it different ways. So it's exciting to see. But the grants program Union has, sounds like an interesting one. So you guys go check that out for sure.

**Boris:**  
All right, thank you everyone for joining. Catch you next time and have a great rest of your day.

---
