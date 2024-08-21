Date: 04/06/24
Title: Aligned meets Gevulot
Links: https://x.com/alignedlayer/status/1797923670670893527

--

01:09 RJ (Aligned): Hello, hello. Hi, Timo. Good afternoon. Good afternoon for you or morning? Now afternoon. We're in Europe at the moment. Thank you for joining.

01:39 Timo (Gevulot): Yeah, good to hear.

01:42 RJ (Aligned): In a second, we'll wait for a little more people to join. We'll give also Diego permissions to speak.

02:09 RJ (Aligned): Mirko, and the listeners, where’s your profile picture?

02:18 Timo (Gevulot): I guess he can’t say anything. You can emote from the heart button. He can communicate only with emojis. Yeah, Mirko is the lead developer for Pathfinder.

02:41 RJ (Aligned): Oh, OK. Also from the StarkNet ecosystem. We’re all over.

04:39 RJ (Aligned): Alright, I think we’re a couple of people now. I’m waiting a couple of minutes so we can start. Yes, Timo and Diego are here, perfect. Alright, everyone, thank you for joining. My name is RJ, I’m using the account, but I’m one of the founders of Aligned. We’re here today with Timo from Gevulot, one of the founders of Gevulot, and Diego from our team, Head of Research. And today we’re going to speak mostly about the partnership, but also I think it will be interesting to see different perspectives of how the ZK market is evolving and how both of the teams see the ZK technology advancing. So maybe first, if you want to, we can do a short intro for yourself and about your project.

05:35 Timo (Gevulot): Sure, yeah. Hello everyone. I’m Timo, the CEO of Gevulot. My co-founder is the CTO, Thomas, and we’re building what we call the ZK Cloud. It’s basically a compute network optimized for generating ZK proofs. I can say more about my background, but I’m not sure it’s that relevant for this conversation. I’ve been in the blockchain space for a very, very long time.

06:04 Timo (Gevulot): I guess that’s about it.

06:07 RJ (Aligned): Yeah, I think it’s also interesting that, similar to us, you have been working with this technology before deciding, “OK, here’s the problem. We can fix it by building new infrastructure.”

06:17 Timo (Gevulot): Yeah. That’s an interesting background. That’s true. And that is something that ties us together. So I’m also the founder of a company called Equilibrium Group, and Gevulot was spun out of Equilibrium Group last year, and I spun myself out with it. But Equilibrium Group, like Lambda Class, where Aligned is from, has been basically working on core infrastructure across a whole bunch of the different projects in this ecosystem. So I think our first ZK-related projects were with Zcash.

07:00 Timo (Gevulot): We worked for a long time with Aleo, worked for a long time with StarkNet, now working also with ZK-Sync and a whole bunch of the other ones. So that’s kind of where it came from. I mean, I guess the market has kind of changed quite a lot. And in the last year, we’ve been working on this in some way, shape or form for almost a year and a half.

07:30 Timo (Gevulot): But when we started, we just noticed that no one was really thinking about proving at all, which is again, probably fairly similar to you guys. I would imagine that you guys saw how much people were paying for on-chain verification costs and were like, “Okay, we need to do something about this.” For us, it was more the fact that there was sort of early focus on decentralizing the prover. And we see that as, or we saw that as kind of like a much bigger vector arguably for centralization than the sequencer, simply because you need more hardware. And so there is this sort of risk that if there’s no sort of distribution of that workload, it kind of just ends up all going to one party or a small group of organizations.

08:26 Timo (Gevulot): that end up dominating the space. And then we get something like our web two cloud infrastructure market, which is sort of three players that control everything. And so that’s what we’re trying to do. And yeah, maybe as a closing thought, because everything we do, all compute we do, comes with or produces a proof, it means that we can actually start to compete with centralized clouds in a very real sense. We don’t need to do re-execution. Like the sort of first wave of blockchains always had to do. We can do compute on a single node, have some fallback mechanisms and get very close or maybe even better efficiency than traditional clouds. Obviously, we also need ZK to...

