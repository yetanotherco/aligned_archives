Date: 21/08/24
Title: Intro and current state of ZK - Diego Kingston - Crecimiento
Links: add youtube

---

00:01  
Hello, happy to be here. I wanted to share with you some thoughts on this game-changing technology.

00:11  
The whole of my presentation is of course starting with what is ZK and why is it useful. Then I am going to talk about two keywords that frequently appear when talking about ZK technology, SNARKs and STARKs. And then I am going to focus on hash-based proof systems, which are what we call also STARKs, because they offer some performance advantages and things like that.

00:41  
of ZKDMs and how that improves the...

00:45  
development of provable applications and then some recent improvements, developments that have been happening that we believe will accelerate the adoption of ZK technologies and then I am going to point at some challenges that we face for mass adoption of ZK and some of the solutions we are proposing. And finally, we can do some summary and of course some final.

01:15  
questions or whatever you have. What is ZK and why is it useful? First, I am going to do the disclaimer. I am going to speak about ZK in a broader sense. Okay, ZK in fact has a more restrictive definition that goes back to its origins but over time it grew to encompass other technologies and so I am going to work on this broader definition. I am going to tell you

01:44  
a problem and how we can solve it. When you want to coordinate between different computers and you want to make sure that something happened, how can you be sure, for example, that if party A did something, then they did it right? Of course, there is one trivial way in which we can be sure, which is re-execution. Okay, what I can do is you say you ran...

02:10  
this code with these inputs and you got an answer and so I run the same, I get the same result, I check and then I convince myself about the result. Of course, the problem with that is that I have to do...

02:25  
the same effort you did. And that's precisely how blockchains work. Blockchains are verifiable computers and we get the verifiability by re-executing. But the problem we get is that the weaker devices in the network act as bottlenecks. Why? Because they don't have the same capacity to process and so they cannot re-execute as fast as the rest, so it gets bottlenecked.

02:54  
Okay? So, is there a way we can possibly do things like faster or avoid this bottleneck? Because we really want this to scale up. So the thing is, how? It happens that a long ago, like in the 90s, we had a series of results where the...

03:22  
analyze the consequences of verifying a computation much faster than re-execution. Typically, what we want is something like what we call a logarithmic scaling. That means if, for example, to do a computation I have to do 1 million steps, maybe I can verify it in something like 20.

03:45  
or proportional to 20, maybe 600. With these technologies, what we can do is then, instead of checking the computation, check this short proof. And this property that the proofs are short is what we call succinctness. What we can do then is somehow generate these proofs.

04:09  
And with that what we can do is eventually bundle arbitrary computations into these very small proofs and then verify them. And this what it enabled was the birth of ZK rollups. What we can do is move execution off-chain.

04:27  
and then submit this proof and people just verify it and since verifying is much faster than re-execution what we get is an increase in throughput. When I talk about ZKE I will be mostly referring to this thing which in fact refers more to what we call scalability. And this proofs what they show is what we call the integrity. The question is, ok, how can we build that?

04:57  
do we need it? To be able to do this verification much faster than the execution what we need is interaction between two parties, one which will be the prover which will be tasked with heavy computations and another party which will be the verifier. Of course then there are ways in which we can transform and avoid this interaction between the prover and the verifier by simulating it using a construction that is called the Fiat-Chamin heuristic.

05:27  
In this case, what we want these proofs to satisfy are two basic properties, which are called completeness. So what I want is that if somebody did things right, he will convince me with probability one that the proof is valid, okay? And another one, which is called soundness, which is that if I have a dishonest prover,

05:50  
he will fail to convince me that he did things right if he didn't. We can express it more concretely, but basically what we want is to accept all valid proofs and to reject false proofs with a very high probability. And there is this other property that is called ZK. ZK stands for Zero Knowledge. It was an idea first proposed in a paper by...

06:19  
Shafi Goldbasser and collaborators. And the idea is that I can prove to you the validity of a given statement without revealing sensitive information. Okay, one example, for example, of this kind of protocols is what we call Schnorr signatures. So when I sign a message using Schnorr signatures, what I want to show you is that I have

06:48  
in my possession a secret key. And how can I convince you that I have this secret key? Of course, one way would be to give you the secret key. But that would lose its purpose, because then you have the secret key, and you could also sign. The thing is, I can devise a mechanism where I can show you that I know that secret key, and I can convince you.

07:16  
that I have it without you knowing that. So that is what we mean by zero knowledge. Of course, we have then these two properties, one which is zero knowledge, which is mostly related to privacy. And then we have this property of succinctness or scalability, which is the one that we need for many applications in blockchains. Of course, privacy matters for other applications.

