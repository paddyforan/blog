---
date: '2012-03-16'
has_tweet: true
quote:
  attr: Peter Cooper
  text: '“A true history of human events would show that a far larger proportion of our acts are the result of sudden impulse and accident than of that reason of which we so much boast.”'
summary: 'The ongoing history of 2cloud; alternate title: “How I Started A Company On Accident”. A narrative exploring how a learning project grew out of control.'
title: The Story of 2cloud
url: /posts/2cloud
---


**Note:** This story is still in-progress. Don't be surprised if it gets updated. 
I'm lazy and inconsistent, so don't be surprised if it doesn't. In fact, just try 
not to be surprised no matter what. On with the show.

I'd like to think you're reading this because of my acerbic wit, my elegant writing,
my engaging style. I'd also like a pony.

The more probable scenario is that you've used my software and wanted to know more 
about the sack of meat that put those ones and zeroes together. The fact of the 
matter is, people tend to know me either because they've met me in person or 
because they've used [2cloud](http://www.2cloudproject.com). My misanthropic nature 
means the scale tips heavily in favour of the second possibility.

People are often surprised by 2cloud's origin story. Users are always taken aback 
that there's just this kid sitting in a small, dark room in Buffalo, New York, not 
a corporate behemoth. People who know me are surprised to hear me refer to it as an 
accident. But, really, that's all it was: an accident.

If I were to be perfectly honest with myself, I'd probably trace the beginning of 2cloud 
to the beginning of 2010. I was just getting out of a messy situation involving relationships, 
the details of which I won't bore you with, and was looking for a way to distract myself. 
For the first time in a long time, I was also looking at my future and wondering what 
to make of it. I knew I'd need a career, knew I'd need a job I was passionate about. 
I started wondering what that job could be.

