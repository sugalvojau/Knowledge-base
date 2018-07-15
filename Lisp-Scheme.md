Reading "Structure and Interpretation of Computer Programs" by Harold Abelson and Gerald Jay Sussman with Julie Sussman, foreword by Alan J. Perlis  
http://www.math.grinnell.edu/~miletijo/m208s15/StructIntCompPrograms.pdf  
Taking some thoughts from the book and making some sort of summary for myself here.  
  
The other important document is this one (not reading it yet):  
https://standards.ieee.org/findstds/standard/1178-1990.html  

# Foreword & Preface to the Second Edition & Preface to the First Edition

- Digital computer vs. mechanical vs. other?
- Since large programs grow from small ones, it is crucial that we develop an arsenal of standard program structures of whose correctness we have become sure — we call them idioms — and learn to combine them into larger structures using organizational techniques of proven value.
- Unlike programs, computers must obey the laws of physics. If they wish to perform rapidly — a few nanoseconds per state change — they must transmit electrons only small distances (at most 11 2 feet).
- Amongthe programs we write, some (but never enough) perform a precise mathematical function such as sorting or finding the maximum of a sequence of numbers, determining primality, or finding the square root. We call such programs algorithms, and a great deal is known of their optimal behavior, particularly with respect to the two important parameters of execution time and data storage requirements. A programmer should acquire good algorithms and idioms. Even though some programs resist precise specifications, it is the responsibility of the programmer to estimate, and always to attempt to improve, their performance.
- The list, Lisp’s native data structure [...]
- It is better to have 100 functions operate on one data structure than to have 10 functions operate on 10 data structures. As a
result the pyramid [aka. Pascal language] must stand unchanged for a millennium; the organism [aka. Lisp language] must evolve or perish.
- No Lisp program of any size beyond a few lines can be written without being saturated with discretionary functions. Invent
and fit; have fits and reinvent! We toast the Lisp programmer who pens his thoughts within nests of parentheses.
- [...] and we have rewritten all the program examples to ensure that any Scheme implementation conforming to the IEEE Scheme standard (IEEE 1990) will be able to run the code.
- This edition emphasizes several new themes. The most important of these is the central role played by different approaches to dealing with time in computational models: objects with state, concurrent programming, functional programming, lazy evaluation, and nondeterministic programming. We have included new sections on concurrency and nondeterminism, and we have tried to integrate this theme throughout the book.
- http://mitpress.mit.edu/sicp provides support for users of this book. This includes programs from the book, sample programming assignments, supplementary materials, and downloadable implementations of the Scheme dialect of Lisp.
- MIT Core Curriculum (GIRs) / common core curriculum: https://mitadmissions.desk.com/customer/portal/articles/1283021-mit-core-curriculum-girs-
- First, we want to establish the idea that a computer language is not just a way of getting a computer to perform operations but rather that it is a novel formal medium for expressing ideas about methodology. Thus, programs must be written for people to read, and only incidentally for machines to execute.
- Second, we believe that the essential material to be addressed by a subject at this level is not the syntax of particular programming-language constructs, nor clever algorithms for computing particular functions efficiently, nor even the mathematical analysis of algorithms and the foundations of computing, but rather the techniques used to control the intellectual complexity of
large software systems.
- We control complexity by building abstractions that hide details when appropriate. We control complexity by establishing conventional interfaces that enable us to construct systems by combining standard, well-understood pieces in a “mix and match” way. We control complex ity by establishing new languages for describing a design, each of which emphasizes particular aspects of the design and deemphasizes others.
- Underlying our approach to this subject is our conviction that “computer science” is not a science and that its significance has little to do with computers. The computer revolution is a revolution in the way we think and in the way we express what we think.
- procedural epistemology —the study of the structure of knowledge from an imperative point of view, as opposed to the more declarative point of view taken by classical mathematical subjects. Mathematics provides a framework for dealing precisely with notions of “what is.” Computation provides a framework for dealing precisely with notions of “how to.”
- Lisp-like languages: They have very few ways of forming compound expressions, and almost no syntactic structure. All of the formal properties can be covered in an hour, like the rules of chess. After a short time we forget about syntactic details of the language (because there are none) and get on with the real issues—figuring out what we want to compute, how we will decompose problems into manageable parts, and how we will work on the parts.
- Another advantage of Lisp is that it supports (but does not enforce) more of the large-scale strategies for modular decomposition of programs than any other language we know.
  - We can make procedural and data abstractions, 
  - we can use higher-order functions to capture common patterns of usage,
  - we can model local state using assignment and data mutation, 
  - we can link parts of a program with streams and delayed evaluation, 
  - and we can easily implement embedded languages.
- From Lisp we take the metalinguistic power that derives from the simple syntax, the uniform representation of programs as data objects, and the garbage-collected heap-allocated data. 
- From Algol we take lexical scoping and block structure, which are gifts from the pioneers of programming-language design who were on the Algol committee.
- Marvin Minsky and Seymour Papert formed many of our attitudes about programming and its place in our intellectual lives. To them we owe the understanding that computation provides a means of expression for exploring ideas that would otherwise be too complex to dealwith precisely. They emphasize that a student’s ability to write and modify programs provides a powerful medium in which exploring becomes a natural activity.
- We also strongly agree with Alan Perlis that programming is lots of fun and we had better be careful to support the joy of programming. Part of this joy derives from observing great masters at work.

# Building Abstractions with Procedures

