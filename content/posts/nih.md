+++
date = "2014-10-22"
summary = "Make. Relentlessly."
title = "Not Invented Here"
url = "/posts/nih"
+++

We’re circling back around in the dev community to talk about reinventing the wheel again. Sometimes you hear this referred to as “Not Invented Here Syndrome”.

Because I’m a white, male, 20-something, _of course_ that means I _need to_ weigh in on this. Because I have a lot of feels about it.

I’ve been criticised in the past for reinventing things. I actually gave [an entire talk]({{< relref "talks/treachery-of-hacker-news.md" >}}) about how people got mad at me for making something and having the audacity to give it to them for free. So I’ve thought about this quite a bit. And I’ve come to a conclusion:

Fuck right off.

No, seriously, take your opinion and shove it.

Here’s the thing: my time is mine. I get to use it however I want. If I want to stand on my head for hours, that’s my business. If I want to spend hours making something that has already been made, that’s my business. If I want to spend hours literally reinventing a wheel, guess what? Still my business.

And a lot of people are on board with that, but still argue that I shouldn’t _want to_ reinvent the wheel. So today I want to talk about why you should reinvent the wheel.

## Because That’s How You Learn

A lot of the hardest learned lessons of my career—the importance of testing, the importance of maintainability and ease of understanding, the importance of documenting what I do—are things I learned working on my own projects. Projects that I didn’t _really_ need to write myself, that _could_ have been accomplished through other means. Sure, I could’ve just stitched together other software to accomplish what I wanted, but then I wouldn’t have learned everything I did.

## Because Knowing How Stuff Works Is Important

Bugs, loosely defined, are when our software doesn’t work the way we expect it to. I’ve found my tendency to _read_ the libraries I use is… not what it should be. Because it turns out it’s harder to read software than to write it.

So the more libraries I use, the less I understand what my software is doing. And if I don’t understand what my software is doing, the more bugs I have, because the more incorrect expectations I have about how my software works.

## Because A Consistent Codebase Is A Clean Codebase

Libraries will not always conform to your particular conventions or styles. And usually that’s fine. If you use camelCase and a library uses snake_case, that generally isn’t a reason to rewrite the library.

But if the way you approach the problem is fundamentally different, if the library integration sticks out like a sore thumb in your codebase, it may be worth it to reimplement the library to match the rest of your codebase. People reading your codebase will have an easier time. People debugging your codebase will have an easier time seeing what’s going on.

## Because Diversity Matters

We all saw what happened when a bug was found on [OpenSSL](http://heartbleed.com/). While I’d argue crypto is a good area to avoid the NIH approach, it’s illustrative of an important point. Maybe a better example would be the relatively easier target that WordPress affords hackers.

The more people use a specific technology, the more catastrophic any bugs or security flaws are. If we start with the premise that software is going to have bugs, and _all_ software is going to have bugs, then putting all of our eggs into a single basket may not be the best idea. Much like biological organisms diversify to keep a single virus from wiping them out, our ecosystem should have several solutions to a single problem.

## It’s A Balance

I’m not advocating Reinvent All The Wheels™—I’m just saying that blanket-condemning any reinvention is harmful, short-sighted, and really annoying.

Some things should not be learning grounds, unless you’re willing to deal with the consequences of getting it wrong. Crypto, for example. Anything to do with money. Do not reinvent this unless you have ample opportunity to test your software, find bugs, and gain maturity… without putting your users at risk. Most people do not have that.

But neither should you be afraid to write software just because someone else has already written something like it.
