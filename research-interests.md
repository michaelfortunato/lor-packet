# Research Interests

 I am interested long term in researching the following question: 
 
    How can we define system level software problems formally, and how can we use machine learning to improve the performance of systems level software?


I am interested in questions such as: 
 
1. How can we use machine learning to get compilers to perform more effective optimization passes? See [here][7] for example papers.
2. How can we use machine learning to improve how a compiler can detect and exploit the cache locality of human written software? For example
	1. A classic [one][2]: A naive implementation of matrix multiplication can cause cache thrashing, but other implementations can better use the cache. A handwritten compiler may implement the transformation to turn naive code into something cache-friendly, but that is simply a heuristic and is hand written by a human engineer. _Can we formalize the cache locality optimization problem for compilers in order that optimization algorithms, machine learning being an example class, be applied to it?_
3. Can we use machine learning to improve the performance of an operating system's process scheduler? For instance:
	1. A basic process scheduler will pause executing a process if that process is waiting on I/O. Can we define a ML model to generate such a process scheduler?  
  

Broadly, I am interested in formalizing hard to express problems in order to make them computable (like the ones above^^). 

    I have a feeling a lot of work can be done to combine machine learning and statistical modeling with classical system programming problems. That is the area in which I want to do research.

[1]: https://github.com/olgabot/sciencemeetproductivity.tumblr.com/blob/master/posts/2012/08/how-to-request-a-letter-of-recommendation.md
[2]: https://passlab.github.io/CSCE513/notes/lecture10_LocalityMM.pdf
[3]: https://www.beckershospitalreview.com/ehrs/epic-s-huge-healthcare-impact-5-stats.html#:~:text=More%20than%20253%20million%20U.S.,an%20electronic%20record%20in%20Epic.
[4]: https://gist.github.com/wojteklu/73c6914cc446146b8b533c0988cf8d29
[5]: https://www.w3schools.com/python/python_for_loops.asp
[6]: https://en.wikipedia.org/wiki/Agile_software_development
[7]: https://github.com/zwang4/awesome-machine-learning-in-compilers