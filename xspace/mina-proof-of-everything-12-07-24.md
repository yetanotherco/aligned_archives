Date: 12/07/24
Title:  Mina Protocol - Alignment of the proof of everything 
Links:  https://x.com/alignedlayer/status/1811777020159729839 

---

02:29 Boris: Hello everybody. Just wanted to see if you can hear us clearly.

02:39 Boris: This is Boris.

02:50 Boris: Nice, gotta get thumbs up from 01 Labs and some of the listeners. A lot of thumbs up. Awesome, thank you.

03:03 Boris: Filter and when it started shortly.

04:13 Boris: We're gonna get started in two more minutes, everyone. Just give people a second to see the notification and join the space. Just hang tight.

05:35 Boris: Alright everyone, welcome. Thanks for joining us today. My name is Boris. I'm gonna be moderating this conversation from the Aligned account today. Next to me here we have RJ, one of our co-founders. Also joining us today we have Diego, our head of research and co-founder, and from 01 Labs and Mina we have Brandon. So I guess we're just gonna get started. Maybe, Brandon, how about you?

06:02 Boris: We're going to do some introductions for every person quickly, just whatever you think is relevant, whatever you want to share with people for those who might not know you. Cool. Hi, everyone. Can you hear me? Okay.

06:17 Brandon: Just checking you can hear me before I, okay, thumbs ups. Right? Before I talk into the void. Cool. Yeah, so I'm Brandon. Hello, everyone. I'm a founding engineer of 01 Labs. And at 01 Labs, we built Mina and we still build Mina. Sorry, I was a founding engineer. Now I'm CEO.

06:47 Brandon: That's important. But yeah, I love Mina. Mina's cool. We're gonna talk about it. That's my intro. Awesome, thanks. Thanks, Brandon. Maybe we'll have Diego hop in next and give a little quick intro. Yeah, hi everybody. I am co-founder of Aligned. I'm head of research. Before that, I was head of research at Lambda class working on different topics.

07:16 Diego: of cryptography and I've been following the development of the Bridgehead lambda class more on the cryptography side of things. And so this is a partnership and everything that is very important for me because I also like a lot. I mean, a protocol, the first time I learned about the technology and the things they use, it was like, wow, this is cool. So excited for this.

07:49 Boris: Thank you, and now RJ right next to me. Hi, everyone. Thank you for joining us. My role is to do a little bit of everything that needs to be done in the company. But I'm yeah, I'm technical as well and I love ZK. So Mina, of course, was one of the first things I saw in the space that was used in ZK in a very unique way. I'm extremely happy to partner with them and explain more what

08:18 RJ: what are our plans with this technology and the community. Thanks everyone. That's yeah, that's awesome. So, I mean, I feel like our audience here today probably has a pretty good understanding of Mina and Aligned or at least one or the other. So I think a good way to start this off is maybe to have you Brandon just give like a quick intro to Mina, you know, a couple of lines and then.

08:44 Boris: I think more importantly, maybe more exciting for people here is if you could talk a bit about this Berkeley upgrade that just happened, what it means for the protocol, why you're excited about it, stuff like that.

08:57 Brandon: Yeah. Okay. So really quickly, Mina protocol is a, a decentralized layer one blockchain. That's like legitimately decentralized. And it achieves this by rolling up everything in the world into one little proof.

09:27 Brandon: And I'll leave it at that. And yeah, and I guess like, so Mina launched on main net in 2021. And really recently, God, I don't even remember, two months ago, maybe even one month ago, the Mina community recently executed like a major, major, major hard fork, which called the Berkeley upgrade.

09:56 Brandon: And what that's enabled is the deployment of ZK apps into Mina, into this one single proof of everything, which are, and ZK apps, they're smart contracts that have, like all of their sort of logic is controlled through predicates described by...

10:25 Brandon: ZK circuits at the application layer. And so with this upgrade, with the ability to actually deploy full ZK apps, we think we've unlocked a real kind of global database of true statements that all interact with each other in interesting ways. It's like...

10:54 Brandon: things that are composable, verifiable, or usable, we've created this, like, we've expanded this world of this, like, super decentralized rolled up ZK blockchain thing and made it a super decentralized rolled up computer that can do anything.

11:25 Brandon: So I'll leave it at that.

