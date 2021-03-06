+++
date = "2012-07-05"
title = "On Go"
url = "/posts/go"
summary = "I’’ve been writing Go for months now. I thought at first that my fascination with it was due to the novelty of a new language. I’’m beginning to realise that Go offers something new: the ability to write code."

[quote]
attr = "Andrew Gerrand"
text = "“In Go, the code does exactly what it says on the page.”"
+++

I never went to school for computer science. I majored in English. My original goal was to teach, before I became disillusioned with the education system.

You would think that, with my background, a “softer” language like Python or (it pains me to type this) Ruby would be my language of choice. Up until the last few months of 2011, you’d be right—Python was the favoured tool in my (admittedly varied) belt. You’d be surprised—[or maybe not](http://commandcenter.blogspot.com/2012/06/less-is-exponentially-more.html)—to find that I’ve abruptly replaced it with Go.

I could wax eloquent about the beauty of [error handling](http://blog.golang.org/2011/07/error-handling-and-go.html), but people will be too busy whining about the lack of exceptions to care that life becomes exponentially easier when you’re forced to deal with errors at their root. Honestly, I love that Go discourages or disallows my (destructively) lazy behaviour. It has made me a better programmer with more reliable code.

I could write a love letter about the [incredibly powerful implicit interfaces](http://research.swtch.com/interfaces) that make duck-typing an absolute pleasure. I’ve never seen a duck-typing implementation that was so natural and easy to use. Just the other day, I was trying to check if an interface was nil, only to discover after some Googling that there is no way to do this that isn’t a dirty hack. The explanation for it, though, was what stuck with me: idiomatic Go says that any type that fulfills an interface should be able to execute any method in the interface safely, so you shouldn’t have to do that check. Just think about that for a moment. How awesome is that? Why can’t everything be that simple?

I could talk at length about the [amazing concurrency primitives](http://www.youtube.com/watch?v=f6kdp27TYZs) (warning: YouTube link) and how they make concurrent programming *fun*. In a multi-core world, these primitives are incredibly important and incredibly powerful. I truly believe they deserve their place as Go’s flagship feature.

I could talk about all these things, and I often do. They’re the responses I give when my peers (and my betters) ask why I use Go, and for good reason: they’re things those people can relate to. They’re the lazy explanation. They’re objective metrics that developers can compare to their current language and can easily conceive of use-cases for. In other words, they’re easy to evaluate, because they deliver an objective value.

Those aren’t the reason I use Go, though. The real reason I use Go goes back to my background in English and writing.

I’ll never forget [watching Rob Pike read his blog post aloud](http://www.meetup.com/golangsf/events/59833112/) before he had published it. I expected to be in awe of him for his contribution to the field (my expectations were met); what surprised me was the respect I felt for him as a writer. It is rare in this line of work to find someone who has that powerful a narrative voice, who is that compelling a writer.

When you think about that, it’s kind of weird. We *write* programs, we don’t *build* them or *engineer* them. We’re supposed to be communicators first—people who can take the concepts and demands of a customer and translate them into ones and zeros for a computer. Why is the ability to write well rare in that field? I don’t know. I don’t have an answer to that.

What I do know is that one line will forever embed itself in some corner of my memory:

> “What you’re given is a set of powerful but easy to understand, easy to use building blocks from which you can assemble—compose—a solution to your problem.”

That correction—“compose”—is what did it for me. Go is the first language I have found that has let me focus on my composition, the way the constituent parts of my software form a whole, instead of my writing, the specific syntax and semantics I used in creating that whole. It puts the focus back where it’s supposed to be: on the ideas, not the implementation.

> **com⋅po⋅si⋅tion** _(n.):_  
> 1. The nature of something’s ingredients or constituents; the way in which a whole or mixture is made up.  
> 2. The action of putting things together; formation or construction.

I use Go because it is the only language that feels like writing a piece of prose or creative literature. I am not worried about remembering a bloated spec or edge cases. I’m not worried about checking every possible error at every possible place—I already checked them where they were raised. I’m only worried about refining my ideas until they are clear and defined enough that a computer can act on them.

And really, isn’t that what this job is supposed to be about?

You can use whatever language you want. Whatever makes you productive, whatever makes you happy to use. All I know is that, for me, nothing I have found beats out the sheer expressive power of good, clean Go.

(Even without the generics and exceptions and GUI library I’ve heard are required for a language to be successful.)
