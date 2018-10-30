---
author: dragan
layout: post
title:  "Programmer, Teach Yourself Foundations of ML and AI with these 6 Books"
date:   2018-10-27 16:50
categories: Machine Learning, AI, Programming, Clojure, Bayes, Uncomplicate
excerpt: Here's what I recommend to programmers if they want to understand machine learning. Six fantastic books that you can work with in your spare time to build yourself a solid foundation for data analysis, deep learning and the likes.
---
These recommendations are created with programmers in mind; PhD students in whatever research area might
find that something else works better for them. Contrary to usual "Top X books for Y" this is not a
top list of redundant books that cover one field sorted by how good they are. Each of these six provides
a piece of the puzzle and complements other five. If you feel you can improve the list, please send suggestions.

# Probability and Inference Fundamentals

Most problems in data analysis and AI are too complex even in theory to render an analytical solution
in the shape of a nice formula in which you can plug the data in and get deterministic answers out.
Few things in the real world are deterministic. Anything can happen, but it does not have to.
Even when we can't be certain, there are ways to discover how these random things tend to turn out.

## [Ian Hacking - Introduction to probability and Inductive Logic](https://www.goodreads.com/book/show/1446899.An_Introduction_to_Probability_and_Inductive_Logic)

Probability is (or should be!) always on the "to learn" list of a programmer entering
any data analysis related field. But how to learn it? Most texts are rather abstract and theory oriented,
either written for a PhD in mathematics, or the statisticians. Impenetrable. On the opposite side are
interesting texts written for the general public that are just too superficial. Or books and courses
that are neither here nor there; they cover the technicalities, without getting you
any wiser about what are you actually doing *and why*.

You may even accept that there's no other way than becoming an amateur statistician,
but finding the *time* to start is difficult after the whole day of programming at work.

This is the ideal book for you. Rather than for mathematics professionals, it is written for philosophy students.
There is not much math in it. No code. But, a lot of logic and common sense that programmers will enjoy.
This is a sort of book that you'll follow along with pen and paper. I'm not talking about proving theorems;
you'll be solving simple practical problems. From finding out which country a bunch of bananas comes from,
which lottery ticket to not buy, which driver did hit and run, to who James the jailed stockbroker is.

It will give you understanding to such fundamentals as Bayesian view of probability,
frequentist view of probability, decision theory, philosophical problem of discovering new knowledge,
and *induction as a cornerstone of the scientific process*.

Most of what AI does, is the automation of things that you'll learn following along with
this enjoyable companion.

## [John Kruschke - Doing Bayesian Data Analysis](https://sites.google.com/site/doingbayesiandataanalysis/)

If the previous book is strong on what and why, but a little bit too simplistic on how, this book
is rather strong on both what and how of data analysis.

John is primarily neither a statistician nor a programmer by his education, but a professor of psychology,
but his book is rather strong on programming examples, and very approachable and practical on probabilistic
and statistic fronts. It uses the R programming language, so the code is not the best example of
good programming practices, but that should not be an issue because *you, the programmer,
already know how to write good code*. You're here to learn about how probability and statistics
are applied to analyze real data on the computer, and draw logical conclusions in real world.
John excels at that!