11:28 Boris: Yeah, that's really awesome. We have so much respect for the work you guys have been doing, real OGs and ZK, and this sounds like a really big deal. So congrats on the upgrade. We are really big on verifiable compute and believe this is the future. So I think maybe a good thing to do now is to pass the mic back to RJ to give a bit of background on the lines as well. What is Aligned? What problem it's solving? And then after that, we'll go to Diego to maybe talk about some of this and how it relates to...

11:58 Boris: to Mina. Yes, thank you. So a line layer is a ZK verification layer, or a building is an infrastructure for Ethereum that can help verify any type of zero-knowledge proofs for cheap and fast, meaning we are designing something new with the sole purpose of only verifying zero-knowledge proofs. This is important for us because we have noticed that many different ZK technologies actually struggle with this.

12:26 RJ: with being in trouble with Ethereum or actually being able to access to verification for a long term. So with our background in ZK, we realized that there was a need for a new ZK infrastructure that can help Ethereum actually be a better verifier for all of these ZK proof applications. And of course, one of them is a bridge like Mina, which Mina has a great technology, but it had some difficulties making it very

12:56 RJ: interoperable with Ethereum, not because of Mina itself, but more because the EBM and Ethereum is not flexible enough to make this work correctly. So, yes, our goal is to build a new security infrastructure with the sole purpose of offering the best place to verify your proofs on Ethereum. Thank you, RJ. And so there's a lot of reasons why you would want to verify zero-knowledge proofs on Ethereum.

13:26 Boris: We really believe that Ethereum is one of the best places to create new technologies and we're big on decentralization. An important part of this is interoperability with other blockchains that also have innovative technologies and cool features. So Diego, I know you were involved with this during your time at Lambda. Can you maybe talk a little bit about verification costs related to bridging and some of the challenges that you saw when the team was working on that?

13:56 Diego: Yeah, sure. So first you have to know that Mina works with a very efficient construction, which is PICLs to deliver incrementally verifiable computation. Okay. And the underlying proof system is Kimchi. Okay. The problem is that even though this construction is super efficient for Mina, the problem is Ethereum does not support

14:25 Diego: the operations needed like natively in the EVM. And so the cost you have to pay to verify these proofs is like enormous. So to avoid this, if you want to verify these proofs, which is the way of getting the correct state from Mina, what you have to do is then do some sort of wrapping, okay? Use like proof recursion to change the proof built with kimchi.

14:53 Diego: to something which you can verify cheaply in Ethereum. Okay, but even with that, the problem is still that the costs remain too high. And it takes like a lot of time because you have to do a lot of elliptic curve operations over non-native fields, okay. And so even with general purpose ZKVMs and everything, this still takes like...

15:23 Diego: a lot of time. So you have that and also once you have like the correct state, you have to kind of show, for example, your balance or the state of your account. And Mina uses Poseidon hash, which is really good for ZK applications. The problem is that again, you don't have Poseidon hashing as a precompiling DVM. So it is like super expensive. So you find the

15:52 Diego: the problem that you need to verify proofs, okay, and do like maybe some changes to make it friendly with Ethereum. So, how can we solve all these problems? Well, clearly, if we don't run on top of the EVM, we don't have all these limitations. And so that is what we did with Aligned. Okay, so we have a decentralized

network of verifiers.

16:21 Diego: that is secured via risk taking, okay, in what we call the fast mode. And each of these verifiers is going to run the verification of kimchi proofs without any need of any wrapping or anything, just like any node in Mina would do. And with that, we can then sign the message containing that the verification is correct. And then we can query the result.

16:50 Diego: to Ethereum, okay, and know that in fact the proof has been verified by a line. So this way we avoid all the complicated steps in the process and we can do it for a much lower cost, okay. So thanks to this effective batching that we have, maybe you can do it for much less than it would take you to do it in Ethereum.

17:21 Boris: That's awesome. Thank you, Diego. Really good summary. So Brandon, now that Aligned is, you know, is working with you guys to build this bridge. Could you maybe tell us why you're excited about this bridge? Why it's very important, what it enables, you know, what it means for the community? Yeah. Well, yes. And I'll work my way towards saying why I'm excited about the bridge.

17:46 Brandon: And just a bit, because I didn't have a chance to say why I'm so excited about Aligned in general. As Diego said, our team and myself are also aware of the difficulties in getting our proof system into the EVM. And moreover, this is a common problem with any kind of ZK.

18:16 Brandon: with most like ZK proofing systems, they're very specific for solving whatever task at hand they are. And, you know, and as like more and more people are building interesting projects with ZK, like, of course they want to be able to like talk to Ethereum. And so like aligned as a project is amazing. And the thing that I find so interesting is like, I imagine that like