09:24 Timo (Gevulot): to improve a lot to be sort of competitive. We wrote about this in a blog post we released, I think, a week ago or so called the ZK End Game, where the most important thing, I think, for the ZK space now is to lower the overhead of using ZK. And so that’s sort of the additional compute you need to apply in order to produce a proof versus if you didn’t do that at all and just were trusting of the...

09:54 Timo (Gevulot): of the counterparty or the person or organization doing the computation. But yeah, I guess that’s a slightly more elaborated background.

10:07 RJ (Aligned): Perfect. Super interesting. In which stage is Gevulot at the moment regarding this mission you guys have for the ZK Cloud?

10:13 Timo (Gevulot): Sorry, in which what?

10:15 RJ (Aligned): In which stage?

10:17 Timo (Gevulot): So we have a test network live, which we called the Gevulot DevNet. It was probably a mistake to call it a DevNet because it’s not really a DevNet. Like it’s actually a network with five, I mean, it’s permissioned and only has five nodes, but they’re running very real hardware behind it. And you can use it right now. You just need to do key registration. You can find instructions in our documentation and you can deploy whatever proof you want on there and generate proofs. I think there’s something like...

11:01 Timo (Gevulot): 30, I should probably check, 40 Provers deployed as of right now. And we’re launching something called Gevulot Firestarter this summer, which is basically a production-ready version of that. So the DevNet, while it works kind of in the way that you would expect for a user, it doesn’t really scale to a large number of Prover nodes.

11:30 Timo (Gevulot): And so we’re launching Firestarter, which will sort of still be permissioned, but will allow us to scale to potentially thousands of Prover nodes, both CPU and GPU. And so that’s where we are aiming to launch kind of our sort of formal main net, which includes kind of the economics piece and it has a blockchain to manage all of this in Q4 this year. And yeah, we’ll see where we go from there.

12:01 RJ (Aligned): OK, so you guys are moving fast. And do you, how do you see the, you mentioned the hardware, right? Regarding for the Prover Network itself. Do you guys have any roadmap or have you noticed any trends regarding which is about hardware to use for the Provers? How do you see hardware acceleration, for example, playing out in a network like Gevulot?

12:28 Timo (Gevulot): That’s a difficult question. I mean, there’s a lot of trends. One clear trend that seems to be happening now is people are moving much more aggressively to GPUs. So like if you’re a fairly new project, you probably don’t focus much on CPU proving at all. You just kind of go straight to GPUs. We’re starting to get close to having ASICs, people have been exploring FPGAs, there’s people building custom chips, things like that. So like there’s a lot of stuff happening on the hardware side. I think the difficult thing right now is that there’s like, there’s sort of no maturity on the implementation side. So a lot of the systems

13:24 Timo (Gevulot): are kind of proof of concepts. They like are running it on some server that they’ve built themselves that you can’t really like easily acquire more of and so on. There’s some things where like a specific, you know, GPU is good. And then some others where it’s like not as good. There’s like no standardization, I guess, across the hardware stuff yet.

13:52 Timo (Gevulot): And that’s hopefully something we’ll be sort of by proxy helpful in, because we kind of do define a standard of hardware, both from a performance and cost perspective on our network. And if people start kind of targeting that, then we should start getting much more kind of standardized setups.

14:19 Timo (Gevulot): And hopefully at some point people when they’re implementing Provers don’t really need to think about the hardware and they don’t need to build servers or anything like that. They can just immediately go to Gevulot. And so it should be quite a lot easier in the future. But I’d say TLDR is right now the hardware software. I don’t know the the the general I don’t know it’s it’s very messy. So every project has their own thing and.

14:49 Timo (Gevulot): It’s, they’re all quite different.

14:52 RJ (Aligned): Everything is still very new and there are no standards, but it’s interesting to see that the only thing that has been clear is that things have been accelerating regarding zero-knowledge research and also the software is improving a lot. So it will be extremely interesting to see how prover markets adapt to the latest prover advancements.