07:42  
And the good thing about having these integrity proofs that are succinct is that then we can prove that arbitrary computations were done correctly. And that that has applications, for example, even outside blockchain. For example, one interesting application is suppose that I want to show you that I have an image and that that image was taken by a real camera. It was not generated by an AI.

08:11  
Of course, when you want to publish that photo in the newspaper or something, you have to do some changes, maybe scale it down or downgrade it a bit. So how can you be sure that, in fact, that came from the camera and not from the AI? In the real image, you have a signature. OK, cameras have a signature you can get. And so you can show that that photograph came from a camera.

08:41  
But the problem is when you edit it, you cannot do that. But what if you could take the original image, say that you run some code on it, and then you obtained the new image? Then what you could do is simply show me the image, the edited image, and prove me.

09:05  
that image comes from a picture taken by a camera. Okay? And these are some kind of applications that we are going to get by having these types of proofs. So there are like two big words that we have when we talk about ZK technologies, which are SNARKs and STARKs. In fact, many people will say that...

09:32  
STARKs are in particular SNARKs, but the distinction is a bit important in terms of maybe engineering and also focusing on certain properties. So first, what do these words mean? SNARKs stand for succinct non-interactive arguments of knowledge.

09:57  
So these are not proofs, but arguments that I know what we call a weakness to some what we call an NP statement. An NP statement is simply a statement related to an NP problem, a problem which we can verify in polynomial time.

10:21  
Okay? And they are non-interactive because even though the protocol originally is interactive, we can render it non-interactive and so the prover can generate the proof by himself without need of a real interaction with the verifier. And it's like seeing because what we want to emphasize is in particular this fact that the proof is much shorter than the witness we need to prove.

10:50  
the computation. And STARKs are a bit different, they are called scalable, transparent arguments of knowledge and here transparent is related to the fact that we don't need what we call a trusted setup. So the thing is that even though these revolutionary ideas were from the late eighties or

11:19  
2013-14 that we got like bio technologies to do so. Why? Because in general what we want to do is be able to prove like arbitrary computations and being able to devise something that can prove rather arbitrary computations is complicated. So the thing is that the first constructions really relied on

11:41  
mostly on something called elliptic curves and needed a lot of pre-processing. So I want to prove you something but then first I needed to calculate like some parameters but there was this thing that I we needed like to have these parameters not be known or some secret parameters not be known by anybody because if not we could forge proofs.

12:05  
Really, SNARK started developing just more or less a decade ago, and it was with their introduction, for example

, in Zcash. Okay, and then also in blockchain, they started acknowledging this interesting part of, okay, we can scale up by building what we call ZK rollups.

12:27  
Okay, so the problem with these early constructions was that they relied on elliptic curves, that they had like some trusted parameters and a lot of pre-processing that in general made things like difficult to prove. Okay, because for example these setups originally were like specific for one kind of program. So if you wanted to prove Fibonacci you had a set of parameters

12:53  
But then if you wanted to prove, I don't know, a larger Fibonacci, then you had to redo all the work. And so it was a bit cumbersome. Of course, then they devised other methods to have what we call universal setups. Okay, and then you can prove like more general programs and you don't have to redo this ceremony. In the case of STARKs, what they devised is a strategy to avoid.

13:19  
having these drastic parameters. They rely on very simple and elegant constructions such as cryptographic hash functions. Everything already builds on top of cryptographic hash functions. So that is not a problem. And what we call linear codes. And in fact, we use linear codes a lot more than we think.

13:42  
Okay, so in this case of STARKs the good thing is you don't need to have any ceremony or anything you just are able to prove computations in a much faster way. So you have this distinction of course there are people that like more elliptic curve based SNARKs some people like more STARKs I think that STARKs what they offer

14:10  
is several advantages in terms of first not having a trusted setup, they are conjectured to be post-quantum secure and in fact in terms of performance they offer like several advantages besides you can do some other constructions designed improving like larger computations such as proof recursion more efficiently than you get with elliptic curves.

14:36  
So I'm going to focus them on these hash-based proof systems. What is the thing that makes them super efficient? First, they depend on hash functions. Hash functions are really fast to compute on hardware. They are really well understood. Then, of course, you also have linear codes. They also depend on, for example, having

15:03  
what we call the fast Fourier transform. And the fast Fourier transform is one of the most widely used and efficient algorithms that we have. And another thing that we have is that in this case, we are able to choose what we call smaller fields. Okay? So when we wanted to prove things, we have to work over some.

