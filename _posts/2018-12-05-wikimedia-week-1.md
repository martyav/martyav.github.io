---
layout: post
title: Wikimedia Week 1
---

My internship with Wikimedia started yesterday! As part of my internship, I'm required to make biweekly blog posts chronicling my journey, so you'll be seeing a lot more of me lately. If you want to keep up, you can join my new [RSS feed](https://martyav.github.io/feed.xml). And if you want to know how to add your own feed to your Github-hosted site, check this handy guide [here](https://github.com/jekyll/jekyll-feed) (assuming you use [Jekyll](https://jekyllrb.com/)).

Never set up a feed before? Me either. RSS, though quite old, is new to me, as is [Phrabicator](), [Zulip](https://zulipchat.com/), [IRC](https://whatis.techtarget.com/definition/Internet-Relay-Chat-IRC), and some of the other official channels I've been encouraged to sign up for during my trial period at [Outreachy](https://www.outreachy.org/). 

Outreachy is the program funding my paid internship, and it is also sponsoring a multitude of internships at other organizations, including [Mozilla](https://www.mozilla.org/en-US/) and [Ceph](https://ceph.com/).

Outreachy is aimed at cis and trans women, trans men, genderqueer folks, and people of color. I learned about it from an LGBT Slack I visit. I decided to apply because I was looking for entry-level work doing web, and I've been curious, yet  wary, about participating in open source. 

I do contribute to [Renegade Coder](https://therenegadecoder.com/), and I host almost all of my side projects on Github, but I haven't felt comfortable or ready to join bigger open source communities with people I don't know or trust. 

I've been on the Internet for more than a day or two, and I know that there is a certain kind of person who is very interested in technology, very arrogant, and very invested in petty arguments and bigoted jokes.

In fact, while I was applying to Outreachy this fall, there was a lot of Twitter debate over prominent open source projects adding Codes of Conduct to set rules for civil communication. 

I don't understand why this would be so controversial -- why wouldn't you want to establish some written ground rules governing behavior for a large project involving lots of human beings who don't know each other? Seeing people in open source act as if this was ridiculous or unreasonable wasn't very encouraging.

I applied to Outreachy anyway, despite these qualms, because I think open source is a powerful and exciting idea, and Outreachy has a specific mission to bring more under-represented groups into open source communities. 

I know these diversity in tech programs may not necessarily provide all the support they claim to, but it was worth a shot. They certainly seemed to have some interesting organizations on board. 

With Outreachy, you make an initial application; then, when you're approved, you get to choose from a variety of open source projects to work on. This is the start of your trial period. 

You introduce yourself to the project you've chosen, make some contributions, and record what you've done on the Outreachy site. Towards the end of the trial period, you make a formal application to the project. 

During the trial period, you can work on multiple projects at once, to see what you like and if you'd be a good fit for the community. 

I initially set to work on Ceph, as well as on Wikimedia, after Outreachy approved me.

I was attracted to Ceph because they seemed to be doing an open source version of my work at Azure, and because they were using Python, a language I like but haven't used much. 

However, I had a very hard time building the project. The build process for such a large amount of code was slow going, and I kept running into issues, often due to my own inexperience with Linux. I learned a lot, but ultimately washed my hands of it, because it was taking up too much time. 

I suspect the final issue I ran into was actually due to my version of Python. At the time, I was not experienced enough to know that if I kept throwing an error while trying to install a dependency, it might be because the dependency only supports Python 2.

While I was trying to get Ceph to build and contacting mentors for help, I was also exploring the Wikimedia project, for improving MediaWiki's top 50 API documentation pages.

The Wikimedia project drew me because it involved a mix of Python, writing, and web. I like coding and I like writing, so it was definitely attractive. 

Even better, the doc writing involved getting really familiar with a variety of APIs, which meant I'd learn a lot about how the project was designed overall, and how web APIs work. I'd also be helping other people learn how to use the APIs.

At first, I was a little overwhelmed by the amount of information on the project, and how much of it was spread out. There were instructions on the Outreachy site, on [Phabricator](https://readwrite.com/2011/09/28/a-look-at-phabricator-facebook/), on [MediaWiki](https://www.mediawiki.org/wiki/MediaWiki), and I wasn't even entirely sure [what the differences between MediaWiki, Wikimedia, and Wikipedia were](https://www.mediawiki.org/wiki/Differences_between_Wikipedia,_Wikimedia,_MediaWiki,_and_wiki). 

Thankfully, my mentors were attentive and willing to answer any questions I had. Not to trash Microsoft too much, but my mentoring experience there had been pretty hands-off. I was prepared for a similar style of mentorship at Wikimedia.

I was very glad to have better communication, and clear advice on what to do, even as I spent a lot of time in self-directed activity, writing and researching what I needed before I sent off emails.

Throughout October, I was working, off and on, on three separate tech docs. As you would expect, they're hosted on a wiki and use [wiki markup](https://en.wikipedia.org/wiki/Help:Cheatsheet). I've been getting more comfortable with [Markdown](https://daringfireball.net/projects/markdown/) because I use Github fairly often, so when I started writing wiki pages, I sometimes found myself getting the two mixed up.

I certainly learned a lot about MediaWiki, even from just those three articles. Much of my time was spent researching, and even more was spent refining the text to make it more clear. 

Two of the articles I worked on were published to the main site, and the last one is still in the works because it needs translation markup I can't provide because I don't have admin privileges. It is more or less finished, according to the spec I was given.

I was also tasked with creating sample code in Python, to demonstrate how to use the APIs. It had been a long time since I had written any scripts in Python, but I had a template to follow, which helped immensely. 

At first, I thought I'd be smart and write the code without referring to the template, but that just led to weird errors that forced me to really read and understand what the template code was doing.

As part of my application process to the Wikimedia project, I had to submit a proposal. The proposal included an idea for a sample app,  to demo how to use the API. I had used similar apps while learning [Azure](https://azure.microsoft.com/en-us/) at Microsoft, so I had an idea of what form this should take. 

Towards the end of the trial period, I was feverishly preparing my proposal and completing my docs. I was competing against a dozen other people to work on Wikimedia, some of whom had dropped out of the project quite early. The ones who stayed to the end were great coders with more traditional tech backgrounds, and I was anxious to really stand out. I was also applying to other jobs and internships, working on a Renegade Coder article, doing side projects to get more practice in, and submitting work for Hacktoberfest. 

It seemed like I was doing everything at once. 

Then I made my final edits, submitted my proposal, and waited.

The next few weeks felt very long. I briefly continued to edit the last article, but I couldn't get too far without being a translation admin. I went on more interviews, and visited my old bootcamp for DSA paractice. I met with a friend from [LEAP](http://www.industryexplorers.com/), who encouraged me to learn C++, since his team was hiring. 

When I got the email that I was accepted as a Wikimedia intern, I almost felt like crying, because I had put so much work in without being certain that it would pan out into an internship. 

It wasn't that I had thought my work would come to nothing; it was already out there, being used, by readers visiting the docs and sample code repo. I was just so relieved to have something steady, doing work I enjoyed, using tech I liked working in, on a project that felt important and meaningful. 

If I had any advice to future Outreachy applicants, it would be, to stick with it. My collaboration with Ceph didn't pan out, but I wasn't as invested in it as I was in Wikimedia. 

If I had continued investigating the problems I ran into with Ceph, I probably could have made a good proposal and been in the running to work with their team. 

Even if you don't come from a traditional tech background, don't feel like you're less and drop out early. You might actually be one of only a handful of active people on the project, and have a better chance than you think. 

For someone from a different background, your past experiences on other projects and in other careers are powerful and useful. Organizations participating in Outreachy want your unique skills and experiences, as well as your technical expertise. Don't be afraid to point to what you know and who you are, outside of tech.

---

I'm really glad to be on board, and eagerly await my first video chat with my mentors. It's later today. 

I spent most of my first day, yesterday, establishing a routine for myself, since I'm working remotely. It's good to have habit to fall back on when I'm not feeling great. I try to work for an hour or two, then get up and take a break. When I come back, I switch tasks, so I'm not draining myself by concentrating intensely on something for too long. 

With writing, as with coding, you can get caught up in details to the point that you're actually blocking yourself from making any progress. It's important to know when to take a break.

Speaking of breaks, my next blog post is due in two weeks. I have a lot of work to do until then: tightening up my app proposal, starting articles, learning Flask. So, thanks for reading, and don't forget to sign up for my feed if you want to keep in touch!