15:22 RJ (Aligned): And regarding, in specific, you’re talking now about our partnership. How do you see the synergies between these prover networks, for example, now this new category of ZK verification layers and other parts of the modular stack working altogether? Is there anything particular that prover networks can bring to the whole modular stack?

15:49 Timo (Gevulot): Um, yeah. So, I mean, I’ve talked about this many times before as well. Um, but I think like now we are finally covering the whole modular stack, right? Like initially it was kind of DA and sequencing. Um, and then it became clear that we need something for proving. And then it became clear we need something for verification to make it at least for like the long tail, like maybe, you know, ZK Sync Era is okay paying Ethereum mainnet verification costs, but most other people are not. Um, and so I think it’s more a question of just coverage. So like, do we have an out of the box solution that works for everyone? And I think like, this is like, we are kind of one piece of that, but then so is DA and other pieces.

16:39 RJ (Aligned): Perfect. In specific about the... Regarding the modular stack, right? Regarding, for example, ZK rollups or new tech we are seeing that is emerging from Zero Knowledge Proofs, like for example, Proving Rust. Have you noticed any particular demand or interest emerging from developers or new companies that are asking for, “OK, now that you’re building a Prover Network, we’re actually using this tech,” that you were surprised by?

17:10 RJ (Aligned): You weren’t expecting this level of adoption or interest?

17:14 Timo (Gevulot): So what we have been surprised by is people’s willingness to move off of AWS. So we were kind of expecting that we would need to wait until everything is kind of permissionless and things like that in order to kind of participate in a lot of different areas.

17:39 Timo (Gevulot): But like most projects are extremely cost sensitive. So like more than we were even anticipating, people have come across or kind of realized that running their own hardware is gonna be incredibly expensive. And I’m sure that applies on the verification side as well. And so they’ve generally been much more open to using.

18:06 Timo (Gevulot): Gevulot, like even before anything is permissionless, using Gevulot as kind of a replacement for AWS, which I think is quite cool. Other things, I mean, not so much. Like, I don’t know if there’s anything else that’s sort of like been distinctly surprising.

18:28 Timo (Gevulot): I think like there’s a surprising amount of projects working on ZK-related things, I think. And a lot of them are not very visible. And we didn’t even know they existed. But after Gevulot has been available in the DevNet forum, just the amount of people that have been contacting us about using it in different ways has been pretty incredible. They’re not necessarily like new or like completely different things. It’s like there’s a lot of people that want to deploy their own kind of small rollups. There’s a lot of people that are doing co-processors. There’s a surprising amount of organizations developing ZKVMs, like completely different ZKVMs. And that’s maybe something that we’re really curious to see how that stuff progresses because there has been this shift.

19:26 Timo (Gevulot): kind of towards more generalized ZKVMs. So in a Tyco is using SP1 and Risk Zero. I think Polygon said they’re gonna be using SP1. I know there’s a whole bunch of teams that I probably can’t name all of them, but that are using Risk Zero on the backend. And then there’s like the new wave of ZKVMs like Valida and Fluent and ZKWasm and things like that. So it does seem like people are moving more towards these generalized ZKVMs. And while that doesn’t like, we kind of don’t care, like whether you’re proving some ZKVM or some ZKVM, I think that has some implications for the whole sector. Because it essentially means that we are.

20:24 Timo (Gevulot): more and more giving up on the EVM on layer two and moving towards a world where kind of layer one is EVM and layer two is probably something else. So that’s quite, quite interesting. And I don’t entirely know what to think about it. But those are the only things that come to mind.

20:46 RJ (Aligned): We have noticed the same thing. Like most of the projects we have been speaking recently for the new projects are either building new ZKVMs or exploring using these new Zero Knowledge VMs. One of the things that we have been discussing a lot that I think prover networks are going to improve as well is ZK is improving the developer experience as well.