15:28  
what we call finite field, which is like the basic data type that we are going to have. Instead of working with bytes, we are going to work with very large integers. Okay, so when you use elliptic curves, the problem is you are forced to use one field and generally it means something like a 256-bit field. So every variable you want to represent is going to take 256 bits.

15:55  
Okay, so you want to represent a bit, no problem, but it's going to cost over 200 times more to represent it with one of these. The good thing about these cache-based proof systems is that you can go, like, way smaller, you can choose very small fields. And for example, one of the recent developments...

16:16  
that has been a game changer is precisely the introduction of circle STARKs. Circle STARKs have been able to prove nearly 600,000 hashes per second in an M2 or M3 notebook,

16:39  
two orders of magnitude more than you can prove with SNARKs currently. And that is because you are able to use a particular field which is called the Mersenne field, which has very fast computations. Okay, so that's why I am a big fan of hash-based proof systems, because you kind of reduce the overhead to represent a lot of things.

17:08  
and you can get a lot of performance gains while avoiding this problem of the trusted setup. And one interesting thing is that, remember I told you that you could prove programs. The problem you had with ZK when it was introduced was that if you wanted to prove your program you had to transform it to what we call an arithmetic circuit, which is something like

17:34  
If you wanted to compute something, you had to code it in assembler. Coding in assembler is way more difficult than coding in Python. So the problem with ZK was originally this. If you wanted to prove a given program, you had to write it in some kind of assembler. Now

17:56  
Some people thought, okay, maybe what we can do is instead of having people write each program they want in assembler, maybe what we can do is just create a ZK virtual machine, okay? And people just write code in some high-level language, for example, you write it in Rust, then you feed it to the virtual machine. And what you prove is the correctness of the execution of the virtual machine. Okay, that way the developer...

18:25  
is saved from all the complexity of having to write these circuits. You just write for the virtual machine and you just write in your favorite language and then it gets proven. Okay, and we think that this of course is going to make the development of what we call provable applications much easier. Okay?

18:55  
two years there have been several virtual machines, you have the Kyro VM, RISC0, Nexus, and the Salt, Valida, and with that what you can do is you just code in Rust, you send it to the virtual machine and you get the proof of your program.

19:15  
no more writing circuits, no more writing that. So we think that in this sense, it's like precisely developing a higher level language for.

19:26  
writing like circuits. As to the improvements, the thing is of course these virtual machines at first were perhaps not as performant. Of course if you want to build an application maybe coding in assembler is going to be faster or what you call in assembler is going to go a bit faster, but the problem is it takes like more time to develop this. So in many cases you prefer like

19:53  
is of development over performance. But the good thing is that there have been a lot of improvements that make proving these virtual machines really easy and really fast.

20:09  
So for example, we've seen the development of what we call faster lookup arguments. So basically what they allow is instead of computing something, maybe you can show that you had a table with results of valid results, and then you went and fetched the result. Then of course we have this development, for example, of certain STARKs of what we call new commitment schemes.

20:38  
or even some new accumulation schemes, okay, that, for example, what they allow is suppose that you want to prove like a very large computation. What you could do is instead of like proving the whole computation, maybe you prove one bit, okay, and you stop there and then you go to the next chunk and okay, you say, okay, my program ended here, but.

21:05  
I'm going to use this as input for the next segment, and then you prove the different segments. And you get different proofs. But then there are some techniques by which you can combine all those proofs into just one. OK? So what we are seeing right now is that the proving capabilities are going up very, very fast. I already told you that even on consumer and hardware, you can prove like.

21:35  
half a million hashes per second, which is crazy. And that, of course, is going to enable lots of new things. Of course, even though we have, or we can say that the development of ZK applications is going easier because we have these virtual machines. And so

22:00  
You don't have to understand all the low-level details, and you can just write code in Rust and then get the proof and everything. There are still some challenges for mass adoption. Of course, improvements in proving technology will continue to go on. And it's just a matter of time until we get maybe to where we would like.

22:25  
but still there is another bottleneck which is related to on-chain proving costs. So if you want to send one of these proofs and have it verified in Ethereum, you'll find that the cost is quite high. Of course that depends on the network congestion, but...

22:45  
This can mean that even for the cheapest proofs, maybe you are going to pay $4, $5, $20, $50, $100. OK? And we think that while, OK, maybe some values seem like small, maybe you don't care paying $1, $4, we still think that we have to go an extra step. What we would like is something where these verification costs.

