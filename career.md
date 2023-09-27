# Career
I was hired out of college to be a software engineer at [InterSystems](https://intersystems.com), a technology company that creates and develops a critical, high performance database management system. Our direct competitors are MongoDB and Oracle. Our company's claim to fame is that it is the database for Epic Systems, the company responsible for holding the medical information of the majority of Americans: 250 million as of [2022][3]. 

	In other words, InterSystems develops the database that stores the medical information of most Americans.

## Role 1: Backend Developer - Created Data Profiling Tool
_Conceived of and Created A High Performance Medical Data Analyzer Application_

My first role was to investigate the cost of implementing our software and create a software solution to reduce that cost. Out of this,  I conceived of an ambitious new app that would analyze medical data from millions of sources and detect any abnormalities in that data using a custom validation algorithm that I also designed. The application would have multi-threading for high performance, user authentication for security, and task based management for audit-ability. I pitched my idea to the head of my department (there are two departments at InterSystems), and got approval to build and design the application myself. This situation was a unique for a junior or even senior developer.

As a junior developer, I designed and built the first version of the application entirely myself over a period of 8 months. This was both good and bad. On one hand, most of the other engineers worked on a team and had mentorship and collaboration. On the other hand, it was a big challenge that allowed me to demonstrate my effectiveness as a developer and critical thinker. 

The first app was good enough that a formal team was assembled to build the production ready version--of which I was the technical lead. The team's internal name was the Time To Value team.

The Data Profiling Tool was finally released this Spring 2023, and was voted by our Customer's as "Most Exciting and Likely To Use" in June at our company's annual developer conference (Global Summit).

Here are some stats about the Data Profiling Tool
1. Designed to process _large_ amounts of healthcare data: **Each profile is typically 1-3GBs**.
2. Designed to be able to query _any_ data attribute within a profile very fast--sub 500ms. Example queries are
	1. Of my 150,000 person data set, what are the unique values for patient names, how many times did each unique value occur, and which values errored? 
4. Internally the Data Profiling Tool had a well thought out, extensible architecture that I designed[4][4], which allowed me to effectively mentor and onboard 7 interns and 2 new full-times developers during my time on the application, and led to very fast growth of the product.
5. The application has user auth (sign in, sign on, and varying levels of permissions), the ability to create, update and delete profiles, and parallel programming. 

## Role 2 - Kernel Developer - Joined Core Group 
(13 developers, 10 of which have at least 20 years of experience as a compiler or database engineer working at company's like DEC, Intel, or were founding developers at InterSystems).

The core group of InterSystems is comprised of 13 operating system developers and is called the Kernel group. As the name suggests, the Kernel group is responsible for the underlying core database of InterSystems. Most members are industries veterans with advanced degrees, and I am one of the two developers under 30.

The Kernel team has a C and Rust codebase (I am writing the first Rust program), and deals in the following areas: 
1. Developing and optimizing the core database of the company. 
2. Developing and optimizing the compiler of the [ObjectScript](https://en.wikipedia.org/wiki/Cach%C3%A9_ObjectScript) language, a byte-code language most similar to Java.
3. Developing and optimizing the ObjectScript runtime/virtual machine.

### How I Got In
As I mentioned above, the majority of members of that team either have advanced degrees or many years of industry expertise. In fact, in order to join that team, InterSystem's founder and CEO decides personally who is able to work for the group and reviews each app himself.

It was my dream to join this team because of its research nature and because of the class of problems they were tackling: compiler theory and general systems development with an emphasis on research and performance. 

In order to join the team, after work I would study the entire C codebase of our company in secret. Then during one weekend, while I was still on the old team, I added the `for x in list` construct to the ObjectScript language (see Python's version [here][5]). 
Concepts I had to use were lexing, parsing, compiler optimization passes, and implementing the runtime/virtual machine for the `for x in list` construct. It was immensely rewarding to get that implementation in. 

Because of the success of the Data Profiling Tool, the direct manager of the team wanted me and we sent my app in, including the `for loop` language changes, for the  CEO to review. They were impressed with how quickly I added the new language change and the fact I did it through entirely independent research.  All of this considered, The CEO looked at my app and approved, and that is how I joined the Kernel team.

### What I am Working On Now

Right now, I am working on finding new ways to optimize the ObjectScript runtime, and am adding new networking functionality in the the our Kernel applications using Rust. I am happy to talk more about it in person. Some very basic examples of what I am thinking about are:
1. Implementing inlining compiler optimization passes.
2. Implementing SIMD optimizations.
3. Implementing for loop optimizations, including
	1. For loop fusing: (combining two for loops together into one loop if able to)
	1. For loop unrolling: Transforming  for loop with static bounds (say `for i in 1..n`, where `n` is known at compile time) to be a series of statements repeated `n` times. This transformation yields benefits in some situations.
4. Happy to talk more in person about the other optimization problems we are thinking of.

[1]: https://github.com/olgabot/sciencemeetproductivity.tumblr.com/blob/master/posts/2012/08/how-to-request-a-letter-of-recommendation.md
[2]: https://passlab.github.io/CSCE513/notes/lecture10_LocalityMM.pdf
[3]: https://www.beckershospitalreview.com/ehrs/epic-s-huge-healthcare-impact-5-stats.html#:~:text=More%20than%20253%20million%20U.S.,an%20electronic%20record%20in%20Epic.
[4]: https://gist.github.com/wojteklu/73c6914cc446146b8b533c0988cf8d29
[5]: https://www.w3schools.com/python/python_for_loops.asp
[6]: https://en.wikipedia.org/wiki/Agile_software_development