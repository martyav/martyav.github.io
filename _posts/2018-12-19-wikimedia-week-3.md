---
layout: post
title: Wikimedia Week 3
---

I'm in the middle of week 3 of my internship with Wikimedia. I'm still working my way through the top 50 articles, but I'm getting faster. We've also started talking about what shape the app I'll be working on will take.

This week's topic is struggle. Tech culture heavily encourages you to pretend you are a tireless genius, so I'm going to have to drop the facade and sit with this a bit.

I suppose the main difficulty I've run into so far is simply the vastness and diversity of Mediawiki. My job is, in part, to make the action API articles more consistent. However, Mediawiki has been around for decades, and the wiki ethos of allowing anyone to edit naturally lends all articles little quirks. 

In addition, the API's themselves can overlap with one another in confusing ways. Some are lists, some are props, and all require linking back to their proper definitions. Some require calling other APIs in order to make a successful request, or have drifted back and forth between versions in terms of how to write a query. 

My job also requires me to improve the docs, by adding relevant information, removing irrelevant information, and rewording the current text for clarity. Most of the docs I've worked on so far have been in good shape, but sometimes they unintentionally mislead the reader. 

For example, while working on API:Properties, I realized that the text I had worked on in API:Lists needed to be amended. API:Lists had an extended discussion on working with limits for returned results. This preoccupation with limits was presented in contrast to API:Properties. However, even properties have limits imposed on them. They have to -- otherwise you'd be getting results in the hundreds or thousands.

There are pages that are no longer seeing much in the way of edits, but which are linked back to more frequently than newer, less neglected pages covering very slightly different topics. There are pages that need their sample code updated to take into account more recent API versions. There are pages describing completely deprecated APIs as if they're still current. The hub pages often overlap, and it can be difficult to decide which to link to.

Talk pages are another matter. Mediawiki's discussions are pretty sedate. I was reading over an argument about Sidney Kubrick's infobox on the English Wikipedia earlier this week -- it had many pages of archives and is currently closed to debate because it got too heated.

While I haven't run into anything like that on Mediawiki, I have seen a few users with a handful of edits use the talk pages to ask a question that goes unanswered. I've recently worked on some sample code based on a talk page question from 2012.

Then there are the images. My sample code this week is chiefly concerned with image APIs. I've been searching through dozens of image files, looking for that perfect combination of interesting topic, interesting visuals, and short URL. 

There are literally millions of images to draw upon from the English Wikipedia, but not all of them are hosted there, and naming conventions vary by the user. This makes composing queries to return them more difficult than you would think.

This is the beauty and complexity of the Internet itself: many people around the world, working over the course of years, building knowledge, arguing, and uploading photographs of their cats. It is a garden in need of watering and of weeding.

I am struck by how my internship's workflow resembles, in some ways, [the original design for Wikipedia](https://en.wikipedia.org/wiki/Wikipedia#History). When Wikipedia was launched, it was intended as a scratch area for articles started by amateurs, which would then then be edited and improved by the  experts at a separate site, called Nupedia. Nupedia never got much headway, while Wikipedia attracted so much enthusiasm it wound up superseding it.

This was over two decades ago, before there was much in the way of staff, admins, veteran editors, or cliques. People could, and very much did, start articles about anything they wanted. It was the wiki Wild West. 

Today, I work with a paid staff member, drafting articles, proposing changes, and only getting my work published to the main site after they give the go-ahead. I also work on articles about APIs that enforce rules around editing, deleting, admin powers, and logging in.

I don't think all information should be organized into perfectly neat, overarching web silos. That gives whoever runs the silo far too much control. We have many recent examples of social media driving political debate, because these websites have so much power over what people see, and what they can say. 

However, much of the popularity of these enormous websites is due to their centralization. It is much easier and more accessible to create a Facebook group than it is to set up a new web forum with a custom domain. It is easier and more accessible to create a Tumblr than it is to get set up with a Neocities account. It was also much easier to check Wikipedia than it was to search through the newsgroups and fansites that characterized the early Web.

On Mediawiki, the problem presents itself in miniature. Having a wide variety of topics covered is good, but if an article is poorly written, if it isn't updated, if it has nothing linking to it, the information it contains will go neglected, and it might as well not exist at all. A combination of decentralized enthusiasm and more centralized maintainence seems ideal.

Too much of the former leads to information overload, while too much of the latter leads to deadlocks, like the entrenched argument over the Stanley Kubrick infobox. We cannot allow either side to win entirely. Vastness and diversity should not, in themselves, be considered problems, even if they can be very challenging. We grow our garden, and then we weed and prune. 