18:46 Brandon: most of the projects that are going to work with Aligned, they're people building individual applications or they're projects that are solving a specific problem because they have a proof system for some use case, whatever. But the cool thing is because Mina itself is a proof, the whole blockchain is a proof, we can use Aligned layer, which is this...

19:13 Brandon: platform that makes it super easy for proofs to get onto Ethereum to get the whole of Mina onto Ethereum. And that whole concept is just really cool. So I just wanted to get that in. And yeah, and of course, practically what does that enable? If the whole of Mina can get onto Ethereum, it means Ethereum is a full node of Mina. Or sorry, Ethereum or...

19:42 Brandon: Ethereum can run a full node of Mina through aligned. So, and that enables bridging. And then here we are. Okay, so yeah, so of course, like bridges are so important in any kind of, like in any pairs of blockchain systems, but especially connecting to Ethereum is so important because Ethereum is, you know, a huge, like.

20:12 Brandon: source of attention, activity, applications, developers, liquidity, it's where a lot of people are. And MENA is really great at doing a lot of things with ZK. And what this bridge can enable, besides the obvious things around like...

20:42 Brandon: getting liquidity between the chains, which is super important. It's a full ZK state bridge. So any state from Ethereum becomes available on Ethereum and that lets you, well, it lets developers build an Ethereum application where one part can use Mina or

21:11 Brandon: or it lets them build a Mina application where like one part uses Ethereum. And, you know, and I'm, anyway, I've been talking for a while, but we can go into some examples too, if that makes sense. But anyway, yeah, I'm very excited.

21:30 Boris: That's awesome, Brandon. Yeah, we definitely are too. You know, it is all about the developers and these are platforms for people to build all sorts of cool things. So I want to actually go back to Diego to spend like a minute.

21:46 Boris: details that might be interesting to the audience here. Like how, Diego, could you guide us on how Align could verify Mina? Just like overview of the steps and I think it'd be cool to talk a little bit about the cost of this. Yeah, no. So verifying proofs should be really straightforward because users or whatever wants to build a bridge can send proofs using the CLI.

22:13 Diego: and we have this batcher that receives requests for proof verification. And he builds what we call a batch structure. It's simply a Merkle tree, okay, containing all the relevant information, like a commitment to the proof, to the public input, to the verified index in the case of Mina or the program or whatever you need, and maybe the sender's address, okay.

22:41 Diego: All the data gets posted to some data service. Okay, so now the service manager where the task has been posted, which is our smart contract, notifies the operators that there is a new task. They download all the information needed from the data service. They run the verification. Each verifier runs each verification.

23:08 Diego: The important thing is proofs can be from different types. Okay. And what they do, if all the proofs are correct, they sign using a BLS signature, the root of this Merkle tree. Okay. And they send it to a signature aggregator. If there is a quorum, then the signature gets posted in Ethereum, it's verified. And then the state of the batch is changed to verified.

23:38 Diego: And then you can query the service manager to get the result and show that in fact, your proof is valid. Okay. And the advantage here is we are not running on top of DBM. We can use like the native verifier from Mina. And really you can get like very high throughput, very low latency, no complicated non-native arithmetic or anything of the sort.

24:09 Diego: And yeah, the interesting part of course is that the more proofs you get, the lower the cost. Okay. So depending on the number of proofs we process in each batch, the cost can be reduced significantly. I can't give like any numbers because of course this depends on the number of proofs you get and some optimizations that we are trying to do to lower the costs.

24:37 Diego: but it will be significantly lower than, for example, the bridge we built using this wrapping and everything at lambda. Okay? And even better than, for example, using something like ROS16 or anything. So it should be simpler. We hope to have more exciting news on the development of Aligned and this.

25:07 Boris: integration.

25:11 Boris: Thank you, Diego. Yeah, really nice overview. We of course have docs you guys can all take a look at if you're curious to hear more. But I think the important thing and I want to go back to Brandon now is, so with this bridge sort of up and running and the ability to very quickly and cheaply verify proofs from Mina, this opens up a lot of possible applications and use cases. And I really, you know, you said you're excited, but I think people would love to hear what exactly you're...

25:39 Boris: excited for, like what kind of use cases or apps are you excited to see being built on Mina?