21:13 RJ (Aligned): By now, maybe in the future, you will no longer need very technical knowledge of what exactly is the latest proofs of the old proofs. And you can just start using them by proving Rust. But it still looked like in the last six months that the developer experience was missing parts in the middle to make it extremely easy to run your own ZK application by having problems with the prover. But I think that’s what prover networks can improve.

21:42 RJ (Aligned): the experience a lot and by actually verifying things on-chain because the costs are pretty high. So how do you see maybe the future of developing these new ZK applications and how all these pieces can work together maybe and how things are improving regarding actually developing applications and launching them into the market compared to the last six months?

22:11 Timo (Gevulot): Yeah, I mean, there’s kind of a crazier long-term vision thing here, which is that maybe we don’t need explicit rollups in the way that we’ve conceptualized them. Maybe users can just run their computation or whatever through a ZKVM of their choosing and then that just gets posted to L1 and gets appended to some...

22:39 Timo (Gevulot): state that a lot of other things are appending to as well. The infrastructure is nowhere near there right now, but that seems like a possibility where you have many, many layers of infrastructure just completely abstracted away. And then that’s served to the user in some very simple way. In the short term, though, I’m...

23:09 Timo (Gevulot): I think just using something like Risk Zero is bound to be way easier for end users. It’s hard to argue that it wouldn’t be easier to just write Rust than learn Solidity. The amount of Solidity developers in the world must be, I don’t know, maximum 10,000 or something like that. And so going for having these mainstream languages is an option. Definitely will make things a lot easier.

23:39 Timo (Gevulot): But yeah, beyond that, I’m not 100% sure how it’ll play out.

23:49 Timo (Gevulot): Sorry, my kid just walked in. Give me a sec.

23:54 RJ (Aligned): No problem. It’s a good moment. Maybe Diego, if you want to ask any questions, it’s a good moment to shift the questions to you.

24:00 Diego (Aligned): Yeah, yeah. It’s super interesting that we are going to have both a very good prover infrastructure and also very fast and cheap verification. I think this is...

24:18 Diego (Aligned): enabling lots of things that we still cannot envision how much they are going to change things. But perhaps I am a little bit more interested in prover technology. And something I’d like to know is what are the best provers to use in Gébulot? Because, for example, I think that GROT16 is

24:46 Diego (Aligned): liked by many because of their short proof sizes. But the problem for proving is that you need very large keys and for each program. So I don’t know which, if any, proof system offers any advantage in the Gébulot or is going to have like a lower cost because that can also, for example, make people choose more transparent

25:13 Diego (Aligned): like Starks instead of, for example, GROT16.

25:17 Timo (Gevulot): Hmm. Yeah, that’s, that’s a good point. So we mostly like don’t care and can support anything. Like we have prover programs deployed that are on the order of like 90 gigabytes and that’s fine.

25:36 Timo (Gevulot): You can handle keys in a couple of different ways. You can either package them directly into the prover program, if that’s an option, or pass them in as inputs. Really, it’s just like, if you’re sending, like if you’re moving large amounts of data into the program as an input, it will just take a little bit longer. Other than that, it doesn’t really matter, but that would be the case if you were using any API service or whatever.

26:04 Timo (Gevulot): So we’re fairly agnostic. The main constraints are if you need to do, if your proof generation time is like, I don’t know, two seconds, then just any latency might be too much. So that’s probably the main thing. But then you really can’t be doing proving in any kind of outsourced way in general.

26:32 Timo (Gevulot): And at least so far we haven’t really seen any applications be very latency sensitive or like somewhat latency sensitive, but not to that degree.

26:45 Diego (Aligned): Awesome. Yeah, just one point regarding kind of the future that I was going to mention is I think, and maybe you guys have a view on this yourself from the verification side, but it seems to us like on the prover implementation side, there’s a lot of low-hanging fruit. Like these simply on an implementation level, these things can be a lot more performant.