23:14  
go down very consistently. Because then, of course, if adding ZK is easy, because you just write ordinary code and you send it to one of these VMs and you get things proven, and then you can verify it really cheaply, then you are going to find new use cases. In this sense, what we envision is that what we are trying to build is something like the broadband for ZK. So if you lived when...

23:45  
I was little and you wanted to use the internet, it was problematic because it went by phone, you could not download things the way you wanted and you were downloading something, somebody picked up the phone and it was interrupted and you had to start again, so you had lots of issues.

24:06  
But as soon as we got the broadband, we started seeing new things such as the rise of social media

, YouTube, other types of interactions. So what we think is that in this case, if we can take these verification costs down, of course people will start finding ways of incorporating this technology in ways we don't really envision. Because when we...

24:35  
build a broadband for example, nobody could foresee that we are going to get, for example, YouTube and that people are going to watch more YouTube than they watch the television. Okay, people would have betted that perhaps YouTube was not a use case of broadband, okay, or having Netflix. And so we think that people of course are going to find ways to do so.

24:57  
So at Aligned, what we are doing is trying to find precisely ways to reduce these on-chain verification costs. And we have like some strategies to do so. We have two different working modes, what we call the fast mode and the aggregation mode. And we think that with these strategies, we will see verification costs go down like by at least an order of magnitude.

25:23  
Okay, if you want to learn more, then we can continue talking after that. So the idea is that the ZK proofs, what they allow us is precisely to prove the integrity of a computation in a way that is more efficient than re-execution. Of course, this technology originally was like complicated to use because the tooling was not well developed and we didn't have a...

25:53  
the sufficient mathematical tools to do it in an efficient way. But in the last at least three years, we have seen the rise of a lot of new proof systems. For example, you might have heard of circle STARKs, or plonk, or the sort. And these have made the proving times go down, and the amount of things that we can prove.

26:23  
really go up really fast. So thanks a lot and if you have any questions I'll be more than happy to answer. Hi, great talk. Thank you for your time. I'm wondering if you've heard about ZK proof validations now possible on Bitcoin mainchain and what your thoughts are on the topic. Well that's a super interesting topic. I heard like Elevance as on has been

26:52  
wanting to add for example ZK proofs to Bitcoin a lot, I think it will help a lot with scalability. Of course already you had like the use of ZK technologies with Zcash, but I think that the point of scalability and all that was not ready yet. I am really excited. I think that it also marks a very big milestone.

27:18  
of the people that have been involved in making these technologies and developing everything. So I don't know, I am super excited about this and I know that some of the teams that are working there are the best in the world. So I don't know, I just follow the developments. Right now we are mostly focused on, in my case, in Ethereum, but I think that could...

27:46  
like benefit us all and also proves that ZK is going to reach new places that we haven't envisioned yet. Hello, thanks a lot for the talk. Maybe what I've been thinking about is a line layer and the whole discussion is based on verification, right? But how do you feel about proving? So distributed proving systems.

28:13  
Relating the proving to external actors instead of doing it on the consumer hardware? Are there any researches that you're doing on top of that? Yeah, no, you have a lot of

28:24  
developments and projects that for example are trying to build like these proving networks where you can just delegate. Of course if I am focusing mostly on the aspect of proof verification, it's because I believe that already the part of proof generation is being already like taken care by other teams. You have all the developments of new proof systems. Then you have...

28:52  
also aspects related to hardware acceleration and even the development of these prover networks. And imagine that we are at this point where you can already prove very large computations even on a consumer notebook. So that's why we decided to focus on verification because really it felt like

29:20  
It was orphaned and it was a problem nobody was paying attention to. Because everybody at first was like, okay, we have to make proving faster, simpler or not. But the problem is, okay, proving right now is already really good. It's going to get better because there are lots of teams giving new developments every day.

29:46  
But the problem is you are not going to use ZK unless it's really expensive. And that involves, of course, proof verification. So if you already see that everybody else is solving all the other problems, then it's good to get to the next bottleneck. And so that's why we targeted on verification. Yeah, that's good.

30:10  
I mean, I can agree with your answer. What I've been thinking about ZK in the latest months, I think, is that most applications are actually built around ZK. And with how much we want to merge ZK into real world usage, we have to tap into web 2 somehow, right? So we're tapping into non-ZK-friendly computations inside ZK, which may prove a lot harder, right? But we do hope that with everything that's

30:40  
in the hardware and also proving systems currently, this becomes also an issue in consumer hardware. Okay, that's good, thank you. Thanks.

30:53  
Thank you very much.

---