25:49 Brandon: Yeah. I mean, so one thing that's like really interesting about our platform is, you know, like, I guess it's important to recognize that it's really the first and only like general purpose

26:18 Brandon: Uh, and. Um, and and because of that, uh, like.

26:28 Brandon: it's we're in we're we're like pioneering a brand new space of like of sort of classes of applications. And and so like, so I guess I want to start by saying like I'm excited for the things that I don't even know about. That's what I'm most excited about. But that but that's a bad answer. So I'll give you some I'll give you some more specific examples

26:57 Brandon: There's the typical stuff like DeFi. I think some basic DeFi applications are important for any ecosystem. Definitely being able to plug into Ethereum and tapping into that liquidity is super, super important. So I'm really excited to see what that unlocks on that axis. There's tons of interesting things you can do with gaming.

27:26 Brandon: There's actually a game engine called ZKnoid that is doing cool stuff on our platform already. I'm interested to see what can happen if we plug that into, if we can supercharge that with Ethereum powers. There's another game engine project called Pima that's like...

27:55 Brandon: using kind of Mina as a privacy co-processor. And I think this is a, or like a ZK verifiable compute co-processor. I think this is a pattern that I'm really excited to see used sort of in other applications. And like when, you know, with the Align Bridge, like you can use Mina as this like,

28:24 Brandon: super powerful, composable, recursive, ZK, co-processor machine that you can plug into any Ethereum application

. So again, that was a bit abstract. So specifically, like, okay, what is ZK really good for? Well, one is identity. So you can do like really, really simply, you know, connect, for example,

28:52 Brandon: You can sort of make some kind of login system for a social product that's on Ethereum, but the entry point into the group is doing some crazy ZK stuff around identity that composes together a bunch of cool different things like how many NFTs you have or something about your age being under a certain amount as attested to by government-issued ID.

29:22 Brandon: the EU or whatever and combine those together.

29:31 Brandon: Yeah, and then there's the sort of, what is the way to say this? Like the ability to work with real data in the real world and compress it or like compute some view about it.

29:59 Brandon: is something that Mina's platform is really, really good at. And that's due to the fact that everything's EK, but also the fact that doing things with recursion, with recursive proofs is super straightforward on Mina. So what do I mean by this? A simple example is typical oracles would...

30:29 Brandon: post a bunch of data on chain, pay a bunch of money to do that. And then later you read that data with some other smart contract. But what you can do with Mina, for example, is you can just in real time look at a much bigger data set and get complete up-to-date information.

30:58 Brandon: compute whatever you want on that, have a proof that verifies that you're not cheating. You can build this proof up in this like incrementally, sort of incremental faction using recursion, so it's super efficient. And then with the align bridge, you can access that Oracle data on an UVM chain. So like that, that's super cool.

31:24 Boris: Anyway, I can keep going, but you should stop me. No, I'm really enjoying hearing this. I think we're very much aligned in terms of how excited we are about all the different things that can be built, the ability to verify computation, bring off-chain data on-chain, how that's used for composability. And we like to say the same thing about Aligned. We have lots of ideas, but we're especially excited for the ideas we haven't even thought of yet because...

31:54 Boris: We think that ZK really just unlocks all kinds of cool new things that we haven't thought of. I actually wanted to take a second to maybe take one or two questions from the audience if there's anybody listening who has some questions from either the Mina or Align community. If not, it's okay, but we figured we didn't want to keep this going on too long, but we have time for one or two questions. So if you...

32:22 Boris: One request to come on stage, we'll wait 30 seconds, think of it quickly.

32:35 Boris: We're just scanning to see if anyone's put their hand up. It's a Friday, at least it's the late afternoon for us right now in Europe, where we're calling in from ECC.

32:50 Boris: But yeah, no, I mean, so actually I'm gonna, I'm gonna pass the mic back to RJ now. Oh, we do have one. Okay, we have two requests. Okay, let's go with.

33:03 Boris: Let's add.

33:07 Boris: these folks on stage. Community. Hello, welcome.

33:23 Community Member: It's difficult to put dates and times on these kind of things, but do you have any kind of roadmap estimation of when you're going to get things sorted with the bridge?

33:50 RJ: Yes. Hi, RJ here. I stole the microphone from Boris. To give you a sense of our timeline, first we need to take into account that a line is to go live into mainnet. For that to happen, we are really close to completing that milestone. We are already in our third testnet with external operators that run usually APSs in IGL later or validators on Ethereum.