27:15 Timo (Gevulot): A lot of them are maybe not proof of concepts, but not too far from that. And I think like mature implementations can be quite a lot more performant and more cost effective. So I don’t know exactly how long or like how far that will take us, but simply by getting more mature proof of implementations, I think we’ll get a lot more performance out of these things. Does that apply in any way on the verification side? I know that

27:45 Diego (Aligned): the latest proof systems at least have much lower gas costs, but I don’t know if there’s other stuff.

27:48 Diego (Aligned): Yeah, totally agree. I think that provers have a lot to prove very easily and the same happens with verification. I think that the verifier code sometimes are fast, but not as fast as they could be. Maybe because people have been

28:14 Diego (Aligned): devoting a lot of effort to reducing like proof proving time, but they tend to neglect that the verification should be like very fast because if not, the thing things don’t make any sense. So it’s been weird that I found like some verifiers that can be a bit slow to what one would expect. But I think that the use of

28:45 Diego (Aligned): smaller fields, more efficient curve operations or switching to faster hashing can lead to significant improvements. And I think that, for example, now that we have, for example,

29:15 Diego (Aligned): hashes like Keccak or Blake that are very fast on hardware and also field operations are like super fast. So I think that we’ll get much better in the coming years. And the good thing is in Aligned, since we don’t run on top of the EVM, we can optimize all the code to be really, really fast.

29:44 Diego (Aligned): and deliver a very high throughput.

29:48 Timo (Gevulot): Yeah. Yeah. It’s interesting because on the other hand, on sort of the cryptography academic side, I feel like most of the focus has been on, uh, verification costs, uh, and actually not enough focus on, on kind of improving, um, proving side of things, especially in terms of like overhead. Um, but then in implementation, they probably have, like they, they can kind

30:18 Timo (Gevulot): of assume that verification will be fast enough and maybe don’t focus on that very much.

30:28 Diego (Aligned): Yeah, it seems that what is happening right now, the trend is research has gotten really good, but now also engineering and improving implementations in general in the whole stack is going to take us to the next level. And luckily we have even more teams that are not only using this tech, but also will be requesting more features and improvements overall.

30:58 Timo (Gevulot): Yeah. I mean, I need to jump off in just a second, but maybe in closing, I definitely think that there’s a lot more to do on the engineering side. The research side, I think, has been going quite strong. But I think a lot of the implementations are, I don’t want to say they’re not very good. They’re kind of a product of their time or a product of the circumstances they were created in.

31:26 Timo (Gevulot): But they’re certainly not ready for massive scale necessarily. And I’m talking about scaling hardware primarily and making maximal use of that hardware. So that’s kind of a bad thing, but on the other hand, it means we have a lot more improvement to go. That’s quite easy as opposed to kind of...

31:54 Timo (Gevulot): cryptographic innovation or something like that, which is more unpredictable. So I’m fairly bullish that we’ll see much better performance and cost efficiency in the coming years, and especially as we start getting production volumes in ASICs, maybe in like, I don’t know, two years’ time.

32:17 RJ (Aligned): Yeah, I think we have a similar vision regarding how things will progress. And the last few months have been extremely evident that things are moving fast. And many of these things that we’re measuring are improving because they were a low-hanging fruit. But thank you for joining us. We don’t want to steal more of your time. And we’re extremely happy and excited to work more together. And we’ll probably have a...

32:47 RJ (Aligned): and our space in the future. And this space, probably both of the projects will have evolved a lot. And also the ecosystem in itself. We will see what we can speak about in the future.

33:00 Timo (Gevulot): Yeah, everything will be completely different, but it’s always nice to see more stuff coming out of like Argentinian teams. It’s our South American teams in general. You guys are amazing.

33:15 Timo (Gevulot): Thanks, thanks a lot for hosting me.

33:19 RJ (Aligned): Thank you. Thank you everyone for coming.

33:23 Timo (Gevulot): Thanks a lot. We will have more of these spaces with our partners in the future. Thank you very much for joining us.

33:28 RJ (Aligned): Bye everyone.

33:29 Timo (Gevulot): Thanks, bye bye.