The DBDA book is self-contained. It does not rely on knowing any advanced math, and what it requires of
probability it teaches you very gradually through practical examples. Especially if you've read
[Ian Hacking - Introduction to probability and Inductive Logic](https://https://www.goodreads.com/book/show/1446899.An_Introduction_to_Probability_and_Inductive_Logic) you'll find DBDA very pleasant to work with.

All of the examples are from the real world data analysis, contain very good motivations,
are fully implemented in R code, are plotted nicely, and, what's more important there is
lots of reasoning why each step is done. I'd say there is 0 bullshit or hand-waving in this book.
It's just pure, good, practical tutorial that teaches data analysis from Bayesian perspective.

Oh, yes, I forgot to tell you: the book uses probabilistic, Bayesian approach. That's another big plus!

While working through examples, you'll notice something that is the common thing in ML/AI software:
things take ages to compute. Even simple models will take minutes. An elegant but naive method that might
seem quite all right logically can easily take years to compute. That's the real challenge in the field:
find shortcuts that would make infinite things finite, and then shortcuts that can make finite things
feasibly brief.

[Bayadera](https://github.com/uncomplicate/bayadera), the
[Clojure library for Bayesian data analysis on the GPU](https://www.youtube.com/watch?v=TGxYfi3Vi3s)
that I develop, comes with many
[examples from this book implemented in Clojure](https://github.com/blueberry/doing-bayesian-data-analysis-gpu-opencl).
Running MCMC on the GPU, Bayadera will typically
speed up the examples by hundreds and thousands of times. And the code is in Clojure. Unfortunately,
I still haven't had time to document it. But I'll do it. Even if you can't contribute your time or knowledge yet,
you can still help me by pledging support on [my Patreon page for donations](https://patreon.com/draganrocks).

# Linear Algebra

Typically, the methods which we use to tackle data analysis and AI are numerical. You plug a large data
structure in, and the method does lots of numerical operations on that data. Naively programming this
as loops working on arrays does not work beyond toy problems. We need a way of treating a bunch
of many numbers as one thing, and operations that can work with this thing as a whole.

## [Gareth Williams - Linear Algebra with Applications, Alternate Edition](https://www.amazon.com/Applications-Alternate-Bartlett-Publishers-Mathematics/dp/0763782491)

The mathematical field that gives us the tools to elegantly work with the things that we usually hold
in arrays of numbers is linear algebra. It deals with vectors, matrices and tensors. Computationally,
we'll use optimized high performance linear algebra libraries such as Clojure's
[Neanderhtal](https://neanderthal.uncomplicate.org) to run our code
on CPU or [even GPU](https://neanderthal.uncomplicate.org/articles/tutorial_opencl.html),
rather than programming our own loops.

But to do that we need to understand how to describe our problem using linear algebra operations.
What does it mean to multiply two matrices, when would you do that, and *why*?

Programmers face similar challenge here as with probability and statistics. Most literature is not
written for programmers, but for mathematicians, so it's too abstract, or for general university population,
so it is too simplistic. In each case, it is often far removed from *the applications*.

One sort of linear algebra books I find better than others *from a perspective of a programmer interested
in AI*, are books written for *engineers*. These are serious enough to really teach you something
applicable, while still not concentrating too much on minute details of theory and proofs.
In my opinion, any good textbook that advertises itself as something in the vein of "for engineers"
or "with applications" has a good chance of being good for programmers.

The one that I like the most is this *alternate edition* of the textbook by Gareth Williams. The key
point in picking the *alternate* edition is that, rather than starting with abstract definitions
(such as vector space) and then building up towards more concrete (vectors, matrices, linear systems)
it starts from the concrete and shows you the applications and technical methods backed by lots of
*concrete* exercises right away. Then, after 100 pages, with all these practical tools under your belt,
it abstracts them to vector spaces and whatnot.

An analogy in the programming community would be to teach you first how to create and call functions
in some nice programming language (let's say Clojure), and only then musing on theoretical things
such as lambda calculus. Hey, that's exactly how how it's *normally* done in the programming world!
That's why you'll love this book!

The book even comes with examples in Matlab. But why use these when I wrote lots of blog posts
to directly accompany this book, with exercises solved with Clojure code:

* [Clojure Linear Algebra Refresher (1) - Vector Spaces](https://dragan.rocks/articles/17/Clojure-Linear-Algebra-Refresher-Vector-Spaces)
* [Clojure Linear Algebra Refresher (2) - Eigenvalues and eigenvectors](https://dragan.rocks/articles/17/Clojure-Linear-Algebra-Refresher-Eigenvalues-and-Eigenvectors)
* [Clojure Linear Algebra Refresher (3) - Matrix Transformations](https://dragan.rocks/articles/17/Clojure-Linear-Algebra-Refresher-Matrix-Transformations)
* [Clojure Linear Algebra Refresher (4) - Linear Transformations](https://dragan.rocks/articles/17/Clojure-Linear-Algebra-Refresher-Linear-Transformations)

Having acquired a fine understanding of linear algebra, you can find
[even more tutorials](https://neanderthal.uncomplicate.org/articles/guides.html) written in a similar way,
which will teach you how to apply them effectively in Clojure, using the highly optimized
linear algebra library that I develop, [Neanderhtal](https://neanderthal.uncomplicate.org).
The same code also works on the GPU, transparently.

If you've found Neanderthal useful, you might want to help me sustain its independent development at
[my Patreon page for donations](https://patreon.com/draganrocks)

# High Performance Computing (on the GPU)

Linear algebra, MCMC, and other methods used in implementation of AI software are usually
implemented in performance libraries that users don't see, and most of the time do not have
to know much about. We're programmers, though. Often, our job *is* to use these libraries in
programs that we build for the users, be it scientist tinkering with AI models, traders implementing new
trading algorithms, or consumers tracking their weight. Sometimes, *we are the ones implementing the code*.

That's why we have to learn massively parallel programming typically used to program GPUs, or
at least to understand it and to know how to effectively call code that uses it.

## [Matthew Scarpino - OpenCL in Action](https://www.manning.com/books/opencl-in-action)

In this area, Nvidia's CUDA is currently the king. Programming in CUDA is basically programming in C++
with proprietary extensions, and using Nvidia's proprietary tools. Free of charge, but still not open.
You're also tied to Nvidia hardware.

OpenCL is an open standard that is roughly equivalent to CUDA. It is supported on Nvidia, AMD, and Intel
hardware, but it has been, unfortunately successfully, sabotaged by Nvidia to stay a niche technology.
However, it is fully functional.

None of the available CUDA books, are, in my opinion, something that I'd recommend to a non-C++ programmer
as an introduction tutorial. Luckily, there is a fantastic introduction tutorial book written with
OpenCL in mind that I can recommend wholeheartedly: Matthew Scarpino's OpenCL in Action.

Matthew dedicates most of the effort to gradually teach you how massively parallel programming
on the GPU is different from everyday programming on the CPU. The book contains lots of C code (OpenCL is
oriented towards C rather than C++). While C API is more verbose than C++, it is also much simpler to
understand for someone who is not coming from a C/C++ background.

You will not need to touch that C/C++ toolchain complexity, since I implemented many examples from
Matthew's book in Clojure, using my library [ClojureCL](http://clojurecl.uncomplicate.org)!

This book looks and feels like other well-written programming books from Manning or O'Reilly, with
a good mix of higher level explanations and working code examples. Browse the TOC and see the details
for yourself. Don't be distracted by it being published in 2011; the book is aging really well! After
this, you'll be able to pick up CUDA with little effort.

There is one key thing I can add to this: a nice programming environment. Regardless of whether you
pick up CUDA or OpenCL (or both!), you'll be faced with C/C++ and its notorious build chain. It's not
something that Clojure (or Python, Ruby, Java, JavaScript) programmer would dream about.
I developed fully functional Clojure libraries for both CUDA and OpenCL ecosystem.

[ClojureCL](http://clojurecl.uncomplicate.org) is a Clojure library for parallel programming in OpenCL.
You'll write high-level Clojure
code with a tiny amount of a simple subset of C99 in kernels. Everything works from the REPL without
any of the C toolchain complexity. Best of all, you won't lose any performance;
[ClojureCL](http://clojurecl.uncomplicate.org) is low overhead
and optimized for speed.

If you find OpenCL too niche, I developed [ClojureCUDA](http://clojurecuda.uncomplicate.org).
With [ClojureCUDA](http://clojurecuda.uncomplicate.org), you'll be able to
tap into the huge ecosystem of CUDA without disturbing yourself with walls of C++ code and long
write-compile-debug cycles. Simply fire up your Clojure REPL, load [ClojureCUDA](http://clojurecuda.uncomplicate.org), and work with
it dynamically, while still claiming CUDA's full power and performance.

In addition to the Clojure companion to the OpenCL in Action, there are a few more tutorials that I wrote:

Sorry for nagging you with my Patreon donations campaign again :)

# Deep Learning

Finally, we should mention the most hyped area lately, and the thing that probably motivates most
programmers to thinker with probability, linear algebra, or high performance computing.

Once you know the fundamentals of probability and linear algebra, grasping the technical details of
deep learning is not much of an issue. Software is abundant, as well as superficial tutorials.
The challenge is that, until recently, the literature that would teach you foundations was not very
good.

There are roughly two groups:

The ones that are written by researchers, where their authors try to show off by discussing every
research topic they'd ever been in contact with, rather than write tutorials that try to *teach* the area.
After one of those, you probably won't be any wiser about how to construct even a hello world example.

The practical ones, that teach you how to classify images and similar things, but that are very
superficial on how this actually work under the hood. These are the newer ones and can be very
useful once you learn these "under the hood" things. But how?

## [Michael Nielsen - Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/)

The key to understanding deep learning is understanding how the back propagation algorithm works
*and how it is implemented*. All the books mention the algorithm, but not in a very practical
step-by-step discussion of the implementation. They may give you high-level algorithm,
and refer you to research articles, but it would be rather difficult to piece together a good
understanding of how modern high performance implementations of back propagation work, if you are
not a researcher working in the field.

This [free online](http://neuralnetworksanddeeplearning.com/) book by Michael Nielsen is an excellent tutorial that teaches the basics of both
how neural networks and deep learning are used *and how back propagation is implemented*, step-by-step.
Of course, you won't be able to implement TensorFlow, PyTorch, or cuDNN, but you'll have a pretty
good idea of the main magic behind these.

The code is in Python with NumPy and is easy to follow. You can get much better performance if
you try to implement that with [Neanderthal](https://neanderthal.uncomplicate.org).
I am planning to write a series of tutorials that will
teach how to do that and even how to optimize it and run on the GPU. I am accepting donations to
enable me to spend more working on my Clojure libraries and tutorials, including that one.

Anyway, this is a nice practical book that the programmers tend to love. It does not cover much
beyond basics of fully connected layers. It uses deep layers, but no convolutions or recurrent networks
are found here.

## [Goodfellow, Bengio, and Courville - Deep Learning](http://www.deeplearningbook.org/)

The full coverage of the Deep Learning field can be found in this book that you can [read for free](http://www.deeplearningbook.org/).
The authors are leading DL researchers,
but they were kind enough to write this book such that people other than DL PhD candidates can
learn from it. There is no programming code there, but there are algorithms, and pretty good practical
explanations. If you've read the other books that I recommended, you'll find this book just right.

I won't dwell on this book more, as it is very well known. After completing it, or better, *while* you
are reading the topics that you're interested in, you'll be able to combine it with other resources,
either research articles, or practical tutorials, and will be able to put both in context, understand
what you're doing and how you'll approach the solution.

These six books are far from capable to teach you *everything*, of course. Nor you need to read them from
cover to cover for them to give you a solid, no bullshit, foundation! With these under your belt,
no matter where you're dropped at, you'll be able to find your way.
