---
layout: post
title: Wikimedia Week 7
---

It's the midpoint of my internship, and this week's official theme is revising expectations. That has certainly been something on my mind these past few weeks. 

I had a very good run for a while. I could finish an article describing a simple GET request in a day.

However, once the holidays were over, the pool of potential articles had been wittled down to those involving complicated POST requests, long overview pages describing how to use multiple APIs, and/or pages whose source contained lots and lots of translation tag markup. 

I had works-in-progress piling up because they needed translation tag review, code review, or both. I felt blocked.

When I was writing my proposal for WikiMedia, I planned for 20 articles to be finished, in total. Even this was a paring-down from the 25 to 30 I expected to actually get done -- it was a lowball.

My initial impression was that most pages that needed work were fairly similar, and that as I gained more familiarity with what needed to be done, my workflow's speed would increase. 

Now, this might have been an accurate mental model if I lived in an RPG, where grinding through many similar articles yields both experience and treasure. However, I live in a world with holiday breaks, illnesses, physical and mental fatigue, and 7 billion other people, of whom only a tiny fraction can answer my newbie questions. 

Furthermore, many of the pages that need work are similar mainly in terms of how complicated they are. They won't fit the template; they have messy markup; they contain obscure information that eventually boils down to one editor's frustration with version 1.17 of the API in 2013. 

The APIs involving the query module were all pretty similar. They were all GET requests, and they all fit into the template well. POST requests, on the other hand, rely on other APIs to work. They require authentication -- except when they don't. They require special permissions -- except when they don't. 

Translation markup, as it currently stands, is certainly also complicated to work with. Any page on Wiikimedia.org with a translations box utilizes this markup. Translation tags wrap around sections of the text, and they must be placed carefully to preserve other editor's translation efforts. This means you can't just break up paragraphs or change wording on the fly. 

There are several proposals to hide the tags from ordinary editors, but as it is, you have to work within the tagging system, whether you have translation rights or not. Without translation rights, though, you don't have as much power to update the tags. You just have to kind of sidle around them, and hope you're not breaking something.

Several pages that I worked on, including one during my trial period in October, sat for weeks, waiting for translation review. Eventually, me and my mentor were able to get in touch with Trizek on the WMF team. He was able to give the go ahead on pushing these articles to the main site.

With four longstanding translation articles in the can, I'm currently back on track towards my 20 articles. I'm relieved, but I still feel that I need to revise my expectations downward. I have 3 other articles that I am currently struggling with due to the sample code not being ready, and one article that may not get pushed afterall, because there might not be a need for it.

I hope to get 2 easier articles pushed to the main site by today or early next week, so I can have my target of 16 done for week 8. After that, I'll feel lucky if the issue with the code on these problematic pages gets resolved. I might have to find other pages to start work on instead.

As the weeks wind down, I'll be slowly refocusing on the app. I recently mapped out an early version of the quiz app, and hope to get some more wireframes done for the other concepts. I need to research libraries and frameworks, practice coding, and tighten up the final designs.

By the time of my next blog post, I'll hopefully have a good plan forward for the app or apps that I'll be working on, and 18 completed articles on the main site. If I don't, I'll still count it as a victory to have gotten as much as I did done.

The project I'm working on has been necessary for a long time, and the 17 articles I've completed so far -- including those from my trial period -- have been a significant chunk of the work needed to make the API docs more accessible to all.