I bet a lot of you are imagining, at this point, that the answer turned out to be 
“working for myself”. That's what any entrepreneur would say, right? I'll admit, at 
this point I was following the happenings at [TechCrunch](http://www.techcrunch.com) 
and thought the lifestyle sounded like a lot of fun. Which I took as a sign that it 
was not right for me. I'd embed the tweet here, but it was from 2 years ago, meaning 
it's impossible to get a link to it on Twitter now.

Instead of dreaming of working for myself, I dreamt of working for Google. Why? 
Because Google seemed like a place where I could work as if I worked for myself, but 
have the financial security and benefits of working for someone else. Also, it was a 
company filled with great people doing amazing things, and I wanted to be part of that. 
In many ways, it still is, and I still do. Sort of.

I started to create a plan of action for getting hired by Google. To put it in perspective, 
I was a 19-year-old English major at a small college in the middle of Buffalo. My odds 
did not look good, and I knew it, but it gave my life a direction, so I went ahead 
with it anyways.

It started by emailing Michael Davidson. I met Michael by accident, as well. I bet you're 
starting to notice a trend here. It was March of 2009. I was working on a personal 
project, something to keep me busy, that was built on App Engine. I wanted to use 
XMPP, which wasn't supported yet. It came up in a tweet.

<blockquote class="twitter-tweet tw-align-center"><p>@<a href="https://twitter.com/jasonsalas">jasonsalas</a>: Thanks! I'm in the US. But I was looking into XMPP support for <a href="https://twitter.com/search/%2523appengine">#appengine</a>- it's coming, but for now I have to use IMified.</p>— Paddy (@paddycarver) <a href="https://twitter.com/paddycarver/status/1303818629" data-datetime="2009-03-10T03:26:55+00:00">March 10, 2009</a></blockquote>

For some reason, I somehow came to the attention of Mike Repass, the project manager 
for the App Engine XMPP API. I still have no idea how this happened.

<blockquote class="twitter-tweet tw-align-center" data-in-reply-to="1303818629"><p>@<a href="https://twitter.com/paddycarver">paddycarver</a> Hi Paddy, would love to get your input on what you'd like to see with XMPP in App engine, drop me a line!</p>— Mike Repass (@mdrcode) <a href="https://twitter.com/mdrcode/status/1304888141" data-datetime="2009-03-10T11:08:07+00:00">March 10, 2009</a></blockquote>

Mike Repass then put me in touch with Michael, the engineer working on the API. Michael 
and I exchanged a few emails, discussing the API.

Fast-forward a few months, and Buzz is released. I'm minding my own business, being 
generally silly and offensive, just like I am on Twitter. And out of nowhere, I get 
followed by Christian Bogeberg, a tech recruiter for Google. He and I chat some, mostly 
about nothing, and I move on with my life.

Fast-forward to 2010, and I find myself emailing Michael and Christian, asking how I 
should prepare myself to get hired. I get [some great information](http://www.suchagit.com/2010/05/story-in-progress.html) 
that basically boils down to “learn more and get more experience”. Generally, I learn 
best when I'm gaining experience. So I start casting about for things to do. I [start 
a blog](http://www.suchagit.com) to catalogue my experiences.

A few weeks later, I'm watching Google I/O from my room in Syracuse, New York. I watch 
the demo of Chrome to Phone and think it's pretty cool. But I also think “Hey, 
it would be cool if you could push links from Android to Chrome, too.” So I 
[decide](http://www.suchagit.com/2010/05/android-to-cloud-push.html) to write it. Worse, 
I already had an algorithm in mind to write it, and it seemed pretty simple, so I 
decided to challenge myself to write the App Engine and Chrome sides in three hours, as 
I rode in the car on the way to my older brother's graduation in Rochester. That was a 
bit ambitious; it ended up taking me the trip there *and* the trip back.

How did I write a system in six hours? Well, remember how I said it seemed simple? 
Note to self: if something seems simple, you're probably doing it in a dumb way. That 
initial version was the stupidest thing that could have possibly worked. The App 
Engine side had two endpoints: one for receiving links, the other for displaying. An 
authenticated POST request to the receiving endpoint would save that link in the system. 
An authenticated GET request to the displaying endpoint would just display the latest 
link pushed. I didn't even use caching. The Chrome extension worked by just hitting 
the display endpoint every 10 seconds. It opened the link, then saved the link in localStorage. 
Next time it hit the display endpoint, it checked the link against the one stored in 
localStorage. If the links didn't match, the link was opened.

It's surprising this didn't scale.

I [announced](http://www.suchagit.com/2010/05/android2cloud-update.html) the completion 
of the Chrome/App Engine components, then hunkered down to wait for my Nexus One to 
arrive so that I could develop on it.

When I got the phone, development started slowing. [Android development](http://www.suchagit.com/2010/05/android-development.html) 
isn't as straightforward as Chrome extension and App Engine site development is. I 
[hit some roadblocks](http://www.suchagit.com/2010/06/roadblocks-are-bad.html) trying 
to use OAuth. To this day, using OAuth on Android remains a giant pain in the ass. 
All in all, it took me from May 22 to July 12 to get a working Android version ready 
for [release](http://www.suchagit.com/2010/07/android2cloud-alpha-release.html).

I never really expected anything to come of android2cloud, as I dubbed it. I put it 
online because I believe that software that dies on your hard drive is a waste of 
perfectly good resources. I believe in releasing everything as open source software 
by default, and only *not* releasing if there's a *very* good reason. So I released 
android2cloud as open source software.

The first night I put it on the Android Market, I got a bug report from [Patrick 
Kettner](https://plus.google.com/100594935715938326713), who (I believe) was the 
first android2cloud user. He was also the first person who donated. Patrick sat on 
IM with me and debugged his issues until they were resolved. I still feel a huge 
amount of gratitude towards him for his role in this.

android2cloud didn't stay small long. By July 26, a mere two weeks after I had 
released the software, I was marveling over the fact that [two Asian publications](http://www.suchagit.com/2010/07/global-entrance.html) 
had covered android2cloud and the project page was getting a decent amount of traffic. 
I also noted a problem that would plague the fledgling project for years: we were 
seeing a huge amount of traffic on the server.

On August 2nd, we had our first downtime. The server ran over its quota, and I had 
a tough decision to make: what the hell should I do? I ended up pulling the email 
addresses from the database and sending a mass email. I apologised for the invasion 
of their inbox, and let them know about the downtime. I also let them know about the 
implementation of Google Analytics tracking in the project. This tracking was short-lived; 
it added unacceptable bloat to the Android app and required us to ask for more permissions 
than we actually needed.

I consider the tipping point of the project to be August 4th, 2010. On August 4th, 
[Kevin Purdy](http://thepurdman.com) of [Lifehacker](http://www.lifehacker.com) 
[covered](http://lifehacker.com/5604248/android2cloud-opens-urls-from-your-phone-in-chrome) 
the app. It went on Lifehacker's homepage. Thousands of users followed almost immediately.

Unsurprisingly, we had downtime that night. I sent out another email, apologising. I 
dealt with email replies and conversations throughout the day, but there was some fallout. 
I got a lot of negative feedback, I got a lot of negative reactions, and I came face-to-face 
with the one enduring truism that this project has given me: nobody cares, and they 
shouldn't have to.

But still, it's hard, as a barely-20-year-old college student whose world is limited 
to his little town and little college, to deal with a sudden influx of complaints, 
criticisms, and opinions. I got a little overwhelmed, but tried to keep my chin up. I 
[posted](http://www.suchagit.com/2010/08/double-edged-sword-users.html) about how 
awesome it was that I had all these new users, but they brought with them a slew of 
problems I didn't know how to deal with.

A mere two days later, I [posted](http://www.suchagit.com/2010/08/am-i-washed-up.html) about 
an experience that would refrain over the next year or two: I updated and 
[broke everything](http://blog.2cloudproject.com/2010/08/authentication-issues.html). 
I began to doubt myself, to wonder if I had had one shot at being a good developer, and 
I had blown it. My nagging self-doubt began to gnaw even more fiercely at me, with the 
very real possibility eating away at my confidence: did everyone figure out what I already 
knew, that I was a hack? Did everyone decide that I didn't know what I was doing and 
just move on? They would've been right.

As I [continued to fight with downtime](http://blog.2cloudproject.com/2010/08/downtime.html), 
I [started looking](http://blog.2cloudproject.com/2010/08/servers-and-money.html) at what 
the community thought I should do. How could I get the server paying for itself when 
it was using $70 a week?

Well, enter Michael. Remember Michael? The engineer who talked with me about the XMPP 
API? Well, Michael had kept android2cloud on his periphery, and when Google's Channel 
API was ready for testing, Michael recommended me for the testing program. The Channel 
API was our godsend. It would let us form a connection with the server and have the 
server just tell Chrome when a new link was available, rather than having Chrome ask 
every fifteen seconds. With Michael's recommendation, [we got early access](http://blog.2cloudproject.com/2010/08/channel-api.html) 
to the API and began testing it. I met Moishe Lettvin, the App Engine Communications APIs 
Lead who was also in charge of the new Channels API. I began implementing the system 
and talking with Moishe about our needs and the Channels API.

We were moving fast, but not fast enough; once again, we were [running out of money](http://blog.2cloudproject.com/2010/09/money-spoils-everything-wholesome.html). 
I had to cut server quotas in half, with plans to remove them entirely in the near 
future. [Downtime became expected](http://blog.2cloudproject.com/2010/09/downtime-imminent.html), 
at that point. But the app didn't die; it got covered by more Android blogs, got 
discussed in podcasts, it was even a top 10 most popular app on AppBrain... twice. 
I didn't know what to do with all the publicity.

Then we were saved. A white knight came riding to our rescue. We [got](http://blog.2cloudproject.com/2010/10/sponsorship.html) 
our first sponsor, [WonderProxy](http://www.wonderproxy.com), through [Paul 
Reinheimer](http://twitter.com/#!/preinheimer). The business dealings were kept to 
a minimum. Paul essentially said “Hey, we'd like to sponsor you. What can we get for 
$200?”, to which I said “We'll link you on the blog and list you on the project page 
as a sponsor.” That was pretty much it.

The money tided us over for a bit, but a few weeks later, we were right back where 
we started: [broke](http://blog.2cloudproject.com/2010/11/more-downtime.html). Once 
again, [we were saved](http://blog.2cloudproject.com/2010/11/another-sponsor.html); 
this time, it was [SiteSpect](http://www.sitespect.com) coming to our aid, through 
[Eric Hansen](http://twitter.com/#!/ericjhansen). Eric basically said “Hey, we'd like 
to sponsor you, too. Can we just have the same deal WonderProxy got?”, to which I said 
“Sure”.

During this time, the Social Network was released. This is important, not because of 
the movie itself, but because of the conversation it started. My friends were aware 
that I had this project going on and that it was getting undeserved popularity. One of 
my friends, [Tino](http://www.twitter.com/tinogalizio), saw the Social Network and 
sent me a text: “If you ever started a company, I'd want to be the Eduardo Saverin to 
your Mark Zuckerberg.” I had already been thinking about how horrible it would be if 
one of the thousands of people I was now hosting sued me, or if I got sued for something 
they did. Really, this project could only survive without a company as long as nothing 
with legal implications happened. That scared me. So Tino's proposition intrigued me. 
We started researching New York State's laws on businesses, and formed an LLC we called 
[Second Bit](http://www.secondbit.org). It was a name I had thought up during the summer, 
along with the tag-line “Untapped potential”. It came from thinking about storing binary 
data; often, it's not good enough to store “yes” or “no”, you tend 
to need “no answer” or “maybe”, too. So you need a second bit, of 
which only one of the values is used. Meaning you're not realising the full potential 
of your data-storage capabilities. This idea struck me as something very true about the 
way I work; I'm never quite working at my full potential. Rather than thinking about 
this as me doing unsatisfactory work, though, it became a mantra for continual 
improvement in my work. “Untapped potential” isn't, as some people who heard 
the rationale purported, a slur on the current level of our work, it's an admonition 
to not be satisfied, to not settle, to not allow ourselves to grow complacent.

As the weeks passed, the Channel API still wasn't available for use in our production 
server. We had it running for our beta testers, but our production environment couldn't 
use it yet; Google wanted to test it with a small subset of our users, and promised that 
they'd give our production server access as the API matured. I grew impatient, and 
started investigating an emerging new language for the server, [NodeJS](http://www.nodejs.org). 
It would mean hosting the server ourselves, but would enable the same push capabilities 
we'd get in the Channel API. Then something happened that fractured all my plans: the 
Channel API got released. My reaction is one I'm not proud of; I felt betrayed. Google 
didn't give me much forewarning, and I was caught with my pants down, without a full launch 
plan. I immediately dropped the NodeJS plans, and [started testing](http://blog.2cloudproject.com/2010/12/hello-channel-api.html) 
the Channel API for production deployment, rather than just testing the technology, 
as I had before.

The API had changed since I had last tested. It no longer worked with Chrome extensions. 
I dug through the code and implemented a workaround, which I then shared with Moishe. 
He thanked me, and fixed it in the production environment. I worked through the month 
of December to get the new system ready for a [release](http://blog.2cloudproject.com/2010/12/version-updates-and-annoying-messages.html) 
at midnight on January 1st.

[I botched it](http://blog.2cloudproject.com/2011/01/about-version-20.html). Horribly. 
For thousands of users, bugs were rampant in the new version, rendering it unusable. 
The upgrade was a catastrophic failure. I had planned to announce that Second Bit was 
“acquiring” (i.e., legally responsible for) android2cloud. That announcement 
was put on hold until I could fix everything.

The good news was that the financial situation was less dire, for the time being; we 
were using about a dollar a day to keep the server running, one tenth of what it cost 
before the upgrade. The bad news was that the upgrade introduced a host of new bugs. 
For example, the Channel API was used to create connections between Chrome and the 
server. The problem was, these connections only lasted two hours before being closed. 
I had to catch the close error, then force a reconnection. This is still unreliable, 
15 months after I introduced it. Also, for some reason, my method of storing the last 
link that the Chrome extension received was no longer functioning for some users; the 
links kept opening.  I issued a [fix](http://blog.2cloudproject.com/2011/01/202-just-pushed.html) 
for this, basically storing whether a link had been read or not on the server. Chrome 
would then tell the server that it had gotten the message, and the server would only 
send messages that hadn't been received. This blew up in my face later.

As anyone who has introduced a large number of bugs into software or broken software 
for a large number of people knows, the user base is pretty vocal when things stop 
working. Which led to another situation I'm not proud of: I [outlined my 
disappointment](http://blog.2cloudproject.com/2011/01/disappointment.html) in a blog 
post. I was worn down, I was hurt, and I was tired of being met with demands every 
time I turned around. Some users, a very vocal minority, were nothing short of rude 
and hateful in their interactions with me, and it was wearing me down to continue 
to be polite and calm with them. By the end of January, I needed to declare a 
[hiatus](http://blog.2cloudproject.com/2011/01/hiatus.html) for a week or two as I 
caught my breath.

When I returned, it was to release [a new version](http://blog.2cloudproject.com/2011/02/203-landing.html) 
that fixed some users' problems with links not opening or links not getting marked 
as read. Which would have been great, if it didn't [introduce a new bug](http://blog.2cloudproject.com/2011/02/links-constantly-being-opened.html) 
that caused *more users* to have their links open every time Chrome started. By the 
way, in case you were wondering, that *really* annoys people. I had long treated the 
ability to open links in people's browsers as a sacred trust, and I'm glad I did.

A few days later, I [had a fix](http://blog.2cloudproject.com/2011/02/204-sort-of.html). 
I was finally tired of having everything break on me, however, so I made it an opt-in 
for those having the problem until I could verify it worked as expected.

Around this time, I met [Dylan Staley](http://www.dstaley.me). Dylan is... well, the 
best way I can think of to describe Dylan is “incredibly ambitious”. He's a 
year younger than I am, but makes me feel lazy. When I met him, he was a student 
ambassador for the Wikimedia Foundation and an Apple Store employee. He's since left 
Apple, become an integral part of an LSU frat, obtained a position as a local 
representative for Square, and is applying for *yet another* position for I-don't-even-know-who. 
The boy is nuts. Dylan and I met because of Google I/O. That's not an exaggeration; 
Google I/O was gearing up, and Dylan and I both happened to be watching the hashtag 
on Twitter. I posted something, and Dylan replied. We started talking, and the rest 
is history.

One of the more surreal moments of this saga was chatting with Dylan and telling him 
about android2cloud, only to have him respond “Oh, yeah, I've used that!”

As Dylan and I talked about android2cloud, he proposed doing a new design for it. I 
was ecstatic. He wanted to use it as an entry in a design competition, I wanted to 
have a design that didn't look like... well, like I designed it. He joined the 
android2cloud team as our lead designer, and in mid-March, we were ready to [unveil 
the redesign](http://blog.2cloudproject.com/2011/03/say-hello-to-2cloud-project.html). 
We had rebranded from android2cloud to just “2cloud”, to allow us to expand 
to other platforms and become more platform-agnostic. We had new icons, a new website, 
the whole shebang.

Two weeks later, another announcement came right on the heels of our redesign: we had 
been [acquired by Second Bit](http://blog.2cloudproject.com/2011/03/weve-been-acquired.html). 
Second Bit had actually acquired the product on January 1st and had subsequently started 
paying the server bills, but we had refrained from saying anything until Second Bit's 
website was launched.

When we announced the acquisition, we reaffirmed our stance: no ads, no asking users 
to pay for it. We were determined to remain free, open source software. That would 
come back to bite us in the ass.

Not even a month later, we [introduced](http://blog.2cloudproject.com/2011/04/android-2051-and-ads.html) 
ads to our Android client. They were opt-in, but I still got a bad taste in my mouth. 
Unfortunately, we were running out of money. There wasn't much of a choice in the 
matter. We had to do *something* to monetise the service, or we'd have to shut it 
down. It wouldn't be the last time we broke a promise, or the last time we felt we 
had no choice. It still makes me feel bad, and I still wonder whether I'm really 
doing the right thing, even as I push further on down this monetization road. I had 
so many principles that I stuck to as long as I could, but abandoned when I was faced 
with a hard choice. I tell myself I'm refining those principles, holding on to the 
ideological core while making them practical, but with each compromise I feel myself 
slipping down a path I never wanted to be on in the first place.

The ads, unfortunately, failed miserably. We never made a dime off them. The problem, 
we deduced, was that our app was, at its most ideal, invisible. It's hard to display 
ads on something invisible. Rather than trying to make a monetisation strategy that was 
completely at odds with the goals of our product work, we abandoned ads.

May was dominated by my visit to San Francisco to attend Google I/O. I flew across 
the country to spend a week with Dylan, Google, and five thousand computer geeks I 
didn't know. It was the best week of my life.

When I got back, I continued working on 2cloud. At that point, I was working on a 
version I called “Honeybadger”. The point of Honeybadger was to be resilient, 
well-architected, clean, and complete. It would integrate Chrome to Phone functionality 
next to Phone to Chrome functionality. It would bring the long-awaited arrival of 
Firefox support.

Then, on June 30th, I got an email that changed everything. Wired contacted me, 
asking if I was the correct contact person for press. They were reviewing 2cloud. 
(They ended up giving it an 8/10).

Remembering the Lifehacker coverage and the results it brought, I decided the only 
appropriate reaction was to [freak out](http://blog.2cloudproject.com/2011/06/time-to-grow-up.html). 
A few frenzied phone calls later, we came up with a plan to pay for the server in the 
long-term: a quota. I stopped working on Honeybadger and [began a codesprint](http://blog.2cloudproject.com/2011/07/they-grow-up-so-fast.html) 
to enable a quota that would cut off after a certain amount of usage unless the user 
paid a dollar. If the user didn't pay a dollar, their links would open when the quota 
reset. We took the opportunity to deprecate support for some of the older Android 
versions, so we could get rid of OAuth in future versions.

A few weeks later, we [released](http://blog.2cloudproject.com/2011/08/21-in-with-new-out-with-old.html) 
the new version with the quota. We set the quota high enough that it wouldn't be hit 
for a few weeks, to be sure the software was working and there were no bugs. For once, 
a release went as planned. I [posted](http://blog.2cloudproject.com/2011/08/about-quota.html) 
about the quota.

When were sure the system was working as intended and there were no bugs, we set the 
quota to a sustainable level. Late that day, the quota ran dry. I tested, and purchasing 
exemption worked just fine. Nobody paid to get around the quota. We theorised that 
maybe the window of opportunity was too slim, and so we set the quota for the next 
day artificially low, trying to force the quota to run out earlier. It did, around noon. 
Still, nobody paid.

Worse, we got a [particularly nasty support request](http://help.2cloudproject.com/discussions/questions/7-server-is-over-quota-and-my-link-will-be-stored-unles-i-cough-up-1-really) 
about it. We tried to be civil in our replies, but we were both really upset. Once 
again, I [posted](http://blog.2cloudproject.com/2011/09/disillusioned.html) about 
my frustration. Again, not something I'm proud of.

Tino and I scheduled a meeting to hash out the money problems and decide what to do. 
I was pretty depressed about the whole thing by this point. I was starting to feel 
dread when it came time to work on or talk about 2cloud, and that made me sick at 
heart. I was at the point of saying “fuck it” and quitting the field of 
business development, letting Tino make all the monetisation decisions. Just declare 
moral bankruptcy and let him worry about it.

The meeting we had grew heated. Very heated. I didn't say anything I regret, and 
I don't think Tino regrets anything he said, but it was a very emotional ordeal 
for the both of us. Creating things and running a business aren't easy. At the end, 
however, as Tino was preparing to leave, I had an idea. A crazy idea. We started 
talking about why people were expecting so much of us but so reluctant to pay us. 
In essence, we started talking about why nobody used the quota. And we came up with 
[a theory](http://blog.secondbit.org/2011/10/apps-and-services.html): psychologically 
speaking, apps and services each provoke different reactions from users. We were 
perceived as an app, but were actually a service, and that was the root of our problems.

During the course of our discussion, Tino made an analogy. He claimed that I was like 
a dairy farmer who had this cow, and delivered milk to users. I kept telling the users 
“Oh, pay if you want to, I don't want to make you”, and the users kept saying 
“But you'll keep delivering milk if I don't? OK, see you tomorrow.” In the 
meantime, the cow was starving. “Bessie is starving, Paddy, and soon nobody will 
have milk!” He was right; the fair thing for the users who were doing the right 
thing was to protect their investment, to make other users do the right thing. But out 
of the analogy came the codename for our next version: “Bessie”.

I asked Tino to let me proceed as we were until December, to give me time to get 
Bessie ready to release. The point of Bessie was to transition 2cloud into a paid 
service *and* to make it clearer to users that this was a service. Before we could 
transition to a paid service, however, we needed to solve some problems that were 
acceptable in a free app, but unacceptable in a paid service. Things like the OAuth 
problems that had been a sporadic nuisance for years. Things like inexplicable 
errors. It became clear we couldn't host a paid service off App Engine.

We launched a new version of the Android app, with [an in-app poll](http://blog.2cloudproject.com/2011/09/upcoming-poll-again-about-money.html) 
about the subscriptions, to gauge the response. I included a field in the poll for 
people to enter their email address, in case they'd like to talk with us about the 
subscriptions. I then spent weeks sending hundreds of emails, conversing with our 
users about the change. It was the most intense customer support work we'd ever done, 
and it ate up hours of time. I think it was worth it.

I chose Google's [Go](http://www.golang.org) to write the server side of Bessie. I 
used Twitter's [Bootstrap](http://twitter.github.com/bootstrap) to create a theme, and 
built the first web interface we've ever had. The web interface was ready for alpha 
testers on December 2nd, in time for a Google+ Hangout we had scheduled to allow people 
to talk with us about subscriptions. We had a [pretty good turnout](http://blog.2cloudproject.com/2011/12/engaging-real-people.html) 
and chatted for a few hours, and I gave everyone that came access to the alpha version 
of Bessie to test and play with.

The testers found some bugs, and I summarily fixed them. I [started a blog](http://updates.2cloud.org) 
to serve as the changelog as we updated the server. The plan was to update the 
Chrome extension, rebuild the Android app from scratch, and release.

Then I dropped out of school.

I had been struggling in college for a while. It wasn't that I wasn't smart enough 
or that I didn't know the material. I had increasingly become plagued with insomnia 
and hypersomnia, and college was making my depression worse and worse. I was having 
trouble completing assigned work or showing up to classes. After some discussion 
with my family over the winter break, I took a medical leave of absence from school. 
I'm not sure I'll be going back.

If I wasn't going to school, I needed to be working, instead. I got hired as a 
Software Engineer Intern at [Iron.io](http://www.iron.io). I've been learning a lot 
there, and have morphed into more of a developer advocate than anything else. It 
takes up a considerable amount of my attention, though, more than school did, and 
it has slowed the progress of 2cloud development. Which explains why it's now mid-March 
and there still aren't public alphas of the Chrome and Android interfaces. I've 
been growing a lot, as a developer, in these last few months, though. The 2cloud 
architecture has been rethought and upgraded to be more scalable, fault-tolerant, 
and with better separation of concerns. We're making use of [IronWorker](http://www.iron.io/products/worker), 
one of the products Iron.io makes, and we'll be using [IronMQ](http://www.iron.io/products/mq) 
as soon as a feature is added. Not because I'm an Iron.io employee, but because 
they make our application better. Which is really all that matters.

I said at the start that I should never be startup founder because I think it would 
be a lot of fun. I became a startup founder on accident, without any input from me, 
really. In doing so, I learned I was right on both counts: I should never be a startup 
founder, and it is a lot of fun.