34:17 RJ: We started our process talking with auditors and trying to finish our code base so we can audit what we have right now in Testnet and try to get into main it in the next two months. Apart from that, we also just started working on integration with Mina to add the verifiers that we need and a team that is going to build the necessary tooling around a line to build the proper bridge. For that, we think by the end of the year we'll probably have it.

34:46 RJ: We want to be conservative on estimations because we know the community is really excited about this. But we want to be conservative so you guys can follow the journey as we build it. And once we have better timelines, we can share them. But for now, the major milestones are completing the audits, going into mainnet, and sharing with you guys as we're learning how the integration is going. We will keep you posted.

35:14 Brandon: and show you different examples and in which part of the whole process of the integration we are. And let me, can I just jump in for a second? Something that's really interesting that I think people wouldn't necessarily know, but a lot of the work, like almost all, I shouldn't say almost all, but like a huge chunk of the

35:43 Brandon: of the Lambda class bridge work. And most importantly, all of the context and like knowledge and learnings from that can be like immediately reused in the aligned bridge. Like it really is just, one way I like to think about it is it's take the original Lambda bridge project and like take the hardest part and make that part easy. And so, so,

36:12 Brandon: I guess all I'm trying to say is like, it's close. Yeah, I'm excited and we're gonna see something soon.

36:25 Boris: Awesome. Thank you, Brandon. And thank you, RJ. So we're kind of coming to the end of this and I'm going to go to RJ and then to Brandon for some closing thoughts. I mean, I guess we already covered the next steps. I was going to ask about timelines myself, but we had someone else do it. So yeah, maybe RJ, I don't know, closing thoughts, why you're excited about the partnership, anything else you wanted to share? Yeah. Yes. Thank you, everyone from the Mina community.

36:53 RJ: for joining us and thank you, Brandon, especially. We're really excited for us. It's the first big use case we're showing to the world about Aligned, and it matches perfectly with our values and also with some stuff that we have been saying for a long time regarding ZK. The tech is already here. We just need the proper infrastructure to make it more interoperable and easy to use in different places. And I think between Aligned and Mina, we can actually start showing

37:23 RJ: developers that they already have everything in place to start building these applications that can improve the internet that we have today. So for me, I'm especially excited about seeing different people from the ecosystems, both Ethereum and Mina, right, work together and build new kind of applications. We already heard from many people in the development community of Mina that they're really excited about this. And they have a bunch of ideas from gaming to...

37:52 RJ: using the tech stack for voting and other different kind of use cases. And I think this is just the beginning. So, yeah, for us, this is one of the most important things we could have built with someone else. And, yeah, it shows the true power of ZK and, in this particular case, everything that Mina has to offer and what we can offer as well.

38:18 Boris: beautifully said, RJ. Brandon, do you wanna close us off closing thoughts? Yeah, so I wanna start off and also say thank you so much for hosting us and you know, it's no secret that like it's been a long journey for Mina to have like a bridge to Ethereum.

38:46 Brandon: And it's like, it's a super hard problem. And as, as RJ was saying, like, um, without, uh, without the infrastructure in place, um, like it's, you know, it's just like, it's been, it's been painful because like a lot of people want to see a working bridge, like it's so, it's so important. Um, and, and so I'm so, I'm so, so excited that like, um,

39:15 Brandon: you know, aligned is here. Like I know it's going to solve a lot of other like important problems for other ecosystems as well. But like, yeah, I guess I agree with RJ. Like I think this is such this is like so so powerful and unlocks so much for Mina. And I think we're going to see a lot of really, really cool people, you know, using this integration.

39:45 Brandon: as it rolls out in testnet and then in mainnet. And yeah, and I'm really excited. I can say I really love the team. I love our team, of course, but what I'm trying to say is I love the Align team. It's been great working with the Lambda class folks and a lot of them are now helping out on the Align bridge. The Align people are amazing. And...

40:14
Brandon: You know, I'm just so excited that we can work more closely together and sort of, I don't know what, what do you call it? Have our like ecosystems crossover in this like beautiful way.

40:28 Boris: Thank you, Brandon. Yeah, we feel 100% the same way. It's great working together and bringing these communities together. So yeah, thank you. Thank you, 01 Labs. Thank you to the Mina community. I guess this is it for today. Stay tuned for future updates and future spaces. But yeah, thank you for joining and I hope you all enjoy the rest of your Friday.

40:52 Boris: Goodbye. Thank you, bye.
